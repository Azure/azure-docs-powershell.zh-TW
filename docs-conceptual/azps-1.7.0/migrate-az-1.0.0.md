---
title: Microsoft Azure PowerShell Az 1.0.0 的重大變更
description: 本移轉指南包含在 Az 第 1 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59363990"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="d8ee4-103">Az 1.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="d8ee4-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="d8ee4-104">本文件說明 6.x 版 AzureRM 和 Az 1.0.0 版之間的變更。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="d8ee4-105">目錄</span><span class="sxs-lookup"><span data-stu-id="d8ee4-105">Table of Contents</span></span>
- [<span data-ttu-id="d8ee4-106">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="d8ee4-107">Cmdlet 名詞前置詞的變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="d8ee4-108">模組名稱的變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="d8ee4-109">移除的模組</span><span class="sxs-lookup"><span data-stu-id="d8ee4-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="d8ee4-110">Windows PowerShell 5.1 和 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="d8ee4-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="d8ee4-111">使用 PSCredential 暫時移除使用者登入</span><span class="sxs-lookup"><span data-stu-id="d8ee4-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="d8ee4-112">預設使用裝置程式碼登入，而非網頁瀏覽器提示</span><span class="sxs-lookup"><span data-stu-id="d8ee4-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="d8ee4-113">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="d8ee4-114">Az.ApiManagement (先前是 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="d8ee4-115">Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="d8ee4-116">Az.CognitiveServices (先前是 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="d8ee4-117">Az.Compute (先前是 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="d8ee4-118">Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="d8ee4-119">Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="d8ee4-120">Az.DataLakeStore (先前是 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="d8ee4-121">Az.KeyVault (先前是 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="d8ee4-122">Az.Media (先前是 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="d8ee4-123">Az.Monitor (先前是 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="d8ee4-124">Az.Network (先前是 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="d8ee4-125">Az.OperationalInsights (先前是 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="d8ee4-126">Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="d8ee4-127">Az.Resources (先前是 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="d8ee4-128">Az.ServiceFabric (先前是 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="d8ee4-129">Az.Sql (先前是 AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="d8ee4-130">Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="d8ee4-131">Az.Websites (先前是 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="d8ee4-132">一般重大變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="d8ee4-133">Cmdlet 名詞前置詞的變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="d8ee4-134">在 AzureRM 中，Cmdlet 使用 'AzureRM' 或 'Azure' 作為名詞前置詞。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="d8ee4-135">Az 則將 Cmndlet 名稱予以簡化和標準化，讓所有 Cmdlet皆使用 'Az' 作為其 Cmdlet 名詞前置詞。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="d8ee4-136">例如︰</span><span class="sxs-lookup"><span data-stu-id="d8ee4-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="d8ee4-137">已變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="d8ee4-138">為了讓您更輕鬆地轉為使用這些新的 Cmdlet 名稱，Az 會引進兩個新的 Cmdlet，這兩者分別是 ```Enable-AzureRmAlias``` 和 ```Disable-AzureRmAlias```。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="d8ee4-139">```Enable-AzureRmAlias``` 會將別名從 AzureRM 中較舊的 Cmdlet 名稱，改建立為較新的 Az Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="d8ee4-140">此 Cmdlet 可讓您在目前的工作階段中建立別名，而您也可以藉由變更使用者或機器的設定檔，在所有工作階段建立別名。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="d8ee4-141">例如，下列的 AzureRM 指令碼：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="d8ee4-142">只要使用 ```Enable-AzureRmAlias``` 稍做變更即可執行：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="d8ee4-143">執行 ```Enable-AzureRmAlias -Scope CurrentUser``` 會對所有已開啟的 PowerShell 工作階段啟用別名，因此在執行此 Cmdlet 之後，就完全不需要變更這類指令碼：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="d8ee4-144">如需如何使用別名 Cmdlet 的完整詳細資訊，請從 PowerShell 提示字元執行 ```Get-Help -Online Enable-AzureRmAlias```。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="d8ee4-145">```Disable-AzureRmAlias``` 會移除 ```Enable-AzureRmAlias``` 所建立的 AzureRM Cmdlet 別名。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="d8ee4-146">如需完整的詳細資訊，請從 PowerShell 提示字元執行 ```Get-Help -Online Disable-AzureRmAlias```。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="d8ee4-147">模組名稱的變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-147">Module Name Changes</span></span>
- <span data-ttu-id="d8ee4-148">模組名稱已從 `AzureRM.*` 變更為 `Az.*`，但下列模組除外：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="d8ee4-149">模組名稱的變更表示，只要指令碼使用 ```#Requires``` 或 ```Import-Module``` 來載入特定模組，就需要進行變更，以改為使用新的模組。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="d8ee4-150">遷移 #Requires 陳述式</span><span class="sxs-lookup"><span data-stu-id="d8ee4-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="d8ee4-151">使用 #Requires 來宣告 AzureRM 模組相依性的指令碼，應更新為使用新的模組名稱</span><span class="sxs-lookup"><span data-stu-id="d8ee4-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="d8ee4-152">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="d8ee4-153">遷移 Import-Module 陳述式</span><span class="sxs-lookup"><span data-stu-id="d8ee4-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="d8ee4-154">使用 ```Import-Module``` 來載入 AzureRM 模組的指令碼，必須加以更新以反映新的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="d8ee4-155">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="d8ee4-156">遷移完整的 Cmdlet 叫用</span><span class="sxs-lookup"><span data-stu-id="d8ee4-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="d8ee4-157">使用模組完整 Cmdlet 叫用的指令碼，例如</span><span class="sxs-lookup"><span data-stu-id="d8ee4-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="d8ee4-158">應變更為使用新的模組和 Cmdlet 名稱</span><span class="sxs-lookup"><span data-stu-id="d8ee4-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="d8ee4-159">遷移模組資訊清單相依性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="d8ee4-160">透過模組資訊清單 (.psd1) 檔案來表達 AzureRM 模組相依性的模組，必須更新其 'RequiredModules' 區段中的模組名稱</span><span class="sxs-lookup"><span data-stu-id="d8ee4-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="d8ee4-161">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="d8ee4-162">移除的模組</span><span class="sxs-lookup"><span data-stu-id="d8ee4-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="d8ee4-163">不再支援這些服務的工具。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="d8ee4-164">建議客戶一有空就立刻遷移至替代服務。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="d8ee4-165">Windows PowerShell 5.1 和 .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="d8ee4-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="d8ee4-166">若要搭配使用 Az 和 Windows PowerShell 5.1，則必須安裝 .NET 4.7.2。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="d8ee4-167">不過，搭配使用 Az 和 PowerShell Core 則不需要 .NET 4.7.2。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="d8ee4-168">使用 PSCredential 暫時移除使用者登入</span><span class="sxs-lookup"><span data-stu-id="d8ee4-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="d8ee4-169">由於 .NET Standard 的驗證流程有變，我們暫時移除透過 PSCredential 來登入使用者的功能。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="d8ee4-170">這項功能會在 2019 年 1 月 15 日版本的 Windows PowerShell 5.1 重新引進。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="d8ee4-171">[此問題](https://github.com/Azure/azure-powershell/issues/7430)中會有這方面的詳細討論。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="d8ee4-172">預設使用裝置程式碼登入，而非網頁瀏覽器提示</span><span class="sxs-lookup"><span data-stu-id="d8ee4-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="d8ee4-173">由於 .NET Standard 的驗證流程有變，我們會在互動式登入期間使用裝置登入作為預設的登入流程。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="d8ee4-174">在 2019 年 1 月 15 日的版本中，會重新引進透過網頁瀏覽器來登入的功能，來作為 Windows PowerShell 5.1 的預設登入功能。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="d8ee4-175">屆時，使用者將能夠使用切換參數來選擇裝置登入功能。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="d8ee4-176">模組的重大變更</span><span class="sxs-lookup"><span data-stu-id="d8ee4-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="d8ee4-177">Az.ApiManagement (先前是 AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="d8ee4-178">即將移除下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="d8ee4-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8ee4-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="d8ee4-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="d8ee4-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="d8ee4-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d8ee4-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="d8ee4-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ee4-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="d8ee4-183">請改為使用 **Set-AzApiManagement** Cmdlet 來設定這些屬性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="d8ee4-184">已移除下列屬性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-184">Following properties were removed</span></span>
  - <span data-ttu-id="d8ee4-185">已從 `PsApiManagementContext` 移除 `PsApiManagementHostnameConfiguration` 類型的 `PortalHostnameConfiguration`、`ProxyHostnameConfiguration`、`ManagementHostnameConfiguration` 和 `ScmHostnameConfiguration` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="d8ee4-186">請改為使用 `PsApiManagementCustomHostNameConfiguration` 類型的 `PortalCustomHostnameConfiguration`、`ProxyCustomHostnameConfiguration`、`ManagementCustomHostnameConfiguration` 和 `ScmCustomHostnameConfiguration`。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="d8ee4-187">已從 PsApiManagementContext 移除 `StaticIPs` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="d8ee4-188">此屬性已分割為 `PublicIPAddresses` 和 `PrivateIPAddresses`。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="d8ee4-189">已從 New-AzureApiManagementVirtualNetwork Cmdlet 移除必要的 `Location` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="d8ee4-190">Az.Billing (先前是 AzureRM.Billing、AzureRM.Consumption 和 AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="d8ee4-191">已從 `Get-AzConsumptionUsageDetail` Cmdlet 移除 `InvoiceName` 參數。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="d8ee4-192">指令碼必須針對發票使用其他身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="d8ee4-193">Az.CognitiveServices (先前是 AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="d8ee4-194">已從 `Get-AzCognitiveServicesAccountSkus` Cmdlet 移除 `GetSkusWithAccountParamSetName` 參數集。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="d8ee4-195">您必須依帳戶類型和位置來取得 SKU，而非使用 ResourceGroupName 和帳戶名稱來取得。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="d8ee4-196">Az.Compute (先前是 AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="d8ee4-197">已從 `PSVirtualMachine` 和 `PSVirtualMachineScaleSet` 物件中的 `Identity` 屬性移除 `IdentityIds`。指令碼不應再使用這個欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="d8ee4-198">`PSVirtualMachineScaleSetVM` 物件的 `InstanceView` 屬性，其類型已從 `VirtualMachineInstanceView` 變更為 `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="d8ee4-199">已從 `UpgradePolicy` 屬性移除 `AutoOSUpgradePolicy` 和 `AutomaticOSUpgrade` 屬性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="d8ee4-200">`PSSnapshotUpdate` 物件中的 `Sku` 屬性，其類型已從 `DiskSku` 變更為 `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="d8ee4-201">已從 `Add-AzVMDataDisk` Cmdlet 移除 `VmScaleSetVMParameterSet`，您無法再將資料磁碟個別地新增至擴展集 VM。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="d8ee4-202">Az.DataFactory (先前是 AzureRM.DataFactories 和 AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="d8ee4-203">`GatewayName` 已成為 `New-AzDataFactoryEncryptValue` Cmdlet 的必要參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="d8ee4-204">已移除 `New-AzDataFactoryGatewayKey` Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8ee4-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="d8ee4-205">已從 `Get-AzDataFactoryV2ActivityRun` Cmdlet 移除 `LinkedServiceName` 參數。指令碼不應再使用這個欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="d8ee4-206">Az.DataLakeAnalytics (先前是 AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="d8ee4-207">已移除淘汰的 Cmdlet：`New-AzDataLakeAnalyticsCatalogSecret`、`Remove-AzDataLakeAnalyticsCatalogSecret` 和 `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="d8ee4-208">Az.DataLakeStore (先前是 AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="d8ee4-209">下列 Cmdlet 已將 `Encoding` 參數的類型從 `FileSystemCmdletProviderEncoding` 變更為 `System.Text.Encoding`。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="d8ee4-210">這項變更會移除編碼值 `String` 和 `Oem`。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="d8ee4-211">其他所有先前的編碼值則會保留。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="d8ee4-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8ee4-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="d8ee4-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d8ee4-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="d8ee4-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d8ee4-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="d8ee4-215">已從 `New-AzDataLakeStoreAccount` 和 `Set-AzDataLakeStoreAccount` Cmdlet 移除淘汰的 `Tags` 屬性別名</span><span class="sxs-lookup"><span data-stu-id="d8ee4-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="d8ee4-216">使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="d8ee4-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="d8ee4-217">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="d8ee4-218">已從 ```PSDataLakeStoreAccountBasic``` 物件移除淘汰的 ```Identity```、```EncryptionState```、```EncrypotionProvisioningState```、```EncryptionConfig```、```FirewallState```、```FirewallRules```、```VirtualNetworkRules```、```TrustedIdProviderState```、```TrustedIdProviders```、```DefaultGroup```、```NewTier```、```CurrentTier```、```FirewallAllowAzureIps``` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="d8ee4-219">指令碼若使用 ```Get-AzDataLakeStoreAccount``` 所傳回的 ```PSDatalakeStoreAccount```，則不應參考這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="d8ee4-220">Az.KeyVault (先前是 AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="d8ee4-221">已從 `PSKeyVaultKeyAttributes`、`PSKeyVaultKeyIdentityItem` 和 `PSKeyVaultSecretAttributes` 物件移除 `PurgeDisabled` 屬性。指令碼不應再參考 ```PurgeDisabled``` 屬性來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="d8ee4-222">Az.Media (先前是 AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="d8ee4-223">已從 `New-AzMediaService` Cmdlet 移除淘汰的 `Tags` 屬性別名。使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="d8ee4-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="d8ee4-224">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="d8ee4-225">Az.Monitor (先前是 AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="d8ee4-226">已從 `Set-AzDiagnosticSetting` Cmdlet 移除複數名稱 `Categories` 和 `Timegrains` 參數，以便支援單一參數名稱。使用下列 Cmdlet 的指令碼</span><span class="sxs-lookup"><span data-stu-id="d8ee4-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="d8ee4-227">應變更為</span><span class="sxs-lookup"><span data-stu-id="d8ee4-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="d8ee4-228">Az.Network (先前是 AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="d8ee4-229">已從 `Get-AzServiceEndpointPolicyDefinition` Cmdlet 移除淘汰的 `ResourceId` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="d8ee4-230">已從 `PSVirtualNetwork` 物件移除淘汰的 `EnableVmProtection` 屬性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="d8ee4-231">已移除淘汰的 `Set-AzVirtualNetworkGatewayVpnClientConfig` Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8ee4-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="d8ee4-232">指令碼不應再根據這些欄位的值來決定處理方式。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="d8ee4-233">Az.OperationalInsights (先前是 AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="d8ee4-234">已移除 `Get-AzOperationalInsightsDataSource` 的預設參數集，由 `ByWorkspaceNameByKind` 成為預設參數集</span><span class="sxs-lookup"><span data-stu-id="d8ee4-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="d8ee4-235">使用下列 Cmdlet 來列出資料來源的指令碼</span><span class="sxs-lookup"><span data-stu-id="d8ee4-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="d8ee4-236">應變更為指定某個種類</span><span class="sxs-lookup"><span data-stu-id="d8ee4-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="d8ee4-237">Az.RecoveryServices (先前是 AzureRM.RecoveryServices、AzureRM.RecoveryServices.Backup 和 AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="d8ee4-238">已從 `New/Set-AzRecoveryServicesAsrPolicy` Cmdlet 移除 `Encryption` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="d8ee4-239">`TargetStorageAccountName` 現在是 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中用於還原受控磁碟的必要參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="d8ee4-240">已在 `Restore-AzRecoveryServicesBackupItem` Cmdlet 中移除 `StorageAccountName` 和 `StorageAccountResourceGroupName` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="d8ee4-241">已在 `Get-AzRecoveryServicesBackupContainer` Cmdlet 中移除 `Name` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="d8ee4-242">Az.Resources (先前是 AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="d8ee4-243">已從 `New/Set-AzPolicyAssignment` Cmdlet 移除 `Sku` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="d8ee4-244">已從 `New-AzADServicePrincipal` 和 `New-AzADSpCredential` Cmdlet 移除 `Password` 參數。密碼會自動產生，提供密碼的指令碼：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="d8ee4-245">應變更為從輸出擷取密碼：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="d8ee4-246">Az.ServiceFabric (先前是 AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="d8ee4-247">已變更下列 Cmdlet 的傳回類型：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="d8ee4-248">已移除 `ApplicationHealthPolicy` 類型的 `SerivceTypeHealthPolicies` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="d8ee4-249">已移除 `ClusterUpgradeDeltaHealthPolicy` 類型的 `ApplicationHealthPolicies` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="d8ee4-250">已移除 `ClusterUpgradePolicy` 類型的 `OverrideUserUpgradePolicy` 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="d8ee4-251">這些變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="d8ee4-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ee4-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="d8ee4-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ee4-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="d8ee4-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d8ee4-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="d8ee4-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d8ee4-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="d8ee4-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d8ee4-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="d8ee4-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ee4-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="d8ee4-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d8ee4-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="d8ee4-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d8ee4-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="d8ee4-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d8ee4-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="d8ee4-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d8ee4-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="d8ee4-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d8ee4-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="d8ee4-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="d8ee4-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="d8ee4-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="d8ee4-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="d8ee4-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="d8ee4-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="d8ee4-266">Az.Sql (previously AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="d8ee4-267">已從 `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除 `State` 和 `ResourceId` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="d8ee4-268">已移除淘汰的 Cmdlet：`Get/Set-AzSqlServerBackupLongTermRetentionVault`、`Get/Start/Stop-AzSqlServerUpgrade`、`Get/Set-AzSqlDatabaseAuditingPolicy`、`Get/Set-AzSqlServerAuditingPolicy`、`Remove-AzSqlDatabaseAuditing`、`Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="d8ee4-269">已從 `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` Cmdlet 移除淘汰的 `Current` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="d8ee4-270">已從 `Get-AzSqlServerServiceObjective` Cmdlet 移除淘汰的 `DatabaseName` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="d8ee4-271">已從 `Set-AzSqlDatabaseDataMaskingPolicy` Cmdlet 移除淘汰的 `PrivilegedLogin` 參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="d8ee4-272">Az.Storage (先前是 Azure.Storage 和 AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="d8ee4-273">為了支援建立僅具有儲存體帳戶名稱的 Oauth 儲存體內容，預設參數集已變更為 `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="d8ee4-274">範例： `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="d8ee4-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="d8ee4-275">`Location` 已成為 `Get-AzStorageUsage` Cmdlet 的必要參數</span><span class="sxs-lookup"><span data-stu-id="d8ee4-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="d8ee4-276">儲存體 API 方法現在會使用以工作為基礎的非同步模式 (TAP)，而非使用同步 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d8ee4-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="d8ee4-277">1.Blob 快照集</span><span class="sxs-lookup"><span data-stu-id="d8ee4-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="d8ee4-278">之前：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="d8ee4-279">之後︰</span><span class="sxs-lookup"><span data-stu-id="d8ee4-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="d8ee4-280">2.共用快照集</span><span class="sxs-lookup"><span data-stu-id="d8ee4-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="d8ee4-281">之前：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="d8ee4-282">之後︰</span><span class="sxs-lookup"><span data-stu-id="d8ee4-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="d8ee4-283">3.取消刪除虛刪除的 Blob</span><span class="sxs-lookup"><span data-stu-id="d8ee4-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="d8ee4-284">之前：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="d8ee4-285">之後︰</span><span class="sxs-lookup"><span data-stu-id="d8ee4-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="d8ee4-286">4.設定 Blob 層</span><span class="sxs-lookup"><span data-stu-id="d8ee4-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="d8ee4-287">之前：</span><span class="sxs-lookup"><span data-stu-id="d8ee4-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="d8ee4-288">之後︰</span><span class="sxs-lookup"><span data-stu-id="d8ee4-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="d8ee4-289">Az.Websites (先前是 AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="d8ee4-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="d8ee4-290">已從 `PSAppServicePlan`、`PSCertificate`、`PSCloningInfo` 和 `PSSite` 物件移除淘汰的屬性</span><span class="sxs-lookup"><span data-stu-id="d8ee4-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>