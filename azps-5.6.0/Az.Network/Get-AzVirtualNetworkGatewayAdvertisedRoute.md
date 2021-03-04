---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904994"
---
# <span data-ttu-id="cd972-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="cd972-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="cd972-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd972-102">SYNOPSIS</span></span>
<span data-ttu-id="cd972-103">列出 Azure 虛擬網路閘道所宣告的路由</span><span class="sxs-lookup"><span data-stu-id="cd972-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="cd972-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd972-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd972-105">描述</span><span class="sxs-lookup"><span data-stu-id="cd972-105">DESCRIPTION</span></span>
<span data-ttu-id="cd972-106">如果具有 BGP 對等的 IP，請列舉由指定的 Azure 虛擬網路閘道向該對等電腦宣告的路由。</span><span class="sxs-lookup"><span data-stu-id="cd972-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="cd972-107">例子</span><span class="sxs-lookup"><span data-stu-id="cd972-107">EXAMPLES</span></span>

### <span data-ttu-id="cd972-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cd972-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="cd972-109">針對在資源群組 resourceGroupName 中名為 gatewayName 的 Azure 閘道，會以 IP 10.0.0.254，從 BGP 對等程式中，取回要宣告至 BGP 對等的路由清單。</span><span class="sxs-lookup"><span data-stu-id="cd972-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="cd972-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="cd972-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="cd972-111">針對資源群組 resourceGroupName 中名為 gatewayName 的 Azure 閘道，會從閘道的 BGP 對等程式清單中，將宣告至第一個 BGP 對等的路由進行取用。</span><span class="sxs-lookup"><span data-stu-id="cd972-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="cd972-112">參數</span><span class="sxs-lookup"><span data-stu-id="cd972-112">PARAMETERS</span></span>

### <span data-ttu-id="cd972-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd972-113">-AsJob</span></span>
<span data-ttu-id="cd972-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd972-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd972-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd972-115">-DefaultProfile</span></span>
<span data-ttu-id="cd972-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd972-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd972-117">-對等</span><span class="sxs-lookup"><span data-stu-id="cd972-117">-Peer</span></span>
<span data-ttu-id="cd972-118">BGP 對等的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cd972-118">BGP peer's IP address.</span></span> <span data-ttu-id="cd972-119">這應該是可從部署閘道之 Azure 虛擬網路內可于位址空間內進行訪問的 IP。</span><span class="sxs-lookup"><span data-stu-id="cd972-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd972-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd972-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd972-121">虛擬網路閘道資源組名</span><span class="sxs-lookup"><span data-stu-id="cd972-121">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd972-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cd972-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cd972-123">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="cd972-123">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd972-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd972-124">CommonParameters</span></span>
<span data-ttu-id="cd972-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd972-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd972-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd972-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd972-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cd972-127">INPUTS</span></span>

### <span data-ttu-id="cd972-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cd972-128">System.String</span></span>

## <span data-ttu-id="cd972-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cd972-129">OUTPUTS</span></span>

### <span data-ttu-id="cd972-130">Microsoft.Azure.Commands.Network.models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="cd972-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="cd972-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cd972-131">NOTES</span></span>
<span data-ttu-id="cd972-132">此命令僅適用于已啟用 BGP 連接的 Azure 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="cd972-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="cd972-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd972-133">RELATED LINKS</span></span>
