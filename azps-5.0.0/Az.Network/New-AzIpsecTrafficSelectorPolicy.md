---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138716"
---
# <span data-ttu-id="3f67d-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3f67d-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="3f67d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f67d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f67d-103">建立流量選取器原則。</span><span class="sxs-lookup"><span data-stu-id="3f67d-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="3f67d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f67d-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f67d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f67d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f67d-106">New-AzTrafficSelectorPolicy Cmdlet 會建立要在虛擬網路閘道連線中使用的流量選取原則方案建議。</span><span class="sxs-lookup"><span data-stu-id="3f67d-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="3f67d-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f67d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f67d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3f67d-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="3f67d-109">建立流量選取器原則的實例，並在建立與 IKEv2 通訊協定的虛擬網路閘道連線時，將它新增為參數。</span><span class="sxs-lookup"><span data-stu-id="3f67d-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="3f67d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3f67d-110">PARAMETERS</span></span>

### <span data-ttu-id="3f67d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f67d-111">-DefaultProfile</span></span>
<span data-ttu-id="3f67d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f67d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f67d-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="3f67d-113">-LocalAddressRange</span></span>
<span data-ttu-id="3f67d-114">CIDR 位址範圍集合</span><span class="sxs-lookup"><span data-stu-id="3f67d-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="3f67d-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="3f67d-115">-RemoteAddressRange</span></span>
<span data-ttu-id="3f67d-116">CIDR 位址範圍集合</span><span class="sxs-lookup"><span data-stu-id="3f67d-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="3f67d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f67d-117">CommonParameters</span></span>
<span data-ttu-id="3f67d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f67d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f67d-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3f67d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f67d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3f67d-120">INPUTS</span></span>

### <span data-ttu-id="3f67d-121">System.object []</span><span class="sxs-lookup"><span data-stu-id="3f67d-121">System.String[]</span></span>

## <span data-ttu-id="3f67d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3f67d-122">OUTPUTS</span></span>

### <span data-ttu-id="3f67d-123">PSTrafficSelectorPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f67d-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="3f67d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3f67d-124">NOTES</span></span>

## <span data-ttu-id="3f67d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f67d-125">RELATED LINKS</span></span>