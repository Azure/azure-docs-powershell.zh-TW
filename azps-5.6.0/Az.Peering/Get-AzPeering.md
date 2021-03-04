---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: e2827d08d813608dbf3f6f40bc15603d5a5a0d99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911509"
---
# <span data-ttu-id="3e878-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="3e878-101">Get-AzPeering</span></span>

## <span data-ttu-id="3e878-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e878-102">SYNOPSIS</span></span>
<span data-ttu-id="3e878-103">獲得訂閱的對等資源</span><span class="sxs-lookup"><span data-stu-id="3e878-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="3e878-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e878-104">SYNTAX</span></span>

### <span data-ttu-id="3e878-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="3e878-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e878-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="3e878-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e878-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e878-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e878-108">描述</span><span class="sxs-lookup"><span data-stu-id="3e878-108">DESCRIPTION</span></span>
<span data-ttu-id="3e878-109">從訂閱、資源群組或名稱獲得對等。</span><span class="sxs-lookup"><span data-stu-id="3e878-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="3e878-110">例子</span><span class="sxs-lookup"><span data-stu-id="3e878-110">EXAMPLES</span></span>

### <span data-ttu-id="3e878-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3e878-111">Example 1</span></span>
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

<span data-ttu-id="3e878-112">獲得訂閱的所有資源。</span><span class="sxs-lookup"><span data-stu-id="3e878-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="3e878-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="3e878-113">Example 2</span></span>
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

<span data-ttu-id="3e878-114">為 Exchange 對等命名 `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="3e878-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="3e878-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="3e878-115">Example 2</span></span>
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

<span data-ttu-id="3e878-116">根據資源識別碼命名 Exchange `myExchangePeering1` 對等。</span><span class="sxs-lookup"><span data-stu-id="3e878-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="3e878-117">參數</span><span class="sxs-lookup"><span data-stu-id="3e878-117">PARAMETERS</span></span>

### <span data-ttu-id="3e878-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e878-118">-DefaultProfile</span></span>
<span data-ttu-id="3e878-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e878-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e878-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="3e878-120">-Kind</span></span>
<span data-ttu-id="3e878-121">顯示所有對等資源 ，並按類型顯示。</span><span class="sxs-lookup"><span data-stu-id="3e878-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="3e878-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e878-122">-Name</span></span>
<span data-ttu-id="3e878-123">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3e878-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3e878-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e878-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e878-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e878-125">The resource group name.</span></span>

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

### <span data-ttu-id="3e878-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e878-126">-ResourceId</span></span>
<span data-ttu-id="3e878-127">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="3e878-127">The resource id string name.</span></span>

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

### <span data-ttu-id="3e878-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e878-128">CommonParameters</span></span>
<span data-ttu-id="3e878-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e878-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e878-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e878-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e878-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e878-131">INPUTS</span></span>

### <span data-ttu-id="3e878-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3e878-132">System.String</span></span>

## <span data-ttu-id="3e878-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3e878-133">OUTPUTS</span></span>

### <span data-ttu-id="3e878-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3e878-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3e878-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3e878-135">NOTES</span></span>

## <span data-ttu-id="3e878-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e878-136">RELATED LINKS</span></span>
