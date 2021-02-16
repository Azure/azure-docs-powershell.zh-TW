---
Module Name: Az.CloudService
Module Guid: a41eb61d-c5a1-4e9b-81a7-b8905fff7f2c
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
ms.openlocfilehash: c9ab8aaefc7d97c7d1082b76b1dcef1546fe96d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127943"
---
# <span data-ttu-id="dd247-101">Az CloudService 模組</span><span class="sxs-lookup"><span data-stu-id="dd247-101">Az.CloudService Module</span></span>
## <span data-ttu-id="dd247-102">說明</span><span class="sxs-lookup"><span data-stu-id="dd247-102">Description</span></span>
<span data-ttu-id="dd247-103">Microsoft Azure PowerShell： CloudService Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd247-103">Microsoft Azure PowerShell: CloudService cmdlets</span></span>

## <span data-ttu-id="dd247-104">Az CloudService Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd247-104">Az.CloudService Cmdlets</span></span>
### [<span data-ttu-id="dd247-105">AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-105">Get-AzCloudService</span></span>](Get-AzCloudService.md)
<span data-ttu-id="dd247-106">顯示雲端服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd247-106">Display information about a cloud service.</span></span>

### [<span data-ttu-id="dd247-107">AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="dd247-107">Get-AzCloudServiceInstanceView</span></span>](Get-AzCloudServiceInstanceView.md)
<span data-ttu-id="dd247-108">取得雲端服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="dd247-108">Gets the status of a cloud service.</span></span>

### [<span data-ttu-id="dd247-109">AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="dd247-109">Get-AzCloudServiceNetworkInterfaces</span></span>](Get-AzCloudServiceNetworkInterfaces.md)
<span data-ttu-id="dd247-110">取得雲端服務的網路介面。</span><span class="sxs-lookup"><span data-stu-id="dd247-110">Get the network interfaces of a cloud service.</span></span>

### [<span data-ttu-id="dd247-111">AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="dd247-111">Get-AzCloudServicePublicIPAddress</span></span>](Get-AzCloudServicePublicIPAddress.md)
<span data-ttu-id="dd247-112">取得雲端服務的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dd247-112">Get the public IP address of a cloud service.</span></span>

### [<span data-ttu-id="dd247-113">AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dd247-113">Get-AzCloudServiceRoleInstance</span></span>](Get-AzCloudServiceRoleInstance.md)
<span data-ttu-id="dd247-114">從雲端服務取得角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-114">Gets a role instance from a cloud service.</span></span>

### [<span data-ttu-id="dd247-115">AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="dd247-115">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>](Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md)
<span data-ttu-id="dd247-116">取得雲端服務中角色實例的遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="dd247-116">Gets a remote desktop file for a role instance in a cloud service.</span></span>

### [<span data-ttu-id="dd247-117">AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="dd247-117">Get-AzCloudServiceRoleInstanceView</span></span>](Get-AzCloudServiceRoleInstanceView.md)
<span data-ttu-id="dd247-118">檢索雲端服務中角色實例之執行時間狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd247-118">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

### [<span data-ttu-id="dd247-119">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="dd247-119">Invoke-AzCloudServiceRebuild</span></span>](Invoke-AzCloudServiceRebuild.md)
<span data-ttu-id="dd247-120">重建角色實例會在網頁角色或 worker 角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="dd247-120">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="dd247-121">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-121">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

### [<span data-ttu-id="dd247-122">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="dd247-122">Invoke-AzCloudServiceReimage</span></span>](Invoke-AzCloudServiceReimage.md)
<span data-ttu-id="dd247-123">重新鏡像非同步作業會重新安裝網頁角色或 worker 角色實例的作業系統。</span><span class="sxs-lookup"><span data-stu-id="dd247-123">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="dd247-124">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="dd247-124">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>](Invoke-AzCloudServiceRoleInstanceRebuild.md)
<span data-ttu-id="dd247-125">[重建角色實例] 非同步作業會在網頁角色或輔助角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="dd247-125">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="dd247-126">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-126">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

### [<span data-ttu-id="dd247-127">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="dd247-127">Invoke-AzCloudServiceRoleInstanceReimage</span></span>](Invoke-AzCloudServiceRoleInstanceReimage.md)
<span data-ttu-id="dd247-128">重新鏡像角色實例非同步作業會重新安裝網頁角色或輔助角色實例的作業系統。</span><span class="sxs-lookup"><span data-stu-id="dd247-128">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="dd247-129">新-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-129">New-AzCloudService</span></span>](New-AzCloudService.md)
<span data-ttu-id="dd247-130">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="dd247-130">Create or update a cloud service.</span></span>
<span data-ttu-id="dd247-131">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="dd247-131">Please note some properties can be set only during cloud service creation.</span></span>

### [<span data-ttu-id="dd247-132">新-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd247-132">New-AzCloudServiceDiagnosticsExtension</span></span>](New-AzCloudServiceDiagnosticsExtension.md)
<span data-ttu-id="dd247-133">在記憶體中建立診斷延伸的物件</span><span class="sxs-lookup"><span data-stu-id="dd247-133">Create a in-memory object for Diagnostics Extension</span></span>

