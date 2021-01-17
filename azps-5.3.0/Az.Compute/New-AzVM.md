---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 21c15b0395479a1a22e6b8420a97a3a7c0b75bce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449807"
---
# <span data-ttu-id="3b629-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-101">New-AzVM</span></span>

## <span data-ttu-id="3b629-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b629-102">SYNOPSIS</span></span>
<span data-ttu-id="3b629-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="3b629-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b629-104">SYNTAX</span></span>

### <span data-ttu-id="3b629-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b629-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b629-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b629-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b629-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b629-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b629-108">說明</span><span class="sxs-lookup"><span data-stu-id="3b629-108">DESCRIPTION</span></span>
<span data-ttu-id="3b629-109">**新的-AzVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="3b629-110">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="3b629-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="3b629-111">使用 New-AzVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="3b629-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="3b629-112">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="3b629-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="3b629-113">您可以透過將 `SimpleParameterSet` 常見的 VM 建立引數設為選用，提供一種便利的方法來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="3b629-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="3b629-114">示例</span><span class="sxs-lookup"><span data-stu-id="3b629-114">EXAMPLES</span></span>

### <span data-ttu-id="3b629-115">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3b629-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="3b629-116">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="3b629-117">此腳本會要求 VM 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="3b629-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="3b629-118">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b629-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="3b629-119">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3b629-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="3b629-120">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="3b629-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="3b629-121">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="3b629-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="3b629-122">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3b629-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="3b629-123">您可以使用 **AzSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="3b629-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="3b629-124">範例3：從不含公用 IP 的 marketplace 影像建立 VM</span><span class="sxs-lookup"><span data-stu-id="3b629-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="3b629-125">這個範例會為您置備新的網路，並從 Marketplace 部署 Windows VM，而不需建立公用 IP 位址或網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3b629-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="3b629-126">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="3b629-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="3b629-127">參數</span><span class="sxs-lookup"><span data-stu-id="3b629-127">PARAMETERS</span></span>

