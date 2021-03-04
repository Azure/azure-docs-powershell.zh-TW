---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: 0d798c5eb70c8c472862e9af0f992d01827a750e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902441"
---
# <span data-ttu-id="24024-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="24024-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="24024-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24024-102">SYNOPSIS</span></span>
<span data-ttu-id="24024-103">在 Azure RouteServer 中獲得 RouteServer 對等</span><span class="sxs-lookup"><span data-stu-id="24024-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="24024-104">語法</span><span class="sxs-lookup"><span data-stu-id="24024-104">SYNTAX</span></span>

### <span data-ttu-id="24024-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24024-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24024-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24024-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24024-107">描述</span><span class="sxs-lookup"><span data-stu-id="24024-107">DESCRIPTION</span></span>
<span data-ttu-id="24024-108">**Get-AzRouteServerPeer Cmdlet** 在 Azure RouteServer 中取得對等</span><span class="sxs-lookup"><span data-stu-id="24024-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="24024-109">例子</span><span class="sxs-lookup"><span data-stu-id="24024-109">EXAMPLES</span></span>

### <span data-ttu-id="24024-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="24024-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="24024-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="24024-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="24024-112">參數</span><span class="sxs-lookup"><span data-stu-id="24024-112">PARAMETERS</span></span>

### <span data-ttu-id="24024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24024-113">-DefaultProfile</span></span>
<span data-ttu-id="24024-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24024-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24024-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="24024-115">-PeerName</span></span>
<span data-ttu-id="24024-116">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="24024-116">The name of the route server peer.</span></span>

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

### <span data-ttu-id="24024-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24024-117">-ResourceGroupName</span></span>
<span data-ttu-id="24024-118">路由伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="24024-118">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="24024-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24024-119">-ResourceId</span></span>
<span data-ttu-id="24024-120">路由伺服器對等的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="24024-120">ResourceId of the route server peer.</span></span>

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

### <span data-ttu-id="24024-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="24024-121">-RouteServerName</span></span>
<span data-ttu-id="24024-122">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="24024-122">The name of the route server.</span></span>

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

### <span data-ttu-id="24024-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24024-123">CommonParameters</span></span>
<span data-ttu-id="24024-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24024-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24024-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24024-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24024-126">輸入</span><span class="sxs-lookup"><span data-stu-id="24024-126">INPUTS</span></span>

### <span data-ttu-id="24024-127">System.String</span><span class="sxs-lookup"><span data-stu-id="24024-127">System.String</span></span>

## <span data-ttu-id="24024-128">輸出</span><span class="sxs-lookup"><span data-stu-id="24024-128">OUTPUTS</span></span>

### <span data-ttu-id="24024-129">Microsoft.Azure.Commands.Network.models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="24024-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="24024-130">筆記</span><span class="sxs-lookup"><span data-stu-id="24024-130">NOTES</span></span>

## <span data-ttu-id="24024-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="24024-131">RELATED LINKS</span></span>
