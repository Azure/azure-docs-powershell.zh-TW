---
title: 使用 MSI 安裝 Azure PowerShell
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409511"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>使用 MSI 在 Windows 上安裝 Azure PowerShell

本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。 MSI 安裝程式是針對 PowerShell 資源庫可能受防火牆封鎖，或需要離線安裝程式的環境所提供。 建議使用 PowerShellGet 來安裝 Azure PowerShell。 如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-az-ps.md)。

## <a name="requirements"></a>需求

Windows 上的 MSI 安裝程式僅用於安裝適用於 PowerShell 5.1 的 Azure PowerShell。 若要在非 Windows 平台或較新版本的 PowerShell 上安裝，請[以 PowerShellGet 安裝](install-az-ps.md)。 若要檢查 PowerShell 版本，請執行下列命令：

```powershell-interactive
$PSVersionTable.PSVersion
```

若要在 PowerShell 5.1 中使用 Azure PowerShell，您需要：

1. 視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)。 如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。
2. 安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。

## <a name="install-or-update-on-windows-using-the-msi-package"></a>使用 MSI 套件在 Windows 上安裝或更新

可從 [GitHub](https://github.com/Azure/azure-powershell/releases) 取得 Azure PowerShell 的 MSI 套件：

1. 前往 https://github.com/Azure/azure-powershell/releases。
2. 尋找 Azure PowerShell 的最新資源庫模組 (依時間順序列出，而且通常只是沒有名稱的發行版本，例如 "4.7.0")。
3. 向下捲動至修補程式附註的底部，然後按一下 [資產] 旁的箭號，以顯示 MSI 選項。
4. 按一下您選擇的 Az Cmdlet MSI 以開始下載。

如果您已使用 MSI 安裝舊版的 Azure PowerShell，安裝程式會自動移除這些模組。 MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。

若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> 如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。 因為模組的結構化方式，可能需要稍等一分鐘。

您必須針對每個啟動的新 PowerShell 工作階段重複此步驟。 若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。

## <a name="provide-feedback"></a>提供意見反應

如果您發現 Azure PowerShell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。 若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。

## <a name="next-steps"></a>後續步驟

若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。 如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。
