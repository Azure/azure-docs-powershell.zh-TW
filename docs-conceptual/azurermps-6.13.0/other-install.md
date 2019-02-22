---
title: Azure PowerShell 的其他安裝方式
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0976fd51b26010702d200cee445d93269405416c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153122"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>使用 MSI 在 Windows 上安裝 Azure PowerShell

本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。  
只有在您的系統需要時才使用這些安裝方法。 在 Windows 上安裝 Azure PowerShell 的建議方法是使用 PowerShellGet。 如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。

> [!NOTE]
> Azure PowerShell 6.x 版和更高版本無法再使用 Web Platform Installer 的安裝方法。 如果您需要使用 Web Platform Installer，請考慮改用 MSI，或可安裝舊版的 Azure PowerShell。

若要在 Linux 或 macOS 環境上安裝，請參閱[在 macOS 或 Linux 上安裝 Azure PowerShell](install-azurermps-maclinux.md)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 套件在 Windows 上安裝或更新

您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) 取得) 來安裝適用於 Azure PowerShell 5.x 的 Azure PowerShell。 如果您已利用 MSI 身分安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。 MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。 `AzureRM` 和 `Azure` 模組都已安裝。

> [!NOTE]
> 僅在您使用 Azure 傳統部署模型時，才使用 `Azure` 模組。

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module AzureRM` 來手動匯入模組。 因為模組的結構化方式，這可能需要幾秒鐘的時間。

您必須針對每個啟動的新 PowerShell 工作階段重複此步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。
