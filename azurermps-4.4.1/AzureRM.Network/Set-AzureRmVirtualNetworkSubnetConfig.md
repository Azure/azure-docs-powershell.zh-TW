---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 179bfced7b73113899f525940114abb342e61f8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625704"
---
# <span data-ttu-id="330a5-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="330a5-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="330a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="330a5-102">SYNOPSIS</span></span>
<span data-ttu-id="330a5-103">在虛擬網路中設定子網配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="330a5-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="330a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="330a5-104">SYNTAX</span></span>

### <span data-ttu-id="330a5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="330a5-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="330a5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="330a5-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="330a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="330a5-107">DESCRIPTION</span></span>
<span data-ttu-id="330a5-108">AzureRmVirtualNetworkSubnetConfig Cmdlet 會針對 Azure 虛擬網路中的子網配置 **設定** 目標狀態。</span><span class="sxs-lookup"><span data-stu-id="330a5-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="330a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="330a5-109">EXAMPLES</span></span>

### <span data-ttu-id="330a5-110">1：修改子網的位址前置詞</span><span class="sxs-lookup"><span data-stu-id="330a5-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="330a5-111">這個範例會建立一個含有一個子網的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="330a5-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="330a5-112">然後，通話 Set-AzureRmVirtualNetworkSubnetConfig 修改子網的 AddressPrefix。</span><span class="sxs-lookup"><span data-stu-id="330a5-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="330a5-113">這只會影響虛擬網路在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="330a5-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="330a5-114">接著，就會呼叫 Set-AzureRmVirtualNetwork 來修改 Azure 中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="330a5-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="330a5-115">2：將網路安全性群組新增至子網</span><span class="sxs-lookup"><span data-stu-id="330a5-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="330a5-116">這個範例會建立一個包含只有一個子網的虛擬網路的資源群組。</span><span class="sxs-lookup"><span data-stu-id="330a5-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="330a5-117">接著，它會建立包含 RDP 流量的 allow 規則的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="330a5-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="330a5-118">Set-AzureRmVirtualNetworkSubnetConfig Cmdlet 可用來修改前端子網的記憶體內表示形式，使其指向新建立的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="330a5-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="330a5-119">接著會呼叫 Set-AzureRmVirtualNetwork Cmdlet，以將修改過的狀態寫回服務。</span><span class="sxs-lookup"><span data-stu-id="330a5-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="330a5-120">參數</span><span class="sxs-lookup"><span data-stu-id="330a5-120">PARAMETERS</span></span>

### <span data-ttu-id="330a5-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="330a5-121">-AddressPrefix</span></span>
<span data-ttu-id="330a5-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="330a5-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="330a5-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="330a5-123">-Name</span></span>
<span data-ttu-id="330a5-124">指定此 Cmdlet 所設定之子網配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="330a5-124">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="330a5-125">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="330a5-125">-NetworkSecurityGroup</span></span>
<span data-ttu-id="330a5-126">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="330a5-126">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="330a5-127">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="330a5-127">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="330a5-128">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="330a5-128">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="330a5-129">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="330a5-129">-RouteTable</span></span>
<span data-ttu-id="330a5-130">指定與網路安全群組相關聯的路由表物件。</span><span class="sxs-lookup"><span data-stu-id="330a5-130">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="330a5-131">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="330a5-131">-RouteTableId</span></span>
<span data-ttu-id="330a5-132">指定與網路安全群組相關聯之路由資料表物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="330a5-132">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="330a5-133">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="330a5-133">-ServiceEndpoint</span></span>
<span data-ttu-id="330a5-134">服務端點值</span><span class="sxs-lookup"><span data-stu-id="330a5-134">Service Endpoint Value</span></span>

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

### <span data-ttu-id="330a5-135">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="330a5-135">-VirtualNetwork</span></span>
<span data-ttu-id="330a5-136">指定包含子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="330a5-136">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="330a5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330a5-137">-DefaultProfile</span></span>
<span data-ttu-id="330a5-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="330a5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="330a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330a5-139">CommonParameters</span></span>
<span data-ttu-id="330a5-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="330a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330a5-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="330a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330a5-142">輸入</span><span class="sxs-lookup"><span data-stu-id="330a5-142">INPUTS</span></span>

### <span data-ttu-id="330a5-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="330a5-143">PSVirtualNetwork</span></span>
<span data-ttu-id="330a5-144">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="330a5-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="330a5-145">輸出</span><span class="sxs-lookup"><span data-stu-id="330a5-145">OUTPUTS</span></span>

### <span data-ttu-id="330a5-146">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="330a5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="330a5-147">筆記</span><span class="sxs-lookup"><span data-stu-id="330a5-147">NOTES</span></span>

## <span data-ttu-id="330a5-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="330a5-148">RELATED LINKS</span></span>

[<span data-ttu-id="330a5-149">附加 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="330a5-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="330a5-150">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="330a5-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="330a5-151">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="330a5-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="330a5-152">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="330a5-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


