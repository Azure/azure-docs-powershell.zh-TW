---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 01116d3a2ad2636776fe29a0e36e34568624f2c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794496"
---
# <span data-ttu-id="48198-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="48198-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="48198-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48198-102">SYNOPSIS</span></span>
<span data-ttu-id="48198-103">新增子網配置至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="48198-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="48198-104">句法</span><span class="sxs-lookup"><span data-stu-id="48198-104">SYNTAX</span></span>

### <span data-ttu-id="48198-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="48198-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48198-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="48198-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48198-107">說明</span><span class="sxs-lookup"><span data-stu-id="48198-107">DESCRIPTION</span></span>
<span data-ttu-id="48198-108">**AzVirtualNetworkSubnetConfig** Cmdlet 會將子網配置新增至現有的 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="48198-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="48198-109">示例</span><span class="sxs-lookup"><span data-stu-id="48198-109">EXAMPLES</span></span>

### <span data-ttu-id="48198-110">1：將子網新增至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="48198-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="48198-111">這個範例會先建立資源群組做為要建立的資源容器。</span><span class="sxs-lookup"><span data-stu-id="48198-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="48198-112">接著，它會建立子網設定，並使用它來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="48198-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="48198-113">然後，使用 Add-AzVirtualNetworkSubnetConfig 將子網新增至虛擬網路的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="48198-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="48198-114">[Set-AzVirtualNetwork] 命令會以新的子網來更新現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="48198-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="48198-115">參數</span><span class="sxs-lookup"><span data-stu-id="48198-115">PARAMETERS</span></span>

### <span data-ttu-id="48198-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="48198-116">-AddressPrefix</span></span>
<span data-ttu-id="48198-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="48198-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="48198-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48198-118">-DefaultProfile</span></span>
<span data-ttu-id="48198-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48198-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48198-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="48198-120">-Name</span></span>
<span data-ttu-id="48198-121">指定要新增的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="48198-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="48198-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48198-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="48198-123">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="48198-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="48198-124">這個 Cmdlet 會將虛擬網路子網配置新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="48198-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="48198-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="48198-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="48198-126">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="48198-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="48198-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="48198-127">-RouteTable</span></span>
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

### <span data-ttu-id="48198-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="48198-128">-RouteTableId</span></span>
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

### <span data-ttu-id="48198-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="48198-129">-ServiceEndpoint</span></span>
<span data-ttu-id="48198-130">服務端點值</span><span class="sxs-lookup"><span data-stu-id="48198-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="48198-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48198-131">-VirtualNetwork</span></span>
<span data-ttu-id="48198-132">指定要在其中新增子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="48198-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="48198-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48198-133">CommonParameters</span></span>
<span data-ttu-id="48198-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48198-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48198-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48198-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48198-136">輸入</span><span class="sxs-lookup"><span data-stu-id="48198-136">INPUTS</span></span>

### <span data-ttu-id="48198-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48198-137">PSVirtualNetwork</span></span>
<span data-ttu-id="48198-138">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="48198-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="48198-139">輸出</span><span class="sxs-lookup"><span data-stu-id="48198-139">OUTPUTS</span></span>

### <span data-ttu-id="48198-140">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="48198-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="48198-141">筆記</span><span class="sxs-lookup"><span data-stu-id="48198-141">NOTES</span></span>

## <span data-ttu-id="48198-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="48198-142">RELATED LINKS</span></span>

[<span data-ttu-id="48198-143">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="48198-143">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="48198-144">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="48198-144">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="48198-145">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="48198-145">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="48198-146">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="48198-146">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


