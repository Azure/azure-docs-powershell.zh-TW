---
Module Name: Az.CloudService
Module Guid: a41eb61d-c5a1-4e9b-81a7-b8905fff7f2c
Download Help Link: https://docs.microsoft.com/powershell/module/az.cloudservice
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
ms.openlocfilehash: 39cd42fb48f2dd40b8c8225df935402e21ca0e37
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906326"
---
# <span data-ttu-id="137a8-101">Az.CloudService 模組</span><span class="sxs-lookup"><span data-stu-id="137a8-101">Az.CloudService Module</span></span>
## <span data-ttu-id="137a8-102">描述</span><span class="sxs-lookup"><span data-stu-id="137a8-102">Description</span></span>
<span data-ttu-id="137a8-103">Microsoft Azure PowerShell：CloudService Cmdlet</span><span class="sxs-lookup"><span data-stu-id="137a8-103">Microsoft Azure PowerShell: CloudService cmdlets</span></span>

## <span data-ttu-id="137a8-104">Az.CloudService Cmdlet</span><span class="sxs-lookup"><span data-stu-id="137a8-104">Az.CloudService Cmdlets</span></span>
### [<span data-ttu-id="137a8-105">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-105">Get-AzCloudService</span></span>](Get-AzCloudService.md)
<span data-ttu-id="137a8-106">顯示雲端服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="137a8-106">Display information about a cloud service.</span></span>

### [<span data-ttu-id="137a8-107">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="137a8-107">Get-AzCloudServiceInstanceView</span></span>](Get-AzCloudServiceInstanceView.md)
<span data-ttu-id="137a8-108">獲得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="137a8-108">Gets the status of a cloud service.</span></span>

### [<span data-ttu-id="137a8-109">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="137a8-109">Get-AzCloudServiceNetworkInterfaces</span></span>](Get-AzCloudServiceNetworkInterfaces.md)
<span data-ttu-id="137a8-110">取得雲端服務的網路介面。</span><span class="sxs-lookup"><span data-stu-id="137a8-110">Get the network interfaces of a cloud service.</span></span>

### [<span data-ttu-id="137a8-111">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="137a8-111">Get-AzCloudServicePublicIPAddress</span></span>](Get-AzCloudServicePublicIPAddress.md)
<span data-ttu-id="137a8-112">取得雲端服務的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="137a8-112">Get the public IP address of a cloud service.</span></span>

### [<span data-ttu-id="137a8-113">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="137a8-113">Get-AzCloudServiceRoleInstance</span></span>](Get-AzCloudServiceRoleInstance.md)
<span data-ttu-id="137a8-114">從雲端服務獲得角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-114">Gets a role instance from a cloud service.</span></span>

### [<span data-ttu-id="137a8-115">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="137a8-115">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>](Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md)
<span data-ttu-id="137a8-116">在雲端服務中為角色實例獲得遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="137a8-116">Gets a remote desktop file for a role instance in a cloud service.</span></span>

### [<span data-ttu-id="137a8-117">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="137a8-117">Get-AzCloudServiceRoleInstanceView</span></span>](Get-AzCloudServiceRoleInstanceView.md)
<span data-ttu-id="137a8-118">在雲端服務中，取回角色實例的執行時間狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="137a8-118">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

### [<span data-ttu-id="137a8-119">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="137a8-119">Invoke-AzCloudServiceRebuild</span></span>](Invoke-AzCloudServiceRebuild.md)
<span data-ttu-id="137a8-120">重建角色實例會以 Web 角色或員工角色實例重新安裝作業系統，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="137a8-120">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="137a8-121">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-121">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

### [<span data-ttu-id="137a8-122">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="137a8-122">Invoke-AzCloudServiceReimage</span></span>](Invoke-AzCloudServiceReimage.md)
<span data-ttu-id="137a8-123">重新映射非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="137a8-123">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="137a8-124">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="137a8-124">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>](Invoke-AzCloudServiceRoleInstanceRebuild.md)
<span data-ttu-id="137a8-125">重建角色實例非同步作業會重新安裝作業系統上的網頁角色或員工角色實例，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="137a8-125">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="137a8-126">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-126">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

### [<span data-ttu-id="137a8-127">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="137a8-127">Invoke-AzCloudServiceRoleInstanceReimage</span></span>](Invoke-AzCloudServiceRoleInstanceReimage.md)
<span data-ttu-id="137a8-128">重新映射角色實例非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="137a8-128">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="137a8-129">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-129">New-AzCloudService</span></span>](New-AzCloudService.md)
<span data-ttu-id="137a8-130">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="137a8-130">Create or update a cloud service.</span></span>
<span data-ttu-id="137a8-131">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="137a8-131">Please note some properties can be set only during cloud service creation.</span></span>

