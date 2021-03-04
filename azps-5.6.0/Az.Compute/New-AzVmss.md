---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: f80441cb3555d78974c5a838e829cb2ab350183f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911178"
---
# <span data-ttu-id="0ad15-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0ad15-101">New-AzVmss</span></span>

## <span data-ttu-id="0ad15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ad15-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad15-103">建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="0ad15-103">Creates a VMSS.</span></span>

## <span data-ttu-id="0ad15-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ad15-104">SYNTAX</span></span>

### <span data-ttu-id="0ad15-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0ad15-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad15-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad15-106">SimpleParameterSet</span></span>
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

## <span data-ttu-id="0ad15-107">描述</span><span class="sxs-lookup"><span data-stu-id="0ad15-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad15-108">**New-Az Vmss** Cmdlet 會建立 Azure (VMSS) 虛擬機器縮放集。</span><span class="sxs-lookup"><span data-stu-id="0ad15-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="0ad15-109">使用簡單的參數集 `SimpleParameterSet` () 快速建立預先設定之 VMSS 及相關資源。</span><span class="sxs-lookup"><span data-stu-id="0ad15-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="0ad15-110">當您需要在建立前精確地設定 VMSS 及每個關聯資源的每個元件時，請使用預設的參數集 () 進一) 的情況 `DefaultParameter` 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="0ad15-111">例子</span><span class="sxs-lookup"><span data-stu-id="0ad15-111">EXAMPLES</span></span>

### <span data-ttu-id="0ad15-112">範例 1：使用 **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="0ad15-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="0ad15-113">上述命令會以下列名稱建立 `$vmssName` 下列專案：</span><span class="sxs-lookup"><span data-stu-id="0ad15-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="0ad15-114">資源群組</span><span class="sxs-lookup"><span data-stu-id="0ad15-114">A Resource Group</span></span>
* <span data-ttu-id="0ad15-115">虛擬網路</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">A virtual network</span></span>
* <span data-ttu-id="0ad15-116">負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">A load balancer</span></span>
* <span data-ttu-id="0ad15-117">公用 IP</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">A public IP</span></span>
* <span data-ttu-id="0ad15-118">具有 2 個實例的 VMSS</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="0ad15-119">為 VMSS 中的虛擬機器選擇的預設影像 `2016-Datacenter Windows Server` 為，且 SKU 為 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="0ad15-120">範例 2：使用 **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="0ad15-121">上述複雜範例會建立 VMSS，以下是發生情況的說明：</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="0ad15-122">第一個命令會建立具有指定名稱和位置的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="0ad15-123">第二個命令使用 **New-AzStorageAccount** Cmdlet 來建立儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="0ad15-124">接著，第三個命令會使用 **Get-AzStorageAccount** Cmdlet 取得第二個命令所建立儲存帳戶，然後將結果儲存在 $STOAccount 變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="0ad15-125">第五個命令使用 **New-AzVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並儲存在名為 $SubNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="0ad15-126">第六個命令使用 **New-AzVirtualNetwork** Cmdlet 來建立虛擬網路，並儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="0ad15-127">第七個命令使用 **Get-AzVirtualNetwork** 來取得第六個命令所建立之虛擬網路的資訊，並儲存在名為 $VNet 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="0ad15-128">第八個和第九個命令使用 **New-AzPublicIpAddress** 和 **Get- AzureRmPublicIpAddress，** 從該公用 IP 位址建立及取得資訊。</span><span class="sxs-lookup"><span data-stu-id="0ad15-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="0ad15-129">命令會儲存在名為 $PubIP 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="0ad15-130">第十個命令使用 **New-AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並儲存在名為 $Frontend 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="0ad15-131">第十一個命令使用 **New-AzLoadBalancerBackendAddressPoolConfig** 來建立後端位址集區組，並儲存在名為 $BackendAddressPool 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="0ad15-132">第十二個命令使用 **New-AzLoadBalancerProbeConfig** 來建立一個測量，並儲存在名為 $Probe 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="0ad15-133">第十三個命令使用 **New-AzLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器輸入網路位址轉譯 (NAT) 集組組。</span><span class="sxs-lookup"><span data-stu-id="0ad15-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="0ad15-134">第十四個命令使用 **New-AzLoadBalancerRuleConfig** 來建立負載平衡器規則組式，並儲存在名為 $LBRule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="0ad15-135">第十五個命令使用 **New-AzLoadBalancer** Cmdlet 來建立負載平衡器，並儲存在名為 $ActualLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="0ad15-136">第十五個命令使用 **Get-AzLoadBalancer** 取得第十五個命令所建立之負載平衡器的資訊，並儲存在名為 $ExpectedLb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="0ad15-137">第十七個命令使用 **New-Az VmssIPConfig** Cmdlet 來建立 VMSS IP 組式，並儲存在名為 $IPCfg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="0ad15-138">第十八個命令使用 **New-Az VmssConfig** Cmdlet 來建立 VMSS 組式物件，並儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="0ad15-139">第一個命令使用 **New-Az Vms Cmdlet** 來建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="0ad15-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="0ad15-140">參數</span><span class="sxs-lookup"><span data-stu-id="0ad15-140">PARAMETERS</span></span>

