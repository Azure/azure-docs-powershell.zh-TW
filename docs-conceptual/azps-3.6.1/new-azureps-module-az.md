---
title: Azure PowerShell Az 模組簡介
description: 介紹新的 Azure PowerShell 模組 Az，也就是 AzureRM 模組的替代項目。
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 36bb0074694947f48d703aebc9119f90b508da57
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2020
ms.locfileid: "79035663"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="89078-103">新的 Azure PowerShell Az 模組簡介</span><span class="sxs-lookup"><span data-stu-id="89078-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="89078-104">從 2018 年 12 月開始，Azure PowerShell Az 模組已正式運作，並已成為與 Azure 互動時的預期 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="89078-104">Starting in December 2018, the Azure PowerShell Az module is in general release and is now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="89078-105">Az 可提供較短的命令、改進的穩定性和跨平台支援。</span><span class="sxs-lookup"><span data-stu-id="89078-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="89078-106">Az 也具有與 AzureRM 的功能同位，提供簡單的移轉路徑。</span><span class="sxs-lookup"><span data-stu-id="89078-106">Az also has feature parity with AzureRM, giving you an easy migration path.</span></span>

<span data-ttu-id="89078-107">透過 Az 模組，Azure PowerShell 現已相容於 Windows 上的 PowerShell 5.1 以及所有支援平台上的 PowerShell Core 6.x 和更新版本，包括 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="89078-107">With the Az module, Azure PowerShell is now compatible with PowerShell 5.1 on Windows and PowerShell Core 6.x and later on all supported platforms - including Windows, macOS, and Linux.</span></span>

<span data-ttu-id="89078-108">Az 是新模組，因此版本已重設為 1.0.0。</span><span class="sxs-lookup"><span data-stu-id="89078-108">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="why-a-new-module"></a><span data-ttu-id="89078-109">為何推出新模組？</span><span class="sxs-lookup"><span data-stu-id="89078-109">Why a new module?</span></span>

<span data-ttu-id="89078-110">重大更新可能不便執行，因此我們必須讓您了解我們為何決定導入一組附有新 Cmdlet 的新模組，供您從 PowerShell 與 Azure 互動。</span><span class="sxs-lookup"><span data-stu-id="89078-110">Major updates can be inconvenient, so it's important that we let you know why the decision was made to introduce a new set of modules, with new cmdlets, for interacting with Azure from PowerShell.</span></span>

<span data-ttu-id="89078-111">最顯著而重要的變更是，隨著 [PowerShell Core 6.x](/powershell/scripting/overview) 的導入 (以 .NET Standard 程式庫為基礎)，PowerShell 已成為跨平台產品。</span><span class="sxs-lookup"><span data-stu-id="89078-111">The biggest and most important change is that PowerShell has been a cross-platform product since the introduction of [PowerShell Core 6.x](/powershell/scripting/overview), based on the .NET Standard library.</span></span>
<span data-ttu-id="89078-112">我們致力於將 Azure 支援導入所有平台，而這意味著 Azure PowerShell 模組必須進行更新，以使用 .NET Standard 並且與 PowerShell Core 相容。</span><span class="sxs-lookup"><span data-stu-id="89078-112">We're committed to bringing Azure support to all platforms, which means that the Azure PowerShell modules needed to be updated to use .NET Standard and be compatible with PowerShell Core.</span></span> <span data-ttu-id="89078-113">我們決定不以現有的 AzureRM 模組導入複雜的變更來加入這項支援，而是建立了 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89078-113">Rather than taking the existing AzureRM module and introduce complex changes to add this support, the Az module was created.</span></span>

<span data-ttu-id="89078-114">建立新模組也讓我們的工程師有機會可將 Cmdlet 和模組的設計與命名趨於一致。</span><span class="sxs-lookup"><span data-stu-id="89078-114">Creating a new module also gave our engineers the opportunity to make the design and naming of cmdlets and modules consistent.</span></span> <span data-ttu-id="89078-115">現在，所有模組皆以 `Az.` 前置詞開頭，且 Cmdlet 全都採用_動詞_-`Az`_名詞_的格式。</span><span class="sxs-lookup"><span data-stu-id="89078-115">All modules now start with the `Az.` prefix and cmdlets all use the _Verb_-`Az`_Noun_ form.</span></span> <span data-ttu-id="89078-116">過去，Cmdlet 名稱不僅較長，這些名稱也有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="89078-116">Previously, cmdlet names were not only longer, there were inconsistencies in cmdlet names.</span></span>

