---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將 Azure PowerShell 指令碼從 AzureRM 遷移至新的 Az PowerShell 模組的步驟和工具。
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893502"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="739e0-103">將 Azure PowerShell 從 AzureRM 移轉至 Az</span><span class="sxs-lookup"><span data-stu-id="739e0-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="739e0-104">所有 AzureRM PowerShell 模組的版本已過時。</span><span class="sxs-lookup"><span data-stu-id="739e0-104">All versions of the AzureRM PowerShell module are outdated.</span></span> <span data-ttu-id="739e0-105">[Az PowerShell 模組](install-az-ps.md)現在是用來與 Azure 互動的建議 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="739e0-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

## <a name="why-a-new-module"></a><span data-ttu-id="739e0-106">為何推出新模組？</span><span class="sxs-lookup"><span data-stu-id="739e0-106">Why a new module?</span></span>

<span data-ttu-id="739e0-107">最大且最重要的變更是自引進以 .NET Standard 程式庫為基礎的 [PowerShell](/powershell/scripting/overview) 後，其如今已成為跨平台產品。</span><span class="sxs-lookup"><span data-stu-id="739e0-107">The biggest and most important change is that [PowerShell](/powershell/scripting/overview), being based on the .NET Standard library, has been a cross-platform product since its introduction.</span></span>

<span data-ttu-id="739e0-108">如同 PowerShell 語言，我們致力於將 Azure 支援帶至所有平台。</span><span class="sxs-lookup"><span data-stu-id="739e0-108">Like the PowerShell language, we're committed to bringing Azure support to all platforms.</span></span> <span data-ttu-id="739e0-109">我們的承諾表示需要更新 Azure PowerShell 模組，才能使用 .NET Standard 並與 PowerShell Core 和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="739e0-109">Our commitment meant that the Azure PowerShell modules needed to be updated to use .NET Standard and be compatible with PowerShell Core.</span></span> <span data-ttu-id="739e0-110">我們決定不修改現有的 AzureRM 模組並導入複雜的變更來加入這項支援，而是建立了 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="739e0-110">Rather than modifying the existing AzureRM module and introducing complex changes to add this support, the Az module was created.</span></span>

<span data-ttu-id="739e0-111">建立新模組也讓我們的工程師可將 Cmdlet 和模組的設計與命名趨於一致。</span><span class="sxs-lookup"><span data-stu-id="739e0-111">Creating a new module also allowed our engineers to make the design, naming of cmdlets, and modules consistent.</span></span> <span data-ttu-id="739e0-112">現在，所有模組皆以 `Az.` 前置詞開頭，且 Cmdlet 全都採用 `Verb-AzNoun` 命名慣例。</span><span class="sxs-lookup"><span data-stu-id="739e0-112">All modules now start with the `Az.` prefix and cmdlets all use the `Verb-AzNoun` naming convention.</span></span> <span data-ttu-id="739e0-113">之前，Cmdlet 名稱較長且不一致。</span><span class="sxs-lookup"><span data-stu-id="739e0-113">Previously, cmdlet names were longer and inconsistent.</span></span>

<span data-ttu-id="739e0-114">模組數目也已減少：某些與相同服務搭配運作的模組已結合在一起。</span><span class="sxs-lookup"><span data-stu-id="739e0-114">The number of modules were also reduced: Some modules that worked with the same services have been combined.</span></span> <span data-ttu-id="739e0-115">相同服務的管理平面和資料平面 Cmdlet 現在也全都包含在單一模組中。</span><span class="sxs-lookup"><span data-stu-id="739e0-115">Management plane and data plane cmdlets for the same service are now contained within a single module.</span></span> <span data-ttu-id="739e0-116">對於手動管理相依性和匯入的使用者，此項合併將可簡化程序。</span><span class="sxs-lookup"><span data-stu-id="739e0-116">For those of you who manually manage dependencies and imports, this consolidation makes things much simpler.</span></span>

<span data-ttu-id="739e0-117">藉由進行這些重要變更，小組成員努力促使 Azure 與 PowerShell Cmdlet 的搭配使用比以往更簡便，並且可在更多平台上使用。</span><span class="sxs-lookup"><span data-stu-id="739e0-117">By making these important changes, the team has committed to making it easier than ever before and on more platforms than previously possible to use Azure with PowerShell cmdlets.</span></span>

## <a name="upgrading-to-az-powershell"></a><span data-ttu-id="739e0-118">升級至 Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="739e0-118">Upgrading to Az PowerShell</span></span>

