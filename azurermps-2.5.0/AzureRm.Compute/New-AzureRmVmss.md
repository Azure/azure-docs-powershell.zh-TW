---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801770"
---
# <span data-ttu-id="947b9-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="947b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="947b9-102">SYNOPSIS</span></span>
<span data-ttu-id="947b9-103">建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="947b9-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="947b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="947b9-104">SYNTAX</span></span>

### <span data-ttu-id="947b9-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="947b9-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947b9-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="947b9-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="947b9-107">DESCRIPTION</span></span>
<span data-ttu-id="947b9-108">**新的-AzureRmVmss** Cmdlet 會在 Azure 中建立 (VMSS) 的虛擬電腦縮放比例集。</span><span class="sxs-lookup"><span data-stu-id="947b9-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="947b9-109">這個 Cmdlet 會採用 **VirtualMachineScaleSet** 物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="947b9-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="947b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="947b9-110">EXAMPLES</span></span>

### <span data-ttu-id="947b9-111">範例1：建立 VMSS</span><span class="sxs-lookup"><span data-stu-id="947b9-111">Example 1: Create a VMSS</span></span>
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

<span data-ttu-id="947b9-112">下列複雜範例會建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="947b9-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="947b9-113">第一個命令會建立具有指定名稱和位置的資源群組。</span><span class="sxs-lookup"><span data-stu-id="947b9-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="947b9-114">第二個命令使用 **新的 AzureRmStorageAccount** Cmdlet 來建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="947b9-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="947b9-115">然後，第三個命令會使用 **AzureRmStorageAccount** Cmdlet 來取得第二個命令中建立的儲存空間帳戶，並將結果儲存在 $STOAccount 變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="947b9-116">第五個命令使用 **新的 AzureRmVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並將結果儲存在名為 $SubNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="947b9-117">第六個命令使用 **新的 AzureRmVirtualNetwork** Cmdlet 來建立虛擬網路，並將結果儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="947b9-118">第七個命令使用 **AzureRmVirtualNetwork** ，以取得在第6個命令中建立的虛擬網路相關資訊，並將資訊儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="947b9-119">第八和第九個命令使用 **新的 AzureRmPublicIpAddress** 和 **AzureRmPublicIpAddress** 來建立並從該公用 IP 位址中取得資訊。</span><span class="sxs-lookup"><span data-stu-id="947b9-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="947b9-120">這些命令會將資訊儲存在名為 $PubIP 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="947b9-121">第十個命令使用 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並將結果儲存在名為 $Frontend 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="947b9-122">第十一個命令使用 **New-AzureRmLoadBalancerBackendAddressPoolConfig** 建立後端位址集區配置，並將結果儲存在名為 $BackendAddressPool 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="947b9-123">第十二個命令使用 **New-AzureRmLoadBalancerProbeConfig** 來建立探測器，並將探測器資訊儲存在名為 $Probe 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="947b9-124">第13個命令使用 **AzureRmLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器入站網路位址轉譯 (NAT) 池設定。</span><span class="sxs-lookup"><span data-stu-id="947b9-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="947b9-125">第十四個命令使用 **New-AzureRmLoadBalancerRuleConfig** 來建立負載平衡器規則設定，並將結果儲存在名為 $LBRule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="947b9-126">第15個命令使用 **AzureRmLoadBalancer** Cmdlet 來建立負載平衡器，並將結果儲存在名為 $ActualLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="947b9-127">第十六個命令使用 **AzureRmLoadBalancer** ，以取得在第15個命令中建立的負載平衡器相關資訊，並將資訊儲存在名為 $ExpectedLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="947b9-128">Seventeenth 命令會使用 **新的-AzureRmVmssIPConfig** Cmdlet 來建立 VMSS IP 設定，並將資訊儲存在名為 $IPCfg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="947b9-129">第十八個命令使用 **AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="947b9-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="947b9-130">十九命令會使用 **新的-AzureRmVmss** Cmdlet 來建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="947b9-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="947b9-131">參數</span><span class="sxs-lookup"><span data-stu-id="947b9-131">PARAMETERS</span></span>

