---
title: 安裝並設定 Azure PowerShell | Microsoft Docs
description: 如何安裝並設定 Azure PowerShell 以供第一次使用。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: a10cb9496ff6822c6f4c10ab336dd21c85084da8
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell"></a>安裝並設定 Azure PowerShell

本文說明在 Windows 環境中安裝 Azure PowerShell 模組的步驟。
如果您想要在 macOS 或 Linux 上使用 Azure PowerShell，請參閱下列文章：[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。

從 PowerShell 資源庫安裝 Azure PowerShell 是慣用的安裝方法。

## <a name="step-1-install-powershellget"></a>步驟 1：安裝 PowerShellGet

從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。 確定您有適當版本的 PowerShellGet 及其他系統需求。 執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

您應該會看到類似下面的輸出：

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

您需要 PowerShellGet 1.1.2.0 版或更高版本。 若要更新 PowerShellGet，請使用下列命令：

```powershell
Install-Module PowerShellGet -Force
```

如果您未安裝 PowerShellGet，請參閱本文的[如何取得 PowerShellGet](#how-to-get-powershellget)一節。

> [!NOTE]
> 若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。 如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。

## <a name="step-2-install-azure-powershell"></a>步驟 2：安裝 Azure PowerShell

從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。 從提高權限的 PowerShell 工作階段執行下列命令︰

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

請回答「是」或「全部皆是」以繼續安裝。

> [!NOTE]
> 如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。

AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。 當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。

若有安裝舊版的 Azure PowerShell，則可能會出現錯誤。 若要解決此問題，請參閱本文的[更新為新版的 Azure PowerShell](#update-azps) 小節。

## <a name="step-3-load-the-azurerm-module"></a>步驟 3︰載入 AzureRM 模組
安裝模組後，您需要將模組載入您的 PowerShell 工作階段。 您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。 使用 `Import-Module`Cmdlet 載入模組，如下所示︰

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>後續步驟

如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：

* [開始使用 Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>報告問題和意見反應

如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-powershell/issues)一節中提出問題。 若要從命令列提供意見反應，請使用 `Send-Feedback` Cmdlet。

## <a name="frequently-asked-questions"></a>常見問題集

### <a name="how-to-get-powershellget"></a>如何取得 PowerShellGet

|案例|安裝指示|
|---|---|
|Windows 10<br/>Windows Server 2016|內建於 OS 包含的 Windows Management Framework (WMF) 5.0|
|我想要升級至 PowerShell 5|<ol><li>[安裝最新版的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>執行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|我是在採用 PowerShell 3 或 PowerShell 4 的 Windows 版本上執行|<ol><il>[取得 PackageManagement 模組](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>執行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>檢查 Azure PowerShell 的版本

雖然我們鼓勵您儘早升級至最新版本，但仍針對數個 Azure PowerShell 版本提供支援。 若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>對於傳統部署方法的支援

如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。 如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。 Azure 和 AzureRM 模組會共用通用相依性。 若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。

### <a id="update-azps"></a>更新為新版的 Azure PowerShell

若有安裝包括服務管理模組的舊版 Azure PowerShell，則可能會出現下列錯誤：

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

如錯誤訊息所述，您必須使用 -AllowClobber 參數來安裝模組。 使用下列命令：

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

如需詳細資訊，請參閱 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的說明主題。

### <a name="installing-module-versions-side-by-side"></a>並存安裝模組版本

PowerShellGet 安裝方法是唯一支援的多個版本安裝方法。 例如，您的指令碼可能是使用您沒有時間或資源更新的舊版 Azure PowerShell 所撰寫。 下列命令說明如何安裝多個 Azure PowerShell 版本︰

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

在一個 PowerShell 工作階段中只可以載入一個模組版本。 您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 AzureRM Cmdlet︰

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> 2.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。 載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。 這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。

### <a name="other-installation-methods"></a>其他安裝方法

如需有關使用 Web Platform Installer 或 MSI 套件進行安裝的資訊，請參閱[其他安裝方法](other-install.md)