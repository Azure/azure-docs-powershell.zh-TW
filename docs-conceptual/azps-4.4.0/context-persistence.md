---
title: Azure 內容和登入認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/14/2020
ms.locfileid: "86381786"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell 內容物件

Azure PowerShell 會使用 _Azure PowerShell 內容物件_ (Azure 內容) 來保存訂用帳戶和驗證資訊。 如果您有多個訂用帳戶，Azure 內容可讓您選取要執行 Azure PowerShell Cmdlet 的訂用帳戶。 Azure 內容也可用來跨多個 PowerShell 工作階段儲存登入資訊，以及執行背景工作。

本文將說明如何管理 Azure 內容，而非管理訂用帳戶或帳戶。 如果您想要管理使用者、訂用帳戶、租用戶或其他帳戶資訊，請參閱 [Azure Active Directory](/azure/active-directory) 文件。 若要了解如何使用內容來執行背景或平行工作，請在熟悉 Azure 內容後，參閱[在 PowerShell 作業中使用 Azure PowerShell Cmdlet](using-psjobs.md)。

## <a name="overview-of-azure-context-objects"></a>Azure 內容物件概觀

Azure 內容是 PowerShell 物件，代表您對其執行命令的有效訂用帳戶，以及連線至 Azure 雲端所需的驗證資訊。 透過 Azure 內容，Azure PowerShell 就不需要在您每次切換訂用帳戶時重新驗證您的帳戶。 Azure 內容包含下列各項：

