---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 42960533c33cc2d5f8f4ee809cdd7a25c483c75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449977"
---
# <span data-ttu-id="6c90a-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="6c90a-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="6c90a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c90a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c90a-103">列出 Azure 虛擬網路閘道的 BGP 對等</span><span class="sxs-lookup"><span data-stu-id="6c90a-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c90a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c90a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c90a-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c90a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c90a-106">這個命令會列舉 Azure 虛擬閘道設定為對等的 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="6c90a-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="6c90a-107">也提供每個對等的狀態。</span><span class="sxs-lookup"><span data-stu-id="6c90a-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="6c90a-108">示例</span><span class="sxs-lookup"><span data-stu-id="6c90a-108">EXAMPLES</span></span>

### <span data-ttu-id="6c90a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="6c90a-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="6c90a-110">針對資源群組 resourceGroup 中名為 gatewayName 的 Azure 虛擬網路閘道，檢索 BGP 對等。</span><span class="sxs-lookup"><span data-stu-id="6c90a-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="6c90a-111">這個範例輸出會顯示一個已連線的 BGP 對等，其中一個 IP 為10.0.0.254。</span><span class="sxs-lookup"><span data-stu-id="6c90a-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="6c90a-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c90a-112">PARAMETERS</span></span>

### <span data-ttu-id="6c90a-113">對等</span><span class="sxs-lookup"><span data-stu-id="6c90a-113">-Peer</span></span>
<span data-ttu-id="6c90a-114">要取得其狀態的對等 IP</span><span class="sxs-lookup"><span data-stu-id="6c90a-114">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="6c90a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c90a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c90a-116">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6c90a-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="6c90a-117">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6c90a-117">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6c90a-118">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="6c90a-118">Virtual network gateway name</span></span>

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

### <span data-ttu-id="6c90a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c90a-119">-DefaultProfile</span></span>
<span data-ttu-id="6c90a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c90a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c90a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c90a-121">CommonParameters</span></span>
<span data-ttu-id="6c90a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c90a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c90a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c90a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c90a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6c90a-124">INPUTS</span></span>

### <span data-ttu-id="6c90a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6c90a-125">System.String</span></span>

## <span data-ttu-id="6c90a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6c90a-126">OUTPUTS</span></span>

### <span data-ttu-id="6c90a-127">PSBGPPeerStatus [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6c90a-127">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="6c90a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6c90a-128">NOTES</span></span>

## <span data-ttu-id="6c90a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c90a-129">RELATED LINKS</span></span>

