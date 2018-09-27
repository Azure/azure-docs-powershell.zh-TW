---
title: Azure PowerShell 的其他安裝方式
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bf66e312557f047a9393e26b9de736c1c55c261
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178828"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>使用 MSI 在 Windows 上安裝 Azure PowerShell

本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。  
只有在您的系統需要時才使用這些安裝方法。 在 Windows 上安裝 Azure PowerShell 的建議方法是使用 PowerShellGet。 如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。

> [!NOTE]
> Azure PowerShell 6.x 版和更高版本無法再使用 Web Platform Installer 的安裝方法。 如果您需要使用 Web Platform Installer，請考慮改用 MSI，或可安裝舊版的 Azure PowerShell。

若要在 Docker 容器中執行 Azure PowerShell，請參閱[在 Docker 中執行 Azure PowerShell](azurerm-ps-in-docker.md)。

若要在 Linux 或 macOS 環境上安裝，請參閱[在 macOS 或 Linux 上安裝 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 套件在 Windows 上安裝或更新

您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 取得) 來安裝 Azure PowerShell。 如果您已利用 MSI 身分安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。 MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。 `AzureRM` 和 `Azure` 模組都已安裝。

> [!NOTE]
> 僅在您使用 Azure 傳統部署模型時，才使用 `Azure` 模組。

若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。 自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。
若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。