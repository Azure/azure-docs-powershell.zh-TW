---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904829"
---
# <span data-ttu-id="6df68-101">Az.ServiceFabric 模組</span><span class="sxs-lookup"><span data-stu-id="6df68-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="6df68-102">描述</span><span class="sxs-lookup"><span data-stu-id="6df68-102">Description</span></span>
<span data-ttu-id="6df68-103">您可以使用 Azure Service Fabric 模組來自動化兩端作業，例如建立安全性群組狀組、捲動組狀憑證、新增或移除該組集中的節點等等。以下列出所有作業的完整清單。</span><span class="sxs-lookup"><span data-stu-id="6df68-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="6df68-104">Az.ServiceFabric Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6df68-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="6df68-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="6df68-106">將常用名稱或指紋新增到該組組，以用於用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="6df68-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="6df68-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="6df68-108">新增次要組群憑證至該組。</span><span class="sxs-lookup"><span data-stu-id="6df68-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="6df68-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="6df68-110">在組塊中新增憑證通用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="6df68-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="6df68-111">這將會再次註冊憑證，以用於用戶端驗證目的。</span><span class="sxs-lookup"><span data-stu-id="6df68-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="6df68-112">Add-AzServiceFabricManagedNodeTypeEVExtension</span><span class="sxs-lookup"><span data-stu-id="6df68-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="6df68-113">新增 vm 擴充功能至節點類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="6df68-114">Add-AzServiceFabricManagedNodeTypeMSSECret</span><span class="sxs-lookup"><span data-stu-id="6df68-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="6df68-115">新增憑證金鑰至節點類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="6df68-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6df68-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="6df68-117">將節點新增到該群中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="6df68-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="6df68-119">新增節點類型至現有組。</span><span class="sxs-lookup"><span data-stu-id="6df68-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="6df68-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6df68-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="6df68-121">取得 Service Fabric 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="6df68-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6df68-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="6df68-123">取得 Service Fabric 應用程式類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="6df68-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6df68-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="6df68-125">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="6df68-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="6df68-127">取得組群資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="6df68-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="6df68-129">取得受管理的組群資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="6df68-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="6df68-131">取得受管理的節點類型資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="6df68-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6df68-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="6df68-133">取得指定應用程式和組群下的 Service Fabric 服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6df68-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="6df68-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6df68-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="6df68-135">在指定的資源群組和群組下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="6df68-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="6df68-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6df68-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="6df68-137">在指定的資源群組和群組下，建立新的服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="6df68-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6df68-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="6df68-139">在指定的資源群組和群組下建立新應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="6df68-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="6df68-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="6df68-141">此命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構組組。</span><span class="sxs-lookup"><span data-stu-id="6df68-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="6df68-142">它可以使用預設範本或您提供的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="6df68-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="6df68-143">您可以選擇指定資料夾，將自我簽署憑證匯出至該憑證，或稍後從金鑰庫抓取。</span><span class="sxs-lookup"><span data-stu-id="6df68-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="6df68-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="6df68-145">建立新受管理的集區。</span><span class="sxs-lookup"><span data-stu-id="6df68-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="6df68-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="6df68-147">建立新節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="6df68-147">Create new node type resource.</span></span>

### [<span data-ttu-id="6df68-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6df68-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="6df68-149">在指定的應用程式和組集中建立新的服務結構服務。</span><span class="sxs-lookup"><span data-stu-id="6df68-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="6df68-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6df68-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="6df68-151">從組群移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="6df68-151">Remove an application from the cluster.</span></span> <span data-ttu-id="6df68-152">這會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="6df68-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="6df68-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6df68-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="6df68-154">從組群移除服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="6df68-155">這會移除此資源下的所有類型版本。</span><span class="sxs-lookup"><span data-stu-id="6df68-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="6df68-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6df68-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="6df68-157">從組集中移除服務結構的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="6df68-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="6df68-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="6df68-159">移除用戶端憑證 () 或憑證 () 名稱 () ，以用於用戶端驗證至該組。</span><span class="sxs-lookup"><span data-stu-id="6df68-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="6df68-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="6df68-161">移除用於保護集區安全性的集區憑證。</span><span class="sxs-lookup"><span data-stu-id="6df68-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="6df68-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="6df68-163">移除組群資源。</span><span class="sxs-lookup"><span data-stu-id="6df68-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="6df68-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6df68-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="6df68-165">以指紋或通用名稱重新叫用用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="6df68-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="6df68-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="6df68-167">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="6df68-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="6df68-168">Remove-AzServiceFabricManagedNodeTypeMSEVExtension</span><span class="sxs-lookup"><span data-stu-id="6df68-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="6df68-169">從節點類型移除 vm 副檔名。</span><span class="sxs-lookup"><span data-stu-id="6df68-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="6df68-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6df68-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="6df68-171">從一個組移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="6df68-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="6df68-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="6df68-173">從一個組移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="6df68-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6df68-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="6df68-175">從組群移除服務。</span><span class="sxs-lookup"><span data-stu-id="6df68-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="6df68-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6df68-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="6df68-177">從組群移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="6df68-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="6df68-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="6df68-179">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="6df68-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="6df68-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6df68-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="6df68-181">設定組群資源屬性。</span><span class="sxs-lookup"><span data-stu-id="6df68-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="6df68-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6df68-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="6df68-183">使用 -Reimage 參數設定節點類型資源屬性，或在節點類型的特定數個數上執行重新映射動作。</span><span class="sxs-lookup"><span data-stu-id="6df68-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="6df68-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6df68-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="6df68-185">新增或更新一或多個服務佈設定至該組。</span><span class="sxs-lookup"><span data-stu-id="6df68-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="6df68-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6df68-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="6df68-187">變更組群的服務結構升級類型。</span><span class="sxs-lookup"><span data-stu-id="6df68-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="6df68-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6df68-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="6df68-189">更新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="6df68-189">Update a service fabric application.</span></span> <span data-ttu-id="6df68-190">這可讓您更新應用程式參數和/或升級應用程式類型版本，以觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="6df68-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="6df68-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6df68-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="6df68-192">更新該組集中節點類型的節點層級或 VmSKU。</span><span class="sxs-lookup"><span data-stu-id="6df68-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="6df68-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6df68-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="6df68-194">更新組集中主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="6df68-194">Update the reliability tier of the primary node type in a cluster.</span></span>

