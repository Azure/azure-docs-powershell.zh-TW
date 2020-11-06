---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 04c51df96a538b32fa42454980ccd4f8cd1f7282
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622753"
---
# <span data-ttu-id="0eac0-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-101">New-AzVM</span></span>

## <span data-ttu-id="0eac0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eac0-102">SYNOPSIS</span></span>
<span data-ttu-id="0eac0-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0eac0-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="0eac0-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eac0-104">SYNTAX</span></span>

### <span data-ttu-id="0eac0-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0eac0-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eac0-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eac0-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eac0-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eac0-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eac0-108">說明</span><span class="sxs-lookup"><span data-stu-id="0eac0-108">DESCRIPTION</span></span>
<span data-ttu-id="0eac0-109">**新的-AzVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0eac0-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="0eac0-110">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="0eac0-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="0eac0-111">使用 New-AzVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="0eac0-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="0eac0-112">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="0eac0-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="0eac0-113">您可以透過將 `SimpleParameterSet` 常見的 VM 建立引數設為選用，提供一種便利的方法來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="0eac0-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="0eac0-114">示例</span><span class="sxs-lookup"><span data-stu-id="0eac0-114">EXAMPLES</span></span>

### <span data-ttu-id="0eac0-115">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="0eac0-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="0eac0-116">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0eac0-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="0eac0-117">此腳本會要求 VM 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="0eac0-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="0eac0-118">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eac0-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="0eac0-119">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="0eac0-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="0eac0-120">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="0eac0-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="0eac0-121">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="0eac0-122">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0eac0-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="0eac0-123">您可以使用 **AzSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="0eac0-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="0eac0-124">範例3：從不含公用 IP 的 marketplace 影像建立 VM</span><span class="sxs-lookup"><span data-stu-id="0eac0-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="0eac0-125">這個範例會為您置備新的網路，並從 Marketplace 部署 Windows VM，而不需建立公用 IP 位址或網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="0eac0-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="0eac0-126">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="0eac0-127">參數</span><span class="sxs-lookup"><span data-stu-id="0eac0-127">PARAMETERS</span></span>

