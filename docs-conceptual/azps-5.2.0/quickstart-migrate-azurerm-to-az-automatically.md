---
title: 將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組
description: 深入了解如何將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組。
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488524"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>快速入門：將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組

在本文中，您將了解如何使用 Az.Tools.Migration PowerShell 模組，將 PowerShell 指令碼和指令碼模組從 AzureRM 自動升級至 Az PowerShell 模組。

> [!IMPORTANT]
> Az.Tools.Migration PowerShell 模組目前為公開預覽狀態。 所提供的這個預覽版本並沒有服務等級協定。 不建議用於生產工作負載。 可能不支援特定功能，或可能已經限制功能。 如需詳細資訊，請參閱 [Microsoft Azure 預覽版增補使用條款](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)。

## <a name="requirements"></a>需求

* 將現有的 PowerShell 指令碼更新至最新版本的 [AzureRM PowerShell 模組 (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)。
* 安裝 Az.Tools.Migration PowerShell 模組。

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>步驟 1：產生升級計劃

您可以使用 **`New-AzUpgradeModulePlan`** Cmdlet 來產生升級計劃，以將您的指令碼和模組遷移至 Az PowerShell 模組。 此 Cmdlet 不會對您現有的指令碼進行任何變更。 使用 **`FilePath`** 參數將目標設為特定的指令碼，或使用 **`DirectoryPath`** 參數將目標設為特定資料夾中的所有指令碼。

> [!NOTE]
> **`New-AzUpgradeModulePlan`** Cmdlet 不會執行此計劃，只會產生升級步驟。

下列範例會針對 _`C:\Scripts`_ 資料夾中的所有指令碼產生計劃。 已指定 **`OutVariable`** 參數，因此會傳回結果，並同時儲存在名為 **`Plan`** 的變數中。

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

如下列輸出所示，升級計劃會詳細說明從 AzureRM 移至 Az PowerShell Cmdlet 時，需要變更的特定檔案和位移點。

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

在執行升級之前，您必須先檢視計劃的結果是否有問題。 下列範例會傳回指令碼清單，以及這些指令碼中可防止其自動升級的項目。

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

下列輸出中所顯示的項目在先行手動修正問題之前，將不會自動升級。 無法自動升級的已知問題包括使用展開的任何命令。

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>步驟 2:執行升級

> [!CAUTION]
> 沒有復原作業。 請務必確定您有 PowerShell 指令碼和您嘗試升級模組的備份複本。

在您滿意此計劃之後，就會使用 **`Invoke-AzUpgradeModulePlan`** Cmdlet 來執行升級。 為 **`FileEditMode`** 參數值指定 **`SaveChangesToNewFiles`** ，以避免對原始指令碼進行變更。 使用此模式時，會建立每個以 _`_az_upgraded` 為目標的指令碼複本，並將_  附加至檔案名稱。

> [!WARNING]
> 當指定 **`-FileEditMode ModifyExistingFiles`** 選項時， **`Invoke-AzUpgradeModulePlan`** Cmdlet 有破壞性！ 會根據 **`New-AzUpgradeModulePlan`** Cmdlet 所產生的模組升級計劃，就地修改您的指令碼和函式。 若為非破壞性選項，請改為指定 **`-FileEditMode SaveChangesToNewFiles`** 。

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

如果傳回任何錯誤，您可以使用下列命令進一步查看錯誤結果：

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>限制

* 不支援對展開的參數集進行自動化參數名稱更新。 如果在升級計劃產生期間發現任何一種情況，就會傳回警告。
* 檔案 I/O 作業會使用預設編碼。 不尋常的檔案編碼狀況可能會造成問題。
* 未偵測到當做引數傳遞至 Pester 單元測試模擬陳述式的 AzureRM Cmdlet。
* 目前僅支援 Az PowerShell 模組版本 4.6.1 作為目標。

## <a name="how-to-report-issues"></a>如何回報問題

透過 `azure-powershell-migration` 存放庫中的 [GitHub 問題](https://github.com/Azure/azure-powershell-migration/issues)，報告 Az.Tools.Migration PowerShell 模組的意見反應和問題。

## <a name="next-steps"></a>後續步驟

若要深入了解 Az PowerShell 模組，請參閱 [Azure PowerShell 文件](/powershell/azure/)