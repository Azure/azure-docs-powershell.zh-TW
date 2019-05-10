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
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048779"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="ca78d-103">從 AzureRM 遷移至 Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="ca78d-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="ca78d-104">Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="ca78d-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="ca78d-105">針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。</span><span class="sxs-lookup"><span data-stu-id="ca78d-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="ca78d-106">為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。</span><span class="sxs-lookup"><span data-stu-id="ca78d-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="ca78d-107">不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。</span><span class="sxs-lookup"><span data-stu-id="ca78d-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

<span data-ttu-id="ca78d-108">若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱 [Az 1.0.0 的移轉指南](migrate-az-1.0.0.md)</span><span class="sxs-lookup"><span data-stu-id="ca78d-108">To see the full list of breaking changes between AzureRM and Az, see the [Migration guide for Az 1.0.0](migrate-az-1.0.0.md)</span></span>

## <a name="check-for-installed-versions-of-azurerm"></a><span data-ttu-id="ca78d-109">檢查所安裝的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="ca78d-109">Check for installed versions of AzureRM</span></span>

<span data-ttu-id="ca78d-110">Az 模組可與 AzureRM 模組安裝在一起，但不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="ca78d-110">The Az module can be installed side-by-side with the AzureRM module, but this is not recommended.</span></span> <span data-ttu-id="ca78d-111">在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="ca78d-111">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span> <span data-ttu-id="ca78d-112">進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道您是否可以啟用命令別名而不必解除安裝 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="ca78d-112">Doing so allows you to make sure scripts are already running on the latest release, and let you know if you can enable command aliases without uninstalling AzureRM.</span></span>