<span data-ttu-id="739e0-119">針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用 Az。</span><span class="sxs-lookup"><span data-stu-id="739e0-119">Scripts written for the AzureRM cmdlets won't automatically work with Az.</span></span> <span data-ttu-id="739e0-120">為了更輕鬆地轉換，已開發 [AzureRM 至 Az 移轉工具組](https://github.com/Azure/azure-powershell-migration)。</span><span class="sxs-lookup"><span data-stu-id="739e0-120">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="739e0-121">不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="739e0-121">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="739e0-122">若要深入了解為何會建立 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](new-azureps-module-az.md)。</span><span class="sxs-lookup"><span data-stu-id="739e0-122">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="739e0-123">新的 Cmdlet 名稱已設計為易於了解。</span><span class="sxs-lookup"><span data-stu-id="739e0-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="739e0-124">請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。</span><span class="sxs-lookup"><span data-stu-id="739e0-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="739e0-125">例如，舊 Cmdlet `New-AzureRMVm` 已變成 `New-AzVm`。</span><span class="sxs-lookup"><span data-stu-id="739e0-125">For example, the old cmdlet `New-AzureRMVm` has become `New-AzVm`.</span></span>
<span data-ttu-id="739e0-126">不過，移轉不僅只是熟悉新的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="739e0-126">However, migration is more than just becoming familiar with the new cmdlet names, though.</span></span> <span data-ttu-id="739e0-127">此外還有重新命名的模組、參數和其他重要變更。</span><span class="sxs-lookup"><span data-stu-id="739e0-127">There are renamed modules, parameters, and other important changes.</span></span>

<span data-ttu-id="739e0-128">若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。</span><span class="sxs-lookup"><span data-stu-id="739e0-128">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="739e0-129">確定現有指令碼可使用最新的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="739e0-129">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="739e0-130">在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="739e0-130">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="739e0-131">進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="739e0-131">Doing so allows you to make sure scripts are already running on the latest release and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="739e0-132">若要檢查您所安裝的 AzureRM 版本，請執行下列範例：</span><span class="sxs-lookup"><span data-stu-id="739e0-132">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="739e0-133">AzureRM **最新的** 可用版本為 **6.13.1**。</span><span class="sxs-lookup"><span data-stu-id="739e0-133">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="739e0-134">如果未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用本文和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="739e0-134">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond the scope of what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="739e0-135">如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。</span><span class="sxs-lookup"><span data-stu-id="739e0-135">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="739e0-136">如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。</span><span class="sxs-lookup"><span data-stu-id="739e0-136">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="739e0-137">選項 1 (建議)：自動遷移您的 PowerShell 指令碼</span><span class="sxs-lookup"><span data-stu-id="739e0-137">Option 1 (recommended): Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="739e0-138">此建議選項可將 AzureRM 指令碼遷移至 Az 所需的工作降到最低。</span><span class="sxs-lookup"><span data-stu-id="739e0-138">This recommended option minimizes the effort required to migrate AzureRM scripts to Az.</span></span>

### <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="739e0-139">安裝 AzureRM 至 Az 移轉工具組</span><span class="sxs-lookup"><span data-stu-id="739e0-139">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a><span data-ttu-id="739e0-140">自動轉換指令碼</span><span class="sxs-lookup"><span data-stu-id="739e0-140">Convert your scripts automatically</span></span>

<span data-ttu-id="739e0-141">透過 AzureRM 至 Az 移轉工具組，您可以產生一個計劃，以判斷在對指令碼進行任何修改之前，以及在安裝 Az PowerShell 模組之前，要對其執行哪些變更。</span><span class="sxs-lookup"><span data-stu-id="739e0-141">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="739e0-142">[將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組](quickstart-migrate-azurerm-to-az-automatically.md)快速入門，會逐步引導您完成從 AzureRM 至 Az PowerShell 模組自動更新 PowerShell 指令碼的整個程序。</span><span class="sxs-lookup"><span data-stu-id="739e0-142">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a><span data-ttu-id="739e0-143">選項 2：使用相容性模式搭配 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="739e0-143">Option 2: Use compatibility mode with Enable-AzureRmAlias</span></span>

