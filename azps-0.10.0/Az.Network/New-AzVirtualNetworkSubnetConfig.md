---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794225"
---
# <span data-ttu-id="d7d0f-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7d0f-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d7d0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d0f-103">建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="d7d0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7d0f-104">SYNTAX</span></span>

### <span data-ttu-id="d7d0f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d7d0f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7d0f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7d0f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7d0f-107">說明</span><span class="sxs-lookup"><span data-stu-id="d7d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="d7d0f-108">**新的-AzVirtualNetworkSubnetConfig** Cmdlet 會建立虛擬網路子網配置。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="d7d0f-109">示例</span><span class="sxs-lookup"><span data-stu-id="d7d0f-109">EXAMPLES</span></span>

### <span data-ttu-id="d7d0f-110">1：使用兩個子網和網路安全群組建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="d7d0f-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d7d0f-111">這個範例會使用 New-AzVirtualSubnetConfig Cmdlet 建立兩個新的子網設定，然後使用它們來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="d7d0f-112">New-AzVirtualSubnetConfig 範本只會建立子網的記憶體內部表示。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="d7d0f-113">在這個範例中，frontendSubnet 有 CIDR 10.0.1.0/24，並參照允許 RDP 存取的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="d7d0f-114">BackendSubnet 有 CIDR 10.0.2.0/24，且參照相同的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="d7d0f-115">參數</span><span class="sxs-lookup"><span data-stu-id="d7d0f-115">PARAMETERS</span></span>

### <span data-ttu-id="d7d0f-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d7d0f-116">-AddressPrefix</span></span>
<span data-ttu-id="d7d0f-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="d7d0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d0f-118">-DefaultProfile</span></span>
<span data-ttu-id="d7d0f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d0f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7d0f-120">-Name</span></span>
<span data-ttu-id="d7d0f-121">指定要建立的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="d7d0f-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7d0f-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d7d0f-123">指定 NetworkSecurityGroup 物件。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="d7d0f-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d7d0f-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d7d0f-125">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d7d0f-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d7d0f-126">-RouteTable</span></span>
<span data-ttu-id="d7d0f-127">指定與子網配置相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d7d0f-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="d7d0f-128">-RouteTableId</span></span>
<span data-ttu-id="d7d0f-129">指定與子網配置相關聯之路由資料表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d7d0f-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7d0f-130">-ServiceEndpoint</span></span>
<span data-ttu-id="d7d0f-131">服務端點值</span><span class="sxs-lookup"><span data-stu-id="d7d0f-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="d7d0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d0f-132">CommonParameters</span></span>
<span data-ttu-id="d7d0f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d0f-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7d0f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d0f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d7d0f-135">INPUTS</span></span>

## <span data-ttu-id="d7d0f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d7d0f-136">OUTPUTS</span></span>

### <span data-ttu-id="d7d0f-137">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d7d0f-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d7d0f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d7d0f-138">NOTES</span></span>

## <span data-ttu-id="d7d0f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7d0f-139">RELATED LINKS</span></span>

[<span data-ttu-id="d7d0f-140">附加 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7d0f-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7d0f-141">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7d0f-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7d0f-142">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7d0f-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d7d0f-143">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d7d0f-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


