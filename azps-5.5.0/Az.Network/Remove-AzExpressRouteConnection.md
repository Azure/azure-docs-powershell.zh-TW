---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134902"
---
# <span data-ttu-id="e8f34-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e8f34-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="e8f34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8f34-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f34-103">移除 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="e8f34-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="e8f34-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8f34-104">SYNTAX</span></span>

### <span data-ttu-id="e8f34-105">ByExpressRouteConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="e8f34-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f34-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f34-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f34-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e8f34-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f34-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8f34-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f34-109">移除 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="e8f34-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="e8f34-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8f34-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f34-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8f34-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="e8f34-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="e8f34-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e8f34-113">在具有2個比例單位的虛擬中樞中，將會建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="e8f34-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e8f34-114">建立閘道之後，就會使用 [New-AzExpressRouteConnection] 命令將它連線至 ExpressRouteSite。</span><span class="sxs-lookup"><span data-stu-id="e8f34-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="e8f34-115">然後它會使用連接名稱移除連線。</span><span class="sxs-lookup"><span data-stu-id="e8f34-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="e8f34-116">範例2</span><span class="sxs-lookup"><span data-stu-id="e8f34-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="e8f34-117">與範例1相同，但現在它會從 AzExpressRouteConnection 中移除使用管道物件的連接。</span><span class="sxs-lookup"><span data-stu-id="e8f34-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="e8f34-118">參數</span><span class="sxs-lookup"><span data-stu-id="e8f34-118">PARAMETERS</span></span>

### <span data-ttu-id="e8f34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f34-119">-DefaultProfile</span></span>
<span data-ttu-id="e8f34-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8f34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f34-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="e8f34-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="e8f34-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f34-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f34-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e8f34-123">-Force</span></span>
<span data-ttu-id="e8f34-124">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="e8f34-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e8f34-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f34-125">-InputObject</span></span>
<span data-ttu-id="e8f34-126">要更新的 ExpressRouteConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="e8f34-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f34-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8f34-127">-Name</span></span>
<span data-ttu-id="e8f34-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f34-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f34-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8f34-129">-PassThru</span></span>
<span data-ttu-id="e8f34-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e8f34-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8f34-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e8f34-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8f34-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f34-132">-ResourceGroupName</span></span>
<span data-ttu-id="e8f34-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f34-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f34-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f34-134">-ResourceId</span></span>
<span data-ttu-id="e8f34-135">要刪除之 ExpressRouteConnection 物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8f34-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f34-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e8f34-136">-Confirm</span></span>
<span data-ttu-id="e8f34-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8f34-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f34-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f34-138">-WhatIf</span></span>
<span data-ttu-id="e8f34-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8f34-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f34-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8f34-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f34-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f34-141">CommonParameters</span></span>
<span data-ttu-id="e8f34-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8f34-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f34-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8f34-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f34-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e8f34-144">INPUTS</span></span>

### <span data-ttu-id="e8f34-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e8f34-145">System.String</span></span>

### <span data-ttu-id="e8f34-146">PSExpressRouteConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8f34-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e8f34-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e8f34-147">OUTPUTS</span></span>

### <span data-ttu-id="e8f34-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e8f34-148">System.Boolean</span></span>

## <span data-ttu-id="e8f34-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e8f34-149">NOTES</span></span>

## <span data-ttu-id="e8f34-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8f34-150">RELATED LINKS</span></span>
