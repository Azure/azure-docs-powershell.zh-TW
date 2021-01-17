---
Module Name: Az.Peering
Module Guid: 6c848b97-4dd4-49ef-b385-43c64905d25a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.peering.md
Help Version: 0.1.0
Locale: e-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
ms.openlocfilehash: 568c235bee84238d53849e8fb9dc3258e907cb18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436279"
---
# <span data-ttu-id="c4356-101">Az。對等模組</span><span class="sxs-lookup"><span data-stu-id="c4356-101">Az.Peering Module</span></span>
## <span data-ttu-id="c4356-102">說明</span><span class="sxs-lookup"><span data-stu-id="c4356-102">Description</span></span>
<span data-ttu-id="c4356-103">Microsoft 對等服務可讓客戶與 Microsoft 連線至 Azure，並將其網路資源表示為 ARM 物件。</span><span class="sxs-lookup"><span data-stu-id="c4356-103">Microsoft Peering Service allows customers and Microsoft to connect to Azure and represent their network resources as ARM objects.</span></span>

## <span data-ttu-id="c4356-104">Az。對等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4356-104">Az.Peering Cmdlets</span></span>
### [<span data-ttu-id="c4356-105">AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="c4356-105">Get-AzLegacyPeering</span></span>](Get-AzLegacyPeering.md)
<span data-ttu-id="c4356-106">用來將舊版對等資源轉換為 Azure 資源管理 (ARM) 資源。</span><span class="sxs-lookup"><span data-stu-id="c4356-106">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

### [<span data-ttu-id="c4356-107">AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-107">Get-AzPeerAsn</span></span>](Get-AzPeerAsn.md)
<span data-ttu-id="c4356-108">從 ARM 取得 PeerAsn 物件。</span><span class="sxs-lookup"><span data-stu-id="c4356-108">Gets PeerAsn object from ARM.</span></span>

### [<span data-ttu-id="c4356-109">AzPeering</span><span class="sxs-lookup"><span data-stu-id="c4356-109">Get-AzPeering</span></span>](Get-AzPeering.md)
<span data-ttu-id="c4356-110">取得訂閱的對等資源</span><span class="sxs-lookup"><span data-stu-id="c4356-110">Gets the Peering Resources for a subscription</span></span>

### [<span data-ttu-id="c4356-111">AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c4356-111">Get-AzPeeringLocation</span></span>](Get-AzPeeringLocation.md)
<span data-ttu-id="c4356-112">取得 Microsoft 提供的對等位置</span><span class="sxs-lookup"><span data-stu-id="c4356-112">Gets the Peering locations offered by Microsoft</span></span>

### [<span data-ttu-id="c4356-113">AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="c4356-113">Get-AzPeeringReceivedRoute</span></span>](Get-AzPeeringReceivedRoute.md)
<span data-ttu-id="c4356-114">列出對等的已接收路線。</span><span class="sxs-lookup"><span data-stu-id="c4356-114">Lists the received routes for a Peering.</span></span>

### [<span data-ttu-id="c4356-115">AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-115">Get-AzPeeringRegisteredAsn</span></span>](Get-AzPeeringRegisteredAsn.md)
<span data-ttu-id="c4356-116">取得網際網路交換路由伺服器類型 peerings 的註冊 ASN。</span><span class="sxs-lookup"><span data-stu-id="c4356-116">Gets the registered ASN for internet exchange route server type peerings.</span></span>

### [<span data-ttu-id="c4356-117">AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-117">Get-AzPeeringRegisteredPrefix</span></span>](Get-AzPeeringRegisteredPrefix.md)
<span data-ttu-id="c4356-118">取得或列出 peerings 的已註冊前置詞。</span><span class="sxs-lookup"><span data-stu-id="c4356-118">Gets or lists the registered prefix for peerings.</span></span>

### [<span data-ttu-id="c4356-119">AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c4356-119">Get-AzPeeringService</span></span>](Get-AzPeeringService.md)
<span data-ttu-id="c4356-120">取得單一物件之對等服務物件的清單。</span><span class="sxs-lookup"><span data-stu-id="c4356-120">Get a list of peering service objects of a single object.</span></span>

