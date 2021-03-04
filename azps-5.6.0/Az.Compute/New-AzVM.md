---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: a7fbf991357e63dbe2436350892f9e601eb586db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903030"
---
# <span data-ttu-id="e9415-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e9415-101">New-AzVM</span></span>

## <span data-ttu-id="e9415-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9415-102">SYNOPSIS</span></span>
<span data-ttu-id="e9415-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="e9415-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9415-104">SYNTAX</span></span>

### <span data-ttu-id="e9415-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9415-105">SimpleParameterSet (Default)</span></span>
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

### <span data-ttu-id="e9415-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9415-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9415-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9415-107">DiskFileParameterSet</span></span>
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

## <span data-ttu-id="e9415-108">描述</span><span class="sxs-lookup"><span data-stu-id="e9415-108">DESCRIPTION</span></span>
<span data-ttu-id="e9415-109">**New-AzMS** Cmdlet 在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="e9415-110">此 Cmdlet 會採用虛擬機器物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="e9415-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="e9415-111">使用 New-AzVMConfig Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="e9415-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="e9415-112">其他 Cmdlet 可以用來設定虛擬機器，例如 Set-Az VIRTUALOperatingSystem、Set-Az VIRTUALSourceImage、Add-Az VIRTUALNetworkInterface 和 Set-Az VIRTUALOSSource。</span><span class="sxs-lookup"><span data-stu-id="e9415-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="e9415-113">這項 `SimpleParameterSet` 功能將常見的 VM 建立引數做為選擇性，提供建立 VM 的便利方法。</span><span class="sxs-lookup"><span data-stu-id="e9415-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="e9415-114">例子</span><span class="sxs-lookup"><span data-stu-id="e9415-114">EXAMPLES</span></span>

### <span data-ttu-id="e9415-115">範例 1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="e9415-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="e9415-116">此範例腳本顯示如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="e9415-117">腳本會詢問 VM 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="e9415-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="e9415-118">此腳本使用數個其他 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9415-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="e9415-119">範例 2：從自訂使用者映射建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="e9415-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="e9415-120">此範例會採用現有 sys 預先準備的一般自訂作業系統映射，並將資料磁片附加到該映射、配置新網路、部署 VHD，然後執行它。</span><span class="sxs-lookup"><span data-stu-id="e9415-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="e9415-121">此腳本可用於自動部署，因為它使用本機虛擬機器系統管理員認證內嵌，而不是呼叫需要使用者互動的 **Get-Credential。**</span><span class="sxs-lookup"><span data-stu-id="e9415-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="e9415-122">此腳本假設您已經登入 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e9415-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="e9415-123">您可以使用 **Get-AzSubscription** Cmdlet 確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="e9415-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="e9415-124">範例 3：從沒有公用 IP 的 Marketplace 映射建立 VM</span><span class="sxs-lookup"><span data-stu-id="e9415-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="e9415-125">此範例會提供新網路，並部署來自 Marketplace 的 Windows VM，而不建立公用 IP 位址或網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="e9415-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="e9415-126">此腳本可用於自動部署，因為它使用本機虛擬機器系統管理員認證內嵌，而不是呼叫需要使用者互動的 **Get-Credential。**</span><span class="sxs-lookup"><span data-stu-id="e9415-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="e9415-127">參數</span><span class="sxs-lookup"><span data-stu-id="e9415-127">PARAMETERS</span></span>

### <span data-ttu-id="e9415-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e9415-128">-AddressPrefix</span></span>
<span data-ttu-id="e9415-129">為 VM 所建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="e9415-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="e9415-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="e9415-130">-AllocationMethod</span></span>
<span data-ttu-id="e9415-131">為 VM 所建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="e9415-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="e9415-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9415-132">-AsJob</span></span>
<span data-ttu-id="e9415-133">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e9415-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e9415-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="e9415-134">-AvailabilitySetName</span></span>
<span data-ttu-id="e9415-135">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="e9415-136">-認證</span><span class="sxs-lookup"><span data-stu-id="e9415-136">-Credential</span></span>
<span data-ttu-id="e9415-137">VM 的系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="e9415-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="e9415-138">-Data以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="e9415-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="e9415-139">指定資料磁片的大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="e9415-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="e9415-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9415-140">-DefaultProfile</span></span>
<span data-ttu-id="e9415-141">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9415-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9415-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="e9415-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="e9415-143">表示此 Cmdlet 未在虛擬機器上安裝 **BG 資訊** 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e9415-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="e9415-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="e9415-144">-DiskFile</span></span>
<span data-ttu-id="e9415-145">要上傳至雲端及建立 VM 的虛擬硬碟檔案之本地路徑，其後綴必須是 '.vhd'。</span><span class="sxs-lookup"><span data-stu-id="e9415-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="e9415-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e9415-146">-DomainNameLabel</span></span>
<span data-ttu-id="e9415-147">完整功能變數名稱的子域標籤 (FQDN) 為 VM。</span><span class="sxs-lookup"><span data-stu-id="e9415-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="e9415-148">這會採取表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="e9415-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="e9415-149">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="e9415-149">-EnableUltraSSD</span></span>
<span data-ttu-id="e9415-150">使用 Vm 的 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="e9415-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="e9415-151">-Policy</span><span class="sxs-lookup"><span data-stu-id="e9415-151">-EvictionPolicy</span></span>
<span data-ttu-id="e9415-152">Azure Spot 虛擬機器的回收政策。</span><span class="sxs-lookup"><span data-stu-id="e9415-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="e9415-153">支援的值為 'Deallocate' 和 'Delete'。</span><span class="sxs-lookup"><span data-stu-id="e9415-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="e9415-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="e9415-154">-HostGroupId</span></span>
<span data-ttu-id="e9415-155">指定虛擬機器所在的專用主機群組。</span><span class="sxs-lookup"><span data-stu-id="e9415-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

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

