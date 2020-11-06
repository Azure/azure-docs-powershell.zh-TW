---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447856"
---
# <span data-ttu-id="e1f2b-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="e1f2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f2b-103">建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1f2b-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f2b-106">**新的-AzureRmVmss** Cmdlet 會在 Azure 中建立 (VMSS) 的虛擬電腦縮放比例集。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="e1f2b-107">這個 Cmdlet 會採用 **VirtualMachineScaleSet** 物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="e1f2b-108">示例</span><span class="sxs-lookup"><span data-stu-id="e1f2b-108">EXAMPLES</span></span>

### <span data-ttu-id="e1f2b-109">範例1：建立 VMSS</span><span class="sxs-lookup"><span data-stu-id="e1f2b-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="e1f2b-110">下列複雜範例會建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="e1f2b-111">第一個命令會建立具有指定名稱和位置的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="e1f2b-112">第二個命令使用 **新的 AzureRmStorageAccount** Cmdlet 來建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="e1f2b-113">然後，第三個命令會使用 **AzureRmStorageAccount** Cmdlet 來取得第二個命令中建立的儲存空間帳戶，並將結果儲存在 $STOAccount 變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="e1f2b-114">第五個命令使用 **新的 AzureRmVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並將結果儲存在名為 $SubNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="e1f2b-115">第六個命令使用 **新的 AzureRmVirtualNetwork** Cmdlet 來建立虛擬網路，並將結果儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="e1f2b-116">第七個命令使用 **AzureRmVirtualNetwork** ，以取得在第6個命令中建立的虛擬網路相關資訊，並將資訊儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="e1f2b-117">第八和第九個命令使用 **新的 AzureRmPublicIpAddress** 和 **AzureRmPublicIpAddress** 來建立並從該公用 IP 位址中取得資訊。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="e1f2b-118">這些命令會將資訊儲存在名為 $PubIP 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="e1f2b-119">第十個命令使用 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並將結果儲存在名為 $Frontend 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="e1f2b-120">第十一個命令使用 **New-AzureRmLoadBalancerBackendAddressPoolConfig** 建立後端位址集區配置，並將結果儲存在名為 $BackendAddressPool 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="e1f2b-121">第十二個命令使用 **New-AzureRmLoadBalancerProbeConfig** 來建立探測器，並將探測器資訊儲存在名為 $Probe 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="e1f2b-122">第13個命令使用 **AzureRmLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器入站網路位址轉譯 (NAT) 池設定。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="e1f2b-123">第十四個命令使用 **New-AzureRmLoadBalancerRuleConfig** 來建立負載平衡器規則設定，並將結果儲存在名為 $LBRule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="e1f2b-124">第15個命令使用 **AzureRmLoadBalancer** Cmdlet 來建立負載平衡器，並將結果儲存在名為 $ActualLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="e1f2b-125">第十六個命令使用 **AzureRmLoadBalancer** ，以取得在第15個命令中建立的負載平衡器相關資訊，並將資訊儲存在名為 $ExpectedLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="e1f2b-126">Seventeenth 命令會使用 **新的-AzureRmVmssIPConfig** Cmdlet 來建立 VMSS IP 設定，並將資訊儲存在名為 $IPCfg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="e1f2b-127">第十八個命令使用 **AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e1f2b-128">十九命令會使用 **新的-AzureRmVmss** Cmdlet 來建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="e1f2b-129">參數</span><span class="sxs-lookup"><span data-stu-id="e1f2b-129">PARAMETERS</span></span>

### <span data-ttu-id="e1f2b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f2b-130">-ResourceGroupName</span></span>
<span data-ttu-id="e1f2b-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f2b-132">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e1f2b-132">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e1f2b-133">指定包含此 Cmdlet 所建立之 VMSS 之屬性的 **VirtualMachineScaleSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-133">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f2b-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e1f2b-134">-VMScaleSetName</span></span>
<span data-ttu-id="e1f2b-135">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-135">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f2b-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e1f2b-136">-Confirm</span></span>
<span data-ttu-id="e1f2b-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f2b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f2b-138">-WhatIf</span></span>
<span data-ttu-id="e1f2b-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e1f2b-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f2b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f2b-141">CommonParameters</span></span>
<span data-ttu-id="e1f2b-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f2b-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f2b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e1f2b-144">INPUTS</span></span>

### <span data-ttu-id="e1f2b-145">所有</span><span class="sxs-lookup"><span data-stu-id="e1f2b-145">None</span></span>
<span data-ttu-id="e1f2b-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1f2b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e1f2b-147">OUTPUTS</span></span>

### <span data-ttu-id="e1f2b-148">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e1f2b-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e1f2b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e1f2b-149">NOTES</span></span>

## <span data-ttu-id="e1f2b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1f2b-150">RELATED LINKS</span></span>

[<span data-ttu-id="e1f2b-151">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-152">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-153">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-155">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-156">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e1f2b-157">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e1f2b-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