### [<span data-ttu-id="c4356-121">AzPeeringServiceCountry</span><span class="sxs-lookup"><span data-stu-id="c4356-121">Get-AzPeeringServiceCountry</span></span>](Get-AzPeeringServiceCountry.md)
<span data-ttu-id="c4356-122">列出對等服務可用的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="c4356-122">Lists the countries available for peering service.</span></span>

### [<span data-ttu-id="c4356-123">AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="c4356-123">Get-AzPeeringServiceLocation</span></span>](Get-AzPeeringServiceLocation.md)
<span data-ttu-id="c4356-124">取得 Microsoft 所提供的對等服務位置清單。</span><span class="sxs-lookup"><span data-stu-id="c4356-124">Gets a list of peering service locations offered by Microsoft.</span></span>

### [<span data-ttu-id="c4356-125">AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-125">Get-AzPeeringServicePrefix</span></span>](Get-AzPeeringServicePrefix.md)
<span data-ttu-id="c4356-126">取得訂閱的對等服務首碼清單。</span><span class="sxs-lookup"><span data-stu-id="c4356-126">Gets a list of peering service prefixes for a subscription.</span></span>

### [<span data-ttu-id="c4356-127">AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c4356-127">Get-AzPeeringServiceProvider</span></span>](Get-AzPeeringServiceProvider.md)
<span data-ttu-id="c4356-128">取得與 Microsoft 合作的對等服務提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="c4356-128">Gets a list of peering service providers partnered with Microsoft.</span></span>

### [<span data-ttu-id="c4356-129">新-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-129">New-AzPeerAsn</span></span>](New-AzPeerAsn.md)
<span data-ttu-id="c4356-130">建立新的對等 ASN</span><span class="sxs-lookup"><span data-stu-id="c4356-130">Creates a new Peer ASN</span></span> 

### [<span data-ttu-id="c4356-131">新-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="c4356-131">New-AzPeerAsnContactDetail</span></span>](New-AzPeerAsnContactDetail.md)
<span data-ttu-id="c4356-132">為 PeerAsn 建立記憶體連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c4356-132">Creates an in memory contact detail for PeerAsn.</span></span> 

### [<span data-ttu-id="c4356-133">新-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c4356-133">New-AzPeering</span></span>](New-AzPeering.md)
<span data-ttu-id="c4356-134">建立新的對等 ARM 資源</span><span class="sxs-lookup"><span data-stu-id="c4356-134">Creates a new Peering ARM Resource</span></span>

### [<span data-ttu-id="c4356-135">新-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c4356-135">New-AzPeeringDirectConnectionObject</span></span>](New-AzPeeringDirectConnectionObject.md)
<span data-ttu-id="c4356-136">在記憶體 PSObject 中建立，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="c4356-136">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

### [<span data-ttu-id="c4356-137">新-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c4356-137">New-AzPeeringExchangeConnectionObject</span></span>](New-AzPeeringExchangeConnectionObject.md)
<span data-ttu-id="c4356-138">在記憶體 PSObject 中建立，以用於建立或修改對等。</span><span class="sxs-lookup"><span data-stu-id="c4356-138">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

### [<span data-ttu-id="c4356-139">新-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-139">New-AzPeeringRegisteredAsn</span></span>](New-AzPeeringRegisteredAsn.md)
<span data-ttu-id="c4356-140">建立對等的註冊 ASN</span><span class="sxs-lookup"><span data-stu-id="c4356-140">Create registered ASN for peering</span></span>

### [<span data-ttu-id="c4356-141">新-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-141">New-AzPeeringRegisteredPrefix</span></span>](New-AzPeeringRegisteredPrefix.md)
<span data-ttu-id="c4356-142">針對對等物件建立已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="c4356-142">Create registered prefixes for peering objects.</span></span>

### [<span data-ttu-id="c4356-143">新-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c4356-143">New-AzPeeringService</span></span>](New-AzPeeringService.md)
<span data-ttu-id="c4356-144">建立新的對等服務。</span><span class="sxs-lookup"><span data-stu-id="c4356-144">Creates a new peering service.</span></span>

### [<span data-ttu-id="c4356-145">新-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-145">New-AzPeeringServicePrefix</span></span>](New-AzPeeringServicePrefix.md)
<span data-ttu-id="c4356-146">建立新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="c4356-146">Creates a new peering service prefix</span></span>