### <span data-ttu-id="0ad15-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="0ad15-141">-AllocationMethod</span></span>
<span data-ttu-id="0ad15-142">靜態或動態縮放比例集的公用 IP 位址 (分配) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="0ad15-143">如果沒有提供值，則配置會為靜態。</span><span class="sxs-lookup"><span data-stu-id="0ad15-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="0ad15-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ad15-144">-AsJob</span></span>
<span data-ttu-id="0ad15-145">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="0ad15-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0ad15-146">-後端多工緩衝處理程式名稱</span><span class="sxs-lookup"><span data-stu-id="0ad15-146">-BackendPoolName</span></span>
<span data-ttu-id="0ad15-147">要用於此縮放集之負載平衡器中的後端位址集名。</span><span class="sxs-lookup"><span data-stu-id="0ad15-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="0ad15-148">如果沒有提供值，將會建立一個新的後端集區，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="0ad15-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="0ad15-149">-後端埠</span><span class="sxs-lookup"><span data-stu-id="0ad15-149">-BackendPort</span></span>
<span data-ttu-id="0ad15-150">縮放集負載平衡器用來與縮放集中的虛擬機器通訊的後端埠號碼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="0ad15-151">如果沒有指定值，Windows VMS 會使用埠 3389 和 5985，而埠 22 則適用于 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="0ad15-152">-認證</span><span class="sxs-lookup"><span data-stu-id="0ad15-152">-Credential</span></span>
<span data-ttu-id="0ad15-153">系統管理員認證 (此縮放) 的虛擬機器使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="0ad15-154">-Data以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="0ad15-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="0ad15-155">指定資料磁片的大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="0ad15-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="0ad15-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad15-156">-DefaultProfile</span></span>
<span data-ttu-id="0ad15-157">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad15-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="0ad15-158">-DomainNameLabel</span></span>
<span data-ttu-id="0ad15-159">此縮放集Fully-Qualified FQDN (公用) 標籤。</span><span class="sxs-lookup"><span data-stu-id="0ad15-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="0ad15-160">這是功能變數名稱的第一個元件，會自動指派給縮放集。</span><span class="sxs-lookup"><span data-stu-id="0ad15-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="0ad15-161">自動指派的功能變數名稱會使用表單 <DomainNameLabel> <Location> (。cloudapp.azure.com) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="0ad15-162">如果沒有提供值，預設的功能變數名稱標籤就是與 的連 <ScaleSetName> 連 <ResourceGroupName> 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="0ad15-163">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="0ad15-163">-EnableUltraSSD</span></span>
<span data-ttu-id="0ad15-164">針對縮放集的虛擬機器使用 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="0ad15-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="0ad15-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="0ad15-165">-EncryptionAtHost</span></span>
<span data-ttu-id="0ad15-166">此參數會針對主機本身的所有磁片啟用加密，包括 Resource/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="0ad15-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="0ad15-167">預設：除非資源的此屬性設為 True，否則會停用主機的加密。</span><span class="sxs-lookup"><span data-stu-id="0ad15-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="0ad15-168">-Policy</span><span class="sxs-lookup"><span data-stu-id="0ad15-168">-EvictionPolicy</span></span>
<span data-ttu-id="0ad15-169">低優先順序虛擬機器縮放集的回收政策。</span><span class="sxs-lookup"><span data-stu-id="0ad15-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="0ad15-170">只有支援的值為 'Deallocate' 和 'Delete'。</span><span class="sxs-lookup"><span data-stu-id="0ad15-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="0ad15-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="0ad15-171">-FrontendPoolName</span></span>
<span data-ttu-id="0ad15-172">要用於縮放集負載平衡器之前端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="0ad15-173">如果沒有提供值，將會建立一個新的 Frontend 位址資料庫，其名稱與縮放集相同。</span><span class="sxs-lookup"><span data-stu-id="0ad15-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="0ad15-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="0ad15-174">-HostGroupId</span></span>
<span data-ttu-id="0ad15-175">指定虛擬機器縮放集所在的專用主機群組。</span><span class="sxs-lookup"><span data-stu-id="0ad15-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="0ad15-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0ad15-176">-ImageName</span></span>
<span data-ttu-id="0ad15-177">此縮放集之虛擬機器的圖像名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="0ad15-178">如果沒有提供值，將會使用 「Windows Server 2016 DataCenter」影像。</span><span class="sxs-lookup"><span data-stu-id="0ad15-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="0ad15-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0ad15-179">-InstanceCount</span></span>
<span data-ttu-id="0ad15-180">縮放集的 VM 影像數目。</span><span class="sxs-lookup"><span data-stu-id="0ad15-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="0ad15-181">如果沒有提供值，將會建立 2 個實例。</span><span class="sxs-lookup"><span data-stu-id="0ad15-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="0ad15-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="0ad15-182">-LoadBalancerName</span></span>
<span data-ttu-id="0ad15-183">要用於此縮放集的負載平衡器名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="0ad15-184">如果沒有指定值，將會建立使用與縮放集相同名稱的新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="0ad15-185">-位置</span><span class="sxs-lookup"><span data-stu-id="0ad15-185">-Location</span></span>
<span data-ttu-id="0ad15-186">建立此縮放集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="0ad15-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="0ad15-187">如果未指定值，將會從參數中參照的其他資源位置推斷位置。</span><span class="sxs-lookup"><span data-stu-id="0ad15-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="0ad15-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="0ad15-188">-MaxPrice</span></span>
<span data-ttu-id="0ad15-189">低優先順序虛擬機器縮放集帳單的最大價格。</span><span class="sxs-lookup"><span data-stu-id="0ad15-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="0ad15-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="0ad15-190">-NatBackendPort</span></span>
<span data-ttu-id="0ad15-191">輸入網路位址轉譯的後端埠。</span><span class="sxs-lookup"><span data-stu-id="0ad15-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="0ad15-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="0ad15-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="0ad15-193">每個位置群組的故障網域計數。</span><span class="sxs-lookup"><span data-stu-id="0ad15-193">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="0ad15-194">-優先順序</span><span class="sxs-lookup"><span data-stu-id="0ad15-194">-Priority</span></span>
<span data-ttu-id="0ad15-195">縮放集內虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="0ad15-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="0ad15-196">只有支援的值是 "Regular"、'Spot' 和 'Low'。</span><span class="sxs-lookup"><span data-stu-id="0ad15-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="0ad15-197">"Regular" 適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="0ad15-198">"Spot" 適用于 Spot 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="0ad15-199">"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。</span><span class="sxs-lookup"><span data-stu-id="0ad15-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="0ad15-200">請使用 "Spot" 而不是 "Low"。</span><span class="sxs-lookup"><span data-stu-id="0ad15-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="0ad15-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="0ad15-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="0ad15-202">要用於此縮放集的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="0ad15-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="0ad15-203">-PublicIpAddressName</span></span>
<span data-ttu-id="0ad15-204">要用於此縮放集的公用 IP 位址名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="0ad15-205">如果沒有提供值，將會建立名稱與縮放集相同的新公用 IPAddress。</span><span class="sxs-lookup"><span data-stu-id="0ad15-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="0ad15-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad15-206">-ResourceGroupName</span></span>
<span data-ttu-id="0ad15-207">指定 VMSS 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="0ad15-208">如果沒有指定值，將會使用與縮放集相同的名稱來建立新的 ResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="0ad15-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="0ad15-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="0ad15-209">-ScaleInPolicy</span></span>
<span data-ttu-id="0ad15-210">縮放虛擬機器縮放比例集時要遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="0ad15-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="0ad15-211">可能的值為：「Default」、'Oldest%。以及'Newest%。。」</span><span class="sxs-lookup"><span data-stu-id="0ad15-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="0ad15-212">當虛擬機器縮放集已調整為比例時，如果這是一個分區比例集，則縮放集會先跨區域進行平衡的預設值。</span><span class="sxs-lookup"><span data-stu-id="0ad15-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="0ad15-213">然後，它會盡可能跨錯誤網域進行平衡。</span><span class="sxs-lookup"><span data-stu-id="0ad15-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="0ad15-214">在每個錯誤網域中，選擇移除的虛擬機器都是不受縮放保護的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="0ad15-215">當虛擬機器縮放集進行縮放時，會選擇最舊、不受縮放保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="0ad15-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="0ad15-216">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="0ad15-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="0ad15-217">在每個區域中，會選擇最舊的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="0ad15-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="0ad15-218">當虛擬機器縮放集進行縮放時，將會選擇不受縮放保護的最新的虛擬機器，以移除最新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0ad15-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="0ad15-219">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="0ad15-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="0ad15-220">在每個區域中，系統將會選擇最新的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="0ad15-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="0ad15-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad15-221">-SecurityGroupName</span></span>
<span data-ttu-id="0ad15-222">要套用至此縮放集的網路安全性群組名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="0ad15-223">如果沒有提供值，將會建立一個與縮放集名稱相同的預設網路安全性群組，並套用至縮放集。</span><span class="sxs-lookup"><span data-stu-id="0ad15-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="0ad15-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0ad15-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="0ad15-225">使用此功能在單一位置群組中建立縮放集，預設為多個群組</span><span class="sxs-lookup"><span data-stu-id="0ad15-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="0ad15-226">-SkipExtensionsOnOverprovisionedVMS</span><span class="sxs-lookup"><span data-stu-id="0ad15-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="0ad15-227">指定擴充功能不會在額外過度配置之虛擬機器上執行。</span><span class="sxs-lookup"><span data-stu-id="0ad15-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="0ad15-228">-子網AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0ad15-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="0ad15-229">此 ScaleSet 將會使用子網的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="0ad15-230">如果沒有提供 (，系統將會) 192.168.1.0/24 系統的預設子網設定。</span><span class="sxs-lookup"><span data-stu-id="0ad15-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="0ad15-231">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="0ad15-231">-SubnetName</span></span>
<span data-ttu-id="0ad15-232">要用於此縮放集的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="0ad15-233">如果沒有提供值，將會建立名稱與縮放集相同的新子網。</span><span class="sxs-lookup"><span data-stu-id="0ad15-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="0ad15-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0ad15-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="0ad15-235">如果參數存在，則縮放 (中) 的 VM (會指派) 自動產生的受管理系統身分識別。</span><span class="sxs-lookup"><span data-stu-id="0ad15-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="0ad15-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="0ad15-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="0ad15-237">此縮放集的 VM 實例升級策略模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="0ad15-238">升級政策可指定自動、手動或輪流升級。</span><span class="sxs-lookup"><span data-stu-id="0ad15-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="0ad15-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0ad15-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="0ad15-240">應指派給 VM 的受管理服務身分識別名稱 (縮放) 設定中。</span><span class="sxs-lookup"><span data-stu-id="0ad15-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="0ad15-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ad15-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0ad15-242">指定 **VirtualMachineScaleSet 物件** ，該物件包含此 Cmdlet 所建立之 VMSS 的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ad15-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0ad15-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0ad15-243">-VirtualNetworkName</span></span>
<span data-ttu-id="0ad15-244">要用於此縮放集的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="0ad15-245">如果沒有提供值，將會建立名稱與縮放集相同的新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="0ad15-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="0ad15-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0ad15-246">-VMScaleSetName</span></span>
<span data-ttu-id="0ad15-247">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad15-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0ad15-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="0ad15-248">-VmSize</span></span>
<span data-ttu-id="0ad15-249">此縮放集的 VM 實例大小。</span><span class="sxs-lookup"><span data-stu-id="0ad15-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="0ad15-250">如果沒有指定 (Standard_DS1_v2) ，將會使用預設大小選項。</span><span class="sxs-lookup"><span data-stu-id="0ad15-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="0ad15-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0ad15-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="0ad15-252">此縮放集所使用之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="0ad15-253">如果沒有提供值， (192.168.0.0/16) 預設虛擬網路位址首碼設定。</span><span class="sxs-lookup"><span data-stu-id="0ad15-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="0ad15-254">-區域</span><span class="sxs-lookup"><span data-stu-id="0ad15-254">-Zone</span></span>
<span data-ttu-id="0ad15-255">表示資源需要配置之 IP 的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="0ad15-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="0ad15-256">-確認</span><span class="sxs-lookup"><span data-stu-id="0ad15-256">-Confirm</span></span>
<span data-ttu-id="0ad15-257">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ad15-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad15-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad15-258">-WhatIf</span></span>
<span data-ttu-id="0ad15-259">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ad15-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad15-260">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ad15-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad15-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad15-261">CommonParameters</span></span>
<span data-ttu-id="0ad15-262">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ad15-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad15-263">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ad15-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad15-264">輸入</span><span class="sxs-lookup"><span data-stu-id="0ad15-264">INPUTS</span></span>

### <span data-ttu-id="0ad15-265">System.String</span><span class="sxs-lookup"><span data-stu-id="0ad15-265">System.String</span></span>

### <span data-ttu-id="0ad15-266">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ad15-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0ad15-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ad15-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0ad15-268">輸出</span><span class="sxs-lookup"><span data-stu-id="0ad15-268">OUTPUTS</span></span>

### <span data-ttu-id="0ad15-269">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ad15-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0ad15-270">筆記</span><span class="sxs-lookup"><span data-stu-id="0ad15-270">NOTES</span></span>

## <span data-ttu-id="0ad15-271">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ad15-271">RELATED LINKS</span></span>

[<span data-ttu-id="0ad15-272">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="0ad15-273">Remove-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="0ad15-274">Restart-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0ad15-275">Set-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0ad15-276">Start-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0ad15-277">Stop-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="0ad15-278">Update-AzEvss</span><span class="sxs-lookup"><span data-stu-id="0ad15-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


