---
title: 使用 MSI 安裝 Azure PowerShell
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d16aea3fa2059cd32f584134e2da43e01e3def31
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537236"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>使用 MSI 在 Windows 上安裝 Azure PowerShell

本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。 MSI 安裝程式是針對 PowerShell 資源庫可能受防火牆封鎖，或需要離線安裝程式的環境所提供。 建議使用 PowerShellGet 來安裝 Azure PowerShell。 如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-az-ps.md)。

## <a name="requirements"></a>需求

適用於 Azure PowerShell 的 MSI 安裝程式「僅」  適用於 Windows 上的 PowerShell 5.1。 若要在非 Windows 平台或較新版本的 PowerShell 上安裝，請[以 PowerShellGet 安裝](install-az-ps.md)。
若要檢查 PowerShell 版本，請執行下列命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

若要在 PowerShell 5.1 中使用 Azure PowerShell，您需要：

1. 視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)。 如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。
2. 安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 套件在 Windows 上安裝或更新

使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019) 取得) 安裝適用於 Windows 的 Azure PowerShell。 如果您已透過 MSI 安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。 MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。 因為模組的結構化方式，可能需要稍等一分鐘。

您必須針對每個啟動的新 PowerShell 工作階段重複此步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="provide-feedback"></a>提供意見反應

如果您發現 Azure Powershell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。
若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。
如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。
