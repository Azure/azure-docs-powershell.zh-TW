---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135806"
---
# <span data-ttu-id="4c0f6-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c0f6-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="4c0f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0f6-103">建立與 VirtualHub 相關聯的中樞路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="4c0f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c0f6-104">SYNTAX</span></span>

### <span data-ttu-id="4c0f6-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="4c0f6-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0f6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4c0f6-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0f6-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0f6-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="4c0f6-108">DESCRIPTION</span></span>
<span data-ttu-id="4c0f6-109">使用提供的路由和標籤，建立與指定的虛擬中樞相關聯的指定路由表。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="4c0f6-110">示例</span><span class="sxs-lookup"><span data-stu-id="4c0f6-110">EXAMPLES</span></span>

### <span data-ttu-id="4c0f6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4c0f6-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="4c0f6-112">這個命令會建立虛擬中樞的中樞路由表。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="4c0f6-113">參數</span><span class="sxs-lookup"><span data-stu-id="4c0f6-113">PARAMETERS</span></span>

### <span data-ttu-id="4c0f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c0f6-114">-AsJob</span></span>
<span data-ttu-id="4c0f6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4c0f6-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0f6-116">-DefaultProfile</span></span>
<span data-ttu-id="4c0f6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-118">-標籤</span><span class="sxs-lookup"><span data-stu-id="4c0f6-118">-Label</span></span>
<span data-ttu-id="4c0f6-119">標籤清單。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c0f6-120">-Name</span></span>
<span data-ttu-id="4c0f6-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c0f6-122">-ParentObject</span></span>
<span data-ttu-id="4c0f6-123">此資源的父虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4c0f6-124">-ParentResourceName</span></span>
<span data-ttu-id="4c0f6-125">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0f6-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c0f6-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0f6-128">-ParentResourceId</span></span>
<span data-ttu-id="4c0f6-129">虛擬中心資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-130">-Route</span><span class="sxs-lookup"><span data-stu-id="4c0f6-130">-Route</span></span>
<span data-ttu-id="4c0f6-131">此路由表的路由清單。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4c0f6-132">-Confirm</span></span>
<span data-ttu-id="4c0f6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0f6-134">-WhatIf</span></span>
<span data-ttu-id="4c0f6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0f6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0f6-137">CommonParameters</span></span>
<span data-ttu-id="4c0f6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0f6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c0f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0f6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4c0f6-140">INPUTS</span></span>

### <span data-ttu-id="4c0f6-141">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c0f6-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4c0f6-142">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c0f6-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="4c0f6-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4c0f6-143">System.String</span></span>

## <span data-ttu-id="4c0f6-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4c0f6-144">OUTPUTS</span></span>

### <span data-ttu-id="4c0f6-145">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c0f6-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="4c0f6-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4c0f6-146">NOTES</span></span>

## <span data-ttu-id="4c0f6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c0f6-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c0f6-148">AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c0f6-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="4c0f6-149">新-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="4c0f6-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="4c0f6-150">移除-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c0f6-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="4c0f6-151">更新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4c0f6-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