### [<span data-ttu-id="137a8-132">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="137a8-132">New-AzCloudServiceDiagnosticsExtension</span></span>](New-AzCloudServiceDiagnosticsExtension.md)
<span data-ttu-id="137a8-133">為診斷擴充功能建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="137a8-133">Create a in-memory object for Diagnostics Extension</span></span>

### [<span data-ttu-id="137a8-134">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="137a8-134">New-AzCloudServiceExtensionObject</span></span>](New-AzCloudServiceExtensionObject.md)
<span data-ttu-id="137a8-135">建立記憶體內物件以用於擴充功能</span><span class="sxs-lookup"><span data-stu-id="137a8-135">Create a in-memory object for Extension</span></span>

### [<span data-ttu-id="137a8-136">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="137a8-136">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerConfigurationObject.md)
<span data-ttu-id="137a8-137">為 LoadBalancerConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="137a8-137">Create a in-memory object for LoadBalancerConfiguration</span></span>

### [<span data-ttu-id="137a8-138">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="137a8-138">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md)
<span data-ttu-id="137a8-139">為 LoadBalancerFrontendIPConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="137a8-139">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

### [<span data-ttu-id="137a8-140">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="137a8-140">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>](New-AzCloudServiceRemoteDesktopExtensionObject.md)
<span data-ttu-id="137a8-141">建立遠端桌面擴充功能的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="137a8-141">Create a in-memory object for Remote Desktop Extension</span></span>

### [<span data-ttu-id="137a8-142">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="137a8-142">New-AzCloudServiceRoleProfilePropertiesObject</span></span>](New-AzCloudServiceRoleProfilePropertiesObject.md)
<span data-ttu-id="137a8-143">為 CloudServiceRoleProfileProperties 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="137a8-143">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

### [<span data-ttu-id="137a8-144">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="137a8-144">New-AzCloudServiceVaultSecretGroupObject</span></span>](New-AzCloudServiceVaultSecretGroupObject.md)
<span data-ttu-id="137a8-145">為機密群組建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="137a8-145">Create a in-memory object for Secret Group</span></span>

### [<span data-ttu-id="137a8-146">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-146">Remove-AzCloudService</span></span>](Remove-AzCloudService.md)
<span data-ttu-id="137a8-147">刪除雲端服務。</span><span class="sxs-lookup"><span data-stu-id="137a8-147">Deletes a cloud service.</span></span>

### [<span data-ttu-id="137a8-148">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="137a8-148">Remove-AzCloudServiceRoleInstance</span></span>](Remove-AzCloudServiceRoleInstance.md)
<span data-ttu-id="137a8-149">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-149">Deletes role instances in a cloud service.</span></span>

### [<span data-ttu-id="137a8-150">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-150">Restart-AzCloudService</span></span>](Restart-AzCloudService.md)
<span data-ttu-id="137a8-151">重新開機雲端服務中的一或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-151">Restarts one or more role instances in a cloud service.</span></span>

### [<span data-ttu-id="137a8-152">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="137a8-152">Restart-AzCloudServiceRoleInstance</span></span>](Restart-AzCloudServiceRoleInstance.md)
<span data-ttu-id="137a8-153">重新開機角色實例非同步作業會要求重新開機雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-153">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

### [<span data-ttu-id="137a8-154">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="137a8-154">Set-AzCloudServiceUpdateDomain</span></span>](Set-AzCloudServiceUpdateDomain.md)
<span data-ttu-id="137a8-155">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="137a8-155">Updates the role instances in the specified update domain.</span></span>

### [<span data-ttu-id="137a8-156">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-156">Start-AzCloudService</span></span>](Start-AzCloudService.md)
<span data-ttu-id="137a8-157">啟動雲端服務。</span><span class="sxs-lookup"><span data-stu-id="137a8-157">Starts the cloud service.</span></span>

### [<span data-ttu-id="137a8-158">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-158">Stop-AzCloudService</span></span>](Stop-AzCloudService.md)
<span data-ttu-id="137a8-159">關閉雲端服務。</span><span class="sxs-lookup"><span data-stu-id="137a8-159">Power off the cloud service.</span></span>
<span data-ttu-id="137a8-160">請注意，資源仍然會附加，而您正被收取資源的費用。</span><span class="sxs-lookup"><span data-stu-id="137a8-160">Note that resources are still attached and you are getting charged for the resources.</span></span>

### [<span data-ttu-id="137a8-161">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-161">Switch-AzCloudService</span></span>](Switch-AzCloudService.md)
<span data-ttu-id="137a8-162">在兩個雲端服務之間交換 IP (延伸支援) 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="137a8-162">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

### [<span data-ttu-id="137a8-163">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="137a8-163">Update-AzCloudService</span></span>](Update-AzCloudService.md)
<span data-ttu-id="137a8-164">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="137a8-164">Create or update a cloud service.</span></span>
<span data-ttu-id="137a8-165">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="137a8-165">Please note some properties can be set only during cloud service creation.</span></span>

