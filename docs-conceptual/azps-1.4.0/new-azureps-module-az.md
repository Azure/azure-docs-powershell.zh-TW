---
title: Azure PowerShell Az 模組簡介
description: 介紹新的 Azure PowerShell 模組 Az，也就是 AzureRM 模組的替代項目。
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837668"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="48da7-103">新的 Azure PowerShell Az 模組簡介</span><span class="sxs-lookup"><span data-stu-id="48da7-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="48da7-104">從 2018 年 12 月開始，Azure PowerShell Az 模組已正式運作，並已成為與 Azure 互動時的預期 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="48da7-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="48da7-105">Az 可提供較短的命令、改進的穩定性和跨平台支援。</span><span class="sxs-lookup"><span data-stu-id="48da7-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="48da7-106">Az 也提供功能同位以及從 AzureRM 遷移的簡單路徑。</span><span class="sxs-lookup"><span data-stu-id="48da7-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="48da7-107">Az 使用會 .NET Standard 程式庫，這表示它在 PowerShell 5 和 PowerShell 6 上執行。</span><span class="sxs-lookup"><span data-stu-id="48da7-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="48da7-108">因為 PowerShell 6 可以在 Linux、macOS 和 Windows 上執行，所以 Azure PowerShell 現在適用於所有平台。</span><span class="sxs-lookup"><span data-stu-id="48da7-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="48da7-109">使用 .NET Standard，可在對使用者造成最小影響的情況下，讓我們統一 Azure PowerShell 的程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="48da7-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="48da7-110">Az 是新模組，因此版本已重設為 1.0.0。</span><span class="sxs-lookup"><span data-stu-id="48da7-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="48da7-111">升級至 Az</span><span class="sxs-lookup"><span data-stu-id="48da7-111">Upgrade to Az</span></span>

<span data-ttu-id="48da7-112">建議所有使用者升級至新的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="48da7-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="48da7-113">若要這樣做：</span><span class="sxs-lookup"><span data-stu-id="48da7-113">To do so:</span></span>

* <span data-ttu-id="48da7-114">__建議__：[將 Azure PowerShell AzureRM 模組解除安裝](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="48da7-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="48da7-115">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="48da7-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="48da7-116">當您熟悉新的命令集時，請使用 `Enable-AzureRMAlias` 啟用相容性模式來新增 AzureRM Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="48da7-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="48da7-117">__只有__在未安裝 AzureRM 時才可啟用別名。</span><span class="sxs-lookup"><span data-stu-id="48da7-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="48da7-118">將現有指令碼遷移至 Az</span><span class="sxs-lookup"><span data-stu-id="48da7-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="48da7-119">主要更新不太方便。</span><span class="sxs-lookup"><span data-stu-id="48da7-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="48da7-120">不過，當您處理新語法的更新時，Az 模組有相容性模式可協助您使用現有指令碼。</span><span class="sxs-lookup"><span data-stu-id="48da7-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="48da7-121">使用 `Enable-AzureRmAlias` Cmdlet 來啟用 AzureRM 相容性模式。</span><span class="sxs-lookup"><span data-stu-id="48da7-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="48da7-122">此 Cmdlet 會將 AzureRM Cmdlet 名稱定義為新 Az Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="48da7-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="48da7-123">新的 Cmdlet 名稱已設計為易於了解。</span><span class="sxs-lookup"><span data-stu-id="48da7-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="48da7-124">請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。</span><span class="sxs-lookup"><span data-stu-id="48da7-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="48da7-125">例如，舊命令 `New-AzureRMVm` 已變成 `New-AzVm`。</span><span class="sxs-lookup"><span data-stu-id="48da7-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="48da7-126">如需移轉程序的完整說明，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="48da7-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="48da7-127">未來的 AzureRM 支援</span><span class="sxs-lookup"><span data-stu-id="48da7-127">The future of support for AzureRM</span></span>

<span data-ttu-id="48da7-128">現有 AzureRM 模組不會再收到新的 Cmdlet 或功能。</span><span class="sxs-lookup"><span data-stu-id="48da7-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="48da7-129">不過，我們仍會正式維護 AzureRM，並在 2020 年 12 月之前都會提供錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="48da7-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="48da7-130">若要保持最新的 Azure 服務和功能，請切換到 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="48da7-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