### <span data-ttu-id="947b9-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="947b9-132">-AllocationMethod</span></span>
<span data-ttu-id="947b9-133">縮放集的公用 IP 位址 (靜態或動態) 的配置方法。</span><span class="sxs-lookup"><span data-stu-id="947b9-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="947b9-134">如果未提供任何值，則分配將是靜態的。</span><span class="sxs-lookup"><span data-stu-id="947b9-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="947b9-135">-AsJob</span></span>
<span data-ttu-id="947b9-136">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="947b9-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="947b9-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="947b9-137">-BackendPoolName</span></span>
<span data-ttu-id="947b9-138">要在此比例集的負載平衡器中使用的後端位址集區名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="947b9-139">如果未提供任何值，則會建立新的後端池，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="947b9-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="947b9-140">-BackendPort</span></span>
<span data-ttu-id="947b9-141">[縮放設定] 負載平衡器所使用的後端埠號，可與小數位集中的 Vm 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="947b9-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="947b9-142">如果未指定任何值，則會將埠3389和5985用於 Windows VM，而埠22將用於 Linux Vm。</span><span class="sxs-lookup"><span data-stu-id="947b9-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-143">-認證</span><span class="sxs-lookup"><span data-stu-id="947b9-143">-Credential</span></span>
<span data-ttu-id="947b9-144">系統管理員認證 (此規模集中之 Vm 的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947b9-145">-DefaultProfile</span></span>
<span data-ttu-id="947b9-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="947b9-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="947b9-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="947b9-147">-DomainNameLabel</span></span>
<span data-ttu-id="947b9-148">此比例集之公用 Fully-Qualified 功能變數名稱的功能變數名稱標籤 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="947b9-149">這是功能變數名稱的第一個元件，會自動指派給比例集。</span><span class="sxs-lookup"><span data-stu-id="947b9-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="947b9-150">自動指派的功能變數名稱使用 [表單 (] <DomainNameLabel> 。 <Location>cloudapp.azure.com [) ]。</span><span class="sxs-lookup"><span data-stu-id="947b9-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="947b9-151">如果未提供任何值，預設的網功能變數名稱稱標籤將會是 and 的串聯 <ScaleSetName> <ResourceGroupName> 。</span><span class="sxs-lookup"><span data-stu-id="947b9-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="947b9-152">-FrontendPoolName</span></span>
<span data-ttu-id="947b9-153">要在縮放集負載平衡器中使用之前端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="947b9-154">如果未提供任何值，則會建立新的前端位址集區，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="947b9-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="947b9-155">-ImageName</span></span>
<span data-ttu-id="947b9-156">此規模集中之 Vm 的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="947b9-157">如果未提供任何值，就會使用 [Windows Server 2016 DataCenter] 影像。</span><span class="sxs-lookup"><span data-stu-id="947b9-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="947b9-158">-InstanceCount</span></span>
<span data-ttu-id="947b9-159">刻度集中的 VM 影像數目。</span><span class="sxs-lookup"><span data-stu-id="947b9-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="947b9-160">如果未提供任何值，則會建立2個實例。</span><span class="sxs-lookup"><span data-stu-id="947b9-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="947b9-161">-LoadBalancerName</span></span>
<span data-ttu-id="947b9-162">要與此比例集搭配使用的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="947b9-163">如果沒有指定任何值，就會建立新的負載平衡器，使用與縮放設定相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-164">-位置</span><span class="sxs-lookup"><span data-stu-id="947b9-164">-Location</span></span>
<span data-ttu-id="947b9-165">將建立此縮放集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="947b9-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="947b9-166">如果未指定任何值，則會從參數中參照的其他資源位置推斷位置。</span><span class="sxs-lookup"><span data-stu-id="947b9-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="947b9-167">-NatBackendPort</span></span>
<span data-ttu-id="947b9-168">入站網路位址轉譯的後端埠。</span><span class="sxs-lookup"><span data-stu-id="947b9-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="947b9-169">-PublicIpAddressName</span></span>
<span data-ttu-id="947b9-170">要與此比例集搭配使用之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="947b9-171">如果未提供任何值，就會建立新的與縮放集同名的公用 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="947b9-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947b9-172">-ResourceGroupName</span></span>
<span data-ttu-id="947b9-173">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="947b9-174">如果未指定任何值，則會使用與縮放集相同的名稱建立新的 ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="947b9-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="947b9-175">-SecurityGroupName</span></span>
<span data-ttu-id="947b9-176">要套用至此比例集的網路安全性群組名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="947b9-177">如果未提供任何值，則會建立與縮放集名稱相同的預設網路安全性群組，並將其套用至比例集。</span><span class="sxs-lookup"><span data-stu-id="947b9-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="947b9-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="947b9-179">此 ScaleSet 將使用之子網的位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="947b9-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="947b9-180">如果未提供任何值，則會套用預設的子網設定 (192.168.1.0/24) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="947b9-181">-SubnetName</span></span>
<span data-ttu-id="947b9-182">要與此比例集搭配使用的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="947b9-183">如果沒有提供任何值，就會建立新的子網，其名稱與縮放設定相同。</span><span class="sxs-lookup"><span data-stu-id="947b9-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="947b9-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="947b9-185">此規模設定中 VM 實例的升級原則模式。</span><span class="sxs-lookup"><span data-stu-id="947b9-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="947b9-186">升級原則可以指定自動、手動或輪流升級。</span><span class="sxs-lookup"><span data-stu-id="947b9-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="947b9-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="947b9-188">指定包含此 Cmdlet 所建立之 VMSS 之屬性的 **VirtualMachineScaleSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="947b9-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="947b9-189">-VirtualNetworkName</span></span>
<span data-ttu-id="947b9-190">要搭配此比例集使用之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="947b9-191">如果未提供任何值，就會建立新的虛擬網路，其名稱與縮放設定相同。</span><span class="sxs-lookup"><span data-stu-id="947b9-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="947b9-192">-VMScaleSetName</span></span>
<span data-ttu-id="947b9-193">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="947b9-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="947b9-194">-VmSize</span></span>
<span data-ttu-id="947b9-195">此規模集中的 VM 實例大小。</span><span class="sxs-lookup"><span data-stu-id="947b9-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="947b9-196">如果沒有指定大小，則會使用預設大小 (Standard_DS1_v2) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="947b9-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="947b9-198">與此比例集搭配使用之虛擬網路的位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="947b9-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="947b9-199">如果未提供任何值，則會使用預設的虛擬網路位址首碼設定 (192.168.0.0/16) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="947b9-200">-Zone</span></span>
<span data-ttu-id="947b9-201">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="947b9-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947b9-202">-確認</span><span class="sxs-lookup"><span data-stu-id="947b9-202">-Confirm</span></span>
<span data-ttu-id="947b9-203">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="947b9-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="947b9-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947b9-204">-WhatIf</span></span>
<span data-ttu-id="947b9-205">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="947b9-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="947b9-206">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="947b9-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="947b9-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947b9-207">CommonParameters</span></span>
<span data-ttu-id="947b9-208">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="947b9-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947b9-209">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="947b9-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947b9-210">輸入</span><span class="sxs-lookup"><span data-stu-id="947b9-210">INPUTS</span></span>

### <span data-ttu-id="947b9-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="947b9-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="947b9-212">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="947b9-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="947b9-213">輸出</span><span class="sxs-lookup"><span data-stu-id="947b9-213">OUTPUTS</span></span>

### <span data-ttu-id="947b9-214">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="947b9-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="947b9-215">筆記</span><span class="sxs-lookup"><span data-stu-id="947b9-215">NOTES</span></span>

## <span data-ttu-id="947b9-216">相關連結</span><span class="sxs-lookup"><span data-stu-id="947b9-216">RELATED LINKS</span></span>

[<span data-ttu-id="947b9-217">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="947b9-218">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="947b9-219">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="947b9-220">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="947b9-221">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="947b9-222">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="947b9-223">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="947b9-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


