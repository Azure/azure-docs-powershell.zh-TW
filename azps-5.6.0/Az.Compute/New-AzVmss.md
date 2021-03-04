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
# New-AzVmss

## 簡介
建立 VMSS。

## 語法

### DefaultParameter (預設) 
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
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

## 描述
**New-Az Vmss** Cmdlet 會建立 Azure (VMSS) 虛擬機器縮放集。
使用簡單的參數集 `SimpleParameterSet` () 快速建立預先設定之 VMSS 及相關資源。 當您需要在建立前精確地設定 VMSS 及每個關聯資源的每個元件時，請使用預設的參數集 () 進一) 的情況 `DefaultParameter` 。

## 例子

### 範例 1：使用 **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

上述命令會以下列名稱建立 `$vmssName` 下列專案：
* 資源群組
* 虛擬網路
* 負載平衡器
* 公用 IP
* 具有 2 個實例的 VMSS

為 VMSS 中的虛擬機器選擇的預設影像 `2016-Datacenter Windows Server` 為，且 SKU 為 `Standard_DS1_v2`

### 範例 2：使用 **`DefaultParameterSet`**
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

上述複雜範例會建立 VMSS，以下是發生情況的說明：
* 第一個命令會建立具有指定名稱和位置的資源群組。
* 第二個命令使用 **New-AzStorageAccount** Cmdlet 來建立儲存帳戶。
* 接著，第三個命令會使用 **Get-AzStorageAccount** Cmdlet 取得第二個命令所建立儲存帳戶，然後將結果儲存在 $STOAccount 變數中。
* 第五個命令使用 **New-AzVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並儲存在名為 $SubNet 的變數中。
* 第六個命令使用 **New-AzVirtualNetwork** Cmdlet 來建立虛擬網路，並儲存在名為 $VNet 的變數中。
* 第七個命令使用 **Get-AzVirtualNetwork** 來取得第六個命令所建立之虛擬網路的資訊，並儲存在名為 $VNet 的變數中。
* 第八個和第九個命令使用 **New-AzPublicIpAddress** 和 **Get- AzureRmPublicIpAddress，** 從該公用 IP 位址建立及取得資訊。
* 命令會儲存在名為 $PubIP 的變數中。
* 第十個命令使用 **New-AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並儲存在名為 $Frontend 的變數中。
* 第十一個命令使用 **New-AzLoadBalancerBackendAddressPoolConfig** 來建立後端位址集區組，並儲存在名為 $BackendAddressPool 的變數中。
* 第十二個命令使用 **New-AzLoadBalancerProbeConfig** 來建立一個測量，並儲存在名為 $Probe 的變數中。
* 第十三個命令使用 **New-AzLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器輸入網路位址轉譯 (NAT) 集組組。
* 第十四個命令使用 **New-AzLoadBalancerRuleConfig** 來建立負載平衡器規則組式，並儲存在名為 $LBRule 的變數中。
* 第十五個命令使用 **New-AzLoadBalancer** Cmdlet 來建立負載平衡器，並儲存在名為 $ActualLb 的變數中。
* 第十五個命令使用 **Get-AzLoadBalancer** 取得第十五個命令所建立之負載平衡器的資訊，並儲存在名為 $ExpectedLb 的變數中。
* 第十七個命令使用 **New-Az VmssIPConfig** Cmdlet 來建立 VMSS IP 組式，並儲存在名為 $IPCfg 的變數中。
* 第十八個命令使用 **New-Az VmssConfig** Cmdlet 來建立 VMSS 組式物件，並儲存在名為 $VMSS 的變數中。
* 第一個命令使用 **New-Az Vms Cmdlet** 來建立 VMSS。

## 參數

### -AllocationMethod
靜態或動態縮放比例集的公用 IP 位址 (分配) 。  如果沒有提供值，則配置會為靜態。

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

### -AsJob
在背景中執行 Cmdlet 並返回工作以追蹤進度。

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

### -後端多工緩衝處理程式名稱
要用於此縮放集之負載平衡器中的後端位址集名。  如果沒有提供值，將會建立一個新的後端集區，其名稱與縮放集相同。

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

### -後端埠
縮放集負載平衡器用來與縮放集中的虛擬機器通訊的後端埠號碼。  如果沒有指定值，Windows VMS 會使用埠 3389 和 5985，而埠 22 則適用于 Linux 虛擬機器。

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

### -認證
系統管理員認證 (此縮放) 的虛擬機器使用者名稱和密碼。

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

### -Data以SizeInGb
指定資料磁片的大小 ，以 GB 為單位。

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

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -DomainNameLabel
此縮放集Fully-Qualified FQDN (公用) 標籤。 這是功能變數名稱的第一個元件，會自動指派給縮放集。 自動指派的功能變數名稱會使用表單 <DomainNameLabel> <Location> (。cloudapp.azure.com) 。 如果沒有提供值，預設的功能變數名稱標籤就是與 的連 <ScaleSetName> 連 <ResourceGroupName> 。

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

### -EnableUltrasSD
針對縮放集的虛擬機器使用 UltraSSD 磁片。

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

### -EncryptionAtHost
此參數會針對主機本身的所有磁片啟用加密，包括 Resource/Temp 磁片。 預設：除非資源的此屬性設為 True，否則會停用主機的加密。

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

### -Policy
低優先順序虛擬機器縮放集的回收政策。  只有支援的值為 'Deallocate' 和 'Delete'。

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

