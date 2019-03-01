---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837702"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>從 AzureRM 遷移至 Azure PowerShell Az

Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。
針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。 為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。 不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。

若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱 [Az 1.0.0 的移轉指南](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>檢查所安裝的 AzureRM 版本

Az 模組可與 AzureRM 模組安裝在一起，但不建議這麼做。 在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。 進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道您是否可以啟用命令別名而不必解除安裝 AzureRM。

若要檢查您所安裝的 AzureRM 版本，請執行下列命令：

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>確保現有指令碼可使用最新的 AzureRM 版本

這是最重要的步驟！ 執行現有指令碼，並確保它們能使用「最新」版的 AzureRM (__6.13.1__)。 如果指令碼沒有作用，請務必閱讀 [AzureRM 移轉指南](/powershell/azure/azurerm/migration-guide.6.0.0)。

## <a name="install-the-azure-powershell-az-module"></a>安裝 Azure PowerShell Az 模組

第一個步驟是在您的平台上安裝 Az 模組。 當您安裝 Az 時，建議您先解除安裝 AzureRM。 在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。

若要安裝 Azure PowerShell Az 模組，請遵循下列步驟：

* __建議__：[將 AzureRM 模組解除安裝](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)。
  務必移除 AzureRM 的「所有」安裝版本，而不只是最近版本。
* [安裝 Az 模組](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>啟用 AzureRM 相容性別名 

> [!IMPORTANT]
>
> 在解除安裝「所有」AzureRM 版本後，才可啟用相容性模式。 在 AzureRM Cmdlet 仍可使用的情況下啟用相容性模式，可能會導致無法預期的行為。 如果您決定讓 AzureRM 繼續保持安裝狀態，請略過此步驟，但請注意所有 AzureRM Cmdlet 均會使用較舊的模組，而不會呼叫任何 Az Cmdlet。

在 AzureRM 已解除安裝且指令碼使用最新 AzureRM 版本的情況下，下一個步驟是啟用 Az 模組的相容性模式。 透過以下命令啟用相容性：

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 Az 模組。 這些別名會寫入至所選範圍的使用者設定檔。 如果沒有使用者設定檔存在，則會建立一個。

> [!WARNING]
>
> 您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做。 別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。 全系統啟用別名，也會對在其本機範圍內安裝 AzureRM 的其他使用者造成問題。

啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。 

## <a name="change-module-imports-and-cmdlet-names"></a>變更模組匯入和 Cmdlet 名稱

一般情況下，模組名稱已變更，所以 `AzureRM` 和 `Azure` 會成為 `Az`，而 Cmdlet 也是如此。
例如，`AzureRM.Compute` 模組已重新命名為 `Az.Compute`。 `New-AzureRMVM` 已成為 `New-AzVM`，而 `Get-AzureStorageBlob` 現在為 `Get-AzStorageBlob`。

此命名變更有一些應該留意的例外狀況。 某些模組已重新命名或合併到現有模組，但這不會影響其 Cmdlet 的尾碼，而只會將 `AzureRM` 或 `Azure` 變更為 `Az`。 否則，便會變更完整的 Cmdlet 尾碼以反映新的模組名稱。

| AzureRM 模組 | Az 模組 | Cmdlet 尾碼有變更嗎？ |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | yes |
| AzureRM.Insights | Az.Monitor | yes |
| AzureRM.DataFactories | Az.DataFactory | yes |
| AzureRM.DataFactoryV2 | Az.DataFactory | yes |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | 否 |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | 否 |
| AzureRM.Tags | Az.Resources | 否 |
| AzureRM.MachineLearningCompute | Az.MachineLearning | 否 |
| AzureRM.UsageAggregates | Az.Billing | 否 |
| AzureRM.Consumption | Az.Billing | 否 |

## <a name="summary"></a>總結

依照下列步驟，您可以將所有現有的指令碼更新為使用新模組。 如果您對於讓移轉變困難的這些步驟有任何疑問或問題，請對本文發表意見，以便我們改進指示。