<span data-ttu-id="739e0-144">當您處理新語法的更新時，Az 模組有相容性模式可協助您使用現有指令碼。</span><span class="sxs-lookup"><span data-stu-id="739e0-144">The Az module has a compatibility mode to help you use existing scripts while you update to the new syntax.</span></span> <span data-ttu-id="739e0-145">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet 會透過別名啟用相容性模式。</span><span class="sxs-lookup"><span data-stu-id="739e0-145">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet enables a compatibility mode through aliases.</span></span> <span data-ttu-id="739e0-146">此模式可讓您在最少修改的情況下使用現有的指令碼，同時也能將完整遷移至 Az。</span><span class="sxs-lookup"><span data-stu-id="739e0-146">This mode allows you to use existing scripts with minimal modification while working towards a full migration to Az.</span></span> <span data-ttu-id="739e0-147">根據預設，`Enable-AzureRmAlias` 只會啟用目前 PowerShell 工作階段的相容性別名。</span><span class="sxs-lookup"><span data-stu-id="739e0-147">By default, `Enable-AzureRmAlias` only enables compatibility aliases for the current PowerShell session.</span></span> <span data-ttu-id="739e0-148">使用其 `Scope` 參數，在 PowerShell 工作階段之間保存相容性別名。</span><span class="sxs-lookup"><span data-stu-id="739e0-148">Use its `Scope` parameter to persist compatibility aliases across PowerShell sessions.</span></span> <span data-ttu-id="739e0-149">如需詳細資訊，請參閱 [Enable-AzureRmAlias 參考文件](/powershell/module/az.accounts/enable-azurermalias)。</span><span class="sxs-lookup"><span data-stu-id="739e0-149">For more information, see [the Enable-AzureRmAlias reference documentation](/powershell/module/az.accounts/enable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="739e0-150">即使 Cmdlet 名稱已有別名，但 Az Cmdlet 仍可能有新的 (或重新命名的) 參數或已變更的傳回值。</span><span class="sxs-lookup"><span data-stu-id="739e0-150">Even though the cmdlet names are aliased, there may still be new (or renamed) parameters or changed return values for the Az cmdlets.</span></span> <span data-ttu-id="739e0-151">請不要誤以為啟用別名就能完成移轉。</span><span class="sxs-lookup"><span data-stu-id="739e0-151">Don't expect enabling aliases to take care of the migration for you!</span></span> <span data-ttu-id="739e0-152">請參閱[完整重大變更清單](migrate-az-1.0.0.md)，找出您的指令碼可能需要更新之處。</span><span class="sxs-lookup"><span data-stu-id="739e0-152">See the [full breaking changes list](migrate-az-1.0.0.md) to find where your scripts may require updates.</span></span>

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a><span data-ttu-id="739e0-153">選項 3：使用 Azure PowerShell 擴充功能，在 Visual Studio Code 中遷移您的指令碼</span><span class="sxs-lookup"><span data-stu-id="739e0-153">Option 3: Migrate your scripts in Visual Studio Code with the Azure PowerShell extension</span></span>

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a><span data-ttu-id="739e0-154">安裝適用於 Visual Studio Code 的 Azure PowerShell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="739e0-154">Install the Azure PowerShell extension for Visual Studio Code</span></span>

<span data-ttu-id="739e0-155">安裝[適用於 VSCode 的 Azure PowerShell 擴充功能](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)</span><span class="sxs-lookup"><span data-stu-id="739e0-155">Install the [Azure PowerShell extension for VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)</span></span>

### <a name="convert-your-scripts-manually"></a><span data-ttu-id="739e0-156">手動轉換指令碼</span><span class="sxs-lookup"><span data-stu-id="739e0-156">Convert your scripts manually</span></span>

1. <span data-ttu-id="739e0-157">在 VSCode 中載入您的 AzureRM 指令碼</span><span class="sxs-lookup"><span data-stu-id="739e0-157">Load your AzureRM script in VSCode</span></span>
2. <span data-ttu-id="739e0-158">開啟命令選擇區 `Ctrl+Shift+P`，然後選取 `Migrate Azure PowerShell script` 開始遷移</span><span class="sxs-lookup"><span data-stu-id="739e0-158">Start the migration by opening the command palette `Ctrl+Shift+P` and select `Migrate Azure PowerShell script`</span></span>
3. <span data-ttu-id="739e0-159">選取來源版本 `AzureRM`</span><span class="sxs-lookup"><span data-stu-id="739e0-159">Select source version `AzureRM`</span></span>
4. <span data-ttu-id="739e0-160">遵循建議的動作，執行每個加底線的命令或參數。</span><span class="sxs-lookup"><span data-stu-id="739e0-160">Follow the recommended actions for each underlined command or parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="739e0-161">後續步驟</span><span class="sxs-lookup"><span data-stu-id="739e0-161">Next steps</span></span>

* [<span data-ttu-id="739e0-162">解除安裝 AzureRM</span><span class="sxs-lookup"><span data-stu-id="739e0-162">Uninstall AzureRM</span></span>](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [<span data-ttu-id="739e0-163">安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="739e0-163">Install Azure PowerShell</span></span>](install-az-ps.md)
