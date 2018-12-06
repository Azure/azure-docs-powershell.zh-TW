---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828717"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="4c4b5-103">從 AzureRM 遷移至 Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="4c4b5-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="4c4b5-104">Az 模組有 AzureRM 的功能同位，但是會使用比較短且更一致的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="4c4b5-105">針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="4c4b5-106">為了更輕鬆進行轉換，Az 提供一些工具，讓您使用 AzureRM 執行現有的指令碼。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="4c4b5-107">不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到新的模組。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="4c4b5-108">確保現有指令碼可使用最新的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="4c4b5-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="4c4b5-109">這是最重要的步驟！</span><span class="sxs-lookup"><span data-stu-id="4c4b5-109">This is the most important step!</span></span> <span data-ttu-id="4c4b5-110">執行現有指令碼，並確保它們能使用「最新」版的 AzureRM (__6.13.0__)。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.13.0__).</span></span> <span data-ttu-id="4c4b5-111">如果指令碼沒有作用，請務必閱讀 [AzureRM 移轉指南](migration-guide.6.0.0.md)。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="4c4b5-112">安裝 Azure PowerShell Az 模組</span><span class="sxs-lookup"><span data-stu-id="4c4b5-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="4c4b5-113">第一個步驟是在您的平台上安裝 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="4c4b5-114">若要安裝 Az，您必須將 AzureRM 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="4c4b5-115">在下列步驟中，您將了解如何繼續執行現有的指令碼，並且讓舊的 Cmdlet 名稱相容。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="4c4b5-116">若要安裝 Azure PowerShell Az 模組，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="4c4b5-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="4c4b5-117">[將 AzureRM 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="4c4b5-118">務必移除 AzureRM 的「所有」安裝版本，而不只是最近版本。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="4c4b5-119">安裝 Az 模組</span><span class="sxs-lookup"><span data-stu-id="4c4b5-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="4c4b5-120"><a name="aliases"/>啟用 AzureRM 別名模式</span><span class="sxs-lookup"><span data-stu-id="4c4b5-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="4c4b5-121">將 AzureRM 解除安裝且您的指令碼使用最新的 AzureRM 版本，現在可以啟用 Az 模組的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="4c4b5-122">透過以下命令啟用相容性：</span><span class="sxs-lookup"><span data-stu-id="4c4b5-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="4c4b5-123">別名讓您能夠使用舊的 Cmdlet 名稱搭配已安裝的 `Az` 模組。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="4c4b5-124">這些別名會寫入至所選範圍的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="4c4b5-125">如果沒有使用者設定檔存在，則會建立一個。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="4c4b5-126">您可以將不同的 `-Scope` 使用於這個命令，但不建議這麼做！</span><span class="sxs-lookup"><span data-stu-id="4c4b5-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="4c4b5-127">別名會寫入至所選範圍的使用者設定檔，所以儘可能在有限範圍內啟用別名。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="4c4b5-128">全系統啟用別名，也會對在其本機範圍內安裝 `AzureRM` 的其他使用者造成問題。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="4c4b5-129">啟用別名模式後，再次執行指令碼以確認它們仍然運作正常。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="4c4b5-130">變更模組匯入和 Cmdlet 名稱</span><span class="sxs-lookup"><span data-stu-id="4c4b5-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="4c4b5-131">一般情況下，模組名稱已變更，所以 `AzureRM` 和 `Azure` 會成為 `Az`，而 Cmdlet 也是如此。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="4c4b5-132">例如，`AzureRM.Compute` 模組已重新命名為 `Az.Compute`。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="4c4b5-133">`New-AzureRmVM` 已成為 `New-AzVM`，而 `Get-AzureStorageBlob` 現在為 `Get-AzStorageBlob`。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="4c4b5-134">此命名變更有一些例外狀況，您應該在進行任何重新命名之前加以留意：</span><span class="sxs-lookup"><span data-stu-id="4c4b5-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="4c4b5-135">AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="4c4b5-135">AzureRM module</span></span> | <span data-ttu-id="4c4b5-136">Az 模組</span><span class="sxs-lookup"><span data-stu-id="4c4b5-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="4c4b5-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="4c4b5-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="4c4b5-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4c4b5-138">Az.DataFactory</span></span> |
| <span data-ttu-id="4c4b5-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4c4b5-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="4c4b5-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4c4b5-140">Az.DataFactory</span></span> |
| <span data-ttu-id="4c4b5-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4c4b5-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="4c4b5-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4c4b5-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="4c4b5-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4c4b5-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="4c4b5-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4c4b5-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="4c4b5-145">總結</span><span class="sxs-lookup"><span data-stu-id="4c4b5-145">Summary</span></span>

<span data-ttu-id="4c4b5-146">依照下列步驟，您可以將所有現有的指令碼更新為使用新模組。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="4c4b5-147">如果您對於讓移轉變困難的這些步驟有任何疑問或問題，請對本文發表意見，以便我們改進指示。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>
