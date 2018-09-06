---
title: 在 PowerShell 工作階段之間保存使用者認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 9496ad0face2fbf4ecd685a6ee8e810a419b55aa
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/06/2018
ms.locfileid: "43384207"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a>在 PowerShell 工作階段之間保存使用者認證

Azure PowerShell 提供了稱為 **Azure 內容自動儲存**的功能，可提供下列功能：

- 在新的 PowerShell 工作階段中重複使用的登入資訊保留。
- 更易於使用的背景工作，可長時間執行 Cmdlet。
- 在帳戶、訂用帳戶及環境之間進行切換，而無須個別登入。
- 使用不同的認證和訂用帳戶，同時從相同的 PowerShell 工作階段執行工作。

## <a name="azure-contexts-defined"></a>定義的 Azure 內容

Azure 內容是一組資訊，可定義 Azure PowerShell Cmdlet 的目標。 內容是由五個部分所組成：

- 帳戶 - 用來驗證與 Azure 通訊的使用者名稱或服務主體
- 訂用帳戶 - 包含要進行處理之資源的 Azure 訂用帳戶。
- 租用戶 - 包含您訂用帳戶的 Azure Active Directory 租用戶。 租用戶對於 ServicePrincipal 驗證較為重要。
- 環境 - 作為目標的特定 Azure 雲端，通常是 Azure 的全域雲端。
  不過，環境設定也可讓您將國家/地區、政府和內部部署 (Azure Stack) 雲端作為目標。
- 認證 - Azure 用來確認您的身分識別，並確定您在 Azure 中存取資源之授權的資訊

在舊版中，您每次開啟新的 PowerShell 工作階段時都必須建立 Azure 內容。 從 Azure PowerShell v4.4.0 開始，您在每次開啟新的 PowerShell 工作階段時，可以啟用自動儲存和重複使用 Azure 內容。

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a>自動儲存內容以供下一次登入使用

從 6.3.0 版開始，Azure PowerShell 會自動保留工作階段之間的內容資訊。 若要將 PowerShell 設定為忘記您的內容和認證，請使用 `Disable-AzureRmContextAutoSave`。 您每次開啟 PowerShell 工作階段時，都必須登入 Azure。

若要讓 Azure PowerShell 在 PowerShell 工作階段關閉之後記住您的內容，請使用 `Enable-AzureRmContextAutosave`。 內容與認證資訊會自動儲存在您使用者目錄中的特殊隱藏資料夾中 (`%AppData%\Roaming\Windows Azure PowerShell`)。
接下來，每個新的 PowerShell 工作階段都會將您最後一個工作階段中使用的內容作為目標。

