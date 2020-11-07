---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: b13a06fbc2bd7f071888dcd0504d3e1963cbedd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801942"
---
# <span data-ttu-id="ab88a-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab88a-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="ab88a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab88a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab88a-103">在虛擬網路中設定子網配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ab88a-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab88a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab88a-104">SYNTAX</span></span>

### <span data-ttu-id="ab88a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ab88a-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab88a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab88a-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab88a-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab88a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab88a-108">AzureRmVirtualNetworkSubnetConfig Cmdlet 會針對 Azure 虛擬網路中的子網配置 **設定** 目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ab88a-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="ab88a-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab88a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab88a-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="ab88a-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="ab88a-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="ab88a-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="ab88a-112">然後，通話 Set-AzureRmVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="ab88a-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="ab88a-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="ab88a-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ab88a-114">接著，就會呼叫 Set-AzureRmVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="ab88a-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="ab88a-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="ab88a-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="ab88a-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ab88a-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="ab88a-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ab88a-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="ab88a-118">Set-AzureRmVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ab88a-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="ab88a-119">接著會呼叫 Set-AzureRmVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="ab88a-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="ab88a-120">參數</span><span class="sxs-lookup"><span data-stu-id="ab88a-120">PARAMETERS</span></span>

### <span data-ttu-id="ab88a-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab88a-121">-AddressPrefix</span></span>
<span data-ttu-id="ab88a-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="ab88a-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="ab88a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab88a-123">-DefaultProfile</span></span>
<span data-ttu-id="ab88a-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab88a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab88a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab88a-125">-Name</span></span>
<span data-ttu-id="ab88a-126">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab88a-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="ab88a-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab88a-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ab88a-128">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="ab88a-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="ab88a-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ab88a-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ab88a-130">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="ab88a-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="ab88a-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ab88a-131">-RouteTable</span></span>
<span data-ttu-id="ab88a-132">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="ab88a-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="ab88a-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="ab88a-133">-RouteTableId</span></span>
<span data-ttu-id="ab88a-134">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab88a-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="ab88a-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab88a-135">-ServiceEndpoint</span></span>
<span data-ttu-id="ab88a-136">服務端點值</span><span class="sxs-lookup"><span data-stu-id="ab88a-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="ab88a-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab88a-137">-VirtualNetwork</span></span>
<span data-ttu-id="ab88a-138">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="ab88a-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="ab88a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab88a-139">CommonParameters</span></span>
<span data-ttu-id="ab88a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab88a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab88a-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab88a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab88a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ab88a-142">INPUTS</span></span>

### <span data-ttu-id="ab88a-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab88a-143">PSVirtualNetwork</span></span>
<span data-ttu-id="ab88a-144">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ab88a-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ab88a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ab88a-145">OUTPUTS</span></span>

### <span data-ttu-id="ab88a-146">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab88a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ab88a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ab88a-147">NOTES</span></span>

## <span data-ttu-id="ab88a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab88a-148">RELATED LINKS</span></span>

[<span data-ttu-id="ab88a-149">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab88a-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ab88a-150">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab88a-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ab88a-151">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab88a-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ab88a-152">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab88a-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


