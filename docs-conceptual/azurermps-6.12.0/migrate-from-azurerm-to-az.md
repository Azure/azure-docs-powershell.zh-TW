---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274887"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>從 AzureRM 遷移至 Azure PowerShell Az

Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。
針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。 為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。 不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>確保現有指令碼可使用最新的 AzureRM 版本

這是最重要的步驟！ 執行現有指令碼，並確保它們能使用「最新」版的 AzureRM (__6.12.0__)。 如果指令碼沒有作用，請務必閱讀 [AzureRM 移轉指南](migration-guide.6.0.0.md)。

## <a name="install-the-azure-powershell-az-module"></a>安裝 Azure PowerShell Az 模組

第一個步驟是在您的平台上安裝 Az 模組。 若要安裝 Az，您必須將 AzureRM 解除安裝。
在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。

若要安裝 Azure PowerShell Az 模組，請遵循下列步驟：

* [將 AzureRM 模組解除安裝](uninstall-azurerm-ps.md)。 務必移除 AzureRM 的「所有」安裝版本，而不只是最近版本。
* [安裝 Az 模組](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>啟用 AzureRM 別名模式

將 AzureRM 解除安裝且您的指令碼使用最新的 AzureRM 版本，現在可以啟用 Az 模組的相容性模式。 透過以下命令啟用相容性：

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 `Az` 模組。 這些別名會寫入至所選範圍的使用者設定檔。 如果沒有使用者設定檔存在，則會建立一個。

> [!WARNING]
>
> 您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做！ 別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。 全系統啟用別名，也會對在其本機範圍內安裝 `AzureRM` 的其他使用者造成問題。

啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。 

## <a name="change-module-imports-and-cmdlet-names"></a>變更模組匯入和 Cmdlet 名稱

一般情況下，模組名稱已變更，所以 `AzureRM` 和 `Azure` 會成為 `Az`，而 Cmdlet 也是如此。
例如，`AzureRM.Compute` 模組已重新命名為 `Az.Compute`。 `New-AzureRmVM` 已成為 `New-AzVM`，而 `Get-AzureStorageBlob` 現在為 `Get-AzStorageBlob`。

此命名變更有一些例外狀況，您應該在進行任何重新命名之前加以留意：

| AzureRM 模組 | Az 模組 |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>總結

依照下列步驟，您可以將所有現有的指令碼更新為使用新模組。 如果您對於讓移轉變困難的這些步驟有任何疑問或問題，請對本文發表意見，以便我們改進指示。