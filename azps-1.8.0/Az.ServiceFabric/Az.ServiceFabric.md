---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611355"
---
# <span data-ttu-id="c8e55-101">Az ServiceFabric 模組</span><span class="sxs-lookup"><span data-stu-id="c8e55-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="c8e55-102">說明</span><span class="sxs-lookup"><span data-stu-id="c8e55-102">Description</span></span>
<span data-ttu-id="c8e55-103">Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。</span><span class="sxs-lookup"><span data-stu-id="c8e55-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="c8e55-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8e55-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="c8e55-105">附加 AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8e55-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="c8e55-106">在組成群集 (s) ，將新憑證新增到虛擬電腦規模集。</span><span class="sxs-lookup"><span data-stu-id="c8e55-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="c8e55-107">憑證是用來做為應用程式憑證的。</span><span class="sxs-lookup"><span data-stu-id="c8e55-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="c8e55-108">附加 AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c8e55-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="c8e55-109">在群集中加入通用名稱或指紋，以進行用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="c8e55-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="c8e55-110">附加 AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c8e55-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="c8e55-111">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="c8e55-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="c8e55-112">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c8e55-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="c8e55-113">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="c8e55-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="c8e55-114">附加 AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c8e55-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="c8e55-115">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="c8e55-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="c8e55-116">AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c8e55-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="c8e55-117">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c8e55-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="c8e55-118">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c8e55-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="c8e55-119">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="c8e55-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c8e55-120">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c8e55-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c8e55-121">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="c8e55-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="c8e55-122">移除-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c8e55-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="c8e55-123">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="c8e55-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="c8e55-124">移除-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c8e55-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="c8e55-125">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="c8e55-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="c8e55-126">移除-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c8e55-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="c8e55-127">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="c8e55-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="c8e55-128">移除-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c8e55-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="c8e55-129">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="c8e55-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="c8e55-130">移除-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c8e55-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="c8e55-131">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="c8e55-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="c8e55-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c8e55-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="c8e55-133">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="c8e55-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="c8e55-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="c8e55-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="c8e55-135">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="c8e55-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="c8e55-136">更新-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c8e55-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="c8e55-137">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="c8e55-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="c8e55-138">更新-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="c8e55-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="c8e55-139">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="c8e55-139">Update the reliability tier of the primary node type in a cluster.</span></span>