可讓您管理 Azure 內容的 Cmdlet 也能讓您進行更細緻的控制。 您是否僅需要將變更套用到目前的 PowerShell 工作階段 (`Process` 範圍) 還是要套用到每個 PowerShell 工作階段 (`CurrentUser` 範圍)。 這些選項將在[使用內容範圍](#Using-Context-Scopes)中深入討論。

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>將 Azure PowerShell Cmdlet 作為背景作業執行

**Azure 內容自動儲存**功能也可讓您與 PowerShell 背景作業共用內容。 PowerShell 可讓您以背景作業形式啟動並監視長時間執行的工作，而不必等候工作完成。 您可以利用兩種不同的方式來與背景作業共用認證：

- 傳遞內容作為引數

  大部分的 AzureRM Cmdlet 可讓您將內容作為參數傳遞至 Cmdlet。 您可以將內容傳遞至背景作業，如下列範例所示：

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- 使用預設內容，並啟用自動儲存

  如果您已啟用**內容自動儲存**，背景作業就會自動使用預設儲存的內容。

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

當您需要知道背景工作的結果時，請使用 `Get-Job` 來檢查作業狀態，並使用 `Wait-Job` 等候作業完成。 使用 `Receive-Job` 可擷取或顯示背景作業的輸出。 如需詳細資訊，請參閱 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。

## <a name="creating-selecting-renaming-and-removing-contexts"></a>建立、選取、重新命名和移除內容

若要建立內容，您必須登入 Azure。 `Connect-AzureRmAccount` Cmdlet (或其別名 `Login-AzureRmAccount`) 會設定後續 Azure PowerShell Cmdlet 所使用的預設內容，並可讓您存取認證所允許的任何租用戶或訂用帳戶。

若要在登入之後新增內容，請使用 `Set-AzureRmContext` (或其別名 `Select-AzureRmSubscription`)。

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

上一個範例會使用目前的認證來新增目標為 'Contoso Subscription 1' 的新內容。 新的內容名為 'Contoso1'。 如果您未提供內容的名稱，就會使用使用帳戶識別碼和訂用帳戶識別碼的預設名稱。

若要將現有的內容重新命名，請使用 `Rename-AzureRmContext` Cmdlet。 例如︰

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

這個範例會將包含自動名稱 `[user1@contoso.org; 123456-7890-1234-564321]` 的內容重新命名為簡單名稱 'Contoso2'。 管理內容的 Cmdlet 也會使用索引標籤完成，讓您能快速選取內容。

最後，若要移除內容，請使用 `Remove-AzureRmContext` Cmdlet。  例如︰

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

忘記名為 'Contoso2' 的內容。 您後續可以使用 `Set-AzureRmContext` 來重新建立此內容

## <a name="removing-credentials"></a>移除認證

您可以使用 `Disconnect-AzureRmAccount` (也稱為 `Logout-AzureRmAccount`) 來移除使用者或服務主體的所有憑證和相關聯內容。 在無參數的情況下執行時，`Disconnect-AzureRmAccount` Cmdlet 會移除目前內容中與使用者或服務主體相關聯的所有認證和內容。 您可以傳入使用者名稱、服務主體名稱或內容，將特定的主體作為目標。

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>使用內容範圍

有時候，您需要在不影響其他工作階段的情況下，選取、變更或移除 PowerShell 工作階段中的內容。 若要變更內容 Cmdlet 的預設行為，請使用 `Scope` 參數。 `Process` 範圍會覆寫預設行為，方法是僅使其套用於目前的工作階段。 相反地，`CurrentUser` 範圍會變更所有工作階段，而非只有目前工作階段中的內容。

例如，若要在不影響其他視窗的情況下，變更目前 PowerShell 工作階段中的預設內容，或是下次開啟工作階段時使用的內容，請使用：

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>會記住內容自動儲存設定的方式

內容自動儲存設定會儲存到使用者 Azure PowerShell 目錄 (`%AppData%\Roaming\Windows Azure PowerShell`)。 部分類型的電腦帳戶可能無法存取此目錄。 如需這類的情節，您可以使用環境變數

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

如果設為 'true'，就會自動儲存內容。 如果設為 'false'，就不會自動儲存內容。

## <a name="changes-to-the-azurermprofile-module"></a>對 AzureRM.Profile 模組的變更

新的 Cmdlet，可管理內容

- [Enable-AzureRmContextAutosave][enable] - 可在 Powershell 工作階段之間儲存內容。
  任何變更都會改變全域內容。
- [Disable-AzureRmContextAutosave][disable] - 關閉自動儲存內容。 需要每個新的 PowerShell 工作階段才能再次登入。
- [Select-AzureRmContext][select] - 選取內容作為預設值。 所有後續的 Cmdlet 都會使用此內容中的認證來進行驗證。
- [Disconnect-AzureRmAccount][remove-cred] - 移除與帳戶相關聯的所有認證和內容。
- [Remove-AzureRmContext][remove-context] - 將已命名的內容移除。
- [Rename-AzureRmContext][rename] - 將現有的內容重新命名。

對現有設定檔 Cmdlet 的變更

- [Add-AzureRmAccount][login] - 允許登入程序或目前使用者的範圍。
  允許驗證之後命名預設內容。
- [Import-AzureRmContext][import] - 允許登入程序或目前使用者的範圍。
- [Set-AzureRmContext][set-context] - 允許選取現有的已命名內容，以及對程序或目前使用者的範圍變更。

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
