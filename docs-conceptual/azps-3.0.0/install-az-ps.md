---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062321"
---
# <a name="install-the-azure-powershell-module"></a>安裝 Azure PowerShell 模組

本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。 這些指示適用於 Windows、macOS 和 Linux 平台。 至於 Az 模組，目前不支援其他安裝方法。

## <a name="requirements"></a>需求

Azure PowerShell 可在 Windows 上與 PowerShell 5.1 或更新版本搭配運作，或在所有平台上與 PowerShell Core 6.x 和更新版本搭配運作。 如果您不確定是否有 PowerShell，或不確定是在 macOS 還是 Linux 上，請[安裝最新版的 PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core)。

若要檢查 PowerShell 版本，請執行下列命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

若要在 Windows 上的 PowerShell 5.1 中執行 Azure PowerShell：

1. 視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)。 如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。
2. 安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。

使用 PowerShell Core 時，Azure PowerShell 沒有額外的需求。

## <a name="install-the-azure-powershell-module"></a>安裝 Azure PowerShell 模組

> [!WARNING]
> 您__無法__同時為 PowerShell 5.1 for Windows 安裝 AzureRM 和 Az 模組。 如果您需要在系統上保留可用的 AzureRM，請安裝適用於 PowerShell Core 6.x 或更新版本的 Az 模組。 若要這樣做，請[安裝 PowerShell Core 6.x 或更新版本](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows)，然後在 PowerShell Core 終端機中依照這些指示操作。

建議的安裝方法是僅供活躍使用者安裝：

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

如果您希望供系統中的所有使用者安裝，則需要系統管理員權限。 在提高權限的 PowerShell 工作階段中以系統管理員身份執行；若使用 macOS 或 Linux 則使用 `sudo` 命令執行：

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

Az 模組是 Azure PowerShell Cmdlet 的彙總套件模組。 安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。

## <a name="install-offline"></a>離線安裝

在某些環境中，無法連線到 PowerShell 資源庫。 在這些情況下，您仍然可以使用下列其中一種方法來離線安裝：

* 將模組下載到另一個位置，並使用該位置做為網路上的安裝來源。 這項流程十分複雜，但可讓您將單一伺服器或檔案共用上的 PowerShell 模組 (已使用 PowerShellGet 部署) 快取到任何已中斷連線的系統上。 了解如何透過[使用本機 PowerShellGet 存放庫](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)設定本機存放庫，並安裝在中斷連線的系統上。
* [將 Azure PowerShell MSI 下載到連線至網路的電腦](install-az-ps-msi.md)，然後將安裝程式複製到系統，無需存取 PowerShell 資源庫。 請記住，MSI 安裝程式僅適用於 Windows 上的 PowerShell 5.1。
* 使用 [Save-Module](/powershell/module/PowershellGet/Save-Module) 將模組儲存至檔案共用，或將儲存至另一個來源，並手動將模組複製到其他電腦：
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>疑難排解

以下是安裝 Azure PowerShell 模組時常見的一些問題。 如果您遇到此處未列出的問題，請[在 GitHub 上提出問題](https://github.com/azure/azure-powershell/issues)。

### <a name="proxy-blocks-connection"></a>Proxy 封鎖連線

如果 `Install-Module` 顯示錯誤指出無法連線到 PowerShell 資源庫，表示您可能在 Proxy 後方。 不同的作業系統在設定全系統的 Proxy 時會有不同的需求，此處並未詳盡說明。 請連絡系統管理員以取得您的 Proxy 設定，並詢問如何為您的 OS 進行其設定。

PowerShell 本身不一定會設定為自動使用此 Proxy。 使用 PowerShell 5.1 和更新版本時，請使用下列命令，設定要用於 PowerShell 工作階段的 Proxy：

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

如果您的作業系統認證已正確設定，此時將會透過 Proxy 路由傳送 PowerShell 要求。
若要在工作階段之間保存此設定，請將命令新增至 [PowerShell 設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)。

若要安裝套件，您的 Proxy 必須允許下列位址的 HTTPS 連線：

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 手動匯入模組。 因為模組的結構化方式，這可能需要幾秒鐘的時間。

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模組

由於 Az 模組的封裝方式，[Update-module](/powershell/module/powershellget/update-module) 命令將不會正確更新您的安裝。 安裝 Az 模組時，此模組實際上會收集並安裝其所有相依的子模組；這些子模組會提供每個服務的 Cmdlet。
這表示，若要更新 Azure PowerShell 模組，您必須__重新安裝__，而不只是__更新__。 其操作方式與安裝相同，但您可能需要新增 `-Force` 引數：

```powershell
Install-Module -Name Az -AllowClobber -Force
```

雖然這可以覆寫已安裝的模組，但您的系統上仍可能殘留較舊的版本。
若要了解如何從系統中移除舊版 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-az-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多個版本的 Azure PowerShell

您可以安裝多個版本的 Azure PowerShell。 若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-az-ps.md)。

您可使用 `-RequiredVersion` 引數來安裝或載入特定版本的 `Az` 模組：

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

如果您安裝了多個模組版本，模組會自動載入，`Import-Module` 則預設會載入最新的版本。

## <a name="provide-feedback"></a>提供意見反應

如果您發現 Azure Powershell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。
若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。
如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。
