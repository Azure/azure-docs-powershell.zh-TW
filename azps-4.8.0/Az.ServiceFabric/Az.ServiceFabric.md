---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971730"
---
# <span data-ttu-id="fb180-101">Az ServiceFabric 模組</span><span class="sxs-lookup"><span data-stu-id="fb180-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="fb180-102">說明</span><span class="sxs-lookup"><span data-stu-id="fb180-102">Description</span></span>
<span data-ttu-id="fb180-103">Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。</span><span class="sxs-lookup"><span data-stu-id="fb180-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="fb180-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb180-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="fb180-105">附加 AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="fb180-106">在群集中加入通用名稱或指紋，以進行用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="fb180-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="fb180-107">附加 AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="fb180-108">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="fb180-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="fb180-109">附加 AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="fb180-110">在群集中新增證書公用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="fb180-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="fb180-111">這會在群集中針對用戶端驗證註冊證書 agains。</span><span class="sxs-lookup"><span data-stu-id="fb180-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="fb180-112">附加 AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb180-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="fb180-113">新增 vm 延伸至節點類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="fb180-114">附加 AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="fb180-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="fb180-115">將憑證機密新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="fb180-116">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fb180-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="fb180-117">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="fb180-118">附加 AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="fb180-119">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="fb180-120">AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb180-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="fb180-121">取得 Service Fabric 應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="fb180-122">AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb180-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb180-123">取得 Service Fabric 應用程式類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="fb180-124">AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb180-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb180-125">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="fb180-126">AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="fb180-127">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="fb180-128">AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="fb180-129">取得受管理的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="fb180-130">AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="fb180-131">取得 managed 節點類型的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="fb180-132">AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb180-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="fb180-133">在指定的應用程式和群集下取得服務結構服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb180-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="fb180-134">新-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb180-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="fb180-135">在指定的資源群組和群集底下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb180-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb180-136">新-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb180-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb180-137">在指定的資源群組和群集底下建立新的 service fabric 應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb180-138">新-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb180-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb180-139">在指定的資源群組和群集底下建立新的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="fb180-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb180-140">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="fb180-141">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="fb180-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="fb180-142">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="fb180-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="fb180-143">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="fb180-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="fb180-144">新-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="fb180-145">建立新的 managed 群集。</span><span class="sxs-lookup"><span data-stu-id="fb180-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="fb180-146">新-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="fb180-147">建立新的節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="fb180-147">Create new node type resource.</span></span>

### [<span data-ttu-id="fb180-148">新-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb180-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="fb180-149">在指定的應用程式和群集下建立新的 service fabric service。</span><span class="sxs-lookup"><span data-stu-id="fb180-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="fb180-150">移除-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb180-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="fb180-151">從群集中移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb180-151">Remove an application from the cluster.</span></span> <span data-ttu-id="fb180-152">這將會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="fb180-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="fb180-153">移除-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb180-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb180-154">從群集中移除服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="fb180-155">這會移除此資源下的所有類型版本。</span><span class="sxs-lookup"><span data-stu-id="fb180-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="fb180-156">移除-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb180-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb180-157">從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="fb180-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="fb180-158">移除-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="fb180-159">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="fb180-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="fb180-160">移除-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="fb180-161">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="fb180-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="fb180-162">移除-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="fb180-163">移除 [群集資源]。</span><span class="sxs-lookup"><span data-stu-id="fb180-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="fb180-164">移除-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb180-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="fb180-165">依指紋或公用名 Remvoe 用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="fb180-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="fb180-166">移除-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="fb180-167">移除節點類型或節點類型中的特定節點。</span><span class="sxs-lookup"><span data-stu-id="fb180-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="fb180-168">移除-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb180-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="fb180-169">從節點類型移除 vm 延伸。</span><span class="sxs-lookup"><span data-stu-id="fb180-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="fb180-170">移除-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fb180-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="fb180-171">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="fb180-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="fb180-172">移除-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="fb180-173">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="fb180-174">移除-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb180-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="fb180-175">從群集中移除服務。</span><span class="sxs-lookup"><span data-stu-id="fb180-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="fb180-176">移除-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fb180-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="fb180-177">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="fb180-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="fb180-178">重新開機-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="fb180-179">從節點類型重新開機特定節點。</span><span class="sxs-lookup"><span data-stu-id="fb180-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="fb180-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="fb180-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="fb180-181">設定群集資源屬性。</span><span class="sxs-lookup"><span data-stu-id="fb180-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="fb180-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fb180-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="fb180-183">針對節點類型的特定 ndes 設定 [節點類型] 資源屬性或執行重新鏡像動作（含重新鏡像參數）。</span><span class="sxs-lookup"><span data-stu-id="fb180-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="fb180-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fb180-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="fb180-185">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="fb180-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="fb180-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="fb180-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="fb180-187">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="fb180-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="fb180-188">更新-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb180-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="fb180-189">更新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb180-189">Update a service fabric application.</span></span> <span data-ttu-id="fb180-190">這可讓您更新應用程式參數和/或升級應用程式類型版本，這將會觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="fb180-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="fb180-191">更新-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="fb180-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="fb180-192">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="fb180-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="fb180-193">更新-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="fb180-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="fb180-194">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="fb180-194">Update the reliability tier of the primary node type in a cluster.</span></span>
