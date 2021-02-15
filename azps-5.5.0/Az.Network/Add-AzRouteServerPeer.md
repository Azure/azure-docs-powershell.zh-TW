---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 70f7573a604ea15c33f1949883503fed2a356e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135023"
---
# <span data-ttu-id="8e264-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="8e264-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="8e264-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e264-102">SYNOPSIS</span></span>
<span data-ttu-id="8e264-103">將對等新增至 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="8e264-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="8e264-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e264-104">SYNTAX</span></span>

### <span data-ttu-id="8e264-105">RouteServerNPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8e264-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e264-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e264-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e264-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e264-107">DESCRIPTION</span></span>
<span data-ttu-id="8e264-108">**AzRouteServerPeer** Cmdlet 會將 RouteServer 對等新增至 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="8e264-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="8e264-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e264-109">EXAMPLES</span></span>

### <span data-ttu-id="8e264-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8e264-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="8e264-111">參數</span><span class="sxs-lookup"><span data-stu-id="8e264-111">PARAMETERS</span></span>

### <span data-ttu-id="8e264-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e264-112">-AsJob</span></span>
<span data-ttu-id="8e264-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e264-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e264-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e264-114">-DefaultProfile</span></span>
<span data-ttu-id="8e264-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e264-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e264-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8e264-116">-Force</span></span>
<span data-ttu-id="8e264-117">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8e264-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e264-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8e264-118">-PeerAsn</span></span>
<span data-ttu-id="8e264-119">遠端路由伺服器對等的 ASN。</span><span class="sxs-lookup"><span data-stu-id="8e264-119">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="8e264-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="8e264-120">-PeerIp</span></span>
<span data-ttu-id="8e264-121">遠端路由伺服器對等的 Ip。</span><span class="sxs-lookup"><span data-stu-id="8e264-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="8e264-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8e264-122">-PeerName</span></span>
<span data-ttu-id="8e264-123">路由伺服器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e264-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="8e264-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e264-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e264-125">路由伺服器/對等的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e264-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="8e264-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="8e264-126">-RouteServerName</span></span>
<span data-ttu-id="8e264-127">對等所在的路由伺服器。</span><span class="sxs-lookup"><span data-stu-id="8e264-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="8e264-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8e264-128">-Confirm</span></span>
<span data-ttu-id="8e264-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e264-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e264-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e264-130">-WhatIf</span></span>
<span data-ttu-id="8e264-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e264-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e264-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e264-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e264-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e264-133">CommonParameters</span></span>
<span data-ttu-id="8e264-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e264-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e264-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e264-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e264-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8e264-136">INPUTS</span></span>

### <span data-ttu-id="8e264-137">System.object</span><span class="sxs-lookup"><span data-stu-id="8e264-137">System.String</span></span>

### <span data-ttu-id="8e264-138">UInt32</span><span class="sxs-lookup"><span data-stu-id="8e264-138">System.UInt32</span></span>

## <span data-ttu-id="8e264-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8e264-139">OUTPUTS</span></span>

### <span data-ttu-id="8e264-140">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e264-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="8e264-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8e264-141">NOTES</span></span>

## <span data-ttu-id="8e264-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e264-142">RELATED LINKS</span></span>
