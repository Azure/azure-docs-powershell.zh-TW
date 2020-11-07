---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
ms.openlocfilehash: 0097cd022387b3ac2ee8ceb1fa2a831b60c4256d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799813"
---
# <span data-ttu-id="171bd-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="171bd-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="171bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="171bd-102">SYNOPSIS</span></span>
<span data-ttu-id="171bd-103">列出由 Azure 虛擬網路閘道宣告的路由</span><span class="sxs-lookup"><span data-stu-id="171bd-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="171bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="171bd-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="171bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="171bd-105">DESCRIPTION</span></span>
<span data-ttu-id="171bd-106">已知 BGP 對等的 IP，列舉由指定的 Azure 虛擬網路閘道宣告到該對等的路由。</span><span class="sxs-lookup"><span data-stu-id="171bd-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="171bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="171bd-107">EXAMPLES</span></span>

### <span data-ttu-id="171bd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="171bd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="171bd-109">針對資源群組 resourceGroupName 中名為 gatewayName 的 Azure 閘道，retrives 使用 IP 10.0.0.254 播發至 BGP 對等的路由清單</span><span class="sxs-lookup"><span data-stu-id="171bd-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="171bd-110">範例2</span><span class="sxs-lookup"><span data-stu-id="171bd-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="171bd-111">針對資源群組 resourceGroupName 中名為 gatewayName 的 Azure 閘道，在 BGP 對等的 BGP 對等用戶端清單中，會檢索播發到第一個 BGP 對等的路由。</span><span class="sxs-lookup"><span data-stu-id="171bd-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="171bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="171bd-112">PARAMETERS</span></span>

### <span data-ttu-id="171bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="171bd-113">-AsJob</span></span>
<span data-ttu-id="171bd-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="171bd-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171bd-115">-DefaultProfile</span></span>
<span data-ttu-id="171bd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="171bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-117">對等</span><span class="sxs-lookup"><span data-stu-id="171bd-117">-Peer</span></span>
<span data-ttu-id="171bd-118">BGP 對等的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="171bd-118">BGP peer's IP address.</span></span> <span data-ttu-id="171bd-119">這應該是在部署閘道之 Azure 虛擬網路中可存取的位址空間內的 IP。</span><span class="sxs-lookup"><span data-stu-id="171bd-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="171bd-121">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="171bd-121">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="171bd-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="171bd-123">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="171bd-123">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171bd-124">CommonParameters</span></span>
<span data-ttu-id="171bd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="171bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171bd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="171bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171bd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="171bd-127">INPUTS</span></span>

### <span data-ttu-id="171bd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="171bd-128">System.String</span></span>

## <span data-ttu-id="171bd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="171bd-129">OUTPUTS</span></span>

### <span data-ttu-id="171bd-130">PSGatewayRoute [] （[]）</span><span class="sxs-lookup"><span data-stu-id="171bd-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="171bd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="171bd-131">NOTES</span></span>
<span data-ttu-id="171bd-132">這個命令只適用于具備 BGP 啟用連線的 Azure 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="171bd-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="171bd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="171bd-133">RELATED LINKS</span></span>