### -FrontendPoolName
要用於縮放集負載平衡器之前端位址集區的名稱。  如果沒有提供值，將會建立一個新的 Frontend 位址資料庫，其名稱與縮放集相同。

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

### -HostGroupId
指定虛擬機器縮放集所在的專用主機群組。

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

### -ImageName
此縮放集之虛擬機器的圖像名稱。 如果沒有提供值，將會使用 「Windows Server 2016 DataCenter」影像。

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

### -InstanceCount
縮放集的 VM 影像數目。  如果沒有提供值，將會建立 2 個實例。

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

### -LoadBalancerName
要用於此縮放集的負載平衡器名稱。  如果沒有指定值，將會建立使用與縮放集相同名稱的新負載平衡器。

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

### -位置
建立此縮放集的 Azure 位置。  如果未指定值，將會從參數中參照的其他資源位置推斷位置。

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

### -MaxPrice
低優先順序虛擬機器縮放集帳單的最大價格。

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

### -NatBackendPort
輸入網路位址轉譯的後端埠。

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

### -PlatformFaultDomainCount
每個位置群組的故障網域計數。

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

### -優先順序
縮放集內虛擬機器的優先順序。  只有支援的值是 "Regular"、'Spot' 和 'Low'。
"Regular" 適用于一般虛擬機器。
"Spot" 適用于 Spot 虛擬機器。
"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。 請使用 "Spot" 而不是 "Low"。

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

### -ProximityPlacementGroupId
要用於此縮放集的鄰近位置群組資源識別碼。

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

### -PublicIpAddressName
要用於此縮放集的公用 IP 位址名稱。  如果沒有提供值，將會建立名稱與縮放集相同的新公用 IPAddress。

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

### -ResourceGroupName
指定 VMSS 資源組的名稱。  如果沒有指定值，將會使用與縮放集相同的名稱來建立新的 ResourceGroup。

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

### -ScaleInPolicy
縮放虛擬機器縮放比例集時要遵循的規則。  可能的值為：「Default」、'Oldest%。以及'Newest%。。」  當虛擬機器縮放集已調整為比例時，如果這是一個分區比例集，則縮放集會先跨區域進行平衡的預設值。  然後，它會盡可能跨錯誤網域進行平衡。  在每個錯誤網域中，選擇移除的虛擬機器都是不受縮放保護的虛擬機器。  當虛擬機器縮放集進行縮放時，會選擇最舊、不受縮放保護的虛擬機器進行移除。  對於分區虛擬機器縮放集，縮放集會先跨區域平衡。  在每個區域中，會選擇最舊的未受到保護的虛擬機器進行移除。  當虛擬機器縮放集進行縮放時，將會選擇不受縮放保護的最新的虛擬機器，以移除最新的虛擬機器。  對於分區虛擬機器縮放集，縮放集會先跨區域平衡。  在每個區域中，系統將會選擇最新的未受到保護的虛擬機器進行移除。

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

### -SecurityGroupName
要套用至此縮放集的網路安全性群組名稱。  如果沒有提供值，將會建立一個與縮放集名稱相同的預設網路安全性群組，並套用至縮放集。

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

### -SinglePlacementGroup
使用此功能在單一位置群組中建立縮放集，預設為多個群組

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

### -SkipExtensionsOnOverprovisionedVMS
指定擴充功能不會在額外過度配置之虛擬機器上執行。

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

### -子網AddressPrefix
此 ScaleSet 將會使用子網的位址首碼。 如果沒有提供 (，系統將會) 192.168.1.0/24 系統的預設子網設定。

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

### -子網名稱
要用於此縮放集的子網名稱。  如果沒有提供值，將會建立名稱與縮放集相同的新子網。

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

### -SystemAssignedIdentity
如果參數存在，則縮放 (中) 的 VM (會指派) 自動產生的受管理系統身分識別。

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

### -UpgradePolicyMode
此縮放集的 VM 實例升級策略模式。  升級政策可指定自動、手動或輪流升級。

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

### -UserAssignedIdentity
應指派給 VM 的受管理服務身分識別名稱 (縮放) 設定中。

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

### -VirtualMachineScaleSet
指定 **VirtualMachineScaleSet 物件** ，該物件包含此 Cmdlet 所建立之 VMSS 的屬性。

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

### -VirtualNetworkName
要用於此縮放集的虛擬網路名稱。  如果沒有提供值，將會建立名稱與縮放集相同的新虛擬網路。

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

### -VMScaleSetName
指定此 Cmdlet 所建立之 VMSS 的名稱。

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

### -VmSize
此縮放集的 VM 實例大小。  如果沒有指定 (Standard_DS1_v2) ，將會使用預設大小選項。

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

### -VnetAddressPrefix
此縮放集所使用之虛擬網路的位址首碼。  如果沒有提供值， (192.168.0.0/16) 預設虛擬網路位址首碼設定。

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

### -區域
表示資源需要配置之 IP 的可用性區域清單。

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

### -確認
執行 Cmdlet 之前，提示您確認。

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

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 輸出

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

## 筆記

## 相關連結

[Get-AzEvss](./Get-AzVmss.md)

[Remove-AzEvss](./Remove-AzVmss.md)

[Restart-AzEvss](./Restart-AzVmss.md)

[Set-AzEvss](./Set-AzVmss.md)

[Start-AzEvss](./Start-AzVmss.md)

[Stop-AzEvss](./Stop-AzVmss.md)

[Update-AzEvss](./Update-AzVmss.md)