### [<span data-ttu-id="dd247-134">新-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="dd247-134">New-AzCloudServiceExtensionObject</span></span>](New-AzCloudServiceExtensionObject.md)
<span data-ttu-id="dd247-135">建立延伸的記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="dd247-135">Create a in-memory object for Extension</span></span>

### [<span data-ttu-id="dd247-136">新-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dd247-136">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerConfigurationObject.md)
<span data-ttu-id="dd247-137">為 LoadBalancerConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="dd247-137">Create a in-memory object for LoadBalancerConfiguration</span></span>

### [<span data-ttu-id="dd247-138">新-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dd247-138">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md)
<span data-ttu-id="dd247-139">為 LoadBalancerFrontendIPConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="dd247-139">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

### [<span data-ttu-id="dd247-140">新-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="dd247-140">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>](New-AzCloudServiceRemoteDesktopExtensionObject.md)
<span data-ttu-id="dd247-141">為遠端桌面延伸建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="dd247-141">Create a in-memory object for Remote Desktop Extension</span></span>

### [<span data-ttu-id="dd247-142">新-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="dd247-142">New-AzCloudServiceRoleProfilePropertiesObject</span></span>](New-AzCloudServiceRoleProfilePropertiesObject.md)
<span data-ttu-id="dd247-143">為 CloudServiceRoleProfileProperties 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="dd247-143">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

### [<span data-ttu-id="dd247-144">新-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="dd247-144">New-AzCloudServiceVaultSecretGroupObject</span></span>](New-AzCloudServiceVaultSecretGroupObject.md)
<span data-ttu-id="dd247-145">針對秘密群組建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="dd247-145">Create a in-memory object for Secret Group</span></span>

### [<span data-ttu-id="dd247-146">移除-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-146">Remove-AzCloudService</span></span>](Remove-AzCloudService.md)
<span data-ttu-id="dd247-147">刪除雲端服務。</span><span class="sxs-lookup"><span data-stu-id="dd247-147">Deletes a cloud service.</span></span>

### [<span data-ttu-id="dd247-148">移除-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dd247-148">Remove-AzCloudServiceRoleInstance</span></span>](Remove-AzCloudServiceRoleInstance.md)
<span data-ttu-id="dd247-149">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-149">Deletes role instances in a cloud service.</span></span>

### [<span data-ttu-id="dd247-150">重新開機-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-150">Restart-AzCloudService</span></span>](Restart-AzCloudService.md)
<span data-ttu-id="dd247-151">重新開機雲端服務中的一個或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-151">Restarts one or more role instances in a cloud service.</span></span>

### [<span data-ttu-id="dd247-152">重新開機-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dd247-152">Restart-AzCloudServiceRoleInstance</span></span>](Restart-AzCloudServiceRoleInstance.md)
<span data-ttu-id="dd247-153">重新開機角色實例非同步作業會要求在雲端服務中重新開機角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-153">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

### [<span data-ttu-id="dd247-154">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="dd247-154">Set-AzCloudServiceUpdateDomain</span></span>](Set-AzCloudServiceUpdateDomain.md)
<span data-ttu-id="dd247-155">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="dd247-155">Updates the role instances in the specified update domain.</span></span>

### [<span data-ttu-id="dd247-156">開始-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-156">Start-AzCloudService</span></span>](Start-AzCloudService.md)
<span data-ttu-id="dd247-157">啟動雲端服務。</span><span class="sxs-lookup"><span data-stu-id="dd247-157">Starts the cloud service.</span></span>

### [<span data-ttu-id="dd247-158">停止 AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-158">Stop-AzCloudService</span></span>](Stop-AzCloudService.md)
<span data-ttu-id="dd247-159">關閉雲端服務的電源。</span><span class="sxs-lookup"><span data-stu-id="dd247-159">Power off the cloud service.</span></span>
<span data-ttu-id="dd247-160">請注意，資源仍已附加，而且您需要支付資源。</span><span class="sxs-lookup"><span data-stu-id="dd247-160">Note that resources are still attached and you are getting charged for the resources.</span></span>

### [<span data-ttu-id="dd247-161">切換 AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-161">Switch-AzCloudService</span></span>](Switch-AzCloudService.md)
<span data-ttu-id="dd247-162">在兩個雲端服務 (延伸支援) 負載平衡器之間交換 Vip。</span><span class="sxs-lookup"><span data-stu-id="dd247-162">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

### [<span data-ttu-id="dd247-163">更新-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd247-163">Update-AzCloudService</span></span>](Update-AzCloudService.md)
<span data-ttu-id="dd247-164">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="dd247-164">Create or update a cloud service.</span></span>
<span data-ttu-id="dd247-165">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="dd247-165">Please note some properties can be set only during cloud service creation.</span></span>

