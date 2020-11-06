---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622128"
---
# <span data-ttu-id="bb4c5-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bb4c5-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="bb4c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4c5-103">新增子網配置至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="bb4c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb4c5-104">SYNTAX</span></span>

### <span data-ttu-id="bb4c5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="bb4c5-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb4c5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb4c5-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb4c5-107">說明</span><span class="sxs-lookup"><span data-stu-id="bb4c5-107">DESCRIPTION</span></span>
<span data-ttu-id="bb4c5-108">**AzVirtualNetworkSubnetConfig** Cmdlet 會將子網配置新增至現有的 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="bb4c5-109">示例</span><span class="sxs-lookup"><span data-stu-id="bb4c5-109">EXAMPLES</span></span>

### <span data-ttu-id="bb4c5-110">1：將子網新增至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="bb4c5-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="bb4c5-111">這個範例會先建立資源群組做為要建立的資源容器。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="bb4c5-112">接著，它會建立子網設定，並使用它來建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="bb4c5-113">然後，使用 Add-AzVirtualNetworkSubnetConfig 將子網新增至虛擬網路的記憶體內表示形式。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="bb4c5-114">[Set-AzVirtualNetwork] 命令會以新的子網來更新現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="bb4c5-115">2：在要新增到現有虛擬網路的子網中新增委派</span><span class="sxs-lookup"><span data-stu-id="bb4c5-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="bb4c5-116">這個範例會先取得現有的 vnet。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="bb4c5-117">接著，它會在記憶體中建立委派物件。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="bb4c5-118">最後，它會建立一個新的子網，並將該委派新增至 vnet。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="bb4c5-119">修改後的設定就會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="bb4c5-120">參數</span><span class="sxs-lookup"><span data-stu-id="bb4c5-120">PARAMETERS</span></span>

### <span data-ttu-id="bb4c5-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bb4c5-121">-AddressPrefix</span></span>
<span data-ttu-id="bb4c5-122">指定子網配置的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb4c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4c5-123">-DefaultProfile</span></span>
<span data-ttu-id="bb4c5-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb4c5-125">委派</span><span class="sxs-lookup"><span data-stu-id="bb4c5-125">-Delegation</span></span>
<span data-ttu-id="bb4c5-126">具有在該子網上執行作業許可權的服務清單。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4c5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb4c5-127">-Name</span></span>
<span data-ttu-id="bb4c5-128">指定要新增的子網配置名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="bb4c5-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb4c5-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bb4c5-130">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="bb4c5-131">這個 Cmdlet 會將虛擬網路子網配置新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb4c5-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bb4c5-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bb4c5-133">指定網路安全性群組的 ID。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="bb4c5-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="bb4c5-134">-RouteTable</span></span>
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

### <span data-ttu-id="bb4c5-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="bb4c5-135">-RouteTableId</span></span>
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

### <span data-ttu-id="bb4c5-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb4c5-136">-ServiceEndpoint</span></span>
<span data-ttu-id="bb4c5-137">服務端點值</span><span class="sxs-lookup"><span data-stu-id="bb4c5-137">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4c5-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bb4c5-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="bb4c5-139">服務端點原則</span><span class="sxs-lookup"><span data-stu-id="bb4c5-139">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4c5-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb4c5-140">-VirtualNetwork</span></span>
<span data-ttu-id="bb4c5-141">指定要在其中新增子網配置的 **VirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="bb4c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4c5-142">CommonParameters</span></span>
<span data-ttu-id="bb4c5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4c5-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb4c5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4c5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bb4c5-145">INPUTS</span></span>

### <span data-ttu-id="bb4c5-146">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb4c5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="bb4c5-147">System.object</span><span class="sxs-lookup"><span data-stu-id="bb4c5-147">System.String</span></span>

### <span data-ttu-id="bb4c5-148">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb4c5-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="bb4c5-149">PSRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb4c5-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="bb4c5-150">System.object []</span><span class="sxs-lookup"><span data-stu-id="bb4c5-150">System.String[]</span></span>

### <span data-ttu-id="bb4c5-151">PSServiceEndpointPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bb4c5-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="bb4c5-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="bb4c5-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="bb4c5-153">輸出</span><span class="sxs-lookup"><span data-stu-id="bb4c5-153">OUTPUTS</span></span>

### <span data-ttu-id="bb4c5-154">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb4c5-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bb4c5-155">筆記</span><span class="sxs-lookup"><span data-stu-id="bb4c5-155">NOTES</span></span>

## <span data-ttu-id="bb4c5-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb4c5-156">RELATED LINKS</span></span>

[<span data-ttu-id="bb4c5-157">AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bb4c5-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bb4c5-158">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bb4c5-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bb4c5-159">移除-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bb4c5-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bb4c5-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bb4c5-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
