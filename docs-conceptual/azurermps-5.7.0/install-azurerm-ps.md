---
title: 使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5f7f65aa25d86feb77a85fc28d122118216542cc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588038"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell

本文說明在 Windows 環境中使用 PowerShellGet 安裝 Azure PowerShell 模組的步驟。 PowerShellGet 和模組管理是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。

如需在其他平台上安裝 Azure PowerShell 的指示，請參閱[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。

這個版本的 Azure PowerShell 不支援 Azure 傳統部署模型。 如需傳統部署的支援，請遵循[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)中的指示。

## <a name="requirements"></a>需求

若要安裝 Azure PowerShell，您需要 PowerShellGet 1.1.2.0 版或更高版本。 若要檢查您的系統上是否可使用，請執行下列命令：

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

您應該會看到類似下面的輸出：

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

若您需要更新 PowerShellGet 的安裝，請執行下列命令：

```powershell-interactive
Install-Module PowerShellGet -Force
```

若您尚未安裝 PowerShellGet，請遵循下表中適用您系統的指示。

|案例|安裝指示|
|---|---|
|Windows 10<br/>Windows Server 2016|內建於 OS 包含的 Windows Management Framework (WMF) 5.0|
|升級至 PowerShell 5| <ol><li>[安裝最新版的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>執行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows 與 PowerShell 3 或 PowerShell 4|<ol><il>[取得 PackageManagement 模組](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>執行以下命令：<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> 若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。 如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。
>
> [!IMPORTANT]
> 本文件中所述的模組 AzureRM 會使用 .NET Framework。 這會造成與使用 .NET Core 的 PowerShell 6.0 不相容。 如果您使用 PowerShell 6.0，請遵循[適用於 macOS 和 Linux 的安裝指示](install-azurermps-maclinux.md)。

## <a name="install-the-azure-powershell-module"></a>安裝 Azure PowerShell 模組

您需要較高的權限，以從 PowerShell 資源庫安裝模組。 若要安裝 Azure PowerShell，請在已提升權限的工作階段中執行下列命令：

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> 如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。

根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。 第一次使用 PSGallery 時，您會看到下列提示：

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

請回答 `Yes` 或 `Yes to All` 以繼續安裝。

`AzureRM` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。 安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。

## <a name="sign-in"></a>登入

若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。
若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="update-the-azure-powershell-module"></a>更新 Azure PowerShell 模組

您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。 這個命令「不會」將舊版解除安裝。

```powershell-interactive
Update-Module -Name AzureRM
```

如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。

## <a name="use-multiple-versions-of-azure-powershell"></a>使用多個版本的 Azure PowerShell

可以安裝多個版本的 Azure PowerShell。 如果您使用內部部署 Azure Stack 資源、執行較舊版本的 Windows 而無法更新至 PowerShell 5.0，或使用 Azure 傳統部署模型，可能需要一個以上的版本。 若要安裝較舊的版本，請在安裝時提供 `-RequiredVersion` 引數。

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

當您載入 Azure PowerShell 模組時，預設會載入最新版本。 若要載入不同的版本，請提供 `-RequiredVersion` 引數。

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>提供意見反應

如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。
若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。
