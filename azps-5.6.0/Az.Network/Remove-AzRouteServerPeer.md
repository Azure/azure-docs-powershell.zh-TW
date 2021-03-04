---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: 52733af41b5f8d84811f1c1f184181a2d45053e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909501"
---
# <span data-ttu-id="66a20-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="66a20-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="66a20-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66a20-102">SYNOPSIS</span></span>
<span data-ttu-id="66a20-103">從 Azure RouteServer 移除對等專案</span><span class="sxs-lookup"><span data-stu-id="66a20-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="66a20-104">語法</span><span class="sxs-lookup"><span data-stu-id="66a20-104">SYNTAX</span></span>

### <span data-ttu-id="66a20-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66a20-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a20-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a20-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a20-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a20-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a20-108">描述</span><span class="sxs-lookup"><span data-stu-id="66a20-108">DESCRIPTION</span></span>
<span data-ttu-id="66a20-109">**Remove-AzRouteServerPeer Cmdlet** 會從 Azure RouteServer 移除 RouteServer 對等程式</span><span class="sxs-lookup"><span data-stu-id="66a20-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="66a20-110">例子</span><span class="sxs-lookup"><span data-stu-id="66a20-110">EXAMPLES</span></span>

### <span data-ttu-id="66a20-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="66a20-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="66a20-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="66a20-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="66a20-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="66a20-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="66a20-114">參數</span><span class="sxs-lookup"><span data-stu-id="66a20-114">PARAMETERS</span></span>

### <span data-ttu-id="66a20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66a20-115">-AsJob</span></span>
<span data-ttu-id="66a20-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66a20-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66a20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a20-117">-DefaultProfile</span></span>
<span data-ttu-id="66a20-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66a20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a20-119">-強制</span><span class="sxs-lookup"><span data-stu-id="66a20-119">-Force</span></span>
<span data-ttu-id="66a20-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="66a20-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="66a20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66a20-121">-InputObject</span></span>
<span data-ttu-id="66a20-122">路由伺服器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="66a20-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66a20-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="66a20-123">-PeerName</span></span>
<span data-ttu-id="66a20-124">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="66a20-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="66a20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a20-125">-ResourceGroupName</span></span>
<span data-ttu-id="66a20-126">路由伺服器/對等體的資源組名。</span><span class="sxs-lookup"><span data-stu-id="66a20-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="66a20-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a20-127">-ResourceId</span></span>
<span data-ttu-id="66a20-128">路由伺服器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="66a20-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="66a20-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="66a20-129">-RouteServerName</span></span>
<span data-ttu-id="66a20-130">對等存在之路由伺服器。</span><span class="sxs-lookup"><span data-stu-id="66a20-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="66a20-131">-確認</span><span class="sxs-lookup"><span data-stu-id="66a20-131">-Confirm</span></span>
<span data-ttu-id="66a20-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66a20-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a20-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a20-133">-WhatIf</span></span>
<span data-ttu-id="66a20-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66a20-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a20-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66a20-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a20-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a20-136">CommonParameters</span></span>
<span data-ttu-id="66a20-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66a20-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a20-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66a20-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a20-139">輸入</span><span class="sxs-lookup"><span data-stu-id="66a20-139">INPUTS</span></span>

### <span data-ttu-id="66a20-140">System.String</span><span class="sxs-lookup"><span data-stu-id="66a20-140">System.String</span></span>

### <span data-ttu-id="66a20-141">Microsoft.Azure.Commands.Network.models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="66a20-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="66a20-142">輸出</span><span class="sxs-lookup"><span data-stu-id="66a20-142">OUTPUTS</span></span>

### <span data-ttu-id="66a20-143">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="66a20-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="66a20-144">筆記</span><span class="sxs-lookup"><span data-stu-id="66a20-144">NOTES</span></span>

## <span data-ttu-id="66a20-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="66a20-145">RELATED LINKS</span></span>
