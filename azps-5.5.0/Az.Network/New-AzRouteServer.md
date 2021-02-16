---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 15a613f4d2c695fe42df5b02012187bdeee615b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128827"
---
# <span data-ttu-id="b7d33-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="b7d33-101">New-AzRouteServer</span></span>

## <span data-ttu-id="b7d33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7d33-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d33-103">建立 Azure RouteServer。</span><span class="sxs-lookup"><span data-stu-id="b7d33-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="b7d33-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7d33-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d33-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7d33-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d33-106">**新的-AzRouteServer** Cmdlet 會建立 Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="b7d33-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="b7d33-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7d33-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d33-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b7d33-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="b7d33-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7d33-109">PARAMETERS</span></span>

### <span data-ttu-id="b7d33-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7d33-110">-AsJob</span></span>
<span data-ttu-id="b7d33-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7d33-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7d33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d33-112">-DefaultProfile</span></span>
<span data-ttu-id="b7d33-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7d33-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d33-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b7d33-114">-Force</span></span>
<span data-ttu-id="b7d33-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b7d33-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b7d33-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="b7d33-116">-HostedSubnet</span></span>
<span data-ttu-id="b7d33-117">主持路由伺服器的子網。</span><span class="sxs-lookup"><span data-stu-id="b7d33-117">The subnet where the route server is hosted.</span></span>

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

### <span data-ttu-id="b7d33-118">-位置</span><span class="sxs-lookup"><span data-stu-id="b7d33-118">-Location</span></span>
<span data-ttu-id="b7d33-119">位置。</span><span class="sxs-lookup"><span data-stu-id="b7d33-119">The location.</span></span>

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

### <span data-ttu-id="b7d33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d33-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7d33-121">路由伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d33-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="b7d33-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="b7d33-122">-RouteServerName</span></span>
<span data-ttu-id="b7d33-123">路由伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d33-123">The name of the route server.</span></span>

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

### <span data-ttu-id="b7d33-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7d33-124">-Tag</span></span>
<span data-ttu-id="b7d33-125">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b7d33-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b7d33-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b7d33-126">-Confirm</span></span>
<span data-ttu-id="b7d33-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7d33-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d33-128">-WhatIf</span></span>
<span data-ttu-id="b7d33-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7d33-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d33-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7d33-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d33-131">CommonParameters</span></span>
<span data-ttu-id="b7d33-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7d33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d33-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7d33-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d33-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b7d33-134">INPUTS</span></span>

### <span data-ttu-id="b7d33-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b7d33-135">System.String</span></span>

### <span data-ttu-id="b7d33-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7d33-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7d33-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b7d33-137">OUTPUTS</span></span>

### <span data-ttu-id="b7d33-138">PSRouteServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7d33-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="b7d33-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b7d33-139">NOTES</span></span>

## <span data-ttu-id="b7d33-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7d33-140">RELATED LINKS</span></span>
