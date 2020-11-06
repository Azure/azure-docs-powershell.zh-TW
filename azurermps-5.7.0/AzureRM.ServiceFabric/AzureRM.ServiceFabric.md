---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441708"
---
# <span data-ttu-id="1e030-101">AzureRM ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="1e030-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="1e030-102">說明</span><span class="sxs-lookup"><span data-stu-id="1e030-102">Description</span></span>
<span data-ttu-id="1e030-103">Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。</span><span class="sxs-lookup"><span data-stu-id="1e030-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="1e030-104">AzureRM ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e030-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="1e030-105">附加 AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="1e030-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="1e030-106">在組成群集 (s) ，將新憑證新增到虛擬電腦規模集。</span><span class="sxs-lookup"><span data-stu-id="1e030-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="1e030-107">憑證是用來做為應用程式憑證的。</span><span class="sxs-lookup"><span data-stu-id="1e030-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="1e030-108">附加 AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1e030-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="1e030-109">在群集中加入通用名稱或指紋，以進行用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="1e030-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="1e030-110">附加 AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1e030-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="1e030-111">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="1e030-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="1e030-112">附加 AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1e030-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="1e030-113">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="1e030-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="1e030-114">附加 AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1e030-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="1e030-115">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="1e030-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="1e030-116">AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1e030-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="1e030-117">取得 [群集] 資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1e030-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="1e030-118">新-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1e030-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="1e030-119">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="1e030-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1e030-120">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="1e030-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="1e030-121">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="1e030-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="1e030-122">移除-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1e030-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="1e030-123">移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。</span><span class="sxs-lookup"><span data-stu-id="1e030-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="1e030-124">移除-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1e030-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="1e030-125">移除群集憑證以用於群集安全。</span><span class="sxs-lookup"><span data-stu-id="1e030-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="1e030-126">移除-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1e030-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="1e030-127">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="1e030-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="1e030-128">移除-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1e030-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="1e030-129">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="1e030-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="1e030-130">移除-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1e030-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="1e030-131">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="1e030-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="1e030-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1e030-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="1e030-133">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="1e030-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="1e030-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="1e030-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="1e030-135">變更群集的 Service Fabric 升級類型。</span><span class="sxs-lookup"><span data-stu-id="1e030-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="1e030-136">更新-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="1e030-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="1e030-137">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="1e030-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="1e030-138">更新-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="1e030-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="1e030-139">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="1e030-139">Update the reliability tier of the primary node type in a cluster.</span></span>