<span data-ttu-id="ca78d-113">若要檢查您所安裝的 AzureRM 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="ca78d-113">To check which version(s) of AzureRM you have installed, run the command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="ca78d-114">確保現有指令碼可使用最新的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="ca78d-114">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="ca78d-115">這是最重要的步驟！</span><span class="sxs-lookup"><span data-stu-id="ca78d-115">This is the most important step!</span></span> <span data-ttu-id="ca78d-116">執行現有指令碼，並確保它們能使用「最新」版的 AzureRM (__6.13.1__)。</span><span class="sxs-lookup"><span data-stu-id="ca78d-116">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.13.1__).</span></span> <span data-ttu-id="ca78d-117">如果指令碼沒有作用，請務必閱讀 [AzureRM 移轉指南](/powershell/azure/azurerm/migration-guide.6.0.0)。</span><span class="sxs-lookup"><span data-stu-id="ca78d-117">If your scripts don't work, make sure to read the [AzureRM migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="ca78d-118">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="ca78d-118">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="ca78d-119">第一個步驟是在您的平台上安裝 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="ca78d-119">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="ca78d-120">當您安裝 Az 時，建議您先解除安裝 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="ca78d-120">When you install Az, it's recommended that you uninstall AzureRM.</span></span> <span data-ttu-id="ca78d-121">在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。</span><span class="sxs-lookup"><span data-stu-id="ca78d-121">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="ca78d-122">若要安裝 Azure PowerShell Az 模組，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="ca78d-122">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="ca78d-123">__建議__：[將 AzureRM 模組解除安裝](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)。</span><span class="sxs-lookup"><span data-stu-id="ca78d-123">__RECOMMENDED__: [Uninstall the AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span></span>
  <span data-ttu-id="ca78d-124">務必移除 AzureRM 的「所有」安裝版本，而不只是最近版本。</span><span class="sxs-lookup"><span data-stu-id="ca78d-124">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="ca78d-125">安裝 Az 模組</span><span class="sxs-lookup"><span data-stu-id="ca78d-125">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><span data-ttu-id="ca78d-126"><a name="aliases"/>啟用 AzureRM 相容性別名</span><span class="sxs-lookup"><span data-stu-id="ca78d-126"><a name="aliases"/>Enable AzureRM compatibility aliases</span></span> 

> [!IMPORTANT]
>
> <span data-ttu-id="ca78d-127">在解除安裝「所有」AzureRM 版本後，才可啟用相容性模式。</span><span class="sxs-lookup"><span data-stu-id="ca78d-127">Only enable compatibility mode if you've uninstalled _all_ versions of AzureRM.</span></span> <span data-ttu-id="ca78d-128">在 AzureRM Cmdlet 仍可使用的情況下啟用相容性模式，可能會導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="ca78d-128">Enabling compatibility mode with AzureRM cmdlets still available may result in unpredictable behavior.</span></span> <span data-ttu-id="ca78d-129">如果您決定讓 AzureRM 繼續保持安裝狀態，請略過此步驟，但請注意所有 AzureRM Cmdlet 均會使用較舊的模組，而不會呼叫任何 Az Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca78d-129">Skip this step if you decided to keep AzureRM installed, but be aware that any AzureRM cmdlets will use the older modules and not call any Az cmdlets.</span></span>

<span data-ttu-id="ca78d-130">在 AzureRM 已解除安裝且指令碼使用最新 AzureRM 版本的情況下，下一個步驟是啟用 Az 模組的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="ca78d-130">With AzureRM uninstalled and your scripts working with the latest AzureRM version, the next step is to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="ca78d-131">透過以下命令啟用相容性：</span><span class="sxs-lookup"><span data-stu-id="ca78d-131">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="ca78d-132">別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="ca78d-132">Aliases enable the ability to use old cmdlet names with the Az module installed.</span></span> <span data-ttu-id="ca78d-133">這些別名會寫入至所選範圍的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="ca78d-133">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="ca78d-134">如果沒有使用者設定檔存在，則會建立一個。</span><span class="sxs-lookup"><span data-stu-id="ca78d-134">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="ca78d-135">您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="ca78d-135">You can use a different `-Scope` for this command, but it's not recommended.</span></span> <span data-ttu-id="ca78d-136">別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。</span><span class="sxs-lookup"><span data-stu-id="ca78d-136">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="ca78d-137">全系統啟用別名，也會對在其本機範圍內安裝 AzureRM 的其他使用者造成問題。</span><span class="sxs-lookup"><span data-stu-id="ca78d-137">Enabling aliases system-wide could also cause issues for other users which have AzureRM installed in their local scope.</span></span>

<span data-ttu-id="ca78d-138">啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。</span><span class="sxs-lookup"><span data-stu-id="ca78d-138">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="ca78d-139">變更模組匯入和 Cmdlet 名稱</span><span class="sxs-lookup"><span data-stu-id="ca78d-139">Change module imports and cmdlet names</span></span>

<span data-ttu-id="ca78d-140">一般情況下，模組名稱已變更，所以 `AzureRM` 和 `Azure` 會成為 `Az`，而 Cmdlet 也是如此。</span><span class="sxs-lookup"><span data-stu-id="ca78d-140">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="ca78d-141">例如，`AzureRM.Compute` 模組已重新命名為 `Az.Compute`。</span><span class="sxs-lookup"><span data-stu-id="ca78d-141">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="ca78d-142">`New-AzureRMVM` 已成為 `New-AzVM`，而 `Get-AzureStorageBlob` 現在為 `Get-AzStorageBlob`。</span><span class="sxs-lookup"><span data-stu-id="ca78d-142">`New-AzureRMVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="ca78d-143">此命名變更有一些應該留意的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ca78d-143">There are exceptions to this naming change that you should be aware of.</span></span> <span data-ttu-id="ca78d-144">某些模組已重新命名或合併到現有模組，但這不會影響其 Cmdlet 的尾碼，而只會將 `AzureRM` 或 `Azure` 變更為 `Az`。</span><span class="sxs-lookup"><span data-stu-id="ca78d-144">Some modules were renamed or merged into existing modules without this affecting the suffix of their cmdlets, other than changing `AzureRM` or `Azure` to `Az`.</span></span> <span data-ttu-id="ca78d-145">否則，便會變更完整的 Cmdlet 尾碼以反映新的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="ca78d-145">Otherwise, the full cmdlet suffix was changed to reflect the new module name.</span></span>

| <span data-ttu-id="ca78d-146">AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="ca78d-146">AzureRM module</span></span> | <span data-ttu-id="ca78d-147">Az 模組</span><span class="sxs-lookup"><span data-stu-id="ca78d-147">Az module</span></span> | <span data-ttu-id="ca78d-148">Cmdlet 尾碼有變更嗎？</span><span class="sxs-lookup"><span data-stu-id="ca78d-148">Cmdlet suffix changed?</span></span> |
|----------------|-----------|------------------------|
| <span data-ttu-id="ca78d-149">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ca78d-149">AzureRM.Profile</span></span> | <span data-ttu-id="ca78d-150">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ca78d-150">Az.Accounts</span></span> | <span data-ttu-id="ca78d-151">yes</span><span class="sxs-lookup"><span data-stu-id="ca78d-151">Yes</span></span> |
| <span data-ttu-id="ca78d-152">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ca78d-152">AzureRM.Insights</span></span> | <span data-ttu-id="ca78d-153">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ca78d-153">Az.Monitor</span></span> | <span data-ttu-id="ca78d-154">yes</span><span class="sxs-lookup"><span data-stu-id="ca78d-154">Yes</span></span> |
| <span data-ttu-id="ca78d-155">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ca78d-155">AzureRM.DataFactories</span></span> | <span data-ttu-id="ca78d-156">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca78d-156">Az.DataFactory</span></span> | <span data-ttu-id="ca78d-157">yes</span><span class="sxs-lookup"><span data-stu-id="ca78d-157">Yes</span></span> |
| <span data-ttu-id="ca78d-158">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ca78d-158">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="ca78d-159">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca78d-159">Az.DataFactory</span></span> | <span data-ttu-id="ca78d-160">yes</span><span class="sxs-lookup"><span data-stu-id="ca78d-160">Yes</span></span> |
| <span data-ttu-id="ca78d-161">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ca78d-161">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="ca78d-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca78d-162">Az.RecoveryServices</span></span> | <span data-ttu-id="ca78d-163">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-163">No</span></span> |
| <span data-ttu-id="ca78d-164">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ca78d-164">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="ca78d-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ca78d-165">Az.RecoveryServices</span></span> | <span data-ttu-id="ca78d-166">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-166">No</span></span> |
| <span data-ttu-id="ca78d-167">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ca78d-167">AzureRM.Tags</span></span> | <span data-ttu-id="ca78d-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ca78d-168">Az.Resources</span></span> | <span data-ttu-id="ca78d-169">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-169">No</span></span> |
| <span data-ttu-id="ca78d-170">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ca78d-170">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="ca78d-171">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ca78d-171">Az.MachineLearning</span></span> | <span data-ttu-id="ca78d-172">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-172">No</span></span> |
| <span data-ttu-id="ca78d-173">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ca78d-173">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="ca78d-174">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ca78d-174">Az.Billing</span></span> | <span data-ttu-id="ca78d-175">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-175">No</span></span> |
| <span data-ttu-id="ca78d-176">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ca78d-176">AzureRM.Consumption</span></span> | <span data-ttu-id="ca78d-177">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ca78d-177">Az.Billing</span></span> | <span data-ttu-id="ca78d-178">否</span><span class="sxs-lookup"><span data-stu-id="ca78d-178">No</span></span> |

## <a name="summary"></a><span data-ttu-id="ca78d-179">總結</span><span class="sxs-lookup"><span data-stu-id="ca78d-179">Summary</span></span>

<span data-ttu-id="ca78d-180">依照下列步驟，您可以將所有現有的指令碼更新為使用新模組。</span><span class="sxs-lookup"><span data-stu-id="ca78d-180">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="ca78d-181">如果您對於讓移轉變困難的這些步驟有任何疑問或問題，請對本文發表意見，以便我們改進指示。</span><span class="sxs-lookup"><span data-stu-id="ca78d-181">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>
