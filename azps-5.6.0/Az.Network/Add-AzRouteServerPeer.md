---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908866"
---
# <span data-ttu-id="94f3c-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="94f3c-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="94f3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="94f3c-103">新增對等專案至 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="94f3c-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="94f3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="94f3c-104">SYNTAX</span></span>

### <span data-ttu-id="94f3c-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94f3c-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f3c-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94f3c-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94f3c-107">描述</span><span class="sxs-lookup"><span data-stu-id="94f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="94f3c-108">**Add-AzRouteServerPeer** Cmdlet 會將 RouteServer 對等新增到 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="94f3c-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="94f3c-109">例子</span><span class="sxs-lookup"><span data-stu-id="94f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="94f3c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="94f3c-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="94f3c-111">參數</span><span class="sxs-lookup"><span data-stu-id="94f3c-111">PARAMETERS</span></span>

### <span data-ttu-id="94f3c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f3c-112">-AsJob</span></span>
<span data-ttu-id="94f3c-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94f3c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f3c-114">-DefaultProfile</span></span>
<span data-ttu-id="94f3c-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f3c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f3c-116">-強制</span><span class="sxs-lookup"><span data-stu-id="94f3c-116">-Force</span></span>
<span data-ttu-id="94f3c-117">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="94f3c-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="94f3c-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="94f3c-118">-PeerAsn</span></span>
<span data-ttu-id="94f3c-119">遠端路由伺服器對等的 ASN。</span><span class="sxs-lookup"><span data-stu-id="94f3c-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f3c-120">-對等互連</span><span class="sxs-lookup"><span data-stu-id="94f3c-120">-PeerIp</span></span>
<span data-ttu-id="94f3c-121">遠端路由伺服器對等的 Ip。</span><span class="sxs-lookup"><span data-stu-id="94f3c-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="94f3c-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="94f3c-122">-PeerName</span></span>
<span data-ttu-id="94f3c-123">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="94f3c-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="94f3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="94f3c-125">路由伺服器/對等體的資源組名。</span><span class="sxs-lookup"><span data-stu-id="94f3c-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="94f3c-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="94f3c-126">-RouteServerName</span></span>
<span data-ttu-id="94f3c-127">對等存在之路由伺服器。</span><span class="sxs-lookup"><span data-stu-id="94f3c-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f3c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="94f3c-128">-Confirm</span></span>
<span data-ttu-id="94f3c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94f3c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f3c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f3c-130">-WhatIf</span></span>
<span data-ttu-id="94f3c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f3c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f3c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f3c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f3c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f3c-133">CommonParameters</span></span>
<span data-ttu-id="94f3c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94f3c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f3c-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94f3c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f3c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="94f3c-136">INPUTS</span></span>

### <span data-ttu-id="94f3c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="94f3c-137">System.String</span></span>

### <span data-ttu-id="94f3c-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="94f3c-138">System.UInt32</span></span>

## <span data-ttu-id="94f3c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="94f3c-139">OUTPUTS</span></span>

### <span data-ttu-id="94f3c-140">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="94f3c-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="94f3c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="94f3c-141">NOTES</span></span>

## <span data-ttu-id="94f3c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f3c-142">RELATED LINKS</span></span>
