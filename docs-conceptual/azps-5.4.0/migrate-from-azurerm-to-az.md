---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將 Azure PowerShell 指令碼從 AzureRM 遷移至新的 Az PowerShell 模組的步驟和工具。
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573630"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>將 Azure PowerShell 從 AzureRM 移轉至 Az

所有 AzureRM PowerShell 模組的版本已過時。 [Az PowerShell 模組](install-az-ps.md)現在是用來與 Azure 互動的建議 PowerShell 模組。

## <a name="why-a-new-module"></a>為何推出新模組？

最大且最重要的變更是自引進以 .NET Standard 程式庫為基礎的 [PowerShell](/powershell/scripting/overview) 後，其如今已成為跨平台產品。

如同 PowerShell 語言，我們致力於將 Azure 支援帶至所有平台。 我們的承諾表示需要更新 Azure PowerShell 模組，才能使用 .NET Standard 並與 PowerShell Core 和更新版本相容。 我們決定不修改現有的 AzureRM 模組並導入複雜的變更來加入這項支援，而是建立了 Az 模組。

建立新模組也讓我們的工程師可將 Cmdlet 和模組的設計與命名趨於一致。 現在，所有模組皆以 `Az.` 前置詞開頭，且 Cmdlet 全都採用 `Verb-AzNoun` 命名慣例。 之前，Cmdlet 名稱較長且不一致。

模組數目也已減少：某些與相同服務搭配運作的模組已結合在一起。 相同服務的管理平面和資料平面 Cmdlet 現在也全都包含在單一模組中。 對於手動管理相依性和匯入的使用者，此項合併將可簡化程序。

藉由進行這些重要變更，小組成員努力促使 Azure 與 PowerShell Cmdlet 的搭配使用比以往更簡便，並且可在更多平台上使用。

## <a name="upgrading-to-az-powershell"></a>升級至 Az PowerShell

針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用 Az。 為了更輕鬆地轉換，已開發 [AzureRM 至 Az 移轉工具組](https://github.com/Azure/azure-powershell-migration)。 不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到 Az PowerShell 模組。 若要深入了解為何會建立 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](new-azureps-module-az.md)。

新的 Cmdlet 名稱已設計為易於了解。 請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。 例如，舊 Cmdlet `New-AzureRMVm` 已變成 `New-AzVm`。
不過，移轉不僅只是熟悉新的 Cmdlet 名稱。 此外還有重新命名的模組、參數和其他重要變更。

若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>確定現有指令碼可使用最新的 AzureRM 版本

在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。
進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。

若要檢查您所安裝的 AzureRM 版本，請執行下列範例：

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

AzureRM **最新的** 可用版本為 **6.13.1**。 如果未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用本文和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。

如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。 如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>選項 1 (建議)：自動遷移您的 PowerShell 指令碼

此建議選項可將 AzureRM 指令碼遷移至 Az 所需的工作降到最低。

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>安裝 AzureRM 至 Az 移轉工具組

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>自動轉換指令碼

透過 AzureRM 至 Az 移轉工具組，您可以產生一個計劃，以判斷在對指令碼進行任何修改之前，以及在安裝 Az PowerShell 模組之前，要對其執行哪些變更。

[將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組](quickstart-migrate-azurerm-to-az-automatically.md)快速入門，會逐步引導您完成從 AzureRM 至 Az PowerShell 模組自動更新 PowerShell 指令碼的整個程序。

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>選項 2：使用相容性模式搭配 Enable-AzureRmAlias

當您處理新語法的更新時，Az 模組有相容性模式可協助您使用現有指令碼。 [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet 會透過別名啟用相容性模式。 此模式可讓您在最少修改的情況下使用現有的指令碼，同時也能將完整遷移至 Az。 根據預設，`Enable-AzureRmAlias` 只會啟用目前 PowerShell 工作階段的相容性別名。 使用其 `Scope` 參數，在 PowerShell 工作階段之間保存相容性別名。 如需詳細資訊，請參閱 [Enable-AzureRmAlias 參考文件](/powershell/module/az.accounts/enable-azurermalias)。

> [!IMPORTANT]
> 即使 Cmdlet 名稱已有別名，但 Az Cmdlet 仍可能有新的 (或重新命名的) 參數或已變更的傳回值。 請不要誤以為啟用別名就能完成移轉。 請參閱[完整重大變更清單](migrate-az-1.0.0.md)，找出您的指令碼可能需要更新之處。

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>選項 3：使用 Azure PowerShell 擴充功能，在 Visual Studio Code 中遷移您的指令碼

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>安裝適用於 Visual Studio Code 的 Azure PowerShell 擴充功能

安裝[適用於 VSCode 的 Azure PowerShell 擴充功能](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>手動轉換指令碼

1. 在 VSCode 中載入您的 AzureRM 指令碼
2. 開啟命令選擇區 `Ctrl+Shift+P`，然後選取 `Migrate Azure PowerShell script` 開始遷移
3. 選取來源版本 `AzureRM`
4. 遵循建議的動作，執行每個加底線的命令或參數。

## <a name="next-steps"></a>後續步驟

* [解除安裝 AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [安裝 Azure PowerShell](install-az-ps.md)
