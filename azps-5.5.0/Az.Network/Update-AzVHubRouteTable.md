---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135658"
---
# <span data-ttu-id="badb7-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="badb7-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="badb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="badb7-102">SYNOPSIS</span></span>
<span data-ttu-id="badb7-103">刪除與 VirtualHub 相關聯的中樞路由表資源。</span><span class="sxs-lookup"><span data-stu-id="badb7-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="badb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="badb7-104">SYNTAX</span></span>

### <span data-ttu-id="badb7-105">ByVHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="badb7-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="badb7-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="badb7-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="badb7-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="badb7-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="badb7-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="badb7-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="badb7-109">說明</span><span class="sxs-lookup"><span data-stu-id="badb7-109">DESCRIPTION</span></span>
<span data-ttu-id="badb7-110">使用提供的路由或標籤，更新與指定的虛擬中心相關聯的指定路由表。</span><span class="sxs-lookup"><span data-stu-id="badb7-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="badb7-111">示例</span><span class="sxs-lookup"><span data-stu-id="badb7-111">EXAMPLES</span></span>

### <span data-ttu-id="badb7-112">範例1</span><span class="sxs-lookup"><span data-stu-id="badb7-112">Example 1</span></span>
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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="badb7-113">這個命令會刪除虛擬中樞的中心路由表。</span><span class="sxs-lookup"><span data-stu-id="badb7-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="badb7-114">參數</span><span class="sxs-lookup"><span data-stu-id="badb7-114">PARAMETERS</span></span>

### <span data-ttu-id="badb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="badb7-115">-AsJob</span></span>
<span data-ttu-id="badb7-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="badb7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="badb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badb7-117">-DefaultProfile</span></span>
<span data-ttu-id="badb7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="badb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="badb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="badb7-119">-InputObject</span></span>
<span data-ttu-id="badb7-120">要更新的 vhubroutetable 資源。</span><span class="sxs-lookup"><span data-stu-id="badb7-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-121">-標籤</span><span class="sxs-lookup"><span data-stu-id="badb7-121">-Label</span></span>
<span data-ttu-id="badb7-122">標籤清單。</span><span class="sxs-lookup"><span data-stu-id="badb7-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="badb7-123">-Name</span></span>
<span data-ttu-id="badb7-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="badb7-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="badb7-125">-ParentObject</span></span>
<span data-ttu-id="badb7-126">此資源的父虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="badb7-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="badb7-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="badb7-127">-ParentResourceName</span></span>
<span data-ttu-id="badb7-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="badb7-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="badb7-129">-ResourceGroupName</span></span>
<span data-ttu-id="badb7-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="badb7-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="badb7-131">-ResourceId</span></span>
<span data-ttu-id="badb7-132">要更新之 vhubroutetable 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="badb7-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-133">-Route</span><span class="sxs-lookup"><span data-stu-id="badb7-133">-Route</span></span>
<span data-ttu-id="badb7-134">此路由表的路由清單。</span><span class="sxs-lookup"><span data-stu-id="badb7-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="badb7-135">-Confirm</span></span>
<span data-ttu-id="badb7-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="badb7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="badb7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="badb7-137">-WhatIf</span></span>
<span data-ttu-id="badb7-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="badb7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="badb7-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="badb7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="badb7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badb7-140">CommonParameters</span></span>
<span data-ttu-id="badb7-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="badb7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badb7-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="badb7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badb7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="badb7-143">INPUTS</span></span>

### <span data-ttu-id="badb7-144">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="badb7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="badb7-145">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="badb7-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="badb7-146">System.object</span><span class="sxs-lookup"><span data-stu-id="badb7-146">System.String</span></span>

## <span data-ttu-id="badb7-147">輸出</span><span class="sxs-lookup"><span data-stu-id="badb7-147">OUTPUTS</span></span>

### <span data-ttu-id="badb7-148">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="badb7-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="badb7-149">筆記</span><span class="sxs-lookup"><span data-stu-id="badb7-149">NOTES</span></span>

## <span data-ttu-id="badb7-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="badb7-150">RELATED LINKS</span></span>

[<span data-ttu-id="badb7-151">AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="badb7-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="badb7-152">新-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="badb7-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="badb7-153">新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="badb7-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="badb7-154">移除-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="badb7-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)