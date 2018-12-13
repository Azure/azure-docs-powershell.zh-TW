---
title: Azure PowerShell Az 模組簡介
description: 介紹新的 Azure PowerShell 模組 Az，也就是 AzureRM 模組的替代項目。
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217536"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>新的 Azure PowerShell Az 模組簡介

從 2018 年 11 月起，Azure PowerShell `Az` 模組即可提供完整公開預覽版。
Az 可提供較短的命令、改進穩定性，以及支援 Windows、macOS 和 Linux。 Az 也提供功能同位以及從 AzureRM 遷移的簡單路徑。

Az 使用會 .NET Standard 程式庫，這表示它在 PowerShell 5.x 和 PowerShell 6.x 上執行。
因為 PowerShell 6.x 可以在 Linux、macOS 和 Windows 上執行，這表示 Az 適用於所有平台。
使用 .NET Standard，可在對使用者造成最小影響的情況下，讓我們統一 Azure PowerShell 的程式碼基底。

Az 是新模組，所以已重設版本。 第一個穩定版本會是 1.0，但是自 2018 年 11 月起，此模組有 AzureRm 的功能同位。

## <a name="upgrade-to-az"></a>升級至 Az

建議使用者升級至新的 `Az` 模組。 若要這樣做：

* [將 Azure PowerShell AzureRM 模組解除安裝](/powershell/azure/uninstall-azurerm-ps)
* [安裝 Azure PowerShell Az 模組](/powershell/azure/install-az-ps)
* 當您熟悉新的命令集時，請使用 `Enable-AzureRMAlias` 啟用 AzureRM 的相容性模式。

## <a name="migrate-existing-scripts-to-az"></a>將現有指令碼遷移至 Az

主要更新不太方便。 不過，當您處理新語法的更新時，`Az` 模組有相容性模式可協助您使用現有指令碼。 使用 `Enable-AzureRmAlias` Cmdlet 來啟用 `AzureRM` 相容性模式。 此 Cmdlet 會將 `AzureRM` Cmdlet 名稱定義為新 `Az` Cmdlet 名稱的別名。

新的 Cmdlet 名稱已設計為易於了解。 請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。 例如，舊命令 `New-AzureRmVm` 已變成 `New-AzVm`。

如需移轉程序的完整說明，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。

## <a name="the-future-of-support-for-azurerm"></a>未來的 AzureRM 支援

在 2018 年 12 月發生 `Az` 1.0 版後，現有 `AzureRM` 模組不會再收到新的 Cmdlet 或功能。 不過，`AzureRM` 仍會正式維護，而且會收到錯誤修正。 若要保持最新的 Azure 服務和功能，您應該切換到 `Az` 模組。