---
title: 從 AzureRM 到 Azure PowerShell Az 1.0.0 的所有變更
description: 本移轉指南包含在 Az 第 1 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: 1d99f04525a33f03f859bfb4abe263b12ca6add9
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657938"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="11a64-103">Az 1.0.0 的重大變更</span><span class="sxs-lookup"><span data-stu-id="11a64-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="11a64-104">本文件詳細說明 AzureRM 6.x 與新的 Az 模組 1.x 版和更新版本之間的變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="11a64-105">目錄有助於引導您進行完整移轉路徑，包括可能會對您的指令碼產生影響的模組特有變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="11a64-106">如需開始從 AzureRM 移轉至 Az 的一般建議，請參閱[開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="11a64-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11a64-107">Az 1.0.0 與 Az 2.0.0 之間也有重大變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="11a64-108">依照本指南從 AzureRM 更新為 Az 之後，請參閱 [Az 2.0.0 重大變更](migrate-az-2.0.0.md)，以確認您是否需要進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="11a64-109">目錄</span><span class="sxs-lookup"><span data-stu-id="11a64-109">Table of Contents</span></span>

- [<span data-ttu-id="11a64-110">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="11a64-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="11a64-111">Cmdlet 名詞前置詞的變更</span><span class="sxs-lookup"><span data-stu-id="11a64-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="11a64-112">模組名稱的變更</span><span class="sxs-lookup"><span data-stu-id="11a64-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="11a64-113">移除的模組</span><span class="sxs-lookup"><span data-stu-id="11a64-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="11a64-114">Windows PowerShell 5.1 和 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="11a64-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="11a64-115">使用 PSCredential 暫時移除使用者登入</span><span class="sxs-lookup"><span data-stu-id="11a64-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="11a64-116">預設使用裝置程式碼登入，而非網頁瀏覽器提示</span><span class="sxs-lookup"><span data-stu-id="11a64-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="11a64-117">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="11a64-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="11a64-118">Az.ApiManagement (先前是 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="11a64-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="11a64-119">Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="11a64-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="11a64-120">Az.CognitiveServices (先前是 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="11a64-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="11a64-121">Az.Compute (先前是 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="11a64-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="11a64-122">Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="11a64-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="11a64-123">Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="11a64-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="11a64-124">Az.DataLakeStore (先前是 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="11a64-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="11a64-125">Az.KeyVault (先前是 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="11a64-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="11a64-126">Az.Media (先前是 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="11a64-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="11a64-127">Az.Monitor (先前是 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="11a64-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="11a64-128">Az.Network (先前是 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="11a64-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="11a64-129">Az.OperationalInsights (先前是 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="11a64-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="11a64-130">Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="11a64-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="11a64-131">Az.Resources (先前是 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="11a64-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="11a64-132">Az.ServiceFabric (先前是 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="11a64-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="11a64-133">Az.Sql (先前是 AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="11a64-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="11a64-134">Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="11a64-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="11a64-135">Az.Websites (先前是 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="11a64-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="11a64-136">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="11a64-136">General breaking changes</span></span>

<span data-ttu-id="11a64-137">本節將詳細說明 Az 模組的重新設計中包含的一般重大變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="11a64-138">Cmdlet 名詞前置詞的變更</span><span class="sxs-lookup"><span data-stu-id="11a64-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="11a64-139">在 AzureRM 模組中，Cmdlet 使用 `AzureRM` 或 `Azure` 作為名詞前置詞。</span><span class="sxs-lookup"><span data-stu-id="11a64-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="11a64-140">Az 則將 Cmdlet 名稱予以簡化和標準化，讓所有 Cmdlet皆使用 'Az' 作為其 Cmdlet 名詞前置詞。</span><span class="sxs-lookup"><span data-stu-id="11a64-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="11a64-141">例如︰</span><span class="sxs-lookup"><span data-stu-id="11a64-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="11a64-142">已變更為：</span><span class="sxs-lookup"><span data-stu-id="11a64-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="11a64-143">為了讓您更輕鬆地轉為使用這些新的 Cmdlet 名稱，Az 導入了兩個新的 Cmdlet，即 [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) 和 [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias)。</span><span class="sxs-lookup"><span data-stu-id="11a64-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="11a64-144">`Enable-AzureRmAlias` 會為 AzureRM 中較舊的 Cmdlet 名稱建立對應於較新 Az Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="11a64-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="11a64-145">搭配使用 `-Scope` 引數與 `Enable-AzureRmAlias` 可讓您選擇要啟用別名的位置。</span><span class="sxs-lookup"><span data-stu-id="11a64-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="11a64-146">例如，下列的 AzureRM 指令碼：</span><span class="sxs-lookup"><span data-stu-id="11a64-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="11a64-147">只要使用 `Enable-AzureRmAlias` 稍做變更即可執行：</span><span class="sxs-lookup"><span data-stu-id="11a64-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="11a64-148">執行 `Enable-AzureRmAlias -Scope CurrentUser` 會對所有已開啟的 PowerShell 工作階段啟用別名，因此在執行此 Cmdlet 之後，就完全不需要變更這類指令碼：</span><span class="sxs-lookup"><span data-stu-id="11a64-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="11a64-149">如需如何使用別名 Cmdlet 的完整詳細資訊，請參閱 [Enable-AzureRmAlias 參考資料](/powershell/module/az.accounts/enable-azurermalias)。</span><span class="sxs-lookup"><span data-stu-id="11a64-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="11a64-150">當您準備好要停用別名時，`Disable-AzureRmAlias` 會移除已建立的別名。</span><span class="sxs-lookup"><span data-stu-id="11a64-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="11a64-151">如需完整的詳細資訊，請參閱 [Disable-AzureRmAlias 參考資料](/powershell/module/az.accounts/disable-azurermalias)。</span><span class="sxs-lookup"><span data-stu-id="11a64-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11a64-152">停用別名時，請確實在_所有_已啟用別名的範圍加以停用。</span><span class="sxs-lookup"><span data-stu-id="11a64-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="11a64-153">模組名稱的變更</span><span class="sxs-lookup"><span data-stu-id="11a64-153">Module Name Changes</span></span>

<span data-ttu-id="11a64-154">模組名稱已從 `AzureRM.*` 變更為 `Az.*`，但下列模組除外：</span><span class="sxs-lookup"><span data-stu-id="11a64-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="11a64-155">AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="11a64-155">AzureRM module</span></span> | <span data-ttu-id="11a64-156">Az 模組</span><span class="sxs-lookup"><span data-stu-id="11a64-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="11a64-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="11a64-157">Azure.Storage</span></span> | <span data-ttu-id="11a64-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11a64-158">Az.Storage</span></span> |
| <span data-ttu-id="11a64-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11a64-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="11a64-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11a64-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="11a64-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="11a64-161">AzureRM.Profile</span></span> | <span data-ttu-id="11a64-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11a64-162">Az.Accounts</span></span> |
| <span data-ttu-id="11a64-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="11a64-163">AzureRM.Insights</span></span> | <span data-ttu-id="11a64-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11a64-164">Az.Monitor</span></span> |
| <span data-ttu-id="11a64-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="11a64-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="11a64-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11a64-166">Az.DataFactory</span></span> |
| <span data-ttu-id="11a64-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="11a64-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="11a64-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11a64-168">Az.DataFactory</span></span> |
| <span data-ttu-id="11a64-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="11a64-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="11a64-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11a64-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="11a64-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="11a64-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="11a64-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11a64-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="11a64-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="11a64-173">AzureRM.Tags</span></span> | <span data-ttu-id="11a64-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11a64-174">Az.Resources</span></span> |
| <span data-ttu-id="11a64-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="11a64-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="11a64-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11a64-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="11a64-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="11a64-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="11a64-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11a64-178">Az.Billing</span></span> |
| <span data-ttu-id="11a64-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="11a64-179">AzureRM.Consumption</span></span> | <span data-ttu-id="11a64-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11a64-180">Az.Billing</span></span> |

<span data-ttu-id="11a64-181">模組名稱的變更表示，只要指令碼使用 `#Requires` 或 `Import-Module` 來載入特定模組，就需要進行變更，以改為使用新的模組。</span><span class="sxs-lookup"><span data-stu-id="11a64-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="11a64-182">對 Cmdlet 後置詞未變更的模組而言，這表示模組名稱雖已變更，但表示作業空間的後置詞_並未_變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="11a64-183">移轉 #Requires 和 Import-Module 陳述式</span><span class="sxs-lookup"><span data-stu-id="11a64-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="11a64-184">使用 `#Requires` 或 `Import-Module` 來宣告 AzureRM 模組相依性的指令碼，必須更新為使用新的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="11a64-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="11a64-185">例如︰</span><span class="sxs-lookup"><span data-stu-id="11a64-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="11a64-186">應變更為：</span><span class="sxs-lookup"><span data-stu-id="11a64-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="11a64-187">針對 `Import-Module`：</span><span class="sxs-lookup"><span data-stu-id="11a64-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="11a64-188">應變更為：</span><span class="sxs-lookup"><span data-stu-id="11a64-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="11a64-189">遷移完整的 Cmdlet 叫用</span><span class="sxs-lookup"><span data-stu-id="11a64-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="11a64-190">使用模組完整 Cmdlet 叫用的指令碼，例如：</span><span class="sxs-lookup"><span data-stu-id="11a64-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="11a64-191">必須變更為使用新的模組和 Cmdlet 名稱：</span><span class="sxs-lookup"><span data-stu-id="11a64-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="11a64-192">移轉模組資訊清單相依性</span><span class="sxs-lookup"><span data-stu-id="11a64-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="11a64-193">透過模組資訊清單 (.psd1) 檔案來表達 AzureRM 模組相依性的模組，必須更新其 `RequiredModules` 區段中的模組名稱：</span><span class="sxs-lookup"><span data-stu-id="11a64-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="11a64-194">必須變更為：</span><span class="sxs-lookup"><span data-stu-id="11a64-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="11a64-195">移除的模組</span><span class="sxs-lookup"><span data-stu-id="11a64-195">Removed modules</span></span>

<span data-ttu-id="11a64-196">下列模組已移除：</span><span class="sxs-lookup"><span data-stu-id="11a64-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="11a64-197">目前已不再支援這些服務的工具。</span><span class="sxs-lookup"><span data-stu-id="11a64-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="11a64-198">建議客戶一有空就立刻遷移至替代服務。</span><span class="sxs-lookup"><span data-stu-id="11a64-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="11a64-199">Windows PowerShell 5.1 和 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="11a64-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="11a64-200">若要搭配使用 Az 與 PowerShell 5.1 for Windows，則必須安裝 .NET Framework 4.7.2。</span><span class="sxs-lookup"><span data-stu-id="11a64-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="11a64-201">使用 PowerShell Core 6.x 或更新版本則不需要 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="11a64-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="11a64-202">使用 PSCredential 暫時移除使用者登入</span><span class="sxs-lookup"><span data-stu-id="11a64-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="11a64-203">由於 .NET Standard 的驗證流程有變，我們暫時移除透過 PSCredential 來登入使用者的功能。</span><span class="sxs-lookup"><span data-stu-id="11a64-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="11a64-204">這項功能會在 2019 年 1 月 15 日版本的 PowerShell 5.1 for Windows 重新導入。</span><span class="sxs-lookup"><span data-stu-id="11a64-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="11a64-205">我們會在[此 GitHub 問題](https://github.com/Azure/azure-powershell/issues/7430)中加以詳細討論。</span><span class="sxs-lookup"><span data-stu-id="11a64-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="11a64-206">預設使用裝置程式碼登入，而非網頁瀏覽器提示</span><span class="sxs-lookup"><span data-stu-id="11a64-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="11a64-207">由於 .NET Standard 的驗證流程有變，我們會在互動式登入期間使用裝置登入作為預設的登入流程。</span><span class="sxs-lookup"><span data-stu-id="11a64-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="11a64-208">在 2019 年 1 月 15 日的版本中，會重新導入透過網頁瀏覽器登入的功能，作為 PowerShell 5.1 for Windows 的預設登入功能。</span><span class="sxs-lookup"><span data-stu-id="11a64-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="11a64-209">屆時，使用者將能夠使用切換參數來選擇裝置登入功能。</span><span class="sxs-lookup"><span data-stu-id="11a64-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="11a64-210">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="11a64-210">Module breaking changes</span></span>

<span data-ttu-id="11a64-211">本節將詳細說明個別模組和 Cmdlet 的特定重大變更。</span><span class="sxs-lookup"><span data-stu-id="11a64-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="11a64-212">Az.ApiManagement (先前是 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="11a64-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="11a64-213">已移除下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11a64-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="11a64-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a64-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="11a64-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="11a64-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="11a64-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="11a64-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="11a64-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="11a64-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="11a64-218">請改為使用 **Set-AzApiManagement** Cmdlet 來設定這些屬性</span><span class="sxs-lookup"><span data-stu-id="11a64-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="11a64-219">已移除下列屬性：</span><span class="sxs-lookup"><span data-stu-id="11a64-219">Removed the following properties:</span></span>
  - <span data-ttu-id="11a64-220">已從 `PsApiManagementContext` 移除 `PsApiManagementHostnameConfiguration` 類型的 `PortalHostnameConfiguration`、`ProxyHostnameConfiguration`、`ManagementHostnameConfiguration` 和 `ScmHostnameConfiguration` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="11a64-221">請改為使用 `PsApiManagementCustomHostNameConfiguration` 類型的 `PortalCustomHostnameConfiguration`、`ProxyCustomHostnameConfiguration`、`ManagementCustomHostnameConfiguration` 和 `ScmCustomHostnameConfiguration`。</span><span class="sxs-lookup"><span data-stu-id="11a64-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="11a64-222">已從 PsApiManagementContext 移除 `StaticIPs` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="11a64-223">此屬性已分割為 `PublicIPAddresses` 和 `PrivateIPAddresses`。</span><span class="sxs-lookup"><span data-stu-id="11a64-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="11a64-224">已從 New-AzureApiManagementVirtualNetwork Cmdlet 移除必要的 `Location` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="11a64-225">Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="11a64-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="11a64-226">已從 `Get-AzConsumptionUsageDetail` Cmdlet 移除 `InvoiceName` 參數。</span><span class="sxs-lookup"><span data-stu-id="11a64-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="11a64-227">指令碼必須針對發票使用其他身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="11a64-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="11a64-228">Az.CognitiveServices (先前是 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="11a64-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="11a64-229">已從 `Get-AzCognitiveServicesAccountSkus` Cmdlet 移除 `GetSkusWithAccountParamSetName` 參數集。</span><span class="sxs-lookup"><span data-stu-id="11a64-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="11a64-230">您必須依帳戶類型和位置來取得 SKU，而非使用 ResourceGroupName 和帳戶名稱來取得。</span><span class="sxs-lookup"><span data-stu-id="11a64-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="11a64-231">Az.Compute (先前是 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="11a64-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="11a64-232">已從 `PSVirtualMachine` 和 `PSVirtualMachineScaleSet` 物件中的 `Identity` 屬性移除 `IdentityIds`。指令碼不應再使用這個欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="11a64-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="11a64-233">`PSVirtualMachineScaleSetVM` 物件的 `InstanceView` 屬性，其類型已從 `VirtualMachineInstanceView` 變更為 `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="11a64-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="11a64-234">已從 `UpgradePolicy` 屬性移除 `AutoOSUpgradePolicy` 和 `AutomaticOSUpgrade` 屬性</span><span class="sxs-lookup"><span data-stu-id="11a64-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="11a64-235">`PSSnapshotUpdate` 物件中的 `Sku` 屬性，其類型已從 `DiskSku` 變更為 `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="11a64-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="11a64-236">已從 `Add-AzVMDataDisk` Cmdlet 移除 `VmScaleSetVMParameterSet`，您無法再將資料磁碟個別地新增至擴展集 VM。</span><span class="sxs-lookup"><span data-stu-id="11a64-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="11a64-237">Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="11a64-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="11a64-238">`GatewayName` 已成為 `New-AzDataFactoryEncryptValue` Cmdlet 的必要參數</span><span class="sxs-lookup"><span data-stu-id="11a64-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="11a64-239">已移除 `New-AzDataFactoryGatewayKey` Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11a64-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="11a64-240">已從 `Get-AzDataFactoryV2ActivityRun` Cmdlet 移除 `LinkedServiceName` 參數。指令碼不應再使用這個欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="11a64-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="11a64-241">Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="11a64-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="11a64-242">已移除淘汰的 Cmdlet：`New-AzDataLakeAnalyticsCatalogSecret`、`Remove-AzDataLakeAnalyticsCatalogSecret` 和 `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="11a64-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="11a64-243">Az.DataLakeStore (先前是 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="11a64-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="11a64-244">下列 Cmdlet 已將 `Encoding` 參數的類型從 `FileSystemCmdletProviderEncoding` 變更為 `System.Text.Encoding`。</span><span class="sxs-lookup"><span data-stu-id="11a64-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="11a64-245">這項變更會移除編碼值 `String` 和 `Oem`。</span><span class="sxs-lookup"><span data-stu-id="11a64-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="11a64-246">其他所有先前的編碼值則會保留。</span><span class="sxs-lookup"><span data-stu-id="11a64-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="11a64-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11a64-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="11a64-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="11a64-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="11a64-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="11a64-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="11a64-250">已從 `New-AzDataLakeStoreAccount` 和 `Set-AzDataLakeStoreAccount` Cmdlet 移除淘汰的 `Tags` 屬性別名</span><span class="sxs-lookup"><span data-stu-id="11a64-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="11a64-251">使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="11a64-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="11a64-252">應變更為</span><span class="sxs-lookup"><span data-stu-id="11a64-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="11a64-253">已從 `PSDataLakeStoreAccountBasic` 物件移除淘汰的 `Identity`、`EncryptionState`、`EncryptionProvisioningState`、`EncryptionConfig`、`FirewallState`、`FirewallRules`、`VirtualNetworkRules`、`TrustedIdProviderState`、`TrustedIdProviders`、`DefaultGroup`、`NewTier`、`CurrentTier`、`FirewallAllowAzureIps` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="11a64-254">指令碼若使用 `Get-AzDataLakeStoreAccount` 所傳回的 `PSDatalakeStoreAccount`，則不應參考這些屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="11a64-255">Az.KeyVault (先前是 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="11a64-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="11a64-256">`PurgeDisabled` 屬性已從 `PSKeyVaultKeyAttributes`、`PSKeyVaultKeyIdentityItem` 和 `PSKeyVaultSecretAttributes` 物件中移除 指令碼不應再參考 ```PurgeDisabled``` 屬性來做出處理決策。</span><span class="sxs-lookup"><span data-stu-id="11a64-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="11a64-257">Az.Media (先前是 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="11a64-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="11a64-258">已從 `New-AzMediaService` Cmdlet 移除淘汰的 `Tags` 屬性別名。使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="11a64-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="11a64-259">應變更為</span><span class="sxs-lookup"><span data-stu-id="11a64-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="11a64-260">Az.Monitor (先前是 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="11a64-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="11a64-261">已從 `Set-AzDiagnosticSetting` Cmdlet 移除複數名稱 `Categories` 和 `Timegrains` 參數，以便支援單一參數名稱。使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="11a64-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="11a64-262">應變更為</span><span class="sxs-lookup"><span data-stu-id="11a64-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="11a64-263">Az.Network (先前是 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="11a64-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="11a64-264">已從 `Get-AzServiceEndpointPolicyDefinition` Cmdlet 移除淘汰的 `ResourceId` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="11a64-265">已從 `PSVirtualNetwork` 物件移除淘汰的 `EnableVmProtection` 屬性</span><span class="sxs-lookup"><span data-stu-id="11a64-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="11a64-266">已移除淘汰的 `Set-AzVirtualNetworkGatewayVpnClientConfig` Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11a64-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="11a64-267">指令碼不應再根據這些欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="11a64-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="11a64-268">Az.OperationalInsights (先前是 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="11a64-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="11a64-269">已移除 `Get-AzOperationalInsightsDataSource` 的預設參數集，由 `ByWorkspaceNameByKind` 成為預設參數集</span><span class="sxs-lookup"><span data-stu-id="11a64-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="11a64-270">使用下列 Cmdlet 來列出資料來源的指令碼</span><span class="sxs-lookup"><span data-stu-id="11a64-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="11a64-271">應變更為指定某個種類</span><span class="sxs-lookup"><span data-stu-id="11a64-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="11a64-272">Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="11a64-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="11a64-273">已從 `New/Set-AzRecoveryServicesAsrPolicy` Cmdlet 移除 `Encryption` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="11a64-274">`TargetStorageAccountName` 現在是 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中用於還原受控磁碟的必要參數</span><span class="sxs-lookup"><span data-stu-id="11a64-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="11a64-275">已在 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中移除 `StorageAccountName` 和 `StorageAccountResourceGroupName` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="11a64-276">已在 `Get-AzRecoveryServicesBackupContainer` Cmdlet 中移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="11a64-277">Az.Resources (先前是 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="11a64-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="11a64-278">已從 `New/Set-AzPolicyAssignment` Cmdlet 移除 `Sku` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="11a64-279">已從 `New-AzADServicePrincipal` 和 `New-AzADSpCredential` Cmdlet 移除 `Password` 參數。密碼會自動產生，提供密碼的指令碼：</span><span class="sxs-lookup"><span data-stu-id="11a64-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="11a64-280">應變更為從輸出擷取密碼：</span><span class="sxs-lookup"><span data-stu-id="11a64-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="11a64-281">Az.ServiceFabric (先前是 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="11a64-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="11a64-282">已變更下列 Cmdlet 的傳回類型：</span><span class="sxs-lookup"><span data-stu-id="11a64-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="11a64-283">已移除 `ApplicationHealthPolicy` 類型的 `ServiceTypeHealthPolicies` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="11a64-284">已移除 `ClusterUpgradeDeltaHealthPolicy` 類型的 `ApplicationHealthPolicies` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="11a64-285">已移除 `ClusterUpgradePolicy` 類型的 `OverrideUserUpgradePolicy` 屬性。</span><span class="sxs-lookup"><span data-stu-id="11a64-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="11a64-286">這些變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="11a64-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="11a64-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="11a64-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="11a64-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="11a64-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="11a64-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="11a64-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="11a64-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="11a64-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="11a64-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="11a64-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="11a64-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="11a64-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="11a64-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="11a64-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="11a64-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="11a64-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="11a64-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="11a64-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="11a64-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="11a64-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="11a64-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="11a64-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="11a64-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="11a64-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="11a64-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="11a64-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="11a64-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="11a64-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="11a64-301">Az.Sql (previously AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="11a64-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="11a64-302">已從 `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除 `State` 和 `ResourceId` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="11a64-303">已移除淘汰的 Cmdlet：`Get/Set-AzSqlServerBackupLongTermRetentionVault`、`Get/Start/Stop-AzSqlServerUpgrade`、`Get/Set-AzSqlDatabaseAuditingPolicy`、`Get/Set-AzSqlServerAuditingPolicy`、`Remove-AzSqlDatabaseAuditing`、`Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="11a64-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="11a64-304">已從 `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除淘汰的 `Current` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="11a64-305">已從 `Get-AzSqlServerServiceObjective` Cmdlet 移除淘汰的 `DatabaseName` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="11a64-306">已從 `Set-AzSqlDatabaseDataMaskingPolicy` Cmdlet 移除淘汰的 `PrivilegedLogin` 參數</span><span class="sxs-lookup"><span data-stu-id="11a64-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="11a64-307">Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="11a64-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="11a64-308">為了支援建立僅具有儲存體帳戶名稱的 Oauth 儲存體內容，預設參數集已變更為 `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="11a64-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="11a64-309">範例： `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="11a64-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="11a64-310">`Location` 已成為 `Get-AzStorageUsage` Cmdlet 的必要參數</span><span class="sxs-lookup"><span data-stu-id="11a64-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="11a64-311">儲存體 API 方法現在會使用以工作為基礎的非同步模式 (TAP)，而非使用同步 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="11a64-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="11a64-312">下列範例示範新的非同步命令：</span><span class="sxs-lookup"><span data-stu-id="11a64-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="11a64-313">Blob 快照集</span><span class="sxs-lookup"><span data-stu-id="11a64-313">Blob Snapshot</span></span>

<span data-ttu-id="11a64-314">AzureRM：</span><span class="sxs-lookup"><span data-stu-id="11a64-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="11a64-315">Az：</span><span class="sxs-lookup"><span data-stu-id="11a64-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="11a64-316">共用快照集</span><span class="sxs-lookup"><span data-stu-id="11a64-316">Share Snapshot</span></span>

<span data-ttu-id="11a64-317">AzureRM：</span><span class="sxs-lookup"><span data-stu-id="11a64-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="11a64-318">Az：</span><span class="sxs-lookup"><span data-stu-id="11a64-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="11a64-319">取消刪除虛刪除的 Blob</span><span class="sxs-lookup"><span data-stu-id="11a64-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="11a64-320">AzureRM：</span><span class="sxs-lookup"><span data-stu-id="11a64-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="11a64-321">Az：</span><span class="sxs-lookup"><span data-stu-id="11a64-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="11a64-322">設定 Blob 層</span><span class="sxs-lookup"><span data-stu-id="11a64-322">Set Blob Tier</span></span>

<span data-ttu-id="11a64-323">AzureRM：</span><span class="sxs-lookup"><span data-stu-id="11a64-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="11a64-324">Az：</span><span class="sxs-lookup"><span data-stu-id="11a64-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="11a64-325">Az.Websites (先前是 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="11a64-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="11a64-326">已從 `PSAppServicePlan`、`PSCertificate`、`PSCloningInfo` 和 `PSSite` 物件移除淘汰的屬性</span><span class="sxs-lookup"><span data-stu-id="11a64-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