### <span data-ttu-id="0eac0-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0eac0-128">-AddressPrefix</span></span>
<span data-ttu-id="0eac0-129">將針對 VM 建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="0eac0-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="0eac0-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="0eac0-130">-AllocationMethod</span></span>
<span data-ttu-id="0eac0-131">將針對 VM 建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="0eac0-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="0eac0-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eac0-132">-AsJob</span></span>
<span data-ttu-id="0eac0-133">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="0eac0-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0eac0-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="0eac0-134">-AvailabilitySetName</span></span>
<span data-ttu-id="0eac0-135">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="0eac0-136">-認證</span><span class="sxs-lookup"><span data-stu-id="0eac0-136">-Credential</span></span>
<span data-ttu-id="0eac0-137">VM 的管理員認證。</span><span class="sxs-lookup"><span data-stu-id="0eac0-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="0eac0-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="0eac0-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="0eac0-139">指定資料磁片的大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="0eac0-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="0eac0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eac0-140">-DefaultProfile</span></span>
<span data-ttu-id="0eac0-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eac0-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="0eac0-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="0eac0-143">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="0eac0-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="0eac0-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="0eac0-144">-DiskFile</span></span>
<span data-ttu-id="0eac0-145">要上傳到雲端及建立 VM 的虛擬硬碟檔案的本機路徑，其後綴必須是 ".vhd"。</span><span class="sxs-lookup"><span data-stu-id="0eac0-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="0eac0-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="0eac0-146">-DomainNameLabel</span></span>
<span data-ttu-id="0eac0-147">[完全合格的功能變數名稱] 的子域標籤 (VM 的 FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="0eac0-148">這將會採用該表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="0eac0-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="0eac0-149">-EnableUltraSSD</span></span>
<span data-ttu-id="0eac0-150">針對 vm 使用 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="0eac0-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="0eac0-151">-影像</span><span class="sxs-lookup"><span data-stu-id="0eac0-151">-Image</span></span>
<span data-ttu-id="0eac0-152">可在其上建立 VM 的友好影像名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-152">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="0eac0-153">這些包括： Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="0eac0-153">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="0eac0-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0eac0-154">-LicenseType</span></span>
<span data-ttu-id="0eac0-155">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="0eac0-155">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="0eac0-156">這個值只適用于包含 Windows Server 作業系統的影像。</span><span class="sxs-lookup"><span data-stu-id="0eac0-156">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="0eac0-157">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eac0-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eac0-158">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="0eac0-158">Windows_Client</span></span>
- <span data-ttu-id="0eac0-159">Windows_Server 此值無法更新。</span><span class="sxs-lookup"><span data-stu-id="0eac0-159">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="0eac0-160">如果您指定此參數進行更新，則此值必須符合虛擬機器的初始值。</span><span class="sxs-lookup"><span data-stu-id="0eac0-160">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="0eac0-161">-Linux</span><span class="sxs-lookup"><span data-stu-id="0eac0-161">-Linux</span></span>
<span data-ttu-id="0eac0-162">指出磁片檔案是否適用于 Linux VM （如果已指定的話）;如果未指定預設，則為 Windows。</span><span class="sxs-lookup"><span data-stu-id="0eac0-162">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="0eac0-163">-位置</span><span class="sxs-lookup"><span data-stu-id="0eac0-163">-Location</span></span>
<span data-ttu-id="0eac0-164">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="0eac0-164">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="0eac0-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eac0-165">-Name</span></span>
<span data-ttu-id="0eac0-166">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-166">The name of the VM resource.</span></span>

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

### <span data-ttu-id="0eac0-167">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="0eac0-167">-OpenPorts</span></span>
<span data-ttu-id="0eac0-168">在已建立的 VM 的網路安全性群組 (NSG) 上開啟的埠清單。</span><span class="sxs-lookup"><span data-stu-id="0eac0-168">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="0eac0-169">預設值取決於您所選取的影像類型 (亦即 Windows：3389、5985和 Linux： 22) 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-169">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="0eac0-170">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="0eac0-170">-PublicIpAddressName</span></span>
<span data-ttu-id="0eac0-171">已建立之 VM 要使用的新 (或現有) 公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-171">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="0eac0-172">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-172">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="0eac0-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eac0-173">-ResourceGroupName</span></span>
<span data-ttu-id="0eac0-174">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-174">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0eac0-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="0eac0-175">-SecurityGroupName</span></span>
<span data-ttu-id="0eac0-176">已建立的要使用之 VM (NSG) 的新 (或現有) 網路安全群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-176">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="0eac0-177">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-177">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="0eac0-178">-大小</span><span class="sxs-lookup"><span data-stu-id="0eac0-178">-Size</span></span>
<span data-ttu-id="0eac0-179">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="0eac0-179">The Virtual Machine Size.</span></span>  <span data-ttu-id="0eac0-180">預設值為： Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="0eac0-180">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="0eac0-181">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0eac0-181">-SubnetAddressPrefix</span></span>
<span data-ttu-id="0eac0-182">將針對 VM 建立之子網上的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="0eac0-182">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="0eac0-183">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0eac0-183">-SubnetName</span></span>
<span data-ttu-id="0eac0-184">已建立的 VM 要使用的新 (或現有) 子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-184">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="0eac0-185">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="0eac0-186">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0eac0-186">-SystemAssignedIdentity</span></span>
<span data-ttu-id="0eac0-187">如果該參數存在，則會將 VM 指派為自動產生的受管理系統身分識別。</span><span class="sxs-lookup"><span data-stu-id="0eac0-187">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="0eac0-188">-Tag</span><span class="sxs-lookup"><span data-stu-id="0eac0-188">-Tag</span></span>
<span data-ttu-id="0eac0-189">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="0eac0-189">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="0eac0-190">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="0eac0-190">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="0eac0-191">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="0eac0-191">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="0eac0-192">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0eac0-192">-UserAssignedIdentity</span></span>
<span data-ttu-id="0eac0-193">應該指派給 VM 之受管理服務身分識別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-193">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="0eac0-194">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0eac0-194">-VirtualNetworkName</span></span>
<span data-ttu-id="0eac0-195">已建立的 VM 要使用的新 (或現有) 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-195">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="0eac0-196">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="0eac0-196">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="0eac0-197">-VM</span><span class="sxs-lookup"><span data-stu-id="0eac0-197">-VM</span></span>
<span data-ttu-id="0eac0-198">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0eac0-198">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="0eac0-199">若要取得虛擬機器物件，請使用 New-AzVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eac0-199">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="0eac0-200">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage 和 Add AzVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="0eac0-200">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="0eac0-201">-Zone</span><span class="sxs-lookup"><span data-stu-id="0eac0-201">-Zone</span></span>
<span data-ttu-id="0eac0-202">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="0eac0-202">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="0eac0-203">-確認</span><span class="sxs-lookup"><span data-stu-id="0eac0-203">-Confirm</span></span>
<span data-ttu-id="0eac0-204">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0eac0-204">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eac0-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eac0-205">-WhatIf</span></span>
<span data-ttu-id="0eac0-206">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eac0-206">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eac0-207">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eac0-207">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eac0-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eac0-208">CommonParameters</span></span>
<span data-ttu-id="0eac0-209">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eac0-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eac0-210">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0eac0-210">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eac0-211">輸入</span><span class="sxs-lookup"><span data-stu-id="0eac0-211">INPUTS</span></span>

### <span data-ttu-id="0eac0-212">System.object</span><span class="sxs-lookup"><span data-stu-id="0eac0-212">System.String</span></span>

### <span data-ttu-id="0eac0-213">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0eac0-213">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0eac0-214">System.object []</span><span class="sxs-lookup"><span data-stu-id="0eac0-214">System.String[]</span></span>

### <span data-ttu-id="0eac0-215">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0eac0-215">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0eac0-216">輸出</span><span class="sxs-lookup"><span data-stu-id="0eac0-216">OUTPUTS</span></span>

### <span data-ttu-id="0eac0-217">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0eac0-217">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="0eac0-218">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0eac0-218">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0eac0-219">筆記</span><span class="sxs-lookup"><span data-stu-id="0eac0-219">NOTES</span></span>

## <span data-ttu-id="0eac0-220">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eac0-220">RELATED LINKS</span></span>

[<span data-ttu-id="0eac0-221">AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-221">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0eac0-222">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-222">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0eac0-223">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-223">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="0eac0-224">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-224">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="0eac0-225">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-225">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0eac0-226">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eac0-226">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="0eac0-227">附加 AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0eac0-227">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="0eac0-228">附加 AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0eac0-228">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="0eac0-229">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0eac0-229">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="0eac0-230">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0eac0-230">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="0eac0-231">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="0eac0-231">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="0eac0-232">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0eac0-232">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


