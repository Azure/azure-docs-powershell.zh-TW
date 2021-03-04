---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 3e9bd0022215f353388e19edb4f5cc6944acbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912706"
---
# <span data-ttu-id="7277c-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7277c-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="7277c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7277c-102">SYNOPSIS</span></span>
<span data-ttu-id="7277c-103">移除 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="7277c-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="7277c-104">語法</span><span class="sxs-lookup"><span data-stu-id="7277c-104">SYNTAX</span></span>

### <span data-ttu-id="7277c-105">ByExpressRouteConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="7277c-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7277c-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7277c-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7277c-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7277c-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7277c-108">描述</span><span class="sxs-lookup"><span data-stu-id="7277c-108">DESCRIPTION</span></span>
<span data-ttu-id="7277c-109">移除 ExpressRouteConnection。</span><span class="sxs-lookup"><span data-stu-id="7277c-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="7277c-110">例子</span><span class="sxs-lookup"><span data-stu-id="7277c-110">EXAMPLES</span></span>

### <span data-ttu-id="7277c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7277c-111">Example 1</span></span>
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

<span data-ttu-id="7277c-112">上述步驟將在 Azure 的 「testRG」資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="7277c-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7277c-113">在此之後，將會以 2 個縮放單位在虛擬中心中建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="7277c-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7277c-114">閘道建立後，會使用命令New-AzExpressRouteConnection ExpressRouteSite。</span><span class="sxs-lookup"><span data-stu-id="7277c-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="7277c-115">接著，它會使用連接名稱移除連接。</span><span class="sxs-lookup"><span data-stu-id="7277c-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="7277c-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="7277c-116">Example 2</span></span>

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

<span data-ttu-id="7277c-117">與範例 1 相同，但現在會從 Get-AzExpressRouteConnection 使用管道物件移除連接。</span><span class="sxs-lookup"><span data-stu-id="7277c-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="7277c-118">參數</span><span class="sxs-lookup"><span data-stu-id="7277c-118">PARAMETERS</span></span>

### <span data-ttu-id="7277c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7277c-119">-DefaultProfile</span></span>
<span data-ttu-id="7277c-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7277c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7277c-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="7277c-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="7277c-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7277c-122">The parent resource name.</span></span>

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

### <span data-ttu-id="7277c-123">-強制</span><span class="sxs-lookup"><span data-stu-id="7277c-123">-Force</span></span>
<span data-ttu-id="7277c-124">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="7277c-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7277c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7277c-125">-InputObject</span></span>
<span data-ttu-id="7277c-126">要更新的 ExpressRouteConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="7277c-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="7277c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="7277c-127">-Name</span></span>
<span data-ttu-id="7277c-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7277c-128">The resource name.</span></span>

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

### <span data-ttu-id="7277c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7277c-129">-PassThru</span></span>
<span data-ttu-id="7277c-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7277c-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7277c-131">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7277c-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7277c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7277c-132">-ResourceGroupName</span></span>
<span data-ttu-id="7277c-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7277c-133">The resource group name.</span></span>

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

### <span data-ttu-id="7277c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7277c-134">-ResourceId</span></span>
<span data-ttu-id="7277c-135">要刪除的 ExpressRouteConnection 物件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7277c-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="7277c-136">-確認</span><span class="sxs-lookup"><span data-stu-id="7277c-136">-Confirm</span></span>
<span data-ttu-id="7277c-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7277c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7277c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7277c-138">-WhatIf</span></span>
<span data-ttu-id="7277c-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7277c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7277c-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7277c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7277c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7277c-141">CommonParameters</span></span>
<span data-ttu-id="7277c-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7277c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7277c-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7277c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7277c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="7277c-144">INPUTS</span></span>

### <span data-ttu-id="7277c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7277c-145">System.String</span></span>

### <span data-ttu-id="7277c-146">Microsoft.Azure.Commands.Network.models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7277c-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7277c-147">輸出</span><span class="sxs-lookup"><span data-stu-id="7277c-147">OUTPUTS</span></span>

### <span data-ttu-id="7277c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7277c-148">System.Boolean</span></span>

## <span data-ttu-id="7277c-149">筆記</span><span class="sxs-lookup"><span data-stu-id="7277c-149">NOTES</span></span>

## <span data-ttu-id="7277c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="7277c-150">RELATED LINKS</span></span>
