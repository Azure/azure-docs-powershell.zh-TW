---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443971"
---
# New-AzureRmVmss

## 摘要
建立 VMSS。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### DefaultParameter (預設) 
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmVmss** Cmdlet 會在 Azure 中建立 (VMSS) 的虛擬電腦縮放比例集。
使用簡單參數集 (`SimpleParameterSet`) 快速建立預先設定 VMSS 及相關聯的資源。 `DefaultParameter`如果您需要在建立 VMSS 和每個相關聯的資源之前，精確設定每個元件，請使用預設參數 set () 來進行更高級的案例。

## 示例

### 範例1：使用下列專案建立 VMSS **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

上述命令會建立下列名稱 `$vmssName` ：
* 資源群組
* 虛擬網路
* 負載平衡器
* 公用 IP
* 含2個實例的 VMSS

在 VMSS 中為 Vm 選取的預設影像是 `2016-Datacenter Windows Server` ，而 SKU 則是 `Standard_DS1_v2`

### 範例2：使用下列專案建立 VMSS **`DefaultParameterSet`**
```powershell
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

上述的複雜範例會建立 VMSS，以下是對發生情況的說明：
* 第一個命令會建立具有指定名稱和位置的資源群組。
* 第二個命令使用 **新的 AzureRmStorageAccount** Cmdlet 來建立儲存空間帳戶。
* 然後，第三個命令會使用 **AzureRmStorageAccount** Cmdlet 來取得第二個命令中建立的儲存空間帳戶，並將結果儲存在 $STOAccount 變數中。
* 第五個命令使用 **新的 AzureRmVirtualNetworkSubnetConfig** Cmdlet 來建立子網，並將結果儲存在名為 $SubNet 的變數中。
* 第六個命令使用 **新的 AzureRmVirtualNetwork** Cmdlet 來建立虛擬網路，並將結果儲存在名為 $VNet 的變數中。
* 第七個命令使用 **AzureRmVirtualNetwork** ，以取得在第6個命令中建立的虛擬網路相關資訊，並將資訊儲存在名為 $VNet 的變數中。
* 第八和第九個命令使用 **新的 AzureRmPublicIpAddress** 和 **AzureRmPublicIpAddress** 來建立並從該公用 IP 位址中取得資訊。
* 這些命令會將資訊儲存在名為 $PubIP 的變數中。
* 第十個命令使用 **AzureRmLoadBalancerFrontendIpConfig** Cmdlet 來建立前端負載平衡器，並將結果儲存在名為 $Frontend 的變數中。
* 第十一個命令使用 **New-AzureRmLoadBalancerBackendAddressPoolConfig** 建立後端位址集區配置，並將結果儲存在名為 $BackendAddressPool 的變數中。
* 第十二個命令使用 **New-AzureRmLoadBalancerProbeConfig** 來建立探測器，並將探測器資訊儲存在名為 $Probe 的變數中。
* 第13個命令使用 **AzureRmLoadBalancerInboundNatPoolConfig** Cmdlet 來建立負載平衡器入站網路位址轉譯 (NAT) 池設定。
* 第十四個命令使用 **New-AzureRmLoadBalancerRuleConfig** 來建立負載平衡器規則設定，並將結果儲存在名為 $LBRule 的變數中。
* 第15個命令使用 **AzureRmLoadBalancer** Cmdlet 來建立負載平衡器，並將結果儲存在名為 $ActualLb 的變數中。
* 第十六個命令使用 **AzureRmLoadBalancer** ，以取得在第15個命令中建立的負載平衡器相關資訊，並將資訊儲存在名為 $ExpectedLb 的變數中。
* Seventeenth 命令會使用 **新的-AzureRmVmssIPConfig** Cmdlet 來建立 VMSS IP 設定，並將資訊儲存在名為 $IPCfg 的變數中。
* 第十八個命令使用 **AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。
* 十九命令會使用 **新的-AzureRmVmss** Cmdlet 來建立 VMSS。

## 參數

### -AllocationMethod
縮放集的公用 IP 位址 (靜態或動態) 的配置方法。  如果未提供任何值，則分配將是靜態的。

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
在背景中執行 Cmdlet，然後返回作業來追蹤進度。

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

### -BackendPoolName
要在此比例集的負載平衡器中使用的後端位址集區名稱。  如果未提供任何值，則會建立新的後端池，其名稱與縮放集相同。

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

### -BackendPort
[縮放設定] 負載平衡器所使用的後端埠號，可與小數位集中的 Vm 進行通訊。  如果未指定任何值，則會將埠3389和5985用於 Windows VM，而埠22將用於 Linux Vm。

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
系統管理員認證 (此規模集中之 Vm 的使用者名稱和密碼) 。

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

### -DataDiskSizeInGb
指定資料磁片的大小（GB）。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
此比例集之公用 Fully-Qualified 功能變數名稱的功能變數名稱標籤 (FQDN) 。 這是功能變數名稱的第一個元件，會自動指派給比例集。 自動指派的功能變數名稱使用 [表單 (] <DomainNameLabel> 。 <Location>cloudapp.azure.com [) ]。 如果未提供任何值，預設的網功能變數名稱稱標籤將會是 and 的串聯 <ScaleSetName> <ResourceGroupName> 。

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
要在縮放集負載平衡器中使用之前端位址集區的名稱。  如果未提供任何值，則會建立新的前端位址集區，其名稱與縮放集相同。

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

### -ImageName
此規模集中之 Vm 的影像名稱。 如果未提供任何值，就會使用 [Windows Server 2016 DataCenter] 影像。

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
刻度集中的 VM 影像數目。  如果未提供任何值，則會建立2個實例。

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
要與此比例集搭配使用的負載平衡器名稱。  如果沒有指定任何值，就會建立新的負載平衡器，使用與縮放設定相同的名稱。

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
將建立此縮放集的 Azure 位置。  如果未指定任何值，則會從參數中參照的其他資源位置推斷位置。

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

### -NatBackendPort
入站網路位址轉譯的後端埠。

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

### -PublicIpAddressName
要與此比例集搭配使用之公用 IP 位址的名稱。  如果未提供任何值，就會建立新的與縮放集同名的公用 Ip 位址。

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
指定 VMSS 之資源群組的名稱。  如果未指定任何值，則會使用與縮放集相同的名稱建立新的 ResourceGroup。

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
要套用至此比例集的網路安全性群組名稱。  如果未提供任何值，則會建立與縮放集名稱相同的預設網路安全性群組，並將其套用至比例集。

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
使用此功能在單一位置群組中建立比例集，預設為多個群組

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

### -SubnetAddressPrefix
此 ScaleSet 將使用之子網的位址前置詞。 如果未提供任何值，則會套用預設的子網設定 (192.168.1.0/24) 。

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

### -SubnetName
要與此比例集搭配使用的子網名稱。  如果沒有提供任何值，就會建立新的子網，其名稱與縮放設定相同。

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
如果該參數存在，則會) 已指派自動產生的受管理系統身分識別，在縮放集 (中) VM (s。

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
此規模設定中 VM 實例的升級原則模式。  升級原則可以指定自動、手動或輪流升級。

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
受管理服務身分識別的名稱，應該指派給 VM (s) 在比例集中。

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
指定包含此 Cmdlet 所建立之 VMSS 之屬性的 **VirtualMachineScaleSet** 物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
要搭配此比例集使用之虛擬網路的名稱。  如果未提供任何值，就會建立新的虛擬網路，其名稱與縮放設定相同。

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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
此規模集中的 VM 實例大小。  如果沒有指定大小，則會使用預設大小 (Standard_DS1_v2) 。

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
與此比例集搭配使用之虛擬網路的位址前置詞。  如果未提供任何值，則會使用預設的虛擬網路位址首碼設定 (192.168.0.0/16) 。

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

### -Zone
代表資源所分派的 IP 必須來自的可用性區域清單。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### PSVirtualMachineScaleSet 中的 [計算] 命令。
參數： VirtualMachineScaleSet (ByValue) 

### [System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

## 輸出

### PSVirtualMachineScaleSet 中的 [計算] 命令。

## 筆記

## 相關連結

[AzureRmVmss](./Get-AzureRmVmss.md)

[移除-AzureRmVmss](./Remove-AzureRmVmss.md)

[重新開機-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[開始-AzureRmVmss](./Start-AzureRmVmss.md)

[停止 AzureRmVmss](./Stop-AzureRmVmss.md)

[更新-AzureRmVmss](./Update-AzureRmVmss.md)


