---
title: 將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組
description: 深入了解如何將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組。
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001750"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="c556c-103">快速入門：將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="c556c-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="c556c-104">在本文中，您將了解如何使用 Az.Tools.Migration PowerShell 模組，將 PowerShell 指令碼和指令碼模組從 AzureRM 自動升級至 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="c556c-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c556c-105">Az.Tools.Migration PowerShell 模組目前為公開預覽狀態。</span><span class="sxs-lookup"><span data-stu-id="c556c-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="c556c-106">所提供的這個預覽版本並沒有服務等級協定。</span><span class="sxs-lookup"><span data-stu-id="c556c-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="c556c-107">不建議用於生產工作負載。</span><span class="sxs-lookup"><span data-stu-id="c556c-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="c556c-108">可能不支援特定功能，或可能已經限制功能。</span><span class="sxs-lookup"><span data-stu-id="c556c-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="c556c-109">如需詳細資訊，請參閱 [Microsoft Azure 預覽版增補使用條款](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)。</span><span class="sxs-lookup"><span data-stu-id="c556c-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="c556c-110">透過 `azure-powershell-migration` 存放庫中的 [GitHub 問題](https://github.com/Azure/azure-powershell-migration/issues)，報告 Az.Tools.Migration PowerShell 模組的意見反應和問題。</span><span class="sxs-lookup"><span data-stu-id="c556c-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="c556c-111">需求</span><span class="sxs-lookup"><span data-stu-id="c556c-111">Requirements</span></span>

* <span data-ttu-id="c556c-112">將現有的 PowerShell 指令碼更新至最新版本的 [AzureRM PowerShell 模組 (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)。</span><span class="sxs-lookup"><span data-stu-id="c556c-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="c556c-113">安裝 Az.Tools.Migration PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="c556c-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="c556c-114">步驟 1：產生升級計劃</span><span class="sxs-lookup"><span data-stu-id="c556c-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="c556c-115">您可以使用 `New-AzUpgradeModulePlan` Cmdlet 來產生升級計劃，以將您的指令碼和模組遷移至 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="c556c-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="c556c-116">升級計劃會詳細說明從 AzureRM 移至 Az PowerShell Cmdlet 時，需要變更的特定檔案和位移點。</span><span class="sxs-lookup"><span data-stu-id="c556c-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="c556c-117">`New-AzUpgradeModulePlan` Cmdlet 不會執行此計劃，只會產生升級步驟。</span><span class="sxs-lookup"><span data-stu-id="c556c-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="c556c-118">檢閱升級計劃的結果。</span><span class="sxs-lookup"><span data-stu-id="c556c-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="c556c-119">執行下列命令，將結果篩選為有警告或錯誤的命令。</span><span class="sxs-lookup"><span data-stu-id="c556c-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="c556c-120">這對大型結果集很有幫助，可在執行升級之前快速找出錯誤。</span><span class="sxs-lookup"><span data-stu-id="c556c-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="c556c-121">步驟 2:執行升級</span><span class="sxs-lookup"><span data-stu-id="c556c-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="c556c-122">當您執行 `Invoke-AzUpgradeModulePlan` Cmdlet 時，就會執行升級計劃。</span><span class="sxs-lookup"><span data-stu-id="c556c-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="c556c-123">此命令會執行指定檔案或資料夾的升級，但是 `New-AzUpgradeModulePlan` Cmdlet 所識別的任何錯誤除外。</span><span class="sxs-lookup"><span data-stu-id="c556c-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="c556c-124">此命令會要求您指定是否應就地修改檔案，或是否要將新檔案連同原始檔案一起儲存 (保留未經修改的原始檔案)。</span><span class="sxs-lookup"><span data-stu-id="c556c-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="c556c-125">沒有復原作業。</span><span class="sxs-lookup"><span data-stu-id="c556c-125">There is no undo operation.</span></span> <span data-ttu-id="c556c-126">請務必確定您有 PowerShell 指令碼和您嘗試升級模組的備份複本。</span><span class="sxs-lookup"><span data-stu-id="c556c-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="c556c-127">當指定 `-FileEditMode ModifyExistingFiles` 選項時，`Invoke-AzUpgradeModulePlan` Cmdlet 有破壞性！</span><span class="sxs-lookup"><span data-stu-id="c556c-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="c556c-128">會根據 `New-AzUpgradeModulePlan` Cmdlet 所產生的模組升級計劃，就地修改您的指令碼和函式。</span><span class="sxs-lookup"><span data-stu-id="c556c-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="c556c-129">若為非破壞性選項，請改為指定 `-FileEditMode SaveChangesToNewFiles`。</span><span class="sxs-lookup"><span data-stu-id="c556c-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="c556c-130">檢閱升級作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c556c-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="c556c-131">如果傳回任何錯誤，您可以使用下列命令進一步查看錯誤結果：</span><span class="sxs-lookup"><span data-stu-id="c556c-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="c556c-132">限制</span><span class="sxs-lookup"><span data-stu-id="c556c-132">Limitations</span></span>

* <span data-ttu-id="c556c-133">不支援對展開的參數集進行自動化參數名稱更新。</span><span class="sxs-lookup"><span data-stu-id="c556c-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="c556c-134">如果在升級計劃產生期間發現任何一種情況，就會傳回警告。</span><span class="sxs-lookup"><span data-stu-id="c556c-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="c556c-135">檔案 I/O 作業會使用預設編碼。</span><span class="sxs-lookup"><span data-stu-id="c556c-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="c556c-136">不尋常的檔案編碼狀況可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="c556c-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="c556c-137">未偵測到當做引數傳遞至 Pester 單元測試模擬陳述式的 AzureRM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c556c-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="c556c-138">目前僅支援 Az PowerShell 模組版本 4.6.1 作為目標。</span><span class="sxs-lookup"><span data-stu-id="c556c-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c556c-139">後續步驟</span><span class="sxs-lookup"><span data-stu-id="c556c-139">Next steps</span></span>

<span data-ttu-id="c556c-140">若要深入了解 Az PowerShell 模組，請參閱 [Azure PowerShell 文件](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="c556c-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>