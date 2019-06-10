---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365727"
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

> [!IMPORTANT]
>
> 您可以同時安裝 AzureRM 和 Az 模組。 若您已安裝了兩個模組，__請勿啟用別名__。
> 啟用別名會讓 AzureRM Cmdlet 和 Az 命令別名產生衝突，且可能導致未預期的行為。
> 建議您在安裝 Az 模組之前，先將 AzureRM 解除安裝。 您可以隨時將 AzureRM 解除安裝，或啟用別名。 若要了解 AzureRM 命令別名，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。
> 如需解除安裝作的指示，請參閱[將 AzureRM 模組解除安裝](uninstall-az-ps.md#uninstall-the-azurerm-module)。 

若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。 若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
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

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。 因為模組的結構化方式，這可能需要幾秒鐘的時間。

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模組

由於 Az 模組的封裝方式，[Update-module](/powershell/module/powershellget/update-module) 命令將不會正確更新您的安裝。 Az 在技術上是中繼模組，其中包含與 Azure 服務互動的 Cmdlet 所屬的所有子模組。 這表示，若要更新 Azure PowerShell 模組，您必須__重新安裝__，而不只是__更新__。 其操作方式與安裝相同，但您可能需要新增 `-Force` 引數：

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
