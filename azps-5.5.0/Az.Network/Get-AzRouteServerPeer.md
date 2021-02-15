---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131350"
---
# <span data-ttu-id="b1a13-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="b1a13-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="b1a13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1a13-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a13-103">取得 Azure RouteServer 中的 RouteServer 對等</span><span class="sxs-lookup"><span data-stu-id="b1a13-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="b1a13-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1a13-104">SYNTAX</span></span>

### <span data-ttu-id="b1a13-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1a13-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a13-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a13-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a13-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1a13-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a13-108">**AzRouteServerPeer** Cmdlet 會取得 Azure RouteServer 中的對等</span><span class="sxs-lookup"><span data-stu-id="b1a13-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="b1a13-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1a13-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a13-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b1a13-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="b1a13-111">範例2</span><span class="sxs-lookup"><span data-stu-id="b1a13-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="b1a13-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1a13-112">PARAMETERS</span></span>

### <span data-ttu-id="b1a13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a13-113">-DefaultProfile</span></span>
<span data-ttu-id="b1a13-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1a13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a13-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="b1a13-115">-PeerName</span></span>
<span data-ttu-id="b1a13-116">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a13-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a13-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1a13-118">路由伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a13-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a13-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a13-119">-ResourceId</span></span>
<span data-ttu-id="b1a13-120">路由伺服器對等的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b1a13-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a13-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="b1a13-121">-RouteServerName</span></span>
<span data-ttu-id="b1a13-122">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a13-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a13-123">CommonParameters</span></span>
<span data-ttu-id="b1a13-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1a13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a13-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1a13-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a13-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b1a13-126">INPUTS</span></span>

### <span data-ttu-id="b1a13-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b1a13-127">System.String</span></span>

## <span data-ttu-id="b1a13-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b1a13-128">OUTPUTS</span></span>

### <span data-ttu-id="b1a13-129">PSRouteServerPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1a13-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="b1a13-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b1a13-130">NOTES</span></span>

## <span data-ttu-id="b1a13-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1a13-131">RELATED LINKS</span></span>
