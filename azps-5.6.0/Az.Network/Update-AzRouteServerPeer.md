---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 3c0be49a09758648bcd2301f2643577ea8dcd951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901825"
---
# <span data-ttu-id="2415a-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2415a-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="2415a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2415a-102">SYNOPSIS</span></span>
<span data-ttu-id="2415a-103">更新 Azure RouteServer 中的對等程式</span><span class="sxs-lookup"><span data-stu-id="2415a-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="2415a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2415a-104">SYNTAX</span></span>

### <span data-ttu-id="2415a-105">RouteServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2415a-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415a-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2415a-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2415a-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2415a-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2415a-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2415a-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2415a-109">描述</span><span class="sxs-lookup"><span data-stu-id="2415a-109">DESCRIPTION</span></span>
<span data-ttu-id="2415a-110">**Update-AzRouteServerPeer** Cmdlet 將 RouteServer 對等更新為 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="2415a-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="2415a-111">例子</span><span class="sxs-lookup"><span data-stu-id="2415a-111">EXAMPLES</span></span>

### <span data-ttu-id="2415a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2415a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2415a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2415a-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2415a-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="2415a-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="2415a-115">參數</span><span class="sxs-lookup"><span data-stu-id="2415a-115">PARAMETERS</span></span>

### <span data-ttu-id="2415a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2415a-116">-AsJob</span></span>
<span data-ttu-id="2415a-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2415a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2415a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2415a-118">-DefaultProfile</span></span>
<span data-ttu-id="2415a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2415a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2415a-120">-強制</span><span class="sxs-lookup"><span data-stu-id="2415a-120">-Force</span></span>
<span data-ttu-id="2415a-121">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="2415a-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2415a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2415a-122">-InputObject</span></span>
<span data-ttu-id="2415a-123">路由伺服器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="2415a-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="2415a-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2415a-124">-PeerAsn</span></span>
<span data-ttu-id="2415a-125">遠端路由伺服器對等的 ASN。</span><span class="sxs-lookup"><span data-stu-id="2415a-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2415a-126">-對等互連</span><span class="sxs-lookup"><span data-stu-id="2415a-126">-PeerIp</span></span>
<span data-ttu-id="2415a-127">遠端路由伺服器對等的 Ip。</span><span class="sxs-lookup"><span data-stu-id="2415a-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="2415a-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2415a-128">-PeerName</span></span>
<span data-ttu-id="2415a-129">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="2415a-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="2415a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2415a-130">-ResourceGroupName</span></span>
<span data-ttu-id="2415a-131">路由伺服器/對等體的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2415a-131">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="2415a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2415a-132">-ResourceId</span></span>
<span data-ttu-id="2415a-133">路由伺服器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2415a-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="2415a-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2415a-134">-RouteServerName</span></span>
<span data-ttu-id="2415a-135">對等存在之路由伺服器。</span><span class="sxs-lookup"><span data-stu-id="2415a-135">The route server where peer exists.</span></span>

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

### <span data-ttu-id="2415a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="2415a-136">-Confirm</span></span>
<span data-ttu-id="2415a-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2415a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2415a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2415a-138">-WhatIf</span></span>
<span data-ttu-id="2415a-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2415a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2415a-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2415a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2415a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2415a-141">CommonParameters</span></span>
<span data-ttu-id="2415a-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2415a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2415a-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2415a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2415a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="2415a-144">INPUTS</span></span>

### <span data-ttu-id="2415a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2415a-145">System.String</span></span>

### <span data-ttu-id="2415a-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2415a-146">System.UInt32</span></span>

### <span data-ttu-id="2415a-147">Microsoft.Azure.Commands.Network.models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2415a-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="2415a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2415a-148">OUTPUTS</span></span>

### <span data-ttu-id="2415a-149">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2415a-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2415a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2415a-150">NOTES</span></span>

## <span data-ttu-id="2415a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2415a-151">RELATED LINKS</span></span>
