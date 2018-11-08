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
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211157"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="ff27c-103">Azure Stack 模組 1.5.0</span><span class="sxs-lookup"><span data-stu-id="ff27c-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ff27c-104">需求：</span><span class="sxs-lookup"><span data-stu-id="ff27c-104">Requirements:</span></span>
<span data-ttu-id="ff27c-105">支援的最低 Azure Stack 版本為 1808 版。</span><span class="sxs-lookup"><span data-stu-id="ff27c-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="ff27c-106">請注意：如果您使用的是舊版，請安裝版本 1.4.0</span><span class="sxs-lookup"><span data-stu-id="ff27c-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="ff27c-107">已知問題：</span><span class="sxs-lookup"><span data-stu-id="ff27c-107">Known issues:</span></span>

- <span data-ttu-id="ff27c-108">New-AzsOffer 不允許建立具公用狀態的供應項目。</span><span class="sxs-lookup"><span data-stu-id="ff27c-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ff27c-109">Set-AzsOffer Cmdlet 之後需要呼叫以變更狀態。</span><span class="sxs-lookup"><span data-stu-id="ff27c-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ff27c-110">必須重新部署才能移除 IP 集區</span><span class="sxs-lookup"><span data-stu-id="ff27c-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="ff27c-111">Install</span><span class="sxs-lookup"><span data-stu-id="ff27c-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a><span data-ttu-id="ff27c-112">版本資訊</span><span class="sxs-lookup"><span data-stu-id="ff27c-112">Release Notes</span></span>
* <span data-ttu-id="ff27c-113">已更新所有 Azure Stack Admin 模組以取得比 AzureRm.Profile 模組上更大或相等的相依性</span><span class="sxs-lookup"><span data-stu-id="ff27c-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="ff27c-114">支援處理所有模組中的巢狀資源名稱</span><span class="sxs-lookup"><span data-stu-id="ff27c-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="ff27c-115">修正所有模組中的錯誤 (bug)，其中 ErrorActionPreference 會複寫為「停止」</span><span class="sxs-lookup"><span data-stu-id="ff27c-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="ff27c-116">Azs.Compute.Admin 模組</span><span class="sxs-lookup"><span data-stu-id="ff27c-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="ff27c-117">已新增配額屬性以支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="ff27c-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="ff27c-118">新增與磁碟移轉相關的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff27c-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="ff27c-119">平台映像和 VM 擴充物件中的其他屬性</span><span class="sxs-lookup"><span data-stu-id="ff27c-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="ff27c-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="ff27c-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="ff27c-121">用於新增縮放單位節點的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff27c-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="ff27c-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="ff27c-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="ff27c-123">Set-AzsBackupShare 現在是 Set-AzsBackupConfiguration Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="ff27c-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ff27c-124">Get-AzsBackupLocation 現在是 Get-AzsBackupConfiguration Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="ff27c-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ff27c-125">Set-AzsBackupConfiguration，BackupShare 參數現在是 path 參數的別名</span><span class="sxs-lookup"><span data-stu-id="ff27c-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="ff27c-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="ff27c-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="ff27c-127">Get-AzsDelegatedProviderOffer，OfferName 參數現在是 Offer 的別名</span><span class="sxs-lookup"><span data-stu-id="ff27c-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="ff27c-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="ff27c-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="ff27c-129">Get-AzsDelegatedProviderOffer，OfferName 參數現在是 Offer 的別名</span><span class="sxs-lookup"><span data-stu-id="ff27c-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="ff27c-130">內容：</span><span class="sxs-lookup"><span data-stu-id="ff27c-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ff27c-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ff27c-131">Azure Bridge</span></span>
<span data-ttu-id="ff27c-132">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="ff27c-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ff27c-133">Backup </span><span class="sxs-lookup"><span data-stu-id="ff27c-133">Backup</span></span>
<span data-ttu-id="ff27c-134">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="ff27c-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ff27c-135">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="ff27c-135">Configure where backups are stored</span></span>
- <span data-ttu-id="ff27c-136">執行備份</span><span class="sxs-lookup"><span data-stu-id="ff27c-136">Perform backups</span></span>
- <span data-ttu-id="ff27c-137">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="ff27c-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ff27c-138">商業</span><span class="sxs-lookup"><span data-stu-id="ff27c-138">Commerce</span></span>
<span data-ttu-id="ff27c-139">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="ff27c-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ff27c-140">計算</span><span class="sxs-lookup"><span data-stu-id="ff27c-140">Compute</span></span>
<span data-ttu-id="ff27c-141">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像、受控磁碟和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="ff27c-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ff27c-142">網狀架構</span><span class="sxs-lookup"><span data-stu-id="ff27c-142">Fabric</span></span>
<span data-ttu-id="ff27c-143">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="ff27c-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ff27c-144">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="ff27c-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ff27c-145">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="ff27c-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ff27c-146">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="ff27c-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ff27c-147">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="ff27c-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ff27c-148">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="ff27c-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ff27c-149">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="ff27c-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ff27c-150">資源庫</span><span class="sxs-lookup"><span data-stu-id="ff27c-150">Gallery</span></span>
<span data-ttu-id="ff27c-151">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="ff27c-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ff27c-152">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="ff27c-152">Infrastructure Insights</span></span>
<span data-ttu-id="ff27c-153">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="ff27c-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ff27c-154">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="ff27c-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ff27c-155">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="ff27c-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ff27c-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff27c-156">KeyVault</span></span>
<span data-ttu-id="ff27c-157">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="ff27c-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ff27c-158">網路</span><span class="sxs-lookup"><span data-stu-id="ff27c-158">Network</span></span>
<span data-ttu-id="ff27c-159">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="ff27c-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ff27c-160">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="ff27c-160">Management of network quotas</span></span>
- <span data-ttu-id="ff27c-161">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="ff27c-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ff27c-162">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="ff27c-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ff27c-163">儲存體</span><span class="sxs-lookup"><span data-stu-id="ff27c-163">Storage</span></span>
<span data-ttu-id="ff27c-164">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="ff27c-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ff27c-165">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="ff27c-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ff27c-166">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="ff27c-166">Manage storage quotas</span></span>
- <span data-ttu-id="ff27c-167">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="ff27c-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ff27c-168">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="ff27c-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ff27c-169">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="ff27c-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ff27c-170">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ff27c-170">View information about the individual storage components</span></span>
- <span data-ttu-id="ff27c-171">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="ff27c-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ff27c-172">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="ff27c-172">Subscription Admin</span></span>
<span data-ttu-id="ff27c-173">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="ff27c-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ff27c-174">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="ff27c-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ff27c-175">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="ff27c-175">Manage plans and offers</span></span>
- <span data-ttu-id="ff27c-176">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="ff27c-176">View usage and performance information</span></span>
- <span data-ttu-id="ff27c-177">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="ff27c-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ff27c-178">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="ff27c-178">Subscription</span></span>
<span data-ttu-id="ff27c-179">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="ff27c-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ff27c-180">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="ff27c-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ff27c-181">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="ff27c-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ff27c-182">更新</span><span class="sxs-lookup"><span data-stu-id="ff27c-182">Update</span></span>
<span data-ttu-id="ff27c-183">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="ff27c-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ff27c-184">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="ff27c-184">In this module administrators can:</span></span>
- <span data-ttu-id="ff27c-185">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="ff27c-185">List and install available updates</span></span>
- <span data-ttu-id="ff27c-186">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="ff27c-186">Resume interrupted updates</span></span>
- <span data-ttu-id="ff27c-187">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="ff27c-187">View installed updates</span></span>