### <span data-ttu-id="e9415-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="e9415-156">-HostId</span></span>
<span data-ttu-id="e9415-157">主機名稱</span><span class="sxs-lookup"><span data-stu-id="e9415-157">The Id of Host</span></span>

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

### <span data-ttu-id="e9415-158">-影像</span><span class="sxs-lookup"><span data-stu-id="e9415-158">-Image</span></span>
<span data-ttu-id="e9415-159">建立 VM 的好用影像名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="e9415-160">這些包括：Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE-Leap、RHEL、SLES。</span><span class="sxs-lookup"><span data-stu-id="e9415-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="e9415-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e9415-161">-LicenseType</span></span>
<span data-ttu-id="e9415-162">指定授權類型，表示虛擬機器的映射或磁片已授權于內部部署。</span><span class="sxs-lookup"><span data-stu-id="e9415-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="e9415-163">Windows Server 的可能值為：</span><span class="sxs-lookup"><span data-stu-id="e9415-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="e9415-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="e9415-164">Windows_Client</span></span>
- <span data-ttu-id="e9415-165">Windows_Server Linux Server 作業系統的可能值有：</span><span class="sxs-lookup"><span data-stu-id="e9415-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="e9415-166">RHEL_BYOS (RHEL) </span><span class="sxs-lookup"><span data-stu-id="e9415-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="e9415-167">SLES_BYOS (SUSE) </span><span class="sxs-lookup"><span data-stu-id="e9415-167">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="e9415-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="e9415-168">-Linux</span></span>
<span data-ttu-id="e9415-169">指出磁片檔案是否適用于 Linux VM ，如果已指定;或 Windows ，如果預設未指定。</span><span class="sxs-lookup"><span data-stu-id="e9415-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="e9415-170">-位置</span><span class="sxs-lookup"><span data-stu-id="e9415-170">-Location</span></span>
<span data-ttu-id="e9415-171">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="e9415-171">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="e9415-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="e9415-172">-MaxPrice</span></span>
<span data-ttu-id="e9415-173">低優先順序虛擬機器帳單的最大價格。</span><span class="sxs-lookup"><span data-stu-id="e9415-173">The max price of the billing of a low priority virtual machine.</span></span>

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

### <span data-ttu-id="e9415-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e9415-174">-EncryptionAtHost</span></span>
<span data-ttu-id="e9415-175">使用者可在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器縮放集的主機加密。</span><span class="sxs-lookup"><span data-stu-id="e9415-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="e9415-176">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="e9415-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="e9415-177">預設：除非資源的此屬性設為 True，否則會停用主機的加密。</span><span class="sxs-lookup"><span data-stu-id="e9415-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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


### <span data-ttu-id="e9415-178">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9415-178">-Name</span></span>
<span data-ttu-id="e9415-179">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-179">The name of the VM resource.</span></span>

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

