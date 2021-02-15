---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140262"
---
# <span data-ttu-id="baed0-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="baed0-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="baed0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="baed0-102">SYNOPSIS</span></span>
<span data-ttu-id="baed0-103">從 Azure RouteServer 中移除對等</span><span class="sxs-lookup"><span data-stu-id="baed0-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="baed0-104">句法</span><span class="sxs-lookup"><span data-stu-id="baed0-104">SYNTAX</span></span>

### <span data-ttu-id="baed0-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="baed0-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baed0-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baed0-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baed0-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="baed0-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baed0-108">說明</span><span class="sxs-lookup"><span data-stu-id="baed0-108">DESCRIPTION</span></span>
<span data-ttu-id="baed0-109">**AzRouteServerPeer** Cmdlet 會從 Azure RouteServer 中移除 RouteServer 對等</span><span class="sxs-lookup"><span data-stu-id="baed0-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="baed0-110">示例</span><span class="sxs-lookup"><span data-stu-id="baed0-110">EXAMPLES</span></span>

### <span data-ttu-id="baed0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="baed0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="baed0-112">範例2</span><span class="sxs-lookup"><span data-stu-id="baed0-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="baed0-113">範例3</span><span class="sxs-lookup"><span data-stu-id="baed0-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="baed0-114">參數</span><span class="sxs-lookup"><span data-stu-id="baed0-114">PARAMETERS</span></span>

### <span data-ttu-id="baed0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baed0-115">-AsJob</span></span>
<span data-ttu-id="baed0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="baed0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baed0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baed0-117">-DefaultProfile</span></span>
<span data-ttu-id="baed0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="baed0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baed0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="baed0-119">-Force</span></span>
<span data-ttu-id="baed0-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="baed0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="baed0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baed0-121">-InputObject</span></span>
<span data-ttu-id="baed0-122">路由伺服器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="baed0-122">The route server peer input object.</span></span>

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

### <span data-ttu-id="baed0-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="baed0-123">-PeerName</span></span>
<span data-ttu-id="baed0-124">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="baed0-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="baed0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baed0-125">-ResourceGroupName</span></span>
<span data-ttu-id="baed0-126">路由伺服器/對等的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="baed0-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="baed0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baed0-127">-ResourceId</span></span>
<span data-ttu-id="baed0-128">路由伺服器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="baed0-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="baed0-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="baed0-129">-RouteServerName</span></span>
<span data-ttu-id="baed0-130">對等所在的路由伺服器。</span><span class="sxs-lookup"><span data-stu-id="baed0-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="baed0-131">-確認</span><span class="sxs-lookup"><span data-stu-id="baed0-131">-Confirm</span></span>
<span data-ttu-id="baed0-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="baed0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baed0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baed0-133">-WhatIf</span></span>
<span data-ttu-id="baed0-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="baed0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baed0-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="baed0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baed0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baed0-136">CommonParameters</span></span>
<span data-ttu-id="baed0-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="baed0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baed0-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="baed0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baed0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="baed0-139">INPUTS</span></span>

### <span data-ttu-id="baed0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="baed0-140">System.String</span></span>

### <span data-ttu-id="baed0-141">PSRouteServerPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baed0-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="baed0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="baed0-142">OUTPUTS</span></span>

### <span data-ttu-id="baed0-143">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baed0-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="baed0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="baed0-144">NOTES</span></span>

## <span data-ttu-id="baed0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="baed0-145">RELATED LINKS</span></span>