### <span data-ttu-id="3b629-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b629-128">-AddressPrefix</span></span>
<span data-ttu-id="3b629-129">將針對 VM 建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3b629-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3b629-130">-AllocationMethod</span></span>
<span data-ttu-id="3b629-131">將針對 VM 建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="3b629-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b629-132">-AsJob</span></span>
<span data-ttu-id="3b629-133">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3b629-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b629-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="3b629-134">-AvailabilitySetName</span></span>
<span data-ttu-id="3b629-135">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-136">-認證</span><span class="sxs-lookup"><span data-stu-id="3b629-136">-Credential</span></span>
<span data-ttu-id="3b629-137">VM 的管理員認證。</span><span class="sxs-lookup"><span data-stu-id="3b629-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="3b629-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="3b629-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="3b629-139">指定資料磁片的大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="3b629-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b629-140">-DefaultProfile</span></span>
<span data-ttu-id="3b629-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b629-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b629-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="3b629-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="3b629-143">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="3b629-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="3b629-144">-DiskFile</span></span>
<span data-ttu-id="3b629-145">要上傳到雲端及建立 VM 的虛擬硬碟檔案的本機路徑，其後綴必須是 ".vhd"。</span><span class="sxs-lookup"><span data-stu-id="3b629-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3b629-146">-DomainNameLabel</span></span>
<span data-ttu-id="3b629-147">[完全合格的功能變數名稱] 的子域標籤 (VM 的 FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="3b629-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="3b629-148">這將會採用該表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="3b629-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="3b629-149">-EnableUltraSSD</span></span>
<span data-ttu-id="3b629-150">針對 vm 使用 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="3b629-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b629-151">-EvictionPolicy</span></span>
<span data-ttu-id="3b629-152">Azure 點虛擬機器的逐出原則。</span><span class="sxs-lookup"><span data-stu-id="3b629-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="3b629-153">支援的值為 "解除配置" 和 "Delete"。</span><span class="sxs-lookup"><span data-stu-id="3b629-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="3b629-154">-HostGroupId</span></span>
<span data-ttu-id="3b629-155">指定虛擬機器將駐留的專用主機群組。</span><span class="sxs-lookup"><span data-stu-id="3b629-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="3b629-156">-HostId</span></span>
<span data-ttu-id="3b629-157">主機的識別碼</span><span class="sxs-lookup"><span data-stu-id="3b629-157">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-158">-影像</span><span class="sxs-lookup"><span data-stu-id="3b629-158">-Image</span></span>
<span data-ttu-id="3b629-159">可在其上建立 VM 的友好影像名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="3b629-160">這些包括： Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="3b629-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3b629-161">-LicenseType</span></span>
<span data-ttu-id="3b629-162">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="3b629-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="3b629-163">Windows Server 可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="3b629-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="3b629-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="3b629-164">Windows_Client</span></span>
- <span data-ttu-id="3b629-165">Windows_Server 的 Linux Server 作業系統可能值為：</span><span class="sxs-lookup"><span data-stu-id="3b629-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="3b629-166">RHEL) 的 RHEL_BYOS (</span><span class="sxs-lookup"><span data-stu-id="3b629-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="3b629-167">SUSE) 的 SLES_BYOS (</span><span class="sxs-lookup"><span data-stu-id="3b629-167">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="3b629-168">-Linux</span></span>
<span data-ttu-id="3b629-169">指出磁片檔案是否適用于 Linux VM （如果已指定的話）;如果未指定預設，則為 Windows。</span><span class="sxs-lookup"><span data-stu-id="3b629-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-170">-位置</span><span class="sxs-lookup"><span data-stu-id="3b629-170">-Location</span></span>
<span data-ttu-id="3b629-171">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="3b629-171">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="3b629-172">-MaxPrice</span></span>
<span data-ttu-id="3b629-173">低優先順序虛擬機器的帳單最大價格。</span><span class="sxs-lookup"><span data-stu-id="3b629-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3b629-174">-EncryptionAtHost</span></span>
<span data-ttu-id="3b629-175">使用者可以在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器規模設定的主機加密。</span><span class="sxs-lookup"><span data-stu-id="3b629-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="3b629-176">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="3b629-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="3b629-177">預設：除非針對資源將此屬性設為 true，否則將停用主機上的加密。</span><span class="sxs-lookup"><span data-stu-id="3b629-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="3b629-178">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b629-178">-Name</span></span>
<span data-ttu-id="3b629-179">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-179">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="3b629-180">-OpenPorts</span></span>
<span data-ttu-id="3b629-181">在已建立的 VM 的網路安全性群組 (NSG) 上開啟的埠清單。</span><span class="sxs-lookup"><span data-stu-id="3b629-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="3b629-182">預設值取決於您所選取的影像類型 (亦即 Windows：3389、5985和 Linux： 22) 。</span><span class="sxs-lookup"><span data-stu-id="3b629-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-183">-優先順序</span><span class="sxs-lookup"><span data-stu-id="3b629-183">-Priority</span></span>
<span data-ttu-id="3b629-184">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="3b629-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="3b629-185">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="3b629-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="3b629-186">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="3b629-187">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="3b629-188">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="3b629-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="3b629-189">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="3b629-189">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3b629-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3b629-191">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b629-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="3b629-192">-PublicIpAddressName</span></span>
<span data-ttu-id="3b629-193">已建立之 VM 要使用的新 (或現有) 公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="3b629-194">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b629-195">-ResourceGroupName</span></span>
<span data-ttu-id="3b629-196">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-196">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="3b629-197">-SecurityGroupName</span></span>
<span data-ttu-id="3b629-198">已建立的要使用之 VM (NSG) 的新 (或現有) 網路安全群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="3b629-199">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-199">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-200">-大小</span><span class="sxs-lookup"><span data-stu-id="3b629-200">-Size</span></span>
<span data-ttu-id="3b629-201">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="3b629-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="3b629-202">預設值為： Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="3b629-202">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b629-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="3b629-204">將針對 VM 建立之子網上的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3b629-204">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3b629-205">-SubnetName</span></span>
<span data-ttu-id="3b629-206">已建立的 VM 要使用的新 (或現有) 子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="3b629-207">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-207">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b629-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="3b629-209">如果該參數存在，則會將 VM 指派為自動產生的受管理系統身分識別。</span><span class="sxs-lookup"><span data-stu-id="3b629-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-210">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b629-210">-Tag</span></span>
<span data-ttu-id="3b629-211">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="3b629-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3b629-212">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="3b629-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3b629-213">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="3b629-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b629-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="3b629-215">應該指派給 VM 之受管理服務身分識別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-215">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3b629-216">-VirtualNetworkName</span></span>
<span data-ttu-id="3b629-217">已建立的 VM 要使用的新 (或現有) 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="3b629-218">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3b629-218">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-219">-VM</span><span class="sxs-lookup"><span data-stu-id="3b629-219">-VM</span></span>
<span data-ttu-id="3b629-220">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3b629-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="3b629-221">若要取得虛擬機器物件，請使用 New-AzVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b629-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="3b629-222">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage 和 Add AzVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="3b629-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="3b629-223">-VmssId</span></span>
<span data-ttu-id="3b629-224">此 VM 將與之關聯的虛擬機器規模集識別碼</span><span class="sxs-lookup"><span data-stu-id="3b629-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="3b629-225">-Zone</span></span>
<span data-ttu-id="3b629-226">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="3b629-226">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b629-227">-確認</span><span class="sxs-lookup"><span data-stu-id="3b629-227">-Confirm</span></span>
<span data-ttu-id="3b629-228">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b629-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b629-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b629-229">-WhatIf</span></span>
<span data-ttu-id="3b629-230">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b629-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b629-231">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b629-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b629-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b629-232">CommonParameters</span></span>
<span data-ttu-id="3b629-233">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b629-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b629-234">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b629-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b629-235">輸入</span><span class="sxs-lookup"><span data-stu-id="3b629-235">INPUTS</span></span>

### <span data-ttu-id="3b629-236">System.object</span><span class="sxs-lookup"><span data-stu-id="3b629-236">System.String</span></span>

### <span data-ttu-id="3b629-237">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3b629-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3b629-238">System.object []</span><span class="sxs-lookup"><span data-stu-id="3b629-238">System.String[]</span></span>

### <span data-ttu-id="3b629-239">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b629-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b629-240">輸出</span><span class="sxs-lookup"><span data-stu-id="3b629-240">OUTPUTS</span></span>

### <span data-ttu-id="3b629-241">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3b629-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="3b629-242">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3b629-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3b629-243">筆記</span><span class="sxs-lookup"><span data-stu-id="3b629-243">NOTES</span></span>

## <span data-ttu-id="3b629-244">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b629-244">RELATED LINKS</span></span>

[<span data-ttu-id="3b629-245">AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3b629-246">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3b629-247">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3b629-248">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3b629-249">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3b629-250">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b629-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="3b629-251">附加 AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3b629-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="3b629-252">附加 AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b629-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="3b629-253">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3b629-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="3b629-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3b629-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="3b629-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="3b629-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="3b629-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3b629-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


