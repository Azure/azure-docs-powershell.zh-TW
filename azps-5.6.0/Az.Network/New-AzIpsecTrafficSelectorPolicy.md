---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: 6980ccc3e3ad9c69755253183da1d83f522973da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916716"
---
# <span data-ttu-id="b657c-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b657c-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b657c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b657c-102">SYNOPSIS</span></span>
<span data-ttu-id="b657c-103">建立流量選取器策略。</span><span class="sxs-lookup"><span data-stu-id="b657c-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="b657c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b657c-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b657c-105">描述</span><span class="sxs-lookup"><span data-stu-id="b657c-105">DESCRIPTION</span></span>
<span data-ttu-id="b657c-106">此New-AzTrafficSelectorPolicy Cmdlet 會建立流量選取器策略提案，以用於虛擬網路閘道連接。</span><span class="sxs-lookup"><span data-stu-id="b657c-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="b657c-107">例子</span><span class="sxs-lookup"><span data-stu-id="b657c-107">EXAMPLES</span></span>

### <span data-ttu-id="b657c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b657c-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="b657c-109">使用 IKEv2 通訊協定建立虛擬網路閘道連接時，建立流量選取器策略的實例，並將它新增為參數。</span><span class="sxs-lookup"><span data-stu-id="b657c-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="b657c-110">參數</span><span class="sxs-lookup"><span data-stu-id="b657c-110">PARAMETERS</span></span>

### <span data-ttu-id="b657c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b657c-111">-DefaultProfile</span></span>
<span data-ttu-id="b657c-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b657c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b657c-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="b657c-113">-LocalAddressRange</span></span>
<span data-ttu-id="b657c-114">CIDR 位址範圍的集合</span><span class="sxs-lookup"><span data-stu-id="b657c-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b657c-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="b657c-115">-RemoteAddressRange</span></span>
<span data-ttu-id="b657c-116">CIDR 位址範圍的集合</span><span class="sxs-lookup"><span data-stu-id="b657c-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b657c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b657c-117">CommonParameters</span></span>
<span data-ttu-id="b657c-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b657c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b657c-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b657c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b657c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b657c-120">INPUTS</span></span>

### <span data-ttu-id="b657c-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b657c-121">System.String[]</span></span>

## <span data-ttu-id="b657c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b657c-122">OUTPUTS</span></span>

### <span data-ttu-id="b657c-123">Microsoft.Azure.Commands.Network.models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b657c-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b657c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b657c-124">NOTES</span></span>

## <span data-ttu-id="b657c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b657c-125">RELATED LINKS</span></span>
