---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 5d963384d08dfed2e7e8516b892d2a3680c9332c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965738"
---
# <span data-ttu-id="2fd55-101">Az ServiceFabric 模組</span><span class="sxs-lookup"><span data-stu-id="2fd55-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="2fd55-102">說明</span><span class="sxs-lookup"><span data-stu-id="2fd55-102">Description</span></span>
<span data-ttu-id="2fd55-103">Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。</span><span class="sxs-lookup"><span data-stu-id="2fd55-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="2fd55-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2fd55-104">Az.ServiceFabric Cmdlets</span></span>

### [<span data-ttu-id="2fd55-105">附加 AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2fd55-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2fd55-106">在群集中加入通用名稱或指紋，以進行用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="2fd55-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2fd55-107">附加 AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2fd55-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2fd55-108">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="2fd55-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="2fd55-109">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2fd55-109">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="2fd55-110">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-110">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="2fd55-111">附加 AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2fd55-111">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="2fd55-112">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-112">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="2fd55-113">AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fd55-113">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="2fd55-114">取得 Service Fabric 應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2fd55-114">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="2fd55-115">AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fd55-115">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="2fd55-116">取得 Service Fabric 應用程式類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2fd55-116">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="2fd55-117">AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fd55-117">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2fd55-118">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2fd55-118">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="2fd55-119">AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2fd55-119">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="2fd55-120">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2fd55-120">Get the cluster resource details.</span></span>

### [<span data-ttu-id="2fd55-121">AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2fd55-121">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="2fd55-122">在指定的應用程式和群集下取得服務結構服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2fd55-122">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="2fd55-123">新-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fd55-123">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="2fd55-124">在指定的資源群組和群集底下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="2fd55-124">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2fd55-125">新-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fd55-125">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="2fd55-126">在指定的資源群組和群集底下建立新的 service fabric 應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-126">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2fd55-127">新-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fd55-127">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2fd55-128">在指定的資源群組和群集底下建立新的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="2fd55-128">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2fd55-129">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2fd55-129">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="2fd55-130">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="2fd55-130">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="2fd55-131">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="2fd55-131">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="2fd55-132">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="2fd55-132">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="2fd55-133">新-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2fd55-133">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="2fd55-134">在指定的應用程式和群集下建立新的 service fabric service。</span><span class="sxs-lookup"><span data-stu-id="2fd55-134">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="2fd55-135">移除-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fd55-135">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="2fd55-136">從群集中移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="2fd55-136">Remove an application from the cluster.</span></span> <span data-ttu-id="2fd55-137">這將會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="2fd55-137">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="2fd55-138">移除-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fd55-138">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="2fd55-139">從群集中移除服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-139">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="2fd55-140">這會移除此資源下的所有類型版本。</span><span class="sxs-lookup"><span data-stu-id="2fd55-140">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="2fd55-141">移除-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fd55-141">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2fd55-142">從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="2fd55-142">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="2fd55-143">移除-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2fd55-143">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2fd55-144">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="2fd55-144">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="2fd55-145">移除-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2fd55-145">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2fd55-146">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="2fd55-146">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="2fd55-147">移除-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2fd55-147">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="2fd55-148">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="2fd55-148">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="2fd55-149">移除-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2fd55-149">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="2fd55-150">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-150">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="2fd55-151">移除-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2fd55-151">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="2fd55-152">從群集中移除服務。</span><span class="sxs-lookup"><span data-stu-id="2fd55-152">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="2fd55-153">移除-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2fd55-153">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="2fd55-154">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="2fd55-154">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="2fd55-155">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2fd55-155">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="2fd55-156">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="2fd55-156">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="2fd55-157">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2fd55-157">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="2fd55-158">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="2fd55-158">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="2fd55-159">更新-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fd55-159">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="2fd55-160">更新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="2fd55-160">Update a service fabric application.</span></span> <span data-ttu-id="2fd55-161">這可讓您更新應用程式參數和/或升級應用程式類型版本，這將會觸發應用程式升級。</span><span class="sxs-lookup"><span data-stu-id="2fd55-161">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="2fd55-162">更新-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2fd55-162">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="2fd55-163">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="2fd55-163">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="2fd55-164">更新-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2fd55-164">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="2fd55-165">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="2fd55-165">Update the reliability tier of the primary node type in a cluster.</span></span>

