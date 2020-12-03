---
title: 將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組
description: 深入了解如何將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組。
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427831"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>快速入門：將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組

在本文中，您將了解如何使用 Az.Tools.Migration PowerShell 模組，將 PowerShell 指令碼和指令碼模組從 AzureRM 自動升級至 Az PowerShell 模組。

> [!IMPORTANT]
> Az.Tools.Migration PowerShell 模組目前為公開預覽狀態。 所提供的這個預覽版本並沒有服務等級協定。 不建議用於生產工作負載。 可能不支援特定功能，或可能已經限制功能。 如需詳細資訊，請參閱 [Microsoft Azure 預覽版增補使用條款](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)。

透過 `azure-powershell-migration` 存放庫中的 [GitHub 問題](https://github.com/Azure/azure-powershell-migration/issues)，報告 Az.Tools.Migration PowerShell 模組的意見反應和問題。

## <a name="requirements"></a>需求

* 將現有的 PowerShell 指令碼更新至最新版本的 [AzureRM PowerShell 模組 (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)。
* 安裝 Az.Tools.Migration PowerShell 模組。

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>步驟 1：產生升級計劃

您可以使用 `New-AzUpgradeModulePlan` Cmdlet 來產生升級計劃，以將您的指令碼和模組遷移至 Az PowerShell 模組。 升級計劃會詳細說明從 AzureRM 移至 Az PowerShell Cmdlet 時，需要變更的特定檔案和位移點。

> [!NOTE]
> `New-AzUpgradeModulePlan` Cmdlet 不會執行此計劃，只會產生升級步驟。

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

檢閱升級計劃的結果。

```powershell
# Show the entire upgrade plan
$Plan
```

執行下列命令，將結果篩選為有警告或錯誤的命令。 這對大型結果集很有幫助，可在執行升級之前快速找出錯誤。

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>步驟 2:執行升級

當您執行 `Invoke-AzUpgradeModulePlan` Cmdlet 時，就會執行升級計劃。 此命令會執行指定檔案或資料夾的升級，但是 `New-AzUpgradeModulePlan` Cmdlet 所識別的任何錯誤除外。

此命令會要求您指定是否應就地修改檔案，或是否要將新檔案連同原始檔案一起儲存 (保留未經修改的原始檔案)。

> [!CAUTION]
> 沒有復原作業。 請務必確定您有 PowerShell 指令碼和您嘗試升級模組的備份複本。

> [!WARNING]
> 當指定 `-FileEditMode ModifyExistingFiles` 選項時，`Invoke-AzUpgradeModulePlan` Cmdlet 有破壞性！ 會根據 `New-AzUpgradeModulePlan` Cmdlet 所產生的模組升級計劃，就地修改您的指令碼和函式。 若為非破壞性選項，請改為指定 `-FileEditMode SaveChangesToNewFiles`。

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

檢閱升級作業的結果。

```powershell
# Show the results for the entire upgrade operation
$Results
```

如果傳回任何錯誤，您可以使用下列命令進一步查看錯誤結果：

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>限制

* 不支援對展開的參數集進行自動化參數名稱更新。 如果在升級計劃產生期間發現任何一種情況，就會傳回警告。
* 檔案 I/O 作業會使用預設編碼。 不尋常的檔案編碼狀況可能會造成問題。
* 未偵測到當做引數傳遞至 Pester 單元測試模擬陳述式的 AzureRM Cmdlet。
* 目前僅支援 Az PowerShell 模組版本 4.6.1 作為目標。

## <a name="next-steps"></a>後續步驟

若要深入了解 Az PowerShell 模組，請參閱 [Azure PowerShell 文件](/powershell/azure/)