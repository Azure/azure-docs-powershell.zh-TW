---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882362"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="42083-103">Azure Stack 模組 1.4.0</span><span class="sxs-lookup"><span data-stu-id="42083-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="42083-104">需求：</span><span class="sxs-lookup"><span data-stu-id="42083-104">Requirements:</span></span>
<span data-ttu-id="42083-105">支援的最低 Azure Stack 版本為 1804 版。</span><span class="sxs-lookup"><span data-stu-id="42083-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="42083-106">請注意：如果您使用的是舊版，請安裝版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="42083-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="42083-107">已知問題：</span><span class="sxs-lookup"><span data-stu-id="42083-107">Known issues:</span></span>

- <span data-ttu-id="42083-108">需要 Azure Stack 1803 版本才能關閉警示</span><span class="sxs-lookup"><span data-stu-id="42083-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="42083-109">New-AzsOffer 不允許建立具公用狀態的供應項目。</span><span class="sxs-lookup"><span data-stu-id="42083-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="42083-110">Set-AzsOffer Cmdlet 之後需要呼叫以變更狀態。</span><span class="sxs-lookup"><span data-stu-id="42083-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="42083-111">必須重新部署才能移除 IP 集區</span><span class="sxs-lookup"><span data-stu-id="42083-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="42083-112">重大變更</span><span class="sxs-lookup"><span data-stu-id="42083-112">Breaking Changes</span></span>
<span data-ttu-id="42083-113">自版本 1.3.0 以來均無重大變更。</span><span class="sxs-lookup"><span data-stu-id="42083-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="42083-114">從 1.2.11 移轉的所有中斷性變更記錄於此 https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="42083-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="42083-115">Install</span><span class="sxs-lookup"><span data-stu-id="42083-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="42083-116">版本資訊</span><span class="sxs-lookup"><span data-stu-id="42083-116">Release Notes</span></span>
    * <span data-ttu-id="42083-117">Azurestack 1.4.0 版本自先前版本 1.3.0 以來並無重大變更</span><span class="sxs-lookup"><span data-stu-id="42083-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="42083-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="42083-119">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="42083-121">已將 BackupFrequencyInHours、IsBackupSchedulerEnabled 及 BackupRetentionPeriodInDays 等新參數新增至 Cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="42083-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="42083-122">已新增 Cmdlet New-EncyptionKeyBase64，以協助建立加密金鑰</span><span class="sxs-lookup"><span data-stu-id="42083-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="42083-123">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="42083-125">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="42083-127">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="42083-128">已新增 Cmdlet Add-AzsScaleUnitNode，讓管理員可將新的縮放單位節點新增至 azurestack 戳記</span><span class="sxs-lookup"><span data-stu-id="42083-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="42083-129">已新增 Cmdlet 和 New-AzsScaleUnitNodeObject，以協助建立縮放單位參數物件</span><span class="sxs-lookup"><span data-stu-id="42083-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="42083-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="42083-131">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="42083-133">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="42083-135">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="42083-137">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="42083-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="42083-139">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="42083-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="42083-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="42083-141">已新增 Cmdlet Move-AzsSubscription，以便在受委派的提供者供應項目之間移動訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="42083-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="42083-142">已新增 Cmdlet Test-AzsMoveSubscription，以便驗證該使用者訂用帳戶可以在受委派的提供者供應項目之間移動</span><span class="sxs-lookup"><span data-stu-id="42083-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="42083-143">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="42083-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="42083-144">內容：</span><span class="sxs-lookup"><span data-stu-id="42083-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="42083-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="42083-145">Azure Bridge</span></span>
<span data-ttu-id="42083-146">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="42083-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="42083-147">Backup </span><span class="sxs-lookup"><span data-stu-id="42083-147">Backup</span></span>
<span data-ttu-id="42083-148">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="42083-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="42083-149">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="42083-149">Configure where backups are stored</span></span>
- <span data-ttu-id="42083-150">執行備份</span><span class="sxs-lookup"><span data-stu-id="42083-150">Perform backups</span></span>
- <span data-ttu-id="42083-151">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="42083-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="42083-152">商業</span><span class="sxs-lookup"><span data-stu-id="42083-152">Commerce</span></span>
<span data-ttu-id="42083-153">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="42083-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="42083-154">計算</span><span class="sxs-lookup"><span data-stu-id="42083-154">Compute</span></span>
<span data-ttu-id="42083-155">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="42083-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="42083-156">網狀架構</span><span class="sxs-lookup"><span data-stu-id="42083-156">Fabric</span></span>
<span data-ttu-id="42083-157">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="42083-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="42083-158">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="42083-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="42083-159">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="42083-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="42083-160">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="42083-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="42083-161">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="42083-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="42083-162">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="42083-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="42083-163">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="42083-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="42083-164">資源庫</span><span class="sxs-lookup"><span data-stu-id="42083-164">Gallery</span></span>
<span data-ttu-id="42083-165">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="42083-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="42083-166">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="42083-166">Infrastructure Insights</span></span>
<span data-ttu-id="42083-167">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="42083-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="42083-168">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="42083-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="42083-169">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="42083-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="42083-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="42083-170">KeyVault</span></span>
<span data-ttu-id="42083-171">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="42083-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="42083-172">網路</span><span class="sxs-lookup"><span data-stu-id="42083-172">Network</span></span>
<span data-ttu-id="42083-173">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="42083-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="42083-174">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="42083-174">Management of network quotas</span></span>
- <span data-ttu-id="42083-175">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="42083-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="42083-176">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="42083-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="42083-177">儲存體</span><span class="sxs-lookup"><span data-stu-id="42083-177">Storage</span></span>
<span data-ttu-id="42083-178">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="42083-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="42083-179">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="42083-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="42083-180">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="42083-180">Manage storage quotas</span></span>
- <span data-ttu-id="42083-181">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="42083-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="42083-182">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="42083-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="42083-183">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="42083-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="42083-184">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="42083-184">View information about the individual storage components</span></span>
- <span data-ttu-id="42083-185">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="42083-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="42083-186">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="42083-186">Subscription Admin</span></span>
<span data-ttu-id="42083-187">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="42083-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="42083-188">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="42083-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="42083-189">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="42083-189">Manage plans and offers</span></span>
- <span data-ttu-id="42083-190">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="42083-190">View usage and performance information</span></span>
- <span data-ttu-id="42083-191">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="42083-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="42083-192">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="42083-192">Subscription</span></span>
<span data-ttu-id="42083-193">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="42083-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="42083-194">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="42083-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="42083-195">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="42083-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="42083-196">更新</span><span class="sxs-lookup"><span data-stu-id="42083-196">Update</span></span>
<span data-ttu-id="42083-197">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="42083-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="42083-198">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="42083-198">In this module administrators can:</span></span>
- <span data-ttu-id="42083-199">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="42083-199">List and install available updates</span></span>
- <span data-ttu-id="42083-200">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="42083-200">Resume interrupted updates</span></span>
- <span data-ttu-id="42083-201">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="42083-201">View installed updates</span></span>
