---
title: Azure PowerShell Az 模組簡介
description: 介紹新的 Azure PowerShell 模組 Az，也就是 AzureRM 模組的替代項目。
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574799"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="c0f60-103">新的 Azure PowerShell Az 模組簡介</span><span class="sxs-lookup"><span data-stu-id="c0f60-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="c0f60-104">從 2018 年 11 月起，Azure PowerShell `Az` 模組即可提供完整公開預覽版。</span><span class="sxs-lookup"><span data-stu-id="c0f60-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="c0f60-105">Az 可提供較短的命令、改進穩定性，以及支援 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="c0f60-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="c0f60-106">Az 也提供功能同位以及從 AzureRM 遷移的簡單路徑。</span><span class="sxs-lookup"><span data-stu-id="c0f60-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="c0f60-107">Az 使用會 .NET Standard 程式庫，這表示它在 PowerShell 5.x 和 PowerShell 6.x 上執行。</span><span class="sxs-lookup"><span data-stu-id="c0f60-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="c0f60-108">因為 PowerShell 6.x 可以在 Linux、macOS 和 Windows 上執行，這表示 Az 適用於所有平台。</span><span class="sxs-lookup"><span data-stu-id="c0f60-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="c0f60-109">使用 .NET Standard，可在對使用者造成最小影響的情況下，讓我們統一 Azure PowerShell 的程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="c0f60-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="c0f60-110">Az 是新模組，所以已重設版本。</span><span class="sxs-lookup"><span data-stu-id="c0f60-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="c0f60-111">第一個穩定版本會是 1.0，但是自 2018 年 11 月起，此模組有 AzureRm 的功能同位。</span><span class="sxs-lookup"><span data-stu-id="c0f60-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="c0f60-112">升級至 Az</span><span class="sxs-lookup"><span data-stu-id="c0f60-112">Upgrade to Az</span></span>

<span data-ttu-id="c0f60-113">建議使用者升級至新的 `Az` 模組。</span><span class="sxs-lookup"><span data-stu-id="c0f60-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="c0f60-114">若要這樣做：</span><span class="sxs-lookup"><span data-stu-id="c0f60-114">To do so:</span></span>

* [<span data-ttu-id="c0f60-115">將 Azure PowerShell AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="c0f60-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="c0f60-116">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="c0f60-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="c0f60-117">當您熟悉新的命令集時，請使用 `Enable-AzureRMAlias` 啟用 AzureRM 的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="c0f60-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="c0f60-118">將現有指令碼遷移至 Az</span><span class="sxs-lookup"><span data-stu-id="c0f60-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="c0f60-119">主要更新不太方便。</span><span class="sxs-lookup"><span data-stu-id="c0f60-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="c0f60-120">不過，當您處理新語法的更新時，`Az` 模組有相容性模式可協助您使用現有指令碼。</span><span class="sxs-lookup"><span data-stu-id="c0f60-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="c0f60-121">使用 `Enable-AzureRmAlias` Cmdlet 來啟用 `AzureRM` 相容性模式。</span><span class="sxs-lookup"><span data-stu-id="c0f60-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="c0f60-122">此 Cmdlet 會將 `AzureRM` Cmdlet 名稱定義為新 `Az` Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="c0f60-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="c0f60-123">新的 Cmdlet 名稱已設計為易於了解。</span><span class="sxs-lookup"><span data-stu-id="c0f60-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="c0f60-124">請在 Cmdlet 名稱中使用 `Az`，而非使用 `AzureRm` 或 `Azure`。</span><span class="sxs-lookup"><span data-stu-id="c0f60-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="c0f60-125">例如，舊命令 `New-AzureRmVm` 已變成 `New-AzVm`。</span><span class="sxs-lookup"><span data-stu-id="c0f60-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="c0f60-126">如需移轉程序的完整說明，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f60-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="c0f60-127">未來的 AzureRM 支援</span><span class="sxs-lookup"><span data-stu-id="c0f60-127">The future of support for AzureRM</span></span>

<span data-ttu-id="c0f60-128">在 2018 年 12 月發生 `Az` 1.0 版後，現有 `AzureRM` 模組不會再收到新的 Cmdlet 或功能。</span><span class="sxs-lookup"><span data-stu-id="c0f60-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="c0f60-129">不過，`AzureRM` 仍會正式維護，而且會收到錯誤修正。</span><span class="sxs-lookup"><span data-stu-id="c0f60-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="c0f60-130">若要保持最新的 Azure 服務和功能，您應該切換到 `Az` 模組。</span><span class="sxs-lookup"><span data-stu-id="c0f60-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>