### <span data-ttu-id="e9415-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="e9415-180">-OpenPorts</span></span>
<span data-ttu-id="e9415-181">在已建立之 VM 的 NSG (上) 的埠清單。</span><span class="sxs-lookup"><span data-stu-id="e9415-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="e9415-182">預設值取決於所選影像類型， (Windows： 3389、5985 和 Linux：22) 。</span><span class="sxs-lookup"><span data-stu-id="e9415-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="e9415-183">-優先順序</span><span class="sxs-lookup"><span data-stu-id="e9415-183">-Priority</span></span>
<span data-ttu-id="e9415-184">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e9415-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="e9415-185">只有支援的值是 "Regular"、'Spot' 和 'Low'。</span><span class="sxs-lookup"><span data-stu-id="e9415-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="e9415-186">"Regular" 適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="e9415-187">"Spot" 適用于 Spot 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="e9415-188">"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。</span><span class="sxs-lookup"><span data-stu-id="e9415-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="e9415-189">請使用 "Spot" 而不是 "Low"。</span><span class="sxs-lookup"><span data-stu-id="e9415-189">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="e9415-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e9415-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e9415-191">要用於此虛擬機器的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9415-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="e9415-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="e9415-192">-PublicIpAddressName</span></span>
<span data-ttu-id="e9415-193">新資料庫的名稱 (或) 建立之 VM 的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e9415-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="e9415-194">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="e9415-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9415-195">-ResourceGroupName</span></span>
<span data-ttu-id="e9415-196">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-196">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e9415-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="e9415-197">-SecurityGroupName</span></span>
<span data-ttu-id="e9415-198">新使用者名稱或 (網路) 組的名稱 (NSG) 建立之 VM 使用。</span><span class="sxs-lookup"><span data-stu-id="e9415-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="e9415-199">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-199">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="e9415-200">-大小</span><span class="sxs-lookup"><span data-stu-id="e9415-200">-Size</span></span>
<span data-ttu-id="e9415-201">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e9415-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="e9415-202">預設值為：Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="e9415-202">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="e9415-203">-子網AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e9415-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="e9415-204">為 VM 所建立之子網的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="e9415-204">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="e9415-205">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="e9415-205">-SubnetName</span></span>
<span data-ttu-id="e9415-206">新資料庫的名稱 (現有) 的 VM 使用。</span><span class="sxs-lookup"><span data-stu-id="e9415-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="e9415-207">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-207">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="e9415-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e9415-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e9415-209">如果參數存在，則系統會為 VM 指派自動產生的受管理系統身分識別。</span><span class="sxs-lookup"><span data-stu-id="e9415-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="e9415-210">-標記</span><span class="sxs-lookup"><span data-stu-id="e9415-210">-Tag</span></span>
<span data-ttu-id="e9415-211">指定可以使用一組名稱值組標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9415-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="e9415-212">將標記新增到資源，可讓您跨資源群組將資源分組，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="e9415-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="e9415-213">每個資源或資源群組最多可以有 15 個標記。</span><span class="sxs-lookup"><span data-stu-id="e9415-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="e9415-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e9415-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="e9415-215">應指派給 VM 的受管理服務身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-215">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="e9415-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e9415-216">-VirtualNetworkName</span></span>
<span data-ttu-id="e9415-217">新使用者名稱 (或) 建立之 VM 使用之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="e9415-218">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="e9415-218">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="e9415-219">-VM</span><span class="sxs-lookup"><span data-stu-id="e9415-219">-VM</span></span>
<span data-ttu-id="e9415-220">指定要建立本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9415-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="e9415-221">若要取得虛擬機器物件，請使用 New-AzVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9415-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="e9415-222">其他 Cmdlet 可以用來設定虛擬機器，例如 Set-Az VIRTUALOperatingSystem、Set-Az VIRTUALSourceImage 和 Add-Az VIRTUALNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="e9415-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="e9415-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="e9415-223">-VmssId</span></span>
<span data-ttu-id="e9415-224">此 VM 所關聯的虛擬機器縮放集識別碼</span><span class="sxs-lookup"><span data-stu-id="e9415-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

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

### <span data-ttu-id="e9415-225">-區域</span><span class="sxs-lookup"><span data-stu-id="e9415-225">-Zone</span></span>
<span data-ttu-id="e9415-226">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="e9415-226">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="e9415-227">-確認</span><span class="sxs-lookup"><span data-stu-id="e9415-227">-Confirm</span></span>
<span data-ttu-id="e9415-228">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9415-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9415-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9415-229">-WhatIf</span></span>
<span data-ttu-id="e9415-230">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9415-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9415-231">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9415-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9415-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9415-232">CommonParameters</span></span>
<span data-ttu-id="e9415-233">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9415-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9415-234">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9415-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9415-235">輸入</span><span class="sxs-lookup"><span data-stu-id="e9415-235">INPUTS</span></span>

### <span data-ttu-id="e9415-236">System.String</span><span class="sxs-lookup"><span data-stu-id="e9415-236">System.String</span></span>

### <span data-ttu-id="e9415-237">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9415-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e9415-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e9415-238">System.String[]</span></span>

### <span data-ttu-id="e9415-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9415-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9415-240">輸出</span><span class="sxs-lookup"><span data-stu-id="e9415-240">OUTPUTS</span></span>

### <span data-ttu-id="e9415-241">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e9415-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="e9415-242">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9415-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e9415-243">筆記</span><span class="sxs-lookup"><span data-stu-id="e9415-243">NOTES</span></span>

## <span data-ttu-id="e9415-244">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9415-244">RELATED LINKS</span></span>

[<span data-ttu-id="e9415-245">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e9415-246">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e9415-247">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e9415-248">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e9415-249">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e9415-250">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="e9415-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="e9415-251">Add-AzDATAData至</span><span class="sxs-lookup"><span data-stu-id="e9415-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="e9415-252">Add-AzEVNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e9415-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="e9415-253">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="e9415-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="e9415-254">Set-AzEVOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9415-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="e9415-255">Set-AzEVSourceImage</span><span class="sxs-lookup"><span data-stu-id="e9415-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="e9415-256">Set-AzEVOSCio</span><span class="sxs-lookup"><span data-stu-id="e9415-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


