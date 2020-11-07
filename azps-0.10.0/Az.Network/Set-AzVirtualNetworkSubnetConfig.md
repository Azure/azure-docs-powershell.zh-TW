---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 73649f0f04cf1de07d991cb454b44308c4ff6443
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795378"
---
# <span data-ttu-id="a2efd-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2efd-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a2efd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2efd-102">SYNOPSIS</span></span>
<span data-ttu-id="a2efd-103">在虛擬網路中設定子網配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a2efd-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

## <span data-ttu-id="a2efd-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2efd-104">SYNTAX</span></span>

### <span data-ttu-id="a2efd-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a2efd-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2efd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2efd-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2efd-107">說明</span><span class="sxs-lookup"><span data-stu-id="a2efd-107">DESCRIPTION</span></span>
<span data-ttu-id="a2efd-108">AzVirtualNetworkSubnetConfig Cmdlet 會針對 Azure 虛擬網路中的子網配置 **設定** 目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a2efd-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="a2efd-109">示例</span><span class="sxs-lookup"><span data-stu-id="a2efd-109">EXAMPLES</span></span>

### <span data-ttu-id="a2efd-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="a2efd-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="a2efd-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2efd-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="a2efd-112">然後，通話 Set-AzVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="a2efd-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="a2efd-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="a2efd-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a2efd-114">接著，就會呼叫 Set-AzVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a2efd-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="a2efd-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="a2efd-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="a2efd-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a2efd-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="a2efd-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a2efd-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="a2efd-118">Set-AzVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a2efd-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="a2efd-119">接著會呼叫 Set-AzVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="a2efd-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="a2efd-120">參數</span><span class="sxs-lookup"><span data-stu-id="a2efd-120">PARAMETERS</span></span>

### <span data-ttu-id="a2efd-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a2efd-121">-AddressPrefix</span></span>
<span data-ttu-id="a2efd-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="a2efd-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2efd-123">-DefaultProfile</span></span>
<span data-ttu-id="a2efd-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2efd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2efd-125">-Name</span></span>
<span data-ttu-id="a2efd-126">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2efd-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2efd-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a2efd-128">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="a2efd-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a2efd-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a2efd-130">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="a2efd-130">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a2efd-131">-RouteTable</span></span>
<span data-ttu-id="a2efd-132">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="a2efd-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a2efd-133">-RouteTableId</span></span>
<span data-ttu-id="a2efd-134">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2efd-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2efd-135">-ServiceEndpoint</span></span>
<span data-ttu-id="a2efd-136">服務端點值</span><span class="sxs-lookup"><span data-stu-id="a2efd-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a2efd-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2efd-137">-VirtualNetwork</span></span>
<span data-ttu-id="a2efd-138">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="a2efd-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2efd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2efd-139">CommonParameters</span></span>
<span data-ttu-id="a2efd-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2efd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2efd-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2efd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2efd-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a2efd-142">INPUTS</span></span>

### <span data-ttu-id="a2efd-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2efd-143">PSVirtualNetwork</span></span>
<span data-ttu-id="a2efd-144">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a2efd-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a2efd-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a2efd-145">OUTPUTS</span></span>

### <span data-ttu-id="a2efd-146">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2efd-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a2efd-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a2efd-147">NOTES</span></span>

## <span data-ttu-id="a2efd-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2efd-148">RELATED LINKS</span></span>

[<span data-ttu-id="a2efd-149">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2efd-149">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2efd-150">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2efd-150">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2efd-151">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2efd-151">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a2efd-152">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a2efd-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)


