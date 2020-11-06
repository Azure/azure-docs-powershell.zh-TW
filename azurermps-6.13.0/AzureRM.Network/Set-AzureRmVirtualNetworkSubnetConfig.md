---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e8aeb73c694229e290ee96fa11d3de71bb510ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448289"
---
# <span data-ttu-id="05fa5-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05fa5-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="05fa5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="05fa5-103">在虛擬網路中設定子網配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="05fa5-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05fa5-104">句法</span><span class="sxs-lookup"><span data-stu-id="05fa5-104">SYNTAX</span></span>

### <span data-ttu-id="05fa5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="05fa5-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05fa5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="05fa5-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05fa5-107">說明</span><span class="sxs-lookup"><span data-stu-id="05fa5-107">DESCRIPTION</span></span>
<span data-ttu-id="05fa5-108">AzureRmVirtualNetworkSubnetConfig Cmdlet 會針對 Azure 虛擬網路中的子網配置 **設定** 目標狀態。</span><span class="sxs-lookup"><span data-stu-id="05fa5-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="05fa5-109">示例</span><span class="sxs-lookup"><span data-stu-id="05fa5-109">EXAMPLES</span></span>

### <span data-ttu-id="05fa5-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="05fa5-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="05fa5-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="05fa5-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="05fa5-112">然後，通話 Set-AzureRmVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="05fa5-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="05fa5-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="05fa5-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="05fa5-114">接著，就會呼叫 Set-AzureRmVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="05fa5-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="05fa5-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="05fa5-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="05fa5-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="05fa5-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="05fa5-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="05fa5-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="05fa5-118">Set-AzureRmVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="05fa5-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="05fa5-119">接著會呼叫 Set-AzureRmVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="05fa5-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="05fa5-120">參數</span><span class="sxs-lookup"><span data-stu-id="05fa5-120">PARAMETERS</span></span>

### <span data-ttu-id="05fa5-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="05fa5-121">-AddressPrefix</span></span>
<span data-ttu-id="05fa5-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="05fa5-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05fa5-123">-DefaultProfile</span></span>
<span data-ttu-id="05fa5-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05fa5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-125">委派</span><span class="sxs-lookup"><span data-stu-id="05fa5-125">-Delegation</span></span>
<span data-ttu-id="05fa5-126">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="05fa5-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="05fa5-127">-Name</span></span>
<span data-ttu-id="05fa5-128">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="05fa5-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="05fa5-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="05fa5-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="05fa5-130">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="05fa5-130">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="05fa5-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="05fa5-132">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="05fa5-132">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="05fa5-133">-RouteTable</span></span>
<span data-ttu-id="05fa5-134">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="05fa5-134">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="05fa5-135">-RouteTableId</span></span>
<span data-ttu-id="05fa5-136">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="05fa5-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="05fa5-137">-ServiceEndpoint</span></span>
<span data-ttu-id="05fa5-138">服務端點值</span><span class="sxs-lookup"><span data-stu-id="05fa5-138">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05fa5-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="05fa5-140">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="05fa5-140">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05fa5-141">-VirtualNetwork</span></span>
<span data-ttu-id="05fa5-142">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="05fa5-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05fa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05fa5-143">CommonParameters</span></span>
<span data-ttu-id="05fa5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05fa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05fa5-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05fa5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05fa5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="05fa5-146">INPUTS</span></span>

### <span data-ttu-id="05fa5-147">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="05fa5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="05fa5-148">System.object</span><span class="sxs-lookup"><span data-stu-id="05fa5-148">System.String</span></span>

### <span data-ttu-id="05fa5-149">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="05fa5-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="05fa5-150">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="05fa5-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="05fa5-151">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="05fa5-151">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="05fa5-152">[System.object]. 清單 ' 1 [PSServiceEndpointPolicy，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="05fa5-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="05fa5-153">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.Network.Models.PSDelegation，6.7.0.0 "Network，版本 =，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="05fa5-153">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="05fa5-154">輸出</span><span class="sxs-lookup"><span data-stu-id="05fa5-154">OUTPUTS</span></span>

### <span data-ttu-id="05fa5-155">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="05fa5-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="05fa5-156">筆記</span><span class="sxs-lookup"><span data-stu-id="05fa5-156">NOTES</span></span>

## <span data-ttu-id="05fa5-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="05fa5-157">RELATED LINKS</span></span>

[<span data-ttu-id="05fa5-158">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05fa5-158">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="05fa5-159">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05fa5-159">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="05fa5-160">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05fa5-160">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="05fa5-161">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05fa5-161">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


