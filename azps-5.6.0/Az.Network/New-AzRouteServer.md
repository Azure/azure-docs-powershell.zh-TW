---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 24e53b7f7bfd0f09e93184b2862deed4608af544
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903470"
---
# <span data-ttu-id="b5ee5-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="b5ee5-101">New-AzRouteServer</span></span>

## <span data-ttu-id="b5ee5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ee5-103">建立 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="b5ee5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5ee5-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ee5-105">描述</span><span class="sxs-lookup"><span data-stu-id="b5ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ee5-106">**New-AzRouteServer** Cmdlet 會建立 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="b5ee5-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="b5ee5-107">例子</span><span class="sxs-lookup"><span data-stu-id="b5ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ee5-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5ee5-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="b5ee5-109">參數</span><span class="sxs-lookup"><span data-stu-id="b5ee5-109">PARAMETERS</span></span>

### <span data-ttu-id="b5ee5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5ee5-110">-AsJob</span></span>
<span data-ttu-id="b5ee5-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5ee5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5ee5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ee5-112">-DefaultProfile</span></span>
<span data-ttu-id="b5ee5-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ee5-114">-強制</span><span class="sxs-lookup"><span data-stu-id="b5ee5-114">-Force</span></span>
<span data-ttu-id="b5ee5-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="b5ee5-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5ee5-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="b5ee5-116">-HostedSubnet</span></span>
<span data-ttu-id="b5ee5-117">路由伺服器託管的子網。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-117">The subnet where the route server is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee5-118">-位置</span><span class="sxs-lookup"><span data-stu-id="b5ee5-118">-Location</span></span>
<span data-ttu-id="b5ee5-119">位置。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-119">The location.</span></span>

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

### <span data-ttu-id="b5ee5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ee5-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5ee5-121">路由伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="b5ee5-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="b5ee5-122">-RouteServerName</span></span>
<span data-ttu-id="b5ee5-123">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-123">The name of the route server.</span></span>

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

### <span data-ttu-id="b5ee5-124">-標記</span><span class="sxs-lookup"><span data-stu-id="b5ee5-124">-Tag</span></span>
<span data-ttu-id="b5ee5-125">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b5ee5-126">-Confirm</span></span>
<span data-ttu-id="b5ee5-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ee5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ee5-128">-WhatIf</span></span>
<span data-ttu-id="b5ee5-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ee5-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ee5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ee5-131">CommonParameters</span></span>
<span data-ttu-id="b5ee5-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5ee5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ee5-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5ee5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ee5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b5ee5-134">INPUTS</span></span>

### <span data-ttu-id="b5ee5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b5ee5-135">System.String</span></span>

### <span data-ttu-id="b5ee5-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5ee5-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5ee5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b5ee5-137">OUTPUTS</span></span>

### <span data-ttu-id="b5ee5-138">Microsoft.Azure.Commands.Network.models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="b5ee5-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="b5ee5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b5ee5-139">NOTES</span></span>

## <span data-ttu-id="b5ee5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5ee5-140">RELATED LINKS</span></span>
