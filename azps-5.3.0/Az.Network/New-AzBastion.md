---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: e2e2feacaefb0ce29c77263c0b733f503b8e9a74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286940"
---
# <span data-ttu-id="daabb-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="daabb-101">New-AzBastion</span></span>

## <span data-ttu-id="daabb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daabb-102">SYNOPSIS</span></span>
<span data-ttu-id="daabb-103">建立堡壘資源。</span><span class="sxs-lookup"><span data-stu-id="daabb-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="daabb-104">句法</span><span class="sxs-lookup"><span data-stu-id="daabb-104">SYNTAX</span></span>

### <span data-ttu-id="daabb-105">ByPublicIpAddressByVirtualNetwork (預設) </span><span class="sxs-lookup"><span data-stu-id="daabb-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="daabb-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="daabb-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="daabb-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="daabb-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="daabb-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daabb-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="daabb-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="daabb-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daabb-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="daabb-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daabb-114">說明</span><span class="sxs-lookup"><span data-stu-id="daabb-114">DESCRIPTION</span></span>
<span data-ttu-id="daabb-115">建立堡壘資源。這將需要公用 Ip 位址與 VirtualNetwork。</span><span class="sxs-lookup"><span data-stu-id="daabb-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="daabb-116">此 VirtualNetwork 中必須有一個名為 AzureBastionSubnet 的子網。必須使用 Sku 標準建立 Pubic Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="daabb-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="daabb-117">示例</span><span class="sxs-lookup"><span data-stu-id="daabb-117">EXAMPLES</span></span>

### <span data-ttu-id="daabb-118">範例1</span><span class="sxs-lookup"><span data-stu-id="daabb-118">Example 1</span></span>
```powershell
$subnetName = "AzureBastionSubnet"
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name "TestVnet" -ResourceGroupName "BastionPowershellTest" -Location "westeurope" -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$publicip = New-AzPublicIpAddress -ResourceGroupName "BastionPowershellTest" -name "Test-Ip" -location "westeurope" -AllocationMethod Dynamic -Sku Standard
$bastion = New-AzBastion -ResourceGroupName "BastionPowershellTest" â€“Name "test-Bastion2" -PublicIpAddress $publicip -VirtualNetwork $vnet

IpConfigurations     : {IpConf}
DnsName              : bst-a9ca868f-ddab-4a50-9f45-a443ea8a0187.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic",
                           "Name": "IpConf",
                           "Etag": "W/\"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2/bastionHostIpConfigurations/IpConf"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : test-Bastion2
Etag                 : W/"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2

This example creates a bastion attached to virtual network "vnet" in the same resource group as the bastion.
There must be a subnet with name AzureBastionSubnet in this vnet.
The Ip Address must be created with Sku Standard.
```

### <span data-ttu-id="daabb-119">範例2</span><span class="sxs-lookup"><span data-stu-id="daabb-119">Example 2</span></span>
```powershell
$vnet = Get-AzVirtualNetwork -ResourceGroupName "BastionPowershellTest" -Name "testVnet2"
Add-AzVirtualNetworkSubnetConfig -Name "AzureBastionSubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.0.0/24"
$vnet| Set-AzVirtualNetwork
New-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2" -PublicIpAddressRgName "BastionPowershellTest" -PublicIpAddressName "testIp2" -VirtualNetworkRgName "BastionPowershellTest" -VirtualNetworkName "testVnet2"

IpConfigurations     : {IpConf}
DnsName              : bst-53757658-c4fd-4908-b1a7-0849e555d489.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7460e5f6-ad41-438b-a595-a63346ed8f16\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/testVnet2/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/testIp2"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion2
Etag                 : W/"7460e5f6-ad41-438b-a595-a63346ed8f16"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2
```

## <span data-ttu-id="daabb-120">參數</span><span class="sxs-lookup"><span data-stu-id="daabb-120">PARAMETERS</span></span>

### <span data-ttu-id="daabb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daabb-121">-AsJob</span></span>
<span data-ttu-id="daabb-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="daabb-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="daabb-123">-Confirm</span></span>
<span data-ttu-id="daabb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="daabb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daabb-125">-DefaultProfile</span></span>
<span data-ttu-id="daabb-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="daabb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="daabb-127">-Name</span></span>
<span data-ttu-id="daabb-128">堡壘資源名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-128">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="daabb-129">-PublicIpAddress</span></span>
<span data-ttu-id="daabb-130">堡壘的公用 IP 位址物件。</span><span class="sxs-lookup"><span data-stu-id="daabb-130">The public IP address object for bastion.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressByVirtualNetworkId
Aliases: PublicIpAddressObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="daabb-131">-PublicIpAddressId</span></span>
<span data-ttu-id="daabb-132">適用于堡壘的公用 Ip 位址 Azure 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="daabb-132">The public Ip address Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkId
Aliases: PublicIpAddressResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="daabb-133">-PublicIpAddressName</span></span>
<span data-ttu-id="daabb-134">堡壘的公用 Ip 位址資源名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-134">The public Ip address resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="daabb-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="daabb-136">堡壘的公用 Ip 位址資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-136">The public Ip address resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: PublicIpAddressResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daabb-137">-ResourceGroupName</span></span>
<span data-ttu-id="daabb-138">您需要建立堡壘之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-138">The resource group name where you need to create bastion.</span></span>

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

### <span data-ttu-id="daabb-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="daabb-139">-Tag</span></span>
<span data-ttu-id="daabb-140">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="daabb-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="daabb-141">-VirtualNetwork</span></span>
<span data-ttu-id="daabb-142">適用于堡壘的虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="daabb-142">The virtual network object for bastion.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork
Aliases: VirtualNetworkObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="daabb-143">-VirtualNetworkId</span></span>
<span data-ttu-id="daabb-144">適用于堡壘的虛擬網路 Azure 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="daabb-144">The virtual network Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkId, ByPublicIpAddressIdByVirtualNetworkId, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: VirtualNetworkResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="daabb-145">-VirtualNetworkName</span></span>
<span data-ttu-id="daabb-146">適用于堡壘的虛擬網路資源名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-146">The virtual network resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="daabb-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="daabb-148">適用于堡壘的虛擬網路資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="daabb-148">The virtual network resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases: VirtualNetworkResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daabb-149">-WhatIf</span></span>
<span data-ttu-id="daabb-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="daabb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daabb-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daabb-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daabb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daabb-152">CommonParameters</span></span>
<span data-ttu-id="daabb-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daabb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daabb-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="daabb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daabb-155">輸入</span><span class="sxs-lookup"><span data-stu-id="daabb-155">INPUTS</span></span>

### <span data-ttu-id="daabb-156">所有</span><span class="sxs-lookup"><span data-stu-id="daabb-156">None</span></span>

## <span data-ttu-id="daabb-157">輸出</span><span class="sxs-lookup"><span data-stu-id="daabb-157">OUTPUTS</span></span>

### <span data-ttu-id="daabb-158">PSBastion 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="daabb-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="daabb-159">筆記</span><span class="sxs-lookup"><span data-stu-id="daabb-159">NOTES</span></span>

## <span data-ttu-id="daabb-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="daabb-160">RELATED LINKS</span></span>
[<span data-ttu-id="daabb-161">AzBastion</span><span class="sxs-lookup"><span data-stu-id="daabb-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="daabb-162">移除-AzBastion</span><span class="sxs-lookup"><span data-stu-id="daabb-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)