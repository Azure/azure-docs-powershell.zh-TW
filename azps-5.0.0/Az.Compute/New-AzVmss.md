---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286115"
---
# <span data-ttu-id="11951-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-101">New-AzVmss</span></span>

## <span data-ttu-id="11951-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11951-102">SYNOPSIS</span></span>
<span data-ttu-id="11951-103">建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="11951-103">Creates a VMSS.</span></span>

## <span data-ttu-id="11951-104">句法</span><span class="sxs-lookup"><span data-stu-id="11951-104">SYNTAX</span></span>

### <span data-ttu-id="11951-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="11951-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11951-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="11951-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11951-107">說明</span><span class="sxs-lookup"><span data-stu-id="11951-107">DESCRIPTION</span></span>
<span data-ttu-id="11951-108">**新的-AzVmss** Cmdlet 會在 Azure 中建立 (VMSS) 的虛擬電腦縮放比例集。</span><span class="sxs-lookup"><span data-stu-id="11951-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="11951-109">使用簡單參數集 (`SimpleParameterSet`) 快速建立預先設定 VMSS 及相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="11951-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="11951-110">`DefaultParameter`如果您需要在建立 VMSS 和每個相關聯的資源之前，精確設定每個元件，請使用預設參數 set () 來進行更高級的案例。</span><span class="sxs-lookup"><span data-stu-id="11951-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="11951-111">示例</span><span class="sxs-lookup"><span data-stu-id="11951-111">EXAMPLES</span></span>

### <span data-ttu-id="11951-112">範例1：使用下列專案建立 VMSS **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="11951-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="11951-113">上述命令會建立下列名稱 `$vmssName` ：</span><span class="sxs-lookup"><span data-stu-id="11951-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="11951-114">資源群組</span><span class="sxs-lookup"><span data-stu-id="11951-114">A Resource Group</span></span>
* <span data-ttu-id="11951-115">虛擬網路</span><span class="sxs-lookup"><span data-stu-id="11951-115">A virtual network</span></span>
* <span data-ttu-id="11951-116">負載平衡器</span><span class="sxs-lookup"><span data-stu-id="11951-116">A load balancer</span></span>
* <span data-ttu-id="11951-117">公用 IP</span><span class="sxs-lookup"><span data-stu-id="11951-117">A public IP</span></span>
* <span data-ttu-id="11951-118">含2個實例的 VMSS</span><span class="sxs-lookup"><span data-stu-id="11951-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="11951-119">在 VMSS 中為 Vm 選取的預設影像是 `2016-Datacenter Windows Server` ，而 SKU 則是 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="11951-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="11951-120">範例2：使用下列專案建立 VMSS **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="11951-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="11951-121">上述的複雜範例會建立 VMSS，以下是對發生情況的說明：</span><span class="sxs-lookup"><span data-stu-id="11951-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="11951-122">第一個命令會建立具有指定名稱和位置的資源群組。</span><span class="sxs-lookup"><span data-stu-id="11951-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="11951-123">第二個命令使用 **新的 AzStorageAccount** Cmdlet 來建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="11951-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="11951-124">然後，第三個命令會使用 **AzStorageAccount** Cmdlet 來取得第二個命令中建立的儲存空間帳戶，並將結果儲存在 $STOAccount 變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="11951-125">第五個命令使用 **新的 AzVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並將結果儲存在名為 $SubNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="11951-126">第六個命令使用 **新的 AzVirtualNetwork** Cmdlet 來建立虛擬網路，並將結果儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="11951-127">第七個命令使用 **AzVirtualNetwork** ，以取得在第6個命令中建立的虛擬網路相關資訊，並將資訊儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="11951-128">第八和第九個命令使用 **新的 AzPublicIpAddress** 和 **AzureRmPublicIpAddress** 來建立並從該公用 IP 位址中取得資訊。</span><span class="sxs-lookup"><span data-stu-id="11951-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="11951-129">這些命令會將資訊儲存在名為 $PubIP 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="11951-130">第十個命令使用 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並將結果儲存在名為 $Frontend 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="11951-131">第十一個命令使用 **New-AzLoadBalancerBackendAddressPoolConfig** 建立後端位址集區配置，並將結果儲存在名為 $BackendAddressPool 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="11951-132">第十二個命令使用 **New-AzLoadBalancerProbeConfig** 來建立探測器，並將探測器資訊儲存在名為 $Probe 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="11951-133">第13個命令使用 **AzLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器入站網路位址轉譯 (NAT) 池設定。</span><span class="sxs-lookup"><span data-stu-id="11951-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="11951-134">第十四個命令使用 **New-AzLoadBalancerRuleConfig** 來建立負載平衡器規則設定，並將結果儲存在名為 $LBRule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="11951-135">第15個命令使用 **AzLoadBalancer** Cmdlet 來建立負載平衡器，並將結果儲存在名為 $ActualLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="11951-136">第十六個命令使用 **AzLoadBalancer** ，以取得在第15個命令中建立的負載平衡器相關資訊，並將資訊儲存在名為 $ExpectedLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="11951-137">Seventeenth 命令會使用 **新的-AzVmssIPConfig** Cmdlet 來建立 VMSS IP 設定，並將資訊儲存在名為 $IPCfg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="11951-138">第十八個命令使用 **AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11951-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="11951-139">十九命令會使用 **新的-AzVmss** Cmdlet 來建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="11951-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="11951-140">參數</span><span class="sxs-lookup"><span data-stu-id="11951-140">PARAMETERS</span></span>

