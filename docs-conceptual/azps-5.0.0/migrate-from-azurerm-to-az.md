---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753392"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>將 Azure PowerShell 從 AzureRM 移轉至 Az

所有 AzureRM PowerShell 模組的版本已過時，但依然可支援。 [Az PowerShell 模組](install-az-ps.md)現在是用來與 Azure 互動的建議 PowerShell 模組。

針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。 為了更輕鬆地轉換，已開發 [AzureRM 至 Az 移轉工具組](https://github.com/Azure/azure-powershell-migration)。 不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到 Az PowerShell 模組。 若要深入了解為何會建立 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](new-azureps-module-az.md)。

若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>確定現有指令碼可使用最新的 AzureRM 版本

在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。
進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。

若要檢查您所安裝的 AzureRM 版本，請執行下列範例：

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

AzureRM **最新的** 可用版本為 **6.13.1** 。 如果您未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用本文和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。

如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。 如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>安裝 AzureRM 至 Az 移轉工具組

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>自動遷移您的 PowerShell 指令碼

透過 AzureRM 至 Az 移轉工具組，您可以產生一個計劃，以判斷在對指令碼進行任何修改之前，以及在安裝 Az PowerShell 模組之前，要對其執行哪些變更。

[將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組](quickstart-migrate-azurerm-to-az-automatically.md)快速入門，會逐步引導您完成從 AzureRM 至 Az PowerShell 模組自動更新 PowerShell 指令碼的整個程序。

## <a name="next-steps"></a>後續步驟

[安裝 Azure PowerShell](install-az-ps.md)
[解除安裝 AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
