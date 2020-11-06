---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 0987823d2658778266f861a5115962d6cf8c4830
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451439"
---
# <span data-ttu-id="b0489-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0489-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b0489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0489-102">SYNOPSIS</span></span>
<span data-ttu-id="b0489-103">新增子網配置至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b0489-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0489-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0489-104">SYNTAX</span></span>

### <span data-ttu-id="b0489-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b0489-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0489-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0489-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0489-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0489-107">DESCRIPTION</span></span>
<span data-ttu-id="b0489-108">**AzureRmVirtualNetworkSubnetConfig** Cmdlet 會將子網配置新增至現有的 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b0489-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="b0489-109">示例</span><span class="sxs-lookup"><span data-stu-id="b0489-109">EXAMPLES</span></span>

### <span data-ttu-id="b0489-110">1：將子網新增至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="b0489-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="b0489-111">這個範例會先建立資源群組做為要建立的資源容器。</span><span class="sxs-lookup"><span data-stu-id="b0489-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="b0489-112">接著，它會建立子網設定，並使用它來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b0489-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="b0489-113">然後，使用 Add-AzureRmVirtualNetworkSubnetConfig 將子網新增至虛擬網路的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="b0489-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b0489-114">[Set-AzureRmVirtualNetwork] 命令會以新的子網來更新現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b0489-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="b0489-115">參數</span><span class="sxs-lookup"><span data-stu-id="b0489-115">PARAMETERS</span></span>

### <span data-ttu-id="b0489-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0489-116">-AddressPrefix</span></span>
<span data-ttu-id="b0489-117">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="b0489-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="b0489-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0489-118">-DefaultProfile</span></span>
<span data-ttu-id="b0489-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0489-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0489-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0489-120">-Name</span></span>
<span data-ttu-id="b0489-121">指定要新增的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b0489-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="b0489-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b0489-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b0489-123">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0489-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b0489-124">這個 Cmdlet 會將虛擬網路子網配置新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="b0489-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0489-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b0489-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b0489-126">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="b0489-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b0489-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b0489-127">-RouteTable</span></span>
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

### <span data-ttu-id="b0489-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b0489-128">-RouteTableId</span></span>
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

### <span data-ttu-id="b0489-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0489-129">-ServiceEndpoint</span></span>
<span data-ttu-id="b0489-130">服務端點值</span><span class="sxs-lookup"><span data-stu-id="b0489-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="b0489-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0489-131">-VirtualNetwork</span></span>
<span data-ttu-id="b0489-132">指定要在其中新增子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0489-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="b0489-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0489-133">CommonParameters</span></span>
<span data-ttu-id="b0489-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0489-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0489-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0489-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0489-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b0489-136">INPUTS</span></span>

### <span data-ttu-id="b0489-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0489-137">PSVirtualNetwork</span></span>
<span data-ttu-id="b0489-138">形參 "VirtualNetwork" 接受管線中 "PSVirtualNetwork" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b0489-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="b0489-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b0489-139">OUTPUTS</span></span>

### <span data-ttu-id="b0489-140">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b0489-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b0489-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b0489-141">NOTES</span></span>

## <span data-ttu-id="b0489-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0489-142">RELATED LINKS</span></span>

[<span data-ttu-id="b0489-143">AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0489-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0489-144">新-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0489-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0489-145">移除-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0489-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0489-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0489-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


