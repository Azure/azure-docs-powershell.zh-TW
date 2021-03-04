---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: fd0bb4c3035eb2def0a1d0fa64038299cee4ec48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904990"
---
# <span data-ttu-id="06c34-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="06c34-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="06c34-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06c34-102">SYNOPSIS</span></span>
<span data-ttu-id="06c34-103">列出 Azure 虛擬網路閘道的 BGP 對等</span><span class="sxs-lookup"><span data-stu-id="06c34-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="06c34-104">語法</span><span class="sxs-lookup"><span data-stu-id="06c34-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c34-105">描述</span><span class="sxs-lookup"><span data-stu-id="06c34-105">DESCRIPTION</span></span>
<span data-ttu-id="06c34-106">此命令會列舉 Azure 虛擬網路閘道已進行對等的 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="06c34-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="06c34-107">系統也會提供每個對等專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="06c34-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="06c34-108">例子</span><span class="sxs-lookup"><span data-stu-id="06c34-108">EXAMPLES</span></span>

### <span data-ttu-id="06c34-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="06c34-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="06c34-110">在資源群組資源群組中，為名為 gatewayName 的 Azure 虛擬網路閘道，檢索 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="06c34-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="06c34-111">此範例輸出會顯示一個連接的 BGP 對等，其 IP 為 10.0.0.254。</span><span class="sxs-lookup"><span data-stu-id="06c34-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="06c34-112">參數</span><span class="sxs-lookup"><span data-stu-id="06c34-112">PARAMETERS</span></span>

### <span data-ttu-id="06c34-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06c34-113">-AsJob</span></span>
<span data-ttu-id="06c34-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06c34-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06c34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c34-115">-DefaultProfile</span></span>
<span data-ttu-id="06c34-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06c34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c34-117">-對等</span><span class="sxs-lookup"><span data-stu-id="06c34-117">-Peer</span></span>
<span data-ttu-id="06c34-118">對等的 IP 以針對</span><span class="sxs-lookup"><span data-stu-id="06c34-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c34-119">-ResourceGroupName</span></span>
<span data-ttu-id="06c34-120">虛擬網路閘道資源組名</span><span class="sxs-lookup"><span data-stu-id="06c34-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="06c34-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="06c34-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="06c34-122">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="06c34-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="06c34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c34-123">CommonParameters</span></span>
<span data-ttu-id="06c34-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06c34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c34-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06c34-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c34-126">輸入</span><span class="sxs-lookup"><span data-stu-id="06c34-126">INPUTS</span></span>

### <span data-ttu-id="06c34-127">System.String</span><span class="sxs-lookup"><span data-stu-id="06c34-127">System.String</span></span>

## <span data-ttu-id="06c34-128">輸出</span><span class="sxs-lookup"><span data-stu-id="06c34-128">OUTPUTS</span></span>

### <span data-ttu-id="06c34-129">Microsoft.Azure.Commands.Network.models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="06c34-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="06c34-130">筆記</span><span class="sxs-lookup"><span data-stu-id="06c34-130">NOTES</span></span>

## <span data-ttu-id="06c34-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="06c34-131">RELATED LINKS</span></span>