<span data-ttu-id="89078-117">模組數目也已減少：某些與相同服務搭配運作的模組已彙整在一起，且管理平面和資料平面 Cmdlet 現在也全都包含在其服務的單一模組中。</span><span class="sxs-lookup"><span data-stu-id="89078-117">The number of modules was also reduced: Some modules which worked with the same services have been rolled together, and management plane and data plane cmdlets are now contained all within single modules for their services.</span></span> <span data-ttu-id="89078-118">對於手動管理相依性和匯入的使用者，其作業將可因此而簡化。</span><span class="sxs-lookup"><span data-stu-id="89078-118">For those of you who manually manage dependencies and imports, this makes things much simpler.</span></span>

<span data-ttu-id="89078-119">藉由進行這些需要建置新 Azure PowerShell 模組的重要變更，小組成員努力促使 Azure 與 PowerShell Cmdlet 的搭配使用比以往更簡便，並且可在更多平台上使用。</span><span class="sxs-lookup"><span data-stu-id="89078-119">By making these important changes that required building a new Azure PowerShell module, the team has committed to making it easier than ever, and on more platforms than previously possible, to use Azure with PowerShell cmdlets.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="89078-120">升級至 Az</span><span class="sxs-lookup"><span data-stu-id="89078-120">Upgrade to Az</span></span>

<span data-ttu-id="89078-121">為了運用 PowerShell 中的最新 Azure 功能，您應盡速移轉至 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89078-121">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module as soon as possible.</span></span> <span data-ttu-id="89078-122">若您尚未準備好要安裝 Az 模組來取代 AzureRM，您可以透過下列方式試用 Az：</span><span class="sxs-lookup"><span data-stu-id="89078-122">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="89078-123">在 `PowerShell` 環境中使用 [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview)。</span><span class="sxs-lookup"><span data-stu-id="89078-123">Use a `PowerShell` environment with [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview).</span></span>
  <span data-ttu-id="89078-124">Azure Cloud Shell 是一種以瀏覽器為基礎的殼層環境，隨附有已安裝的 Az 模組，且已啟用 `Enable-AzureRM` 相容性別名。</span><span class="sxs-lookup"><span data-stu-id="89078-124">Azure Cloud Shell is a browser-based shell environment which comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="89078-125">保留隨著 PowerShell 5.1 for Windows 而安裝的 AzureRM 模組，但安裝適用於 PowerShell Core 6.x 或更新版本的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89078-125">Keep the AzureRM module installed with PowerShell 5.1 for Windows, but install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="89078-126">PowerShell 5.1 for Windows 和 PowerShell Core 分別使用不同的模組集合。</span><span class="sxs-lookup"><span data-stu-id="89078-126">PowerShell 5.1 for Windows and PowerShell Core use separate collections of modules.</span></span> <span data-ttu-id="89078-127">請依照指示從 PowerShell Core 終端機[安裝 PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows)，然後[安裝 Az 模組](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="89078-127">Follow the instructions to [install PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) and then [install the Az module](install-az-ps.md) from a PowerShell Core terminal.</span></span>

<span data-ttu-id="89078-128">若要從現有的 AzureRM 安裝升級：</span><span class="sxs-lookup"><span data-stu-id="89078-128">To upgrade from an existing AzureRM install:</span></span>

