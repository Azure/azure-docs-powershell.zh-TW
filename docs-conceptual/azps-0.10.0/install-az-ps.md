---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: c6767d99690a04d1001dd76a218cc90c9cecca39
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409879"
---
# <a name="install-azure-powershell"></a>安裝 Azure PowerShell

本文說明如何使用 [PowerShellGet](/powershell/scripting/gallery/installing-psget) 安裝 Azure PowerShell 模組。 這些指示適用於 Windows、macOS 和 Linux 平台。

Azure PowerShell 也可在 Azure [Cloud Shell](/azure/cloud-shell/overview) 取得。

## <a name="requirements"></a>需求

Azure PowerShell 可在 Windows 上與 PowerShell 5.1 或更新版本搭配運作，或在所有平台上與 PowerShell Core 6.x 和更新版本搭配運作。 您應為本身的作業系統安裝可使用的[最新版 PowerShell](/powershell/scripting/install/installing-powershell)。 在 PowerShell 6.2.4 和更新版本上執行時，Azure PowerShell 沒有額外的需求。

若要檢查 PowerShell 版本，請執行下列命令：

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

在 Windows 上的 PowerShell 5.1 中使用 Azure PowerShell：

1. 更新至 [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)。
   如果您是在 Windows 10 版本 1607 或更高版本上，則已安裝 PowerShell 5.1。
2. 安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。
3. 確定您有最新版的 PowerShellGet。 執行 `Install-Module -Name PowerShellGet -Force`。

## <a name="install-the-azure-powershell-module"></a>安裝 Azure PowerShell 模組

> [!WARNING]
> 我們不支援同時為 Windows 上的 PowerShell 5.1 安裝 AzureRM 和 Az 模組。 如果您需要在系統上保留可用的 AzureRM，請安裝適用於 PowerShell 6.2.4 或更新版本的 Az 模組。

使用 PowerShellGet Cmdlet 是慣用的安裝方法。 僅安裝適用於目前使用者的 Az 模組。 這是建議的安裝範圍。 這個方法在 Windows、macOS、Linux 平台上的做法相同。 從 PowerShell 工作階段執行下列命令︰

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

為系統上的所有使用者安裝模組需要較高的權限。 在 Windows 中使用 **Run as administrator** ，在 macOS 或 Linux 上使用 `sudo` 命令，以啟動 PowerShell 工作階段：

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Az 模組是 Azure PowerShell Cmdlet 的彙總套件模組。 安裝此模組會下載所有正式推出的 Az PowerShell 模組，並使這些模組的 Cmdlet 可供使用。

## <a name="install-offline"></a>離線安裝

在某些環境中，無法連線到 PowerShell 資源庫。 在這些情況下，您仍然可以使用下列其中一種方法來離線安裝：

* 將模組下載到您網路中的另一個位置，並使用該位置做為安裝來源。
  此方法可讓您將單一伺服器或檔案共用上的 PowerShell 模組 (已使用 PowerShellGet 部署) 快取到任何已中斷連線的系統上。 了解如何透過[使用本機 PowerShellGet 存放庫](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)設定本機存放庫，並安裝在中斷連線的系統上。
* [將 Azure PowerShell MSI 下載到連線至網路的電腦](install-az-ps-msi.md)，然後將安裝程式複製到系統，無需存取 PowerShell 資源庫。 請記住，MSI 安裝程式僅適用於 Windows 上的 PowerShell 5.1。
* 使用 [Save-Module](/powershell/module/PowershellGet/Save-Module) 將模組儲存至檔案共用，或將儲存至另一個來源，並手動將模組複製到其他電腦：

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>疑難排解

以下是安裝 Azure PowerShell 模組時常見的一些問題。 如果您遇到此處未列出的問題，請[在 GitHub 上提出問題](https://github.com/azure/azure-powershell/issues)。

### <a name="proxy-blocks-connection"></a>Proxy 封鎖連線

如果 `Install-Module` 顯示錯誤指出無法連線到 PowerShell 資源庫，表示您可能在 Proxy 後方。 不同的作業系統和網路環境在設定全系統的 Proxy 時會有不同的需求。 請連絡系統管理員以取得您的 Proxy 設定，並詢問如何為您的作業系統進行其設定。

PowerShell 本身不一定會設定為自動使用此 Proxy。 使用 PowerShell 5.1 和更新版本，並使用下列命令，將 PowerShell 工作階段設定為使用 Proxy：

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

如果您的作業系統認證已正確設定，此設定將會透過 Proxy 路由傳送 PowerShell 要求。 若要在工作階段之間保存此設定，請將命令新增至您的 [PowerShell 設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)。

若要安裝此套件，您的 Proxy 必須允許下列位址的 HTTPS 連線：

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module -Name Az` 手動匯入模組。
> 因為模組的結構化方式，這可能需要幾秒鐘的時間。

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模組

若要更新任何 PowerShell 模組，您應該使用先前安裝該模組的相同方法。 例如，如果您最初是使用 `Install-Module`，則應該使用 [Update-Module](/powershell/module/powershellget/update-module) 來取得最新版本。 如果您最初使用的是 MSI 套件，則應該下載並安裝新的 MSI 套件。

PowerShellGet Cmdlet 無法更新從 MSI 套件安裝的模組。 MSI 套件不會更新使用 PowerShellGet 安裝的模組。 如果您有任何使用 PowershellGet 進行更新的問題，請 **重新安裝** ，不要只是 **更新** 。 重新安裝的操作方式與安裝相同，但您可能需要新增 `-Force` 參數：

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

和 MSI 型安裝不同，使用 PowerShellGet 進行安裝或更新，不會移除您的系統上可能存在的較舊版本。 若要移除系統中的舊版 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-az-ps.md)。 如需有關 MSI 型安裝的詳細資訊，請參閱[使用 MSI 安裝 Azure PowerShell](install-az-ps-msi.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多個版本的 Azure PowerShell

您可以安裝多個版本的 Azure PowerShell。 若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-az-ps.md)。

如果您安裝了多個模組版本，模組會自動載入，`Import-Module` 則預設會載入最新的版本。

您可使用 `-RequiredVersion` 參數來安裝或載入特定版本的 `Az` 模組：

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a>提供意見反應

如果您發現 Azure PowerShell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。 若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。 如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。