### <span data-ttu-id="11951-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="11951-141">-AllocationMethod</span></span>
<span data-ttu-id="11951-142">縮放集的公用 IP 位址 (靜態或動態) 的配置方法。</span><span class="sxs-lookup"><span data-stu-id="11951-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="11951-143">如果未提供任何值，則分配將是靜態的。</span><span class="sxs-lookup"><span data-stu-id="11951-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11951-144">-AsJob</span></span>
<span data-ttu-id="11951-145">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="11951-145">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="11951-146">-BackendPoolName</span></span>
<span data-ttu-id="11951-147">要在此比例集的負載平衡器中使用的後端位址集區名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="11951-148">如果未提供任何值，則會建立新的後端池，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="11951-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="11951-149">-BackendPort</span></span>
<span data-ttu-id="11951-150">[縮放設定] 負載平衡器所使用的後端埠號，可與小數位集中的 Vm 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="11951-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="11951-151">如果未指定任何值，則會將埠3389和5985用於 Windows VM，而埠22將用於 Linux Vm。</span><span class="sxs-lookup"><span data-stu-id="11951-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-152">-認證</span><span class="sxs-lookup"><span data-stu-id="11951-152">-Credential</span></span>
<span data-ttu-id="11951-153">系統管理員認證 (此規模集中之 Vm 的使用者名稱和密碼) 。</span><span class="sxs-lookup"><span data-stu-id="11951-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="11951-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="11951-155">指定資料磁片的大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="11951-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11951-156">-DefaultProfile</span></span>
<span data-ttu-id="11951-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11951-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11951-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="11951-158">-DomainNameLabel</span></span>
<span data-ttu-id="11951-159">此比例集之公用 Fully-Qualified 功能變數名稱的功能變數名稱標籤 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="11951-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="11951-160">這是功能變數名稱的第一個元件，會自動指派給比例集。</span><span class="sxs-lookup"><span data-stu-id="11951-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="11951-161">自動指派的功能變數名稱使用 [表單 (] <DomainNameLabel> 。 <Location>cloudapp.azure.com [) ]。</span><span class="sxs-lookup"><span data-stu-id="11951-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="11951-162">如果未提供任何值，預設的網功能變數名稱稱標籤將會是 and 的串聯 <ScaleSetName> <ResourceGroupName> 。</span><span class="sxs-lookup"><span data-stu-id="11951-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="11951-163">-EnableUltraSSD</span></span>
<span data-ttu-id="11951-164">在規模集中針對 Vm 使用 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="11951-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="11951-165">-EncryptionAtHost</span></span>
<span data-ttu-id="11951-166">這個參數會針對所有磁片啟用加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="11951-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="11951-167">預設：除非針對資源將此屬性設為 true，否則將停用主機上的加密。</span><span class="sxs-lookup"><span data-stu-id="11951-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="11951-168">-EvictionPolicy</span></span>
<span data-ttu-id="11951-169">低優先順序虛擬機器規模集的逐出原則。</span><span class="sxs-lookup"><span data-stu-id="11951-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="11951-170">僅支援的值為 "解除配置" 和 "Delete"。</span><span class="sxs-lookup"><span data-stu-id="11951-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="11951-171">-FrontendPoolName</span></span>
<span data-ttu-id="11951-172">要在縮放集負載平衡器中使用之前端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="11951-173">如果未提供任何值，則會建立新的前端位址集區，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="11951-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="11951-174">-HostGroupId</span></span>
<span data-ttu-id="11951-175">指定虛擬機器縮放集將駐留在其中的專用主機群組。</span><span class="sxs-lookup"><span data-stu-id="11951-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="11951-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="11951-176">-ImageName</span></span>
<span data-ttu-id="11951-177">此規模集中之 Vm 的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="11951-178">如果未提供任何值，就會使用 [Windows Server 2016 DataCenter] 影像。</span><span class="sxs-lookup"><span data-stu-id="11951-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="11951-179">-InstanceCount</span></span>
<span data-ttu-id="11951-180">刻度集中的 VM 影像數目。</span><span class="sxs-lookup"><span data-stu-id="11951-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="11951-181">如果未提供任何值，則會建立2個實例。</span><span class="sxs-lookup"><span data-stu-id="11951-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="11951-182">-LoadBalancerName</span></span>
<span data-ttu-id="11951-183">要與此比例集搭配使用的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="11951-184">如果沒有指定任何值，就會建立新的負載平衡器，使用與縮放設定相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-185">-位置</span><span class="sxs-lookup"><span data-stu-id="11951-185">-Location</span></span>
<span data-ttu-id="11951-186">將建立此縮放集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="11951-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="11951-187">如果未指定任何值，則會從參數中參照的其他資源位置推斷位置。</span><span class="sxs-lookup"><span data-stu-id="11951-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="11951-188">-MaxPrice</span></span>
<span data-ttu-id="11951-189">低優先順序虛擬機器規模集的帳單最大價格。</span><span class="sxs-lookup"><span data-stu-id="11951-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="11951-190">-NatBackendPort</span></span>
<span data-ttu-id="11951-191">入站網路位址轉譯的後端埠。</span><span class="sxs-lookup"><span data-stu-id="11951-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="11951-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="11951-193">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="11951-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11951-194">-優先順序</span><span class="sxs-lookup"><span data-stu-id="11951-194">-Priority</span></span>
<span data-ttu-id="11951-195">規模集中虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="11951-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="11951-196">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="11951-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="11951-197">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11951-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="11951-198">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11951-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="11951-199">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="11951-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="11951-200">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="11951-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="11951-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="11951-202">要與此比例集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11951-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="11951-203">-PublicIpAddressName</span></span>
<span data-ttu-id="11951-204">要與此比例集搭配使用之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="11951-205">如果未提供任何值，就會建立新的與縮放集同名的公用 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="11951-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11951-206">-ResourceGroupName</span></span>
<span data-ttu-id="11951-207">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="11951-208">如果未指定任何值，則會使用與縮放集相同的名稱建立新的 ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="11951-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11951-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="11951-209">-ScaleInPolicy</span></span>
<span data-ttu-id="11951-210">在虛擬電腦規模集中進行伸縮時遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="11951-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="11951-211">可能的值為： "Default"、"OldestVM" 和 "NewestVM"。</span><span class="sxs-lookup"><span data-stu-id="11951-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="11951-212">[預設值] 當虛擬電腦縮放比例設定為放大時，如果區域為區域性比例集，則比例集會先平衡在各個區域。</span><span class="sxs-lookup"><span data-stu-id="11951-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="11951-213">接著，它會盡可能在故障網域之間平衡。</span><span class="sxs-lookup"><span data-stu-id="11951-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="11951-214">在每個容錯網域中，選取要移除的虛擬機器將是無法從擴展保護的最新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11951-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="11951-215">"OldestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選擇要移除的最舊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11951-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="11951-216">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="11951-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="11951-217">在每個區域中，將會選取未受保護的舊虛擬機器，以供移除。</span><span class="sxs-lookup"><span data-stu-id="11951-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="11951-218">"NewestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選取任何不受放大的虛擬機器來進行移除。</span><span class="sxs-lookup"><span data-stu-id="11951-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="11951-219">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="11951-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="11951-220">在每個區域中，將會選取未受到保護的新虛擬機器電腦來移除。</span><span class="sxs-lookup"><span data-stu-id="11951-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="11951-221">-SecurityGroupName</span></span>
<span data-ttu-id="11951-222">要套用至此比例集的網路安全性群組名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="11951-223">如果未提供任何值，則會建立與縮放集名稱相同的預設網路安全性群組，並將其套用至比例集。</span><span class="sxs-lookup"><span data-stu-id="11951-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="11951-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="11951-225">使用此功能在單一位置群組中建立比例集，預設為多個群組</span><span class="sxs-lookup"><span data-stu-id="11951-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="11951-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="11951-227">指定延伸不會在額外的 overprovisioned Vm 上執行。</span><span class="sxs-lookup"><span data-stu-id="11951-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11951-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="11951-229">此 ScaleSet 將使用之子網的位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="11951-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="11951-230">如果未提供任何值，則會套用預設的子網設定 (192.168.1.0/24) 。</span><span class="sxs-lookup"><span data-stu-id="11951-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="11951-231">-SubnetName</span></span>
<span data-ttu-id="11951-232">要與此比例集搭配使用的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="11951-233">如果沒有提供任何值，就會建立新的子網，其名稱與縮放設定相同。</span><span class="sxs-lookup"><span data-stu-id="11951-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="11951-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="11951-235">如果該參數存在，則會) 已指派自動產生的受管理系統身分識別，在縮放集 (中) VM (s。</span><span class="sxs-lookup"><span data-stu-id="11951-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="11951-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="11951-237">此規模設定中 VM 實例的升級原則模式。</span><span class="sxs-lookup"><span data-stu-id="11951-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="11951-238">升級原則可以指定自動、手動或輪流升級。</span><span class="sxs-lookup"><span data-stu-id="11951-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="11951-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="11951-240">受管理服務身分識別的名稱，應該指派給 VM (s) 在比例集中。</span><span class="sxs-lookup"><span data-stu-id="11951-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11951-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="11951-242">指定包含此 Cmdlet 所建立之 VMSS 之屬性的 **VirtualMachineScaleSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="11951-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11951-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="11951-243">-VirtualNetworkName</span></span>
<span data-ttu-id="11951-244">要搭配此比例集使用之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="11951-245">如果未提供任何值，就會建立新的虛擬網路，其名稱與縮放設定相同。</span><span class="sxs-lookup"><span data-stu-id="11951-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="11951-246">-VMScaleSetName</span></span>
<span data-ttu-id="11951-247">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11951-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11951-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="11951-248">-VmSize</span></span>
<span data-ttu-id="11951-249">此規模集中的 VM 實例大小。</span><span class="sxs-lookup"><span data-stu-id="11951-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="11951-250">如果沒有指定大小，則會使用預設大小 (Standard_DS1_v2) 。</span><span class="sxs-lookup"><span data-stu-id="11951-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11951-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="11951-252">與此比例集搭配使用之虛擬網路的位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="11951-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="11951-253">如果未提供任何值，則會使用預設的虛擬網路位址首碼設定 (192.168.0.0/16) 。</span><span class="sxs-lookup"><span data-stu-id="11951-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="11951-254">-Zone</span></span>
<span data-ttu-id="11951-255">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="11951-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="11951-256">-確認</span><span class="sxs-lookup"><span data-stu-id="11951-256">-Confirm</span></span>
<span data-ttu-id="11951-257">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11951-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11951-258">-WhatIf</span></span>
<span data-ttu-id="11951-259">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11951-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11951-260">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11951-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11951-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11951-261">CommonParameters</span></span>
<span data-ttu-id="11951-262">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11951-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11951-263">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11951-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11951-264">輸入</span><span class="sxs-lookup"><span data-stu-id="11951-264">INPUTS</span></span>

### <span data-ttu-id="11951-265">System.object</span><span class="sxs-lookup"><span data-stu-id="11951-265">System.String</span></span>

### <span data-ttu-id="11951-266">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="11951-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="11951-267">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11951-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11951-268">輸出</span><span class="sxs-lookup"><span data-stu-id="11951-268">OUTPUTS</span></span>

### <span data-ttu-id="11951-269">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="11951-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="11951-270">筆記</span><span class="sxs-lookup"><span data-stu-id="11951-270">NOTES</span></span>

## <span data-ttu-id="11951-271">相關連結</span><span class="sxs-lookup"><span data-stu-id="11951-271">RELATED LINKS</span></span>

[<span data-ttu-id="11951-272">AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="11951-273">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="11951-274">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="11951-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="11951-276">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="11951-277">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="11951-278">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11951-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


