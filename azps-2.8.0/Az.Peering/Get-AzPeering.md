---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: bcf26466c87a98d6a44486c5314c3541a7192a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791743"
---
# <span data-ttu-id="77496-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="77496-101">Get-AzPeering</span></span>

## <span data-ttu-id="77496-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77496-102">SYNOPSIS</span></span>
<span data-ttu-id="77496-103">取得訂閱的對等資源</span><span class="sxs-lookup"><span data-stu-id="77496-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="77496-104">句法</span><span class="sxs-lookup"><span data-stu-id="77496-104">SYNTAX</span></span>

### <span data-ttu-id="77496-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="77496-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77496-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="77496-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77496-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="77496-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77496-108">說明</span><span class="sxs-lookup"><span data-stu-id="77496-108">DESCRIPTION</span></span>
<span data-ttu-id="77496-109">從訂閱、資源群組或名稱取得 Peerings。</span><span class="sxs-lookup"><span data-stu-id="77496-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="77496-110">示例</span><span class="sxs-lookup"><span data-stu-id="77496-110">EXAMPLES</span></span>

### <span data-ttu-id="77496-111">範例1</span><span class="sxs-lookup"><span data-stu-id="77496-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="77496-112">取得訂閱的所有資源。</span><span class="sxs-lookup"><span data-stu-id="77496-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="77496-113">範例2</span><span class="sxs-lookup"><span data-stu-id="77496-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="77496-114">取得名為 #a0 的 Exchange 對等 `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="77496-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="77496-115">範例2</span><span class="sxs-lookup"><span data-stu-id="77496-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="77496-116">根據資源識別碼取得命名的 Exchange 對等 `myExchangePeering1` 。</span><span class="sxs-lookup"><span data-stu-id="77496-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="77496-117">參數</span><span class="sxs-lookup"><span data-stu-id="77496-117">PARAMETERS</span></span>

### <span data-ttu-id="77496-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77496-118">-DefaultProfile</span></span>
<span data-ttu-id="77496-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77496-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77496-120">類型</span><span class="sxs-lookup"><span data-stu-id="77496-120">-Kind</span></span>
<span data-ttu-id="77496-121">依類型顯示所有對等資源。</span><span class="sxs-lookup"><span data-stu-id="77496-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77496-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="77496-122">-Name</span></span>
<span data-ttu-id="77496-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="77496-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77496-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77496-124">-ResourceGroupName</span></span>
<span data-ttu-id="77496-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77496-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77496-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77496-126">-ResourceId</span></span>
<span data-ttu-id="77496-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="77496-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77496-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77496-128">CommonParameters</span></span>
<span data-ttu-id="77496-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77496-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77496-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="77496-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77496-131">輸入</span><span class="sxs-lookup"><span data-stu-id="77496-131">INPUTS</span></span>

### <span data-ttu-id="77496-132">System.object</span><span class="sxs-lookup"><span data-stu-id="77496-132">System.String</span></span>

## <span data-ttu-id="77496-133">輸出</span><span class="sxs-lookup"><span data-stu-id="77496-133">OUTPUTS</span></span>

### <span data-ttu-id="77496-134">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="77496-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="77496-135">筆記</span><span class="sxs-lookup"><span data-stu-id="77496-135">NOTES</span></span>

## <span data-ttu-id="77496-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="77496-136">RELATED LINKS</span></span>