* 用來透過 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) 登入 Azure 的_帳戶_。 就帳戶的觀點而言，Azure 內容會將使用者、應用程式識別碼和服務主體等同視之。
* 有效_訂用帳戶_是 Microsoft 提供的服務合約，用來建立和執行與_租用戶_相關聯的 Azure 資源。 租用戶在文件中或使用 Active Directory 時，通常稱為_組織_。
* _權杖快取_的參考是用來存取 Azure 雲端的預存驗證權杖。 此權杖的儲存位置及其保存的時間長度，取決於[內容自動儲存設定](#save-azure-contexts-across-powershell-sessions)。

如需這些字詞的詳細資訊，請參閱 [Azure Active Directory 術語](/azure/active-directory/fundamentals/active-directory-whatis#terminology)。 Azure 內容所使用的驗證權杖與持續性工作階段中其他已儲存的權杖相同。 

當您使用 `Connect-AzAccount` 登入時，系統會為您的預設訂用帳戶建立至少一個 Azure 內容。 `Connect-AzAccount` 傳回的物件是預設的 Azure 內容，用於其餘的 PowerShell 工作階段。

## <a name="get-azure-contexts"></a>取得 Azure 內容

可用的 Azure 內容可使用 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) Cmdlet 來擷取。 您可以使用 `-ListAvailable` 列出所有可用的內容：

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

或依名稱取得內容：

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

內容名稱可能與相關聯的訂用帳戶名稱不同。

> [!IMPORTANT]
> 可用的 Azure 內容__不一定__是您可用的訂用帳戶。 Azure 內容僅代表本機儲存的資訊。 您可以使用 [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) Cmdlet 取得訂用帳戶。

## <a name="create-a-new-azure-context-from-subscription-information"></a>從訂用帳戶資訊建立新的 Azure 內容

[Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) Cmdlet 可用來建立新的 Azure 內容，並將其設定為有效內容。
要建立新的 Azure 內容，最簡單的方式是使用現有的訂用帳戶資訊。 此 Cmdlet 依設計會使用 `Get-AzSubscription` 的輸出物件作為管線值，並設定新的 Azure 內容：

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

或者，視需要提供訂用帳戶名稱或識別碼和租用戶識別碼：

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

如果省略 `-Name` 引數，則會以訂用帳戶的名稱和識別碼作為 `Subscription Name (subscription-id)` 格式的內容名稱。

## <a name="change-the-active-azure-context"></a>變更有效的 Azure 內容

`Set-AzContext` 和 [Select-AzContext](/powershell/module/az.accounts/set-azcontext) 都可用來變更有效的 Azure 內容。 如[建立新的 Azure 內容](#create-a-new-azure-context-from-subscription-information)中所說明，`Set-AzContext` 會為訂用帳戶建立新的 Azure 內容 (如果沒有的話)，然後切換為以該內容作為有效內容。

`Select-AzContext` 僅適用於現有的 Azure 內容，且其運作方式與使用 `Set-AzContext -Context` 時類似，但正規用途為管線輸送：

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

如同 Azure PowerShell 中的許多其他帳戶和內容管理命令，`Set-AzContext` 和 `Select-AzContext` 均支援 `-Scope` 引數，讓您可以控制內容的有效期間。 `-Scope` 可讓您直接變更單一工作階段的有效內容，而無須變更預設值：

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

若要避免切換整個 PowerShell 工作階段的內容，您可以使用 `-AzContext` 引數對指定內容執行所有的 Azure PowerShell 命令：

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

以 Azure PowerShell Cmdlet 處理內容的另一項主要用途，是執行背景命令。 若要深入了解如何使用 Azure PowerShell 執行 PowerShell 作業，請參閱[在 PowerShell 作業中執行 Azure PowerShell Cmdlet](using-psjobs.md)。

## <a name="save-azure-contexts-across-powershell-sessions"></a>跨 PowerShell 工作階段儲存 Azure 內容

根據預設，Azure 內容會儲存起來以在 PowerShell 工作階段之間使用。 您可以透過下列方式變更此行為︰

* 搭配使用 `-Scope Process` 與 `Connect-AzAccount` 登入。

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  在此登入的過程中傳回的 Azure 內容，有效性_僅_及於目前的工作階段，且無論 Azure PowerShell 內容自動儲存設定為何，都不會自動儲存。
* 使用 [Disable-AzCoNtextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) Cmdlet 將 AzurePowershell 的內容自動儲存停用。
  停用內容自動儲存並__不會__清除任何已儲存的權杖。 若要了解如何清除已儲存的 Azure 內容資訊，請參閱[移除 Azure 內容和認證](#remove-azure-contexts-and-stored-credentials)。
* 若要明確啟用 Azure 內容自動儲存，可以使用 [Enable-AzCoNtextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) Cmdlet 來啟用。 自動儲存啟用時，所有使用者內容都會儲存在本機，以供後續的 PowerShell 工作階段使用。
* 使用 [Save-AzContext](/powershell/module/az.accounts/save-azcontext) 手動儲存內容以供未來的 PowerShell 工作階段使用，並可在 [Import-AzContext](/powershell/module/az.accounts/import-azcontext) 來載入：

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> 停用內容自動儲存並__不會__清除任何已儲存的預存內容資訊。 若要移除已儲存的資訊，請使用 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) Cmdlet。 如需移除已儲存內容的詳細資訊，請參閱[移除內容和認證](#remove-azure-contexts-and-stored-credentials)。

前述每個命令都支援 `-Scope` 參數，此參數可使用 `Process` 值而僅套用至目前執行中的程序。 例如，若要確保在結束 PowerShell 工作階段之後不會儲存新建立的內容：

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

內容資訊和權杖都會儲存在 Windows 上的 `$env:USERPROFILE\.Azure` 目錄中，以及其他平台的 `$HOME/.Azure` 中。 敏感性資訊 (例如訂用帳戶識別碼和租用戶識別碼) 可能仍會透過記錄或已儲存的內容公開於已儲存的資訊中。 若要了解如何清除已儲存的資訊，請參閱[移除內容和認證](#remove-azure-contexts-and-stored-credentials)一節。

## <a name="remove-azure-contexts-and-stored-credentials"></a>移除 Azure 內容和已儲存的認證

若要清除 Azure 內容和認證：

* 使用 [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) 登出帳戶。
  您可以透過帳戶或內容登出任何帳戶：

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  中斷連線後一律會移除已儲存的驗證權杖，並清除與中斷連線的使用者或內容相關聯的已儲存內容。
* 使用 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext)。 此 Cmdlet 一律會移除已儲存的內容和驗證權杖，而且也會將您登出。
* 使用 [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) 移除內容：
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  如果您移除有效內容，您將會與 Azure 中斷連線，而需要使用 `Connect-AzAccount` 重新進行驗證。

## <a name="see-also"></a>另請參閱

* [在 PowerShell 作業中執行 Azure PowerShell Cmdlet](using-psjobs.md)
* [Azure Active Directory 術語](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Az.Accounts 參考](/powershell/module/az.accounts)
