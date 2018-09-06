---
title: 使用實驗性 Azure PowerShell 模組
description: 了解實驗性 Azure PowerShell 模組的原理和使用方式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: ac571363d79c83b268b5c25f65b14f16d4b86e71
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383765"
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="24ab2-103">使用實驗性 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="24ab2-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="24ab2-104">Azure PowerShell 小組著重於 Azure 中的開發人員工具 (特別是 CLI)，正針對 Azure PowerShell 體驗的許多增強功能進行實驗。</span><span class="sxs-lookup"><span data-stu-id="24ab2-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="24ab2-105">實驗方法</span><span class="sxs-lookup"><span data-stu-id="24ab2-105">Experimentation methodology</span></span>

<span data-ttu-id="24ab2-106">為簡化實驗，我們會建立新的 Azure PowerShell 模組，透過全新且更輕鬆的方式來實作現有的 Azure SDK 功能。</span><span class="sxs-lookup"><span data-stu-id="24ab2-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="24ab2-107">在大部分情況下，Cmdlet 會完全鏡像現有的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24ab2-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="24ab2-108">不過，實驗性 Cmdlet 會提供縮寫標記法和更有效率的預設值，讓您能更輕鬆地建立及管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="24ab2-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="24ab2-109">可透過現有的 Azure PowerShell 模組來並行安裝這些模組。</span><span class="sxs-lookup"><span data-stu-id="24ab2-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="24ab2-110">已將 Cmdlet 名稱縮短來提供較短的名稱，並防止名稱與現有的非實驗性 Cmdlet 發生衝突。</span><span class="sxs-lookup"><span data-stu-id="24ab2-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="24ab2-111">實驗性模組使用下列命名慣例：`AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="24ab2-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="24ab2-112">此命名慣例類似於預覽模組的命名：`AzureRM.*.Preview`。</span><span class="sxs-lookup"><span data-stu-id="24ab2-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="24ab2-113">預覽模組與實驗性模組不同。</span><span class="sxs-lookup"><span data-stu-id="24ab2-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="24ab2-114">預覽模組所實作的 Azure 服務新功能僅可作為預覽供應項目。</span><span class="sxs-lookup"><span data-stu-id="24ab2-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="24ab2-115">預覽模組會取代現有的 Azure PowerShell 模組，並使用相同的 Cmdlet 和參數名稱。</span><span class="sxs-lookup"><span data-stu-id="24ab2-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="24ab2-116">如何安裝實驗性模組</span><span class="sxs-lookup"><span data-stu-id="24ab2-116">How to install an experimental module</span></span>

<span data-ttu-id="24ab2-117">系統會將實驗性模組發佈至 PowerShell 資源庫，就如同現有的 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="24ab2-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="24ab2-118">若要查看實驗模組清單，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="24ab2-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="24ab2-119">若要安裝實驗性模組，請使用下列提升權限 PowerShell 工作階段中的命令：</span><span class="sxs-lookup"><span data-stu-id="24ab2-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="24ab2-120">文件與支援</span><span class="sxs-lookup"><span data-stu-id="24ab2-120">Documentation and support</span></span>

<span data-ttu-id="24ab2-121">文件會包含在安裝套件中，並可使用 `Get-Help` cmdlet 加以存取。</span><span class="sxs-lookup"><span data-stu-id="24ab2-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="24ab2-122">並未發行實驗性模組的官方文件。</span><span class="sxs-lookup"><span data-stu-id="24ab2-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="24ab2-123">建議您測試這些模組。</span><span class="sxs-lookup"><span data-stu-id="24ab2-123">We encourage you to test these modules.</span></span> <span data-ttu-id="24ab2-124">您的意見反應可讓我們改善可用性，並回應您的需求。</span><span class="sxs-lookup"><span data-stu-id="24ab2-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="24ab2-125">不過，由於目前為實驗階段，這些模組的支援很有限。</span><span class="sxs-lookup"><span data-stu-id="24ab2-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="24ab2-126">可在 GitHub 存放庫中建立[問題](https://github.com/Azure/azure-powershell/issues)來提交問題報告。</span><span class="sxs-lookup"><span data-stu-id="24ab2-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="24ab2-127">增強功能的實驗和區域</span><span class="sxs-lookup"><span data-stu-id="24ab2-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="24ab2-128">這些增強功能是以競爭產品中的主要區別作為基礎來加以選取。</span><span class="sxs-lookup"><span data-stu-id="24ab2-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="24ab2-129">例如，Azure CLI 2.0 已提出關於_情節_而非 _API 介面區_的基礎命令論點。</span><span class="sxs-lookup"><span data-stu-id="24ab2-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="24ab2-130">Azure CLI 2.0 使用一系列的智慧型預設值，讓終端使用者能更輕鬆地進行「使用者入門」情節。</span><span class="sxs-lookup"><span data-stu-id="24ab2-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="24ab2-131">核心增強功能</span><span class="sxs-lookup"><span data-stu-id="24ab2-131">Core improvements</span></span>

<span data-ttu-id="24ab2-132">核心增強功能會視為「常識」，且幾乎無須實驗即可繼續實作這些更新。</span><span class="sxs-lookup"><span data-stu-id="24ab2-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="24ab2-133">以情節作為基礎的 Cmdlet - \*All- cmdlet 都應針對情節而非 Azure REST 服務設計。</span><span class="sxs-lookup"><span data-stu-id="24ab2-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="24ab2-134">簡短名稱 - 包含 Cmdlet 的名稱 (例如，`New-AzureRmVM` => `New-AzVm`) 以及參數的名稱 (例如，`-ResourceGroupName` => `-Rg`)。</span><span class="sxs-lookup"><span data-stu-id="24ab2-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="24ab2-135">使用別名可與「舊的」Cmdlet 相容。</span><span class="sxs-lookup"><span data-stu-id="24ab2-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="24ab2-136">提供_回溯相容性_參數集。</span><span class="sxs-lookup"><span data-stu-id="24ab2-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="24ab2-137">智慧型預設值 - 建立智慧型預設值以填入「必要」資訊。</span><span class="sxs-lookup"><span data-stu-id="24ab2-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="24ab2-138">例如︰</span><span class="sxs-lookup"><span data-stu-id="24ab2-138">For example:</span></span>
  - <span data-ttu-id="24ab2-139">資源群組</span><span class="sxs-lookup"><span data-stu-id="24ab2-139">Resource Group</span></span>
  - <span data-ttu-id="24ab2-140">位置</span><span class="sxs-lookup"><span data-stu-id="24ab2-140">Location</span></span>
  - <span data-ttu-id="24ab2-141">相依資源</span><span class="sxs-lookup"><span data-stu-id="24ab2-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="24ab2-142">實驗性增強功能</span><span class="sxs-lookup"><span data-stu-id="24ab2-142">Experimental improvements</span></span>

<span data-ttu-id="24ab2-143">實驗性增強功能所呈現的重大變更是小組需要透過實驗進行驗證的。</span><span class="sxs-lookup"><span data-stu-id="24ab2-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="24ab2-144">簡單類型 - 建立情節應遠離複雜類型和組態物件。</span><span class="sxs-lookup"><span data-stu-id="24ab2-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="24ab2-145">將組態簡化為一個或兩個參數。</span><span class="sxs-lookup"><span data-stu-id="24ab2-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="24ab2-146">「智慧型建立」- 所有實作「智慧型建立」的建立情節都必須_沒有_必要參數：Azure PowerShell 會以武斷的方式選擇所有必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="24ab2-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="24ab2-147">灰色參數 - 在許多情況下，某些參數可能是「灰色」或半選擇性。</span><span class="sxs-lookup"><span data-stu-id="24ab2-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="24ab2-148">如果未指定參數，就會詢問使用者是否需要為他們產生參數。</span><span class="sxs-lookup"><span data-stu-id="24ab2-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="24ab2-149">灰色參數以使用者同意的內容作為基礎來推斷值，也是很合理的做法。</span><span class="sxs-lookup"><span data-stu-id="24ab2-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="24ab2-150">例如，讓灰色參數建議最近使用過的值是很合理的做法。</span><span class="sxs-lookup"><span data-stu-id="24ab2-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="24ab2-151">`-Auto` 參數 - `-Auto` 參數能為使用者提供「選擇加入」的方式來_預設所有事項_，同時維持主線路徑中必要參數的完整性。</span><span class="sxs-lookup"><span data-stu-id="24ab2-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="24ab2-152">特定功能的參數</span><span class="sxs-lookup"><span data-stu-id="24ab2-152">Feature-specific switches</span></span>

<span data-ttu-id="24ab2-153">例如，「建立 web 應用程式」情節可能會有 `-Git` 或 `-AddRemote` 參數，能將 "azure" 遠端自動新增至現有的 Git 存放庫。</span><span class="sxs-lookup"><span data-stu-id="24ab2-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="24ab2-154">可設定的預設值 - 使用者應該能夠預設諸如 `-ResourceGroupName` 和 `-Location` 等特定的通用參數。</span><span class="sxs-lookup"><span data-stu-id="24ab2-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="24ab2-155">大小的預設值 - 資源「大小」會混淆使用者，因為許多資源提供者都會使用不同的名稱 (例如，"Standard\_DS1\_v2" 或 "S1")。</span><span class="sxs-lookup"><span data-stu-id="24ab2-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="24ab2-156">不過，大部分使用者較關心的是成本。</span><span class="sxs-lookup"><span data-stu-id="24ab2-156">However, most users care more about cost.</span></span> <span data-ttu-id="24ab2-157">因此，以定價排程作為基礎來定義「通用」大小是合理的。</span><span class="sxs-lookup"><span data-stu-id="24ab2-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="24ab2-158">使用者可以選擇特定的大小，或是讓 Azure PowerShell 以資源預算作為基礎選擇_最佳選項_。</span><span class="sxs-lookup"><span data-stu-id="24ab2-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="24ab2-159">輸出格式 - Azure PowerShell 目前會傳回 `PSObject`，且幾乎沒有主控台輸出。</span><span class="sxs-lookup"><span data-stu-id="24ab2-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="24ab2-160">Azure PowerShell 需要向使用者顯示一些關於已使用的「智慧型預設值」資訊。</span><span class="sxs-lookup"><span data-stu-id="24ab2-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