1. [<span data-ttu-id="89078-129">將 Azure PowerShell AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="89078-129">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [<span data-ttu-id="89078-130">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="89078-130">Install the Azure PowerShell Az module</span></span>](install-az-ps.md)
3. <span data-ttu-id="89078-131">__選擇性__：當您熟悉新的命令集時，請使用 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) 啟用相容性模式來新增 AzureRM Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="89078-131">__OPTIONAL__: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="89078-132">如需詳細資訊，請參閱下一節或[開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="89078-132">See the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md) for more details.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="89078-133">將現有指令碼遷移至 Az</span><span class="sxs-lookup"><span data-stu-id="89078-133">Migrate existing scripts to Az</span></span>

<span data-ttu-id="89078-134">新的 Cmdlet 名稱已設計為易於了解。</span><span class="sxs-lookup"><span data-stu-id="89078-134">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="89078-135">請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。</span><span class="sxs-lookup"><span data-stu-id="89078-135">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="89078-136">例如，舊命令 `New-AzureRMVm` 已變成 `New-AzVm`。</span><span class="sxs-lookup"><span data-stu-id="89078-136">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>
<span data-ttu-id="89078-137">不過，移轉不僅只是熟悉新的 Cmdlet 名稱：此外還有重新命名的模組、參數和其他重要變更。</span><span class="sxs-lookup"><span data-stu-id="89078-137">Migration is more than just becoming familiar with the new cmdlet names, though: There are renamed modules, parameters, and other important changes.</span></span>

<span data-ttu-id="89078-138">為了協助您執行從 AzureRM 移轉至 Az 的程序，我們提供了一些資源：</span><span class="sxs-lookup"><span data-stu-id="89078-138">To help you with the process of migration from AzureRM to Az, we've got a number of resources:</span></span>

* [<span data-ttu-id="89078-139">開始從 AzureRM 移轉至 Az</span><span class="sxs-lookup"><span data-stu-id="89078-139">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="89078-140">從 AzureRM 到 Az 1.0.0 的重大變更完整清單</span><span class="sxs-lookup"><span data-stu-id="89078-140">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="89078-141">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet</span><span class="sxs-lookup"><span data-stu-id="89078-141">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

<span data-ttu-id="89078-142">當您處理新語法的更新時，Az 模組有相容性模式可協助您使用現有指令碼。</span><span class="sxs-lookup"><span data-stu-id="89078-142">The Az module has a compatibility mode to help you use existing scripts while you update to the new syntax.</span></span> <span data-ttu-id="89078-143">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet 會透過別名啟用相容性模式，讓您在最少的修改下使用現有的指令碼，同時完成完整移轉至 Az 的作業。</span><span class="sxs-lookup"><span data-stu-id="89078-143">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet enables a compatibility mode through aliases, to allow you to use existing scripts with minimal modification while working towards a full migration to Az.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89078-144">即使 Cmdlet 名稱已有別名，但 Az Cmdlet 仍可能有新的 (或重新命名的) 參數或已變更的傳回值。</span><span class="sxs-lookup"><span data-stu-id="89078-144">Even though the cmdlet names are aliased, there may still be new (or renamed) parameters or changed return values for the Az cmdlets.</span></span> <span data-ttu-id="89078-145">請不要誤以為啟用別名就能完成移轉。</span><span class="sxs-lookup"><span data-stu-id="89078-145">Don't expect enabling aliases to take care of the migration for you!</span></span> <span data-ttu-id="89078-146">請參閱[完整重大變更清單](migrate-az-1.0.0.md)，找出您的指令碼可能需要更新之處。</span><span class="sxs-lookup"><span data-stu-id="89078-146">See the [full breaking changes list](migrate-az-1.0.0.md) to find where your scripts may require updates.</span></span>

## <a name="continued-support-for-azurerm"></a><span data-ttu-id="89078-147">對 AzureRM 的持續支援</span><span class="sxs-lookup"><span data-stu-id="89078-147">Continued support for AzureRM</span></span>

<span data-ttu-id="89078-148">AzureRM 不會再收到新的 Cmdlet 或功能。</span><span class="sxs-lookup"><span data-stu-id="89078-148">AzureRM will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="89078-149">不過，我們仍會正式維護 AzureRM 模組，並在 2020 年 12 月之前都會提供錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="89078-149">However, the AzureRM module is still officially maintained and will get bug fixes through December 2020.</span></span>
