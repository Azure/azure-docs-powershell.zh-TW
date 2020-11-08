---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126972"
---
# <span data-ttu-id="75d51-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="75d51-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="75d51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75d51-102">SYNOPSIS</span></span>
<span data-ttu-id="75d51-103">列出 Azure 虛擬網路閘道的 BGP 對等</span><span class="sxs-lookup"><span data-stu-id="75d51-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="75d51-104">句法</span><span class="sxs-lookup"><span data-stu-id="75d51-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d51-105">說明</span><span class="sxs-lookup"><span data-stu-id="75d51-105">DESCRIPTION</span></span>
<span data-ttu-id="75d51-106">這個命令會列舉 Azure 虛擬閘道設定為對等的 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="75d51-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="75d51-107">也提供每個對等的狀態。</span><span class="sxs-lookup"><span data-stu-id="75d51-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="75d51-108">示例</span><span class="sxs-lookup"><span data-stu-id="75d51-108">EXAMPLES</span></span>

### <span data-ttu-id="75d51-109">範例1</span><span class="sxs-lookup"><span data-stu-id="75d51-109">Example 1</span></span>
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

<span data-ttu-id="75d51-110">針對資源群組 resourceGroup 中名為 gatewayName 的 Azure 虛擬網路閘道，檢索 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="75d51-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="75d51-111">這個範例輸出會顯示一個已連線的 BGP 對等，其中一個 IP 為10.0.0.254。</span><span class="sxs-lookup"><span data-stu-id="75d51-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="75d51-112">參數</span><span class="sxs-lookup"><span data-stu-id="75d51-112">PARAMETERS</span></span>

### <span data-ttu-id="75d51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75d51-113">-AsJob</span></span>
<span data-ttu-id="75d51-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75d51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75d51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d51-115">-DefaultProfile</span></span>
<span data-ttu-id="75d51-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75d51-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d51-117">對等</span><span class="sxs-lookup"><span data-stu-id="75d51-117">-Peer</span></span>
<span data-ttu-id="75d51-118">要取得其狀態的對等 IP</span><span class="sxs-lookup"><span data-stu-id="75d51-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="75d51-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d51-119">-ResourceGroupName</span></span>
<span data-ttu-id="75d51-120">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="75d51-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="75d51-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="75d51-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="75d51-122">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="75d51-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="75d51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d51-123">CommonParameters</span></span>
<span data-ttu-id="75d51-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75d51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d51-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75d51-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d51-126">輸入</span><span class="sxs-lookup"><span data-stu-id="75d51-126">INPUTS</span></span>

### <span data-ttu-id="75d51-127">System.object</span><span class="sxs-lookup"><span data-stu-id="75d51-127">System.String</span></span>

## <span data-ttu-id="75d51-128">輸出</span><span class="sxs-lookup"><span data-stu-id="75d51-128">OUTPUTS</span></span>

### <span data-ttu-id="75d51-129">PSBGPPeerStatus 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="75d51-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="75d51-130">筆記</span><span class="sxs-lookup"><span data-stu-id="75d51-130">NOTES</span></span>

## <span data-ttu-id="75d51-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="75d51-131">RELATED LINKS</span></span>
