---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: f37f6fe6211ab05b94249b924eb76c4b98d05082
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801953"
---
# <span data-ttu-id="e8f05-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8f05-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e8f05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8f05-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f05-103">設定 Azure network 介面 IP 配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="e8f05-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f05-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8f05-104">SYNTAX</span></span>

### <span data-ttu-id="e8f05-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e8f05-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8f05-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f05-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f05-107">說明</span><span class="sxs-lookup"><span data-stu-id="e8f05-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f05-108">**AzureRmNetworkInterfaceIpConfig** Cmdlet 會設定 Azure NETWORK 介面 IP 配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="e8f05-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="e8f05-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8f05-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f05-110">1：變更 IP 配置的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="e8f05-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="e8f05-111">前兩個命令會取得名為 myvnet 的虛擬網路，以及稱為 mysubnet 的子網，並將它儲存在 $vnet 與 $subnet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e8f05-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="e8f05-112">第三個命令會取得與需要更新之 IP 配置相關聯的網路介面 nic1。</span><span class="sxs-lookup"><span data-stu-id="e8f05-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="e8f05-113">第三個命令會將主要 IP 配置 ipconfig1 的私人 IP 位址設定為10.0.0.11。</span><span class="sxs-lookup"><span data-stu-id="e8f05-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="e8f05-114">最後，最後一個命令會更新網路介面，以確保已成功進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8f05-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="e8f05-115">2：將 IP 設定與 application security groupp 建立關聯</span><span class="sxs-lookup"><span data-stu-id="e8f05-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="e8f05-116">在這個範例中，變數 $asg 包含對應用程式安全性群組的參照。</span><span class="sxs-lookup"><span data-stu-id="e8f05-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="e8f05-117">第四個命令會取得與需要更新之 IP 配置相關聯的網路介面 nic1。</span><span class="sxs-lookup"><span data-stu-id="e8f05-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="e8f05-118">Set-AzureRmNetworkInterfaceIpConfig 將主要 IP 配置 ipconfig1 的私人 IP 位址設定為10.0.0.11，並建立與已檢索的應用程式安全性群組的關聯。</span><span class="sxs-lookup"><span data-stu-id="e8f05-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="e8f05-119">最後，最後一個命令會更新網路介面，以確保已成功進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8f05-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="e8f05-120">參數</span><span class="sxs-lookup"><span data-stu-id="e8f05-120">PARAMETERS</span></span>

### <span data-ttu-id="e8f05-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8f05-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="e8f05-122">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e8f05-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="e8f05-124">指定此網路介面 IP 配置所屬之應用程式閘道後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8f05-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="e8f05-126">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e8f05-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="e8f05-128">指定此網路介面 IP 配置所屬之應用程式安全性群組參考的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f05-129">-DefaultProfile</span></span>
<span data-ttu-id="e8f05-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8f05-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f05-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8f05-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="e8f05-132">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e8f05-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="e8f05-134">指定此網路介面 IP 配置所屬之負載等化器後端位址集區參照的集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e8f05-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="e8f05-136">指定一個負載平衡器入站網路位址的集合， (NAT) 規則參照，此網路介面 IP 設定屬於這個配置。</span><span class="sxs-lookup"><span data-stu-id="e8f05-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="e8f05-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="e8f05-138">指定此網路介面 IP 配置所屬的負載等化器入站 NAT 規則參照集合。</span><span class="sxs-lookup"><span data-stu-id="e8f05-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8f05-139">-Name</span></span>
<span data-ttu-id="e8f05-140">指定此 Cmdlet 設定的網路 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f05-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="e8f05-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e8f05-141">-NetworkInterface</span></span>
<span data-ttu-id="e8f05-142">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8f05-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="e8f05-143">這個 Cmdlet 會將網路介面 IP 設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="e8f05-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-144">-主要</span><span class="sxs-lookup"><span data-stu-id="e8f05-144">-Primary</span></span>
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

### <span data-ttu-id="e8f05-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e8f05-145">-PrivateIpAddress</span></span>
<span data-ttu-id="e8f05-146">指定網路介面 IP 配置的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e8f05-146">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e8f05-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e8f05-148">指定網路介面 IP 配置的 IP 位址版本。</span><span class="sxs-lookup"><span data-stu-id="e8f05-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="e8f05-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e8f05-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8f05-150">Ipv4/ipv6</span><span class="sxs-lookup"><span data-stu-id="e8f05-150">IPv4</span></span>
- <span data-ttu-id="e8f05-151">Ipv4</span><span class="sxs-lookup"><span data-stu-id="e8f05-151">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e8f05-152">-PublicIpAddress</span></span>
<span data-ttu-id="e8f05-153">指定 **PublicIPAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8f05-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="e8f05-154">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="e8f05-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e8f05-155">-PublicIpAddressId</span></span>
<span data-ttu-id="e8f05-156">這個 Cmdlet 會建立對公用 IP 位址的參照，以與此網路介面 IP 設定建立關聯。</span><span class="sxs-lookup"><span data-stu-id="e8f05-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-157">-子網</span><span class="sxs-lookup"><span data-stu-id="e8f05-157">-Subnet</span></span>
<span data-ttu-id="e8f05-158">指定 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8f05-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="e8f05-159">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e8f05-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8f05-160">-SubnetId</span></span>
<span data-ttu-id="e8f05-161">這個 Cmdlet 會建立一個子網參照，在其中建立此網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="e8f05-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f05-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f05-162">CommonParameters</span></span>
<span data-ttu-id="e8f05-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8f05-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f05-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8f05-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f05-165">輸入</span><span class="sxs-lookup"><span data-stu-id="e8f05-165">INPUTS</span></span>

### <span data-ttu-id="e8f05-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e8f05-166">PSNetworkInterface</span></span>
<span data-ttu-id="e8f05-167">形參 "NetworkInterface" 接受管線中 "PSNetworkInterface" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e8f05-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="e8f05-168">輸出</span><span class="sxs-lookup"><span data-stu-id="e8f05-168">OUTPUTS</span></span>

### <span data-ttu-id="e8f05-169">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8f05-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e8f05-170">筆記</span><span class="sxs-lookup"><span data-stu-id="e8f05-170">NOTES</span></span>
* <span data-ttu-id="e8f05-171">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="e8f05-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e8f05-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8f05-172">RELATED LINKS</span></span>

[<span data-ttu-id="e8f05-173">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8f05-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e8f05-174">AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8f05-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e8f05-175">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8f05-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e8f05-176">移除-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8f05-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


