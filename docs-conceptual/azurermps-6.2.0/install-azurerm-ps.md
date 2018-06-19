---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323096"
---
# <a name="install-azure-powershell-with-powershellget"></a>使用 PowerShellGet 安裝 Azure PowerShell

本文說明在 Windows 環境中使用 PowerShellGet 安裝 Azure PowerShell 模組的步驟。  這是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。

如果您想要在 macOS 或 Linux 上使用 Azure PowerShell，請參閱下列文章：[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="system-requirements"></a>系統需求

Azure PowerShell 版本 6.1.0 需要 PowerShell 版本 5.0 (或更新版本)。 如需升級到 PowerShell 5.0 的詳細資訊，請參閱[升級現有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

PowerShellGet 會自動包含在 PowerShell 5.0 中。

## <a name="install-or-update-the-azure-powershell-module"></a>安裝或更新 Azure PowerShell 模組

從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。 從提高權限的 PowerShell 工作階段執行下列命令︰

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> 這個命令會更新您系統上的任何現有 Azure PowerShell 安裝。 如果您需要安裝一個以上的版本，請參閱[可以安裝多個版本的 Azure PowerShell 嗎？](#multiple-versions)的常見問題集答案

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答「是」或「全部皆是」以繼續安裝。

> [!NOTE]
> 如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。

AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。 當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。

## <a name="load-the-azure-powershell-module"></a>載入 Azure PowerShell 模組

安裝模組後，您需要將模組載入您的 PowerShell 工作階段。 您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。 使用 `Import-Module`Cmdlet 載入模組，如下所示︰

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>報告問題和意見反應

如果您遇到任何工具錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。 若要從命令列提供意見反應，請使用 `Send-Feedback` Cmdlet。

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：

* [開始使用 Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>常見問題集

### <a id="helpmechoose"></a>如何檢查 Azure PowerShell 版本？

雖然我們鼓勵您儘早升級至最新版本，但仍針對數個 Azure PowerShell 版本提供支援。 若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>可以針對 Azure 傳統部署使用 Azure PowerShell 嗎？

如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。 如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。 Azure 和 AzureRM 模組會共用通用相依性。 若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>可以安裝多個版本的 Azure PowerShell 嗎？

PowerShellGet 是唯一支援安裝多個版本的方法。 若要安裝多個版本，您可以將 `-RequiredVersion` 參數新增至 `Install-Module` Cmdlet。 例如，若要同時安裝 6.1.0 版和 1.2.9 版：

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

在一個 PowerShell 工作階段中只可以載入一個模組版本。 您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 Azure PowerShell 模組。

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> 2.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。 載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。 這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。
