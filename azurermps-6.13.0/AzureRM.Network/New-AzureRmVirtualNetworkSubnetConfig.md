---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447346"
---
# <span data-ttu-id="2eb70-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2eb70-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2eb70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2eb70-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb70-103">建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="2eb70-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb70-104">句法</span><span class="sxs-lookup"><span data-stu-id="2eb70-104">SYNTAX</span></span>

### <span data-ttu-id="2eb70-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="2eb70-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb70-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb70-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb70-107">說明</span><span class="sxs-lookup"><span data-stu-id="2eb70-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb70-108">**新的-AzureRmVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="2eb70-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="2eb70-109">示例</span><span class="sxs-lookup"><span data-stu-id="2eb70-109">EXAMPLES</span></span>

### <span data-ttu-id="2eb70-110">1：使用兩個子網和網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="2eb70-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="2eb70-111">這個範例會使用 New-AzureRmVirtualSubnetConfig Cmdlet 建立兩個新的子網設定，然後使用它們來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2eb70-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="2eb70-112">New-AzureRmVirtualSubnetConfig 範本只會建立子網的記憶體內部表示。</span><span class="sxs-lookup"><span data-stu-id="2eb70-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="2eb70-113">在這個範例中，frontendSubnet 有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="2eb70-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="2eb70-114">BackendSubnet 有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="2eb70-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="2eb70-115">參數</span><span class="sxs-lookup"><span data-stu-id="2eb70-115">PARAMETERS</span></span>

### <span data-ttu-id="2eb70-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2eb70-116">-AddressPrefix</span></span>
<span data-ttu-id="2eb70-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="2eb70-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="2eb70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb70-118">-DefaultProfile</span></span>
<span data-ttu-id="2eb70-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2eb70-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eb70-120">委派</span><span class="sxs-lookup"><span data-stu-id="2eb70-120">-Delegation</span></span>
<span data-ttu-id="2eb70-121">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="2eb70-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="2eb70-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2eb70-122">-Name</span></span>
<span data-ttu-id="2eb70-123">指定要建立的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2eb70-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="2eb70-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2eb70-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2eb70-125">指定 NetworkSecurityGroup 物件。</span><span class="sxs-lookup"><span data-stu-id="2eb70-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="2eb70-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2eb70-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2eb70-127">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="2eb70-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2eb70-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2eb70-128">-RouteTable</span></span>
<span data-ttu-id="2eb70-129">指定與子網配置相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="2eb70-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="2eb70-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2eb70-130">-RouteTableId</span></span>
<span data-ttu-id="2eb70-131">指定與子網配置相關聯之路由資料表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eb70-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="2eb70-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2eb70-132">-ServiceEndpoint</span></span>
<span data-ttu-id="2eb70-133">服務端點值</span><span class="sxs-lookup"><span data-stu-id="2eb70-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="2eb70-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2eb70-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2eb70-135">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="2eb70-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="2eb70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb70-136">CommonParameters</span></span>
<span data-ttu-id="2eb70-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2eb70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb70-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2eb70-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb70-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2eb70-139">INPUTS</span></span>

### <span data-ttu-id="2eb70-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2eb70-140">System.String</span></span>

### <span data-ttu-id="2eb70-141">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2eb70-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2eb70-142">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2eb70-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2eb70-143">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2eb70-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2eb70-144">[System.object]. 清單 ' 1 [PSServiceEndpointPolicy，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="2eb70-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2eb70-145">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.Network.Models.PSDelegation，6.7.0.0 "Network，版本 =，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2eb70-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2eb70-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2eb70-146">OUTPUTS</span></span>

### <span data-ttu-id="2eb70-147">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2eb70-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2eb70-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2eb70-148">NOTES</span></span>

## <span data-ttu-id="2eb70-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2eb70-149">RELATED LINKS</span></span>

[<span data-ttu-id="2eb70-150">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2eb70-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2eb70-151">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2eb70-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2eb70-152">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2eb70-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2eb70-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2eb70-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


