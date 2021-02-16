---
title: Azure PowerShell Az 模組簡介
description: 介紹新的 Azure PowerShell 模組 Az，也就是 AzureRM 模組的替代項目。
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: e2a68814550f42e912ea5149e3bdf7c6cc22de13
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404032"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>新的 Azure PowerShell Az 模組簡介

從 2018 年 12 月開始，Azure PowerShell Az 模組已正式運作，並已成為與 Azure 互動時的預期 PowerShell 模組。 Az 可提供較短的命令、改進的穩定性和跨平台支援。 Az 也具有與 AzureRM 的功能同位，提供簡單的移轉路徑。

透過 Az 模組，Azure PowerShell 現已相容於 Windows 上的 PowerShell 5.1 以及所有支援平台上的 PowerShell Core 6.x 和更新版本，包括 Windows、macOS 和 Linux。

Az 是新模組，因此版本已重設為 1.0.0。

## <a name="why-a-new-module"></a>為何推出新模組？

重大更新可能不便執行，因此我們必須讓您了解我們為何決定導入一組附有新 Cmdlet 的新模組，供您從 PowerShell 與 Azure 互動。

最大且最重要的變更是，自從引進 [PowerShell](/powershell/scripting/overview) (以 .NET Standard 程式庫為基礎) 後，PowerShell 已成為跨平台產品。
我們致力於將 Azure 支援導入所有平台，而這意味著 Azure PowerShell 模組必須進行更新，以使用 .NET Standard 並且與 PowerShell Core 相容。 我們決定不以現有的 AzureRM 模組導入複雜的變更來加入這項支援，而是建立了 Az 模組。

建立新模組也讓我們的工程師有機會可將 Cmdlet 和模組的設計與命名趨於一致。 現在，所有模組皆以 `Az.` 前置詞開頭，且 Cmdlet 全都採用 _動詞_-`Az`_名詞_ 的格式。 過去，Cmdlet 名稱不僅較長，這些名稱也有不一致的情況。

模組數目也已減少：某些與相同服務搭配運作的模組已彙整在一起。 管理平面和資料平面 Cmdlet 現在也全都包含在其服務的單一模組中。 對於手動管理相依性和匯入的使用者，其作業將可因此而簡化。

藉由進行這些需要建置新 Azure PowerShell 模組的重要變更，小組成員努力促使 Azure 與 PowerShell Cmdlet 的搭配使用比以往更簡便，並且可在更多平台上使用。

## <a name="upgrade-to-az"></a>升級至 Az

為了運用 PowerShell 中的最新 Azure 功能，您應盡速移轉至 Az 模組。 若您尚未準備好要安裝 Az 模組來取代 AzureRM，您可以透過下列方式試用 Az：

- 在 `PowerShell` 環境中使用 [Azure Cloud Shell](/azure/cloud-shell/overview)。 Azure Cloud Shell 是一種以瀏覽器為基礎的殼層環境，隨附有已安裝的 Az 模組，且已啟用 `Enable-AzureRM` 相容性別名。
- 保留隨著 PowerShell 5.1 for Windows 而安裝的 AzureRM 模組，但安裝適用於 PowerShell 6.2.4 或更新版本的 Az 模組。 PowerShell 5.1 for Windows 以及 PowerShell 6.2.4 和更新版本分別使用不同的模組集合。 請依照指示安裝[最新版 PowerShell](/powershell/scripting/install/installing-powershell)，然後從 PowerShell 6.2.4 或更新版本[安裝 Az 模組](install-az-ps.md)。

若要從現有的 AzureRM 安裝升級：

1. [將 Azure PowerShell AzureRM 模組解除安裝](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [安裝 Azure PowerShell Az 模組](install-az-ps.md)
3. **選擇性**：當您熟悉新的命令集時，請使用 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) 啟用相容性模式來新增 AzureRM Cmdlet 的別名。 如需詳細資訊，請參閱下一節或[開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)。

## <a name="migrate-existing-scripts-to-az"></a>將現有指令碼遷移至 Az

新的 Cmdlet 名稱已設計為易於了解。 請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。 例如，舊命令 `New-AzureRMVm` 已變成 `New-AzVm`。
不過，移轉不僅只是熟悉新的 Cmdlet 名稱：此外還有重新命名的模組、參數和其他重要變更。

我們有數個資源，可協助您執行從 AzureRM 移轉至 Az 的程序：

- [開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)
- [從 AzureRM 到 Az 1.0.0 的重大變更完整清單](migrate-az-1.0.0.md)
- [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet

當您處理新語法的更新時，Az 模組有相容性模式可協助您使用現有指令碼。 [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet 會透過別名啟用相容性模式，讓您在最少的修改下使用現有的指令碼，同時完成完整移轉至 Az 的作業。

> [!IMPORTANT]
> 即使 Cmdlet 名稱已有別名，但 Az Cmdlet 仍可能有新的 (或重新命名的) 參數或已變更的傳回值。 請不要誤以為啟用別名就能完成移轉。 請參閱[完整重大變更清單](migrate-az-1.0.0.md)，找出您的指令碼可能需要更新之處。

## <a name="support-for-azurerm"></a>對 AzureRM 的支援

由於 Az PowerShell 模組現在具備 AzureRM PowerShell 模組的所有功能，因此我們將于2024年2月29日淘汰 AzureRM PowerShell 模組。

若要避免服務中斷，請將使用 AzureRM PowerShell 模組的 [腳本更新為在](https://aka.ms/azpsmigrate) 2024 年2月29日之前使用 Az powershell 模組。 若要自動更新您的腳本，請遵循 [快速入門手冊](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically)。
