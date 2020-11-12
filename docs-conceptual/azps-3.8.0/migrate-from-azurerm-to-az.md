---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a0a6fcbc0a7bdae507ff5e16dd844e8425c929d5
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408950"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>將 Azure PowerShell 從 AzureRM 移轉至 Az

Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。
針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。 為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。 不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。

若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>確定現有指令碼可使用最新的 AzureRM 版本

在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。 進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。

若要檢查您所安裝的 AzureRM 版本，請執行下列命令：

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

AzureRM __最新的__ 可用版本為 __6.13.1__ 。 如果您未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用此處和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。

如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。
如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。

## <a name="uninstall-azurerm"></a>解除安裝 AzureRM

Az 模組不保證能與 PowerShell 5.1 for Windows 中任何現有的 AzureRM 安裝相容。 在安裝 Az 模組之前，請先[解除安裝 AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)。

> [!IMPORTANT]
>
> 如果您尚未準備好要從系統中移除 AzureRM 模組，您可以改為安裝適用於 [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x 或更新版本的 Az 模組。 PowerShell Core 與 PowerShell 5.1 for Windows 使用不同的模組程式庫，因此不會有任何衝突。 您仍然可以在 PowerShell Core 中[啟用別名](#enable-azurerm-compatibility-aliases)。

## <a name="install-the-azure-powershell-az-module"></a>安裝 Azure PowerShell Az 模組

第一個步驟是在您的平台上安裝 Az 模組。 當您安裝 Az 時，建議您先解除安裝 AzureRM。 在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。

若要安裝 Azure PowerShell Az 模組，請依照[安裝 Az 模組](install-az-ps.md)中的指示操作。

> [!NOTE]
> 此時，您可以執行 Az 模組中提供的 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) Cmdlet，以確保所有版本的 AzureRM 都已解除安裝，而不會造成衝突。

## <a name="enable-azurerm-compatibility-aliases"></a>啟用 AzureRM 相容性別名

在 AzureRM 已解除安裝且指令碼使用最新 AzureRM 版本的情況下，下一個步驟是啟用 Az 模組的相容性模式。 透過以下命令啟用相容性：

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 Az 模組。 這些別名會寫入至所選範圍的設定檔。 如果沒有設定檔存在，則會建立一個。
使用大於 `CurrentUser` 的 `-Scope` 時，必須具備適當的權限，才能建立或更新對應的設定檔。

> [!IMPORTANT]
> __只有__ Cmdlet 名稱會使用別名 - 模組名稱並不會。 如果您使用 `#Requires`、`Import-Module`、`.psd1` 中的相依性清單，或完整的 Cmdlet 名稱，此時請確實依照[重大變更清單](migrate-az-1.0.0.md)中列出的模組名稱相關程序加以移轉。

> [!WARNING]
>
> 您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做。 別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。 全系統啟用別名，可能會對在其本機範圍內安裝 AzureRM 的其他使用者造成問題。

啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。
Az 模組已變更、新增部分參數名稱，或將其設為必要項目。 Cmdlet 的輸出類型也可能已變更。 這些變更詳述於[重大變更清單](migrate-az-1.0.0.md)中。

## <a name="update-cmdlets-modules-and-parameters"></a>更新 Cmdlet、模組和參數

指令碼經過更新並以別名執行時，您可以妥善將其更新以使用新的 Cmdlet，並善用其他變更 (例如新功能)。 對於大部分的指令碼，您只需要[依照 Az 中新的 Cmdlet 命名配置](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes)更新 Cmdlet 名稱即可。 您還可能需要進行其他某些變更，指令碼才能運作，視指令碼的功用及其運用的 Azure PowerShell 功能而定。

例如，[Blob 儲存體 Cmdlet](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) 已完全重新撰寫而使用新的非同步模型，因此，相較於僅變更了 Cmdlet 名稱的指令碼，使用這類 Cmdlet 的指令碼將需要更多處理才能更新。

即使您到目前為止只需要對指令碼進行簡單的微幅變更 (或者，您的指令碼在別名啟用時不需要進一步修改即可運作)，仍請參閱 [Az 1.0.0 中重大變更的完整清單](migrate-az-1.0.0.md)，以確定您並未依賴可能在您變更 Cmdlet 名稱和停用別名後即消失的「透明」別名行為。

## <a name="disable-aliases"></a>停用別名

一旦您完成移轉，且不再依賴別名行為時，建議您停用別名。 此作業可透過 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) Cmdlet 來完成。

> [!IMPORTANT]
> 執行此 Cmdlet 時，請 __確實__ 針對您已為其叫用 `Enable-AzureRmAlias` 的每個 `-Scope` 叫用 Cmdlet，否則您的系統上仍可能會有依賴別名行為的指令碼。
