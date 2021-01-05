---
title: 將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組
description: 深入了解如何將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組。
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 3a26dfbb89f83a9d1983ea8d69cd47c9f74eab38
ms.sourcegitcommit: dd90c54d8794109fa7984543649bb3faa0cbb544
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "97701294"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="53233-103">快速入門：將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="53233-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="53233-104">在本文中，您將了解如何使用 Az.Tools.Migration PowerShell 模組，將 PowerShell 指令碼和指令碼模組從 AzureRM 自動升級至 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="53233-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="53233-105">如需其他移轉選項，請參閱[將 Azure PowerShell 從 AzureRM 移轉至 Az](/powershell/azure/migrate-from-azurerm-to-az)。</span><span class="sxs-lookup"><span data-stu-id="53233-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="53233-106">需求</span><span class="sxs-lookup"><span data-stu-id="53233-106">Requirements</span></span>

* <span data-ttu-id="53233-107">將現有的 PowerShell 指令碼更新至最新版本的 [AzureRM PowerShell 模組 (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)。</span><span class="sxs-lookup"><span data-stu-id="53233-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="53233-108">安裝 Az.Tools.Migration PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="53233-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="53233-109">步驟 1：產生升級計劃</span><span class="sxs-lookup"><span data-stu-id="53233-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="53233-110">您可以使用 **`New-AzUpgradeModulePlan`** Cmdlet 來產生升級計劃，以將您的指令碼和模組遷移至 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="53233-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="53233-111">此 Cmdlet 不會對您現有的指令碼進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="53233-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="53233-112">使用 **`FilePath`** 參數將目標設為特定的指令碼，或使用 **`DirectoryPath`** 參數將目標設為特定資料夾中的所有指令碼。</span><span class="sxs-lookup"><span data-stu-id="53233-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="53233-113">**`New-AzUpgradeModulePlan`** Cmdlet 不會執行此計劃，只會產生升級步驟。</span><span class="sxs-lookup"><span data-stu-id="53233-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="53233-114">下列範例會針對 _`C:\Scripts`_ 資料夾中的所有指令碼產生計劃。</span><span class="sxs-lookup"><span data-stu-id="53233-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="53233-115">已指定 **`OutVariable`** 參數，因此會傳回結果，並同時儲存在名為 **`Plan`** 的變數中。</span><span class="sxs-lookup"><span data-stu-id="53233-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="53233-116">如下列輸出所示，升級計劃會詳細說明從 AzureRM 移至 Az PowerShell Cmdlet 時，需要變更的特定檔案和位移點。</span><span class="sxs-lookup"><span data-stu-id="53233-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="53233-117">在執行升級之前，您必須先檢視計劃的結果是否有問題。</span><span class="sxs-lookup"><span data-stu-id="53233-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="53233-118">下列範例會傳回指令碼清單，以及這些指令碼中可防止其自動升級的項目。</span><span class="sxs-lookup"><span data-stu-id="53233-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="53233-119">下列輸出中所顯示的項目在先行手動修正問題之前，將不會自動升級。</span><span class="sxs-lookup"><span data-stu-id="53233-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="53233-120">無法自動升級的已知問題包括使用展開的任何命令。</span><span class="sxs-lookup"><span data-stu-id="53233-120">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="53233-121">步驟 2:執行升級</span><span class="sxs-lookup"><span data-stu-id="53233-121">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="53233-122">沒有復原作業。</span><span class="sxs-lookup"><span data-stu-id="53233-122">There is no undo operation.</span></span> <span data-ttu-id="53233-123">請務必確定您有 PowerShell 指令碼和您嘗試升級模組的備份複本。</span><span class="sxs-lookup"><span data-stu-id="53233-123">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="53233-124">在您滿意此計劃之後，就會使用 **`Invoke-AzUpgradeModulePlan`** Cmdlet 來執行升級。</span><span class="sxs-lookup"><span data-stu-id="53233-124">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="53233-125">為 **`FileEditMode`** 參數值指定 **`SaveChangesToNewFiles`** ，以避免對原始指令碼進行變更。</span><span class="sxs-lookup"><span data-stu-id="53233-125">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="53233-126">使用此模式時，會建立每個以 _`_az_upgraded` 為目標的指令碼複本，並將_  附加至檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="53233-126">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="53233-127">當指定 **`-FileEditMode ModifyExistingFiles`** 選項時， **`Invoke-AzUpgradeModulePlan`** Cmdlet 有破壞性！</span><span class="sxs-lookup"><span data-stu-id="53233-127">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="53233-128">會根據 **`New-AzUpgradeModulePlan`** Cmdlet 所產生的模組升級計劃，就地修改您的指令碼和函式。</span><span class="sxs-lookup"><span data-stu-id="53233-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="53233-129">若為非破壞性選項，請改為指定 **`-FileEditMode SaveChangesToNewFiles`** 。</span><span class="sxs-lookup"><span data-stu-id="53233-129">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="53233-130">如果傳回任何錯誤，您可以使用下列命令進一步查看錯誤結果：</span><span class="sxs-lookup"><span data-stu-id="53233-130">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="53233-131">限制</span><span class="sxs-lookup"><span data-stu-id="53233-131">Limitations</span></span>

* <span data-ttu-id="53233-132">不支援對展開的參數集進行自動化參數名稱更新。</span><span class="sxs-lookup"><span data-stu-id="53233-132">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="53233-133">如果在升級計劃產生期間發現任何一種情況，就會傳回警告。</span><span class="sxs-lookup"><span data-stu-id="53233-133">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="53233-134">檔案 I/O 作業會使用預設編碼。</span><span class="sxs-lookup"><span data-stu-id="53233-134">File I/O operations use default encoding.</span></span> <span data-ttu-id="53233-135">不尋常的檔案編碼狀況可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="53233-135">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="53233-136">未偵測到當做引數傳遞至 Pester 單元測試模擬陳述式的 AzureRM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53233-136">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="53233-137">目前僅支援 Az PowerShell 模組版本 4.6.1 作為目標。</span><span class="sxs-lookup"><span data-stu-id="53233-137">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="53233-138">如何回報問題</span><span class="sxs-lookup"><span data-stu-id="53233-138">How to report issues</span></span>

<span data-ttu-id="53233-139">透過 `azure-powershell-migration` 存放庫中的 [GitHub 問題](https://github.com/Azure/azure-powershell-migration/issues)，報告 Az.Tools.Migration PowerShell 模組的意見反應和問題。</span><span class="sxs-lookup"><span data-stu-id="53233-139">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="53233-140">後續步驟</span><span class="sxs-lookup"><span data-stu-id="53233-140">Next steps</span></span>

<span data-ttu-id="53233-141">若要深入了解 Az PowerShell 模組，請參閱 [Azure PowerShell 文件](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="53233-141">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>