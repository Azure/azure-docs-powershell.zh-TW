---
title: Azure Stack PowerShell 概觀 | Microsoft Docs
description: Azure Stack PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178454"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="932ae-103">AzureRM 模組 2.3.0</span><span class="sxs-lookup"><span data-stu-id="932ae-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="932ae-104">需求：</span><span class="sxs-lookup"><span data-stu-id="932ae-104">Requirements:</span></span>
<span data-ttu-id="932ae-105">支援的最低 Azure Stack 版本為 1808 版。</span><span class="sxs-lookup"><span data-stu-id="932ae-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="932ae-106">請注意：如果您使用的是舊版，請安裝版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="932ae-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="932ae-107">Install</span><span class="sxs-lookup"><span data-stu-id="932ae-107">Install</span></span>
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a><span data-ttu-id="932ae-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="932ae-108">Release Notes</span></span>
* <span data-ttu-id="932ae-109">2.3.0 版中有一些重大變更。</span><span class="sxs-lookup"><span data-stu-id="932ae-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="932ae-110">若要從 1.2.11 版升級，我們已建立移轉指南： https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="932ae-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="932ae-111">此版本對應到 azurestack 特有的 api 設定檔 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="932ae-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="932ae-112">所有模組皆取用比 AzureRm.Profile 模組上更大或相等的相依性。</span><span class="sxs-lookup"><span data-stu-id="932ae-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="932ae-113">每個模組支援的 API 版本都會更新。</span><span class="sxs-lookup"><span data-stu-id="932ae-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="932ae-114">計算 - 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="932ae-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="932ae-115">網路 - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="932ae-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="932ae-116">儲存體 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="932ae-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="932ae-117">資源 - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="932ae-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="932ae-118">KeyVault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="932ae-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="932ae-119">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="932ae-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="932ae-120">您可以在 https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json 中找到每個資源類型的完整 API 版本對應</span><span class="sxs-lookup"><span data-stu-id="932ae-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="932ae-121">內容：</span><span class="sxs-lookup"><span data-stu-id="932ae-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="932ae-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="932ae-122">Azure Bridge</span></span>
<span data-ttu-id="932ae-123">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="932ae-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="932ae-124">Backup </span><span class="sxs-lookup"><span data-stu-id="932ae-124">Backup</span></span>
<span data-ttu-id="932ae-125">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="932ae-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="932ae-126">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="932ae-126">Configure where backups are stored</span></span>
- <span data-ttu-id="932ae-127">執行備份</span><span class="sxs-lookup"><span data-stu-id="932ae-127">Perform backups</span></span>
- <span data-ttu-id="932ae-128">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="932ae-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="932ae-129">商業</span><span class="sxs-lookup"><span data-stu-id="932ae-129">Commerce</span></span>
<span data-ttu-id="932ae-130">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="932ae-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="932ae-131">計算</span><span class="sxs-lookup"><span data-stu-id="932ae-131">Compute</span></span>
<span data-ttu-id="932ae-132">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像、受控磁碟和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="932ae-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="932ae-133">網狀架構</span><span class="sxs-lookup"><span data-stu-id="932ae-133">Fabric</span></span>
<span data-ttu-id="932ae-134">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="932ae-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="932ae-135">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="932ae-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="932ae-136">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="932ae-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="932ae-137">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="932ae-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="932ae-138">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="932ae-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="932ae-139">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="932ae-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="932ae-140">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="932ae-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="932ae-141">資源庫</span><span class="sxs-lookup"><span data-stu-id="932ae-141">Gallery</span></span>
<span data-ttu-id="932ae-142">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="932ae-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="932ae-143">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="932ae-143">Infrastructure Insights</span></span>
<span data-ttu-id="932ae-144">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="932ae-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="932ae-145">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="932ae-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="932ae-146">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="932ae-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="932ae-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="932ae-147">KeyVault</span></span>
<span data-ttu-id="932ae-148">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="932ae-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="932ae-149">網路</span><span class="sxs-lookup"><span data-stu-id="932ae-149">Network</span></span>
<span data-ttu-id="932ae-150">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="932ae-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="932ae-151">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="932ae-151">Management of network quotas</span></span>
- <span data-ttu-id="932ae-152">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="932ae-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="932ae-153">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="932ae-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="932ae-154">儲存體</span><span class="sxs-lookup"><span data-stu-id="932ae-154">Storage</span></span>
<span data-ttu-id="932ae-155">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="932ae-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="932ae-156">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="932ae-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="932ae-157">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="932ae-157">Manage storage quotas</span></span>
- <span data-ttu-id="932ae-158">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="932ae-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="932ae-159">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="932ae-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="932ae-160">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="932ae-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="932ae-161">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="932ae-161">View information about the individual storage components</span></span>
- <span data-ttu-id="932ae-162">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="932ae-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="932ae-163">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="932ae-163">Subscription Admin</span></span>
<span data-ttu-id="932ae-164">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="932ae-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="932ae-165">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="932ae-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="932ae-166">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="932ae-166">Manage plans and offers</span></span>
- <span data-ttu-id="932ae-167">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="932ae-167">View usage and performance information</span></span>
- <span data-ttu-id="932ae-168">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="932ae-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="932ae-169">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="932ae-169">Subscription</span></span>
<span data-ttu-id="932ae-170">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="932ae-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="932ae-171">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="932ae-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="932ae-172">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="932ae-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="932ae-173">更新</span><span class="sxs-lookup"><span data-stu-id="932ae-173">Update</span></span>
<span data-ttu-id="932ae-174">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="932ae-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="932ae-175">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="932ae-175">In this module administrators can:</span></span>
- <span data-ttu-id="932ae-176">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="932ae-176">List and install available updates</span></span>
- <span data-ttu-id="932ae-177">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="932ae-177">Resume interrupted updates</span></span>
- <span data-ttu-id="932ae-178">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="932ae-178">View installed updates</span></span>
