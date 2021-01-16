---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281524"
---
# <span data-ttu-id="b1920-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1920-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="b1920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1920-102">SYNOPSIS</span></span>
<span data-ttu-id="b1920-103">檢索與 VirtualHub 相關聯的中樞路由表資源。</span><span class="sxs-lookup"><span data-stu-id="b1920-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="b1920-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1920-104">SYNTAX</span></span>

### <span data-ttu-id="b1920-105">ByVHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="b1920-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1920-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b1920-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1920-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="b1920-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1920-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1920-108">DESCRIPTION</span></span>
<span data-ttu-id="b1920-109">取得與指定的虛擬中樞相關聯的指定中樞路由表。</span><span class="sxs-lookup"><span data-stu-id="b1920-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="b1920-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1920-110">EXAMPLES</span></span>

### <span data-ttu-id="b1920-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b1920-111">Example 1</span></span>

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

<span data-ttu-id="b1920-112">這個命令會取得虛擬中樞的中心路由表。</span><span class="sxs-lookup"><span data-stu-id="b1920-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="b1920-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b1920-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="b1920-114">這個命令會列出指定 VirtualHub 中的所有中樞路由表。</span><span class="sxs-lookup"><span data-stu-id="b1920-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="b1920-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1920-115">PARAMETERS</span></span>

### <span data-ttu-id="b1920-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1920-116">-AsJob</span></span>
<span data-ttu-id="b1920-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1920-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1920-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1920-118">-DefaultProfile</span></span>
<span data-ttu-id="b1920-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1920-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1920-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1920-120">-Name</span></span>
<span data-ttu-id="b1920-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b1920-121">The resource name.</span></span>

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

### <span data-ttu-id="b1920-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b1920-122">-ParentObject</span></span>
<span data-ttu-id="b1920-123">此資源的父虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="b1920-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="b1920-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b1920-124">-ParentResourceName</span></span>
<span data-ttu-id="b1920-125">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b1920-125">The parent resource name.</span></span>

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

### <span data-ttu-id="b1920-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1920-126">-ResourceGroupName</span></span>
<span data-ttu-id="b1920-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1920-127">The resource group name.</span></span>

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

### <span data-ttu-id="b1920-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1920-128">-ResourceId</span></span>
<span data-ttu-id="b1920-129">要取得之 vhubroutetable 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1920-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="b1920-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b1920-130">-Confirm</span></span>
<span data-ttu-id="b1920-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1920-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1920-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1920-132">-WhatIf</span></span>
<span data-ttu-id="b1920-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1920-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1920-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1920-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1920-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1920-135">CommonParameters</span></span>
<span data-ttu-id="b1920-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1920-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1920-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1920-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1920-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b1920-138">INPUTS</span></span>

### <span data-ttu-id="b1920-139">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1920-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b1920-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b1920-140">System.String</span></span>

## <span data-ttu-id="b1920-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b1920-141">OUTPUTS</span></span>

### <span data-ttu-id="b1920-142">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b1920-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="b1920-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b1920-143">NOTES</span></span>

## <span data-ttu-id="b1920-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1920-144">RELATED LINKS</span></span>

[<span data-ttu-id="b1920-145">新-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b1920-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="b1920-146">新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1920-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b1920-147">更新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1920-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="b1920-148">移除-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1920-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)