### [<span data-ttu-id="c4356-147">移除-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-147">Remove-AzPeerAsn</span></span>](Remove-AzPeerAsn.md)
<span data-ttu-id="c4356-148">移除對等 Asn</span><span class="sxs-lookup"><span data-stu-id="c4356-148">Remove Peer Asn</span></span>

### [<span data-ttu-id="c4356-149">移除-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c4356-149">Remove-AzPeering</span></span>](Remove-AzPeering.md)
<span data-ttu-id="c4356-150">刪除或移除對等。</span><span class="sxs-lookup"><span data-stu-id="c4356-150">Delete or remove a peering.</span></span> <span data-ttu-id="c4356-151">這將會刪除該資源的所有子資源或警示。</span><span class="sxs-lookup"><span data-stu-id="c4356-151">This will delete all child resources or alerting on the resource.</span></span>

### [<span data-ttu-id="c4356-152">移除-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-152">Remove-AzPeeringRegisteredAsn</span></span>](Remove-AzPeeringRegisteredAsn.md)
<span data-ttu-id="c4356-153">從父對等資源刪除或移除已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="c4356-153">Delete or remove a registered ASN from the parent peering resource.</span></span>

### [<span data-ttu-id="c4356-154">移除-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-154">Remove-AzPeeringRegisteredPrefix</span></span>](Remove-AzPeeringRegisteredPrefix.md)
<span data-ttu-id="c4356-155">從父對等資源刪除或移除已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="c4356-155">Delete or remove a registered prefix from the parent peering resource.</span></span>

### [<span data-ttu-id="c4356-156">移除-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-156">Remove-AzPeeringServicePrefix</span></span>](Remove-AzPeeringServicePrefix.md)
<span data-ttu-id="c4356-157">移除新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="c4356-157">Removes a new peering service prefix</span></span>

### [<span data-ttu-id="c4356-158">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-158">Set-AzPeerAsn</span></span>](Set-AzPeerAsn.md)
<span data-ttu-id="c4356-159">更新連絡人資訊</span><span class="sxs-lookup"><span data-stu-id="c4356-159">Update Contact Information</span></span>

### [<span data-ttu-id="c4356-160">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c4356-160">Set-AzPeeringDirectConnectionObject</span></span>](Set-AzPeeringDirectConnectionObject.md)
<span data-ttu-id="c4356-161">設定或更新直連連線資訊。</span><span class="sxs-lookup"><span data-stu-id="c4356-161">Sets or updates the Direct Connection information.</span></span> 

### [<span data-ttu-id="c4356-162">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c4356-162">Set-AzPeeringExchangeConnectionObject</span></span>](Set-AzPeeringExchangeConnectionObject.md)
<span data-ttu-id="c4356-163">設定或更新 Exchange 連線資訊。</span><span class="sxs-lookup"><span data-stu-id="c4356-163">Sets or updates the Exchange Connection information.</span></span> 

### [<span data-ttu-id="c4356-164">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c4356-164">Set-AzPeeringRegisteredAsn</span></span>](Set-AzPeeringRegisteredAsn.md)
<span data-ttu-id="c4356-165">從父對等資源設定或更新已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="c4356-165">Sets or updates a registered ASN from the parent peering resource.</span></span>

### [<span data-ttu-id="c4356-166">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c4356-166">Set-AzPeeringRegisteredPrefix</span></span>](Set-AzPeeringRegisteredPrefix.md)
<span data-ttu-id="c4356-167">從上層對等資源設定或更新已註冊的首碼。</span><span class="sxs-lookup"><span data-stu-id="c4356-167">Sets or updates a registered prefix from the parent peering resource.</span></span>

### [<span data-ttu-id="c4356-168">更新-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c4356-168">Update-AzPeering</span></span>](Update-AzPeering.md)
<span data-ttu-id="c4356-169">設定對等。</span><span class="sxs-lookup"><span data-stu-id="c4356-169">Sets the Peering.</span></span> <span data-ttu-id="c4356-170">將此命令與 or 搭配 `Set-AzDirectPeeringConnectionObject` 使用 `Set-AzExchangePeeringConnectionObject` 。</span><span class="sxs-lookup"><span data-stu-id="c4356-170">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

