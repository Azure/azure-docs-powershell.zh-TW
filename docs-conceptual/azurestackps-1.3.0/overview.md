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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399938"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="be93f-103">Azure Stack 模組 1.3.0</span><span class="sxs-lookup"><span data-stu-id="be93f-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="be93f-104">需求：</span><span class="sxs-lookup"><span data-stu-id="be93f-104">Requirements:</span></span>
<span data-ttu-id="be93f-105">支援的最低 Azure Stack 版本為 1804 版。</span><span class="sxs-lookup"><span data-stu-id="be93f-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="be93f-106">請注意：如果您使用的是舊版，請安裝版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="be93f-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="be93f-107">已知問題：</span><span class="sxs-lookup"><span data-stu-id="be93f-107">Known issues:</span></span>

- <span data-ttu-id="be93f-108">需要 Azure Stack 1803 版本才能關閉警示</span><span class="sxs-lookup"><span data-stu-id="be93f-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="be93f-109">某些儲存體 Cmdlet 需要 Azure Stack 1804 版本</span><span class="sxs-lookup"><span data-stu-id="be93f-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="be93f-110">New-AzsOffer 不允許建立具公用狀態的供應項目。</span><span class="sxs-lookup"><span data-stu-id="be93f-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="be93f-111">Set-AzsOffer Cmdlet 之後需要呼叫以變更狀態。</span><span class="sxs-lookup"><span data-stu-id="be93f-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="be93f-112">必須重新部署才能移除 IP 集區</span><span class="sxs-lookup"><span data-stu-id="be93f-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="be93f-113">重大變更</span><span class="sxs-lookup"><span data-stu-id="be93f-113">Breaking Changes</span></span>
<span data-ttu-id="be93f-114">從 1.2.11 移轉的所有中斷性變更記錄於此 https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="be93f-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="be93f-115">Install</span><span class="sxs-lookup"><span data-stu-id="be93f-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="be93f-116">內容：</span><span class="sxs-lookup"><span data-stu-id="be93f-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="be93f-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="be93f-117">Azure Bridge</span></span>
<span data-ttu-id="be93f-118">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="be93f-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="be93f-119">Backup </span><span class="sxs-lookup"><span data-stu-id="be93f-119">Backup</span></span>
<span data-ttu-id="be93f-120">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="be93f-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="be93f-121">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="be93f-121">Configure where backups are stored</span></span>
- <span data-ttu-id="be93f-122">執行備份</span><span class="sxs-lookup"><span data-stu-id="be93f-122">Perform backups</span></span>
- <span data-ttu-id="be93f-123">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="be93f-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="be93f-124">商業</span><span class="sxs-lookup"><span data-stu-id="be93f-124">Commerce</span></span>
<span data-ttu-id="be93f-125">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="be93f-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="be93f-126">計算</span><span class="sxs-lookup"><span data-stu-id="be93f-126">Compute</span></span>
<span data-ttu-id="be93f-127">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="be93f-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="be93f-128">網狀架構</span><span class="sxs-lookup"><span data-stu-id="be93f-128">Fabric</span></span>
<span data-ttu-id="be93f-129">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="be93f-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="be93f-130">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="be93f-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="be93f-131">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="be93f-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="be93f-132">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="be93f-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="be93f-133">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="be93f-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="be93f-134">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="be93f-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="be93f-135">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="be93f-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="be93f-136">資源庫</span><span class="sxs-lookup"><span data-stu-id="be93f-136">Gallery</span></span>
<span data-ttu-id="be93f-137">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="be93f-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="be93f-138">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="be93f-138">Infrastructure Insights</span></span>
<span data-ttu-id="be93f-139">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="be93f-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="be93f-140">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="be93f-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="be93f-141">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="be93f-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="be93f-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="be93f-142">KeyVault</span></span>
<span data-ttu-id="be93f-143">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="be93f-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="be93f-144">網路</span><span class="sxs-lookup"><span data-stu-id="be93f-144">Network</span></span>
<span data-ttu-id="be93f-145">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="be93f-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="be93f-146">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="be93f-146">Management of network quotas</span></span>
- <span data-ttu-id="be93f-147">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="be93f-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="be93f-148">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="be93f-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="be93f-149">儲存體</span><span class="sxs-lookup"><span data-stu-id="be93f-149">Storage</span></span>
<span data-ttu-id="be93f-150">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="be93f-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="be93f-151">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="be93f-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="be93f-152">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="be93f-152">Manage storage quotas</span></span>
- <span data-ttu-id="be93f-153">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="be93f-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="be93f-154">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="be93f-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="be93f-155">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="be93f-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="be93f-156">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="be93f-156">View information about the individual storage components</span></span>
- <span data-ttu-id="be93f-157">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="be93f-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="be93f-158">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="be93f-158">Subscription Admin</span></span>
<span data-ttu-id="be93f-159">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="be93f-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="be93f-160">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="be93f-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="be93f-161">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="be93f-161">Manage plans and offers</span></span>
- <span data-ttu-id="be93f-162">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="be93f-162">View usage and performance information</span></span>
- <span data-ttu-id="be93f-163">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="be93f-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="be93f-164">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="be93f-164">Subscription</span></span>
<span data-ttu-id="be93f-165">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="be93f-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="be93f-166">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="be93f-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="be93f-167">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="be93f-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="be93f-168">更新</span><span class="sxs-lookup"><span data-stu-id="be93f-168">Update</span></span>
<span data-ttu-id="be93f-169">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="be93f-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="be93f-170">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="be93f-170">In this module administrators can:</span></span>
- <span data-ttu-id="be93f-171">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="be93f-171">List and install available updates</span></span>
- <span data-ttu-id="be93f-172">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="be93f-172">Resume interrupted updates</span></span>
- <span data-ttu-id="be93f-173">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="be93f-173">View installed updates</span></span>
