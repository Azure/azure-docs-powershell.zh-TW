---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446371"
---
# <span data-ttu-id="3a3f1-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-101">New-AzureRmVM</span></span>

## <span data-ttu-id="3a3f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3f1-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a3f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a3f1-104">SYNTAX</span></span>

### <span data-ttu-id="3a3f1-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a3f1-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3f1-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a3f1-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3f1-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a3f1-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a3f1-108">說明</span><span class="sxs-lookup"><span data-stu-id="3a3f1-108">DESCRIPTION</span></span>
<span data-ttu-id="3a3f1-109">**新的-AzureRmVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="3a3f1-110">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="3a3f1-111">使用 New-AzureRmVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="3a3f1-112">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="3a3f1-113">您可以透過將 `SimpleParameterSet` 常見的 VM 建立引數設為選用，提供一種便利的方法來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="3a3f1-114">示例</span><span class="sxs-lookup"><span data-stu-id="3a3f1-114">EXAMPLES</span></span>

### <span data-ttu-id="3a3f1-115">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3a3f1-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="3a3f1-116">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="3a3f1-117">此腳本會要求 VM 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="3a3f1-118">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="3a3f1-119">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3a3f1-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="3a3f1-120">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="3a3f1-121">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="3a3f1-122">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="3a3f1-123">您可以使用 **AzureSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="3a3f1-124">參數</span><span class="sxs-lookup"><span data-stu-id="3a3f1-124">PARAMETERS</span></span>

### <span data-ttu-id="3a3f1-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3a3f1-125">-AddressPrefix</span></span>
<span data-ttu-id="3a3f1-126">將針對 VM 建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3a3f1-127">-AllocationMethod</span></span>
<span data-ttu-id="3a3f1-128">將針對 VM 建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a3f1-129">-AsJob</span></span>
<span data-ttu-id="3a3f1-130">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-130">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3a3f1-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-131">-AvailabilitySetName</span></span>
<span data-ttu-id="3a3f1-132">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-133">-認證</span><span class="sxs-lookup"><span data-stu-id="3a3f1-133">-Credential</span></span>
<span data-ttu-id="3a3f1-134">VM 的管理員認證。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-134">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="3a3f1-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="3a3f1-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="3a3f1-136">指定資料磁片的大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3f1-137">-DefaultProfile</span></span>
<span data-ttu-id="3a3f1-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a3f1-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="3a3f1-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="3a3f1-140">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="3a3f1-141">-DiskFile</span></span>
<span data-ttu-id="3a3f1-142">要上傳到雲端及建立 VM 的虛擬硬碟檔案的本機路徑，其後綴必須是 ".vhd"。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3a3f1-143">-DomainNameLabel</span></span>
<span data-ttu-id="3a3f1-144">[完全合格的功能變數名稱] 的子域標籤 (VM 的 FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="3a3f1-145">這將會採用該表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-146">-ImageName</span></span>
<span data-ttu-id="3a3f1-147">可在其上建立 VM 的友好影像名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="3a3f1-148">這些包括： Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="3a3f1-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3a3f1-149">-LicenseType</span></span>
<span data-ttu-id="3a3f1-150">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="3a3f1-151">這個值只適用于包含 Windows Server 作業系統的影像。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="3a3f1-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3a3f1-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a3f1-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="3a3f1-153">Windows_Client</span></span>
- <span data-ttu-id="3a3f1-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="3a3f1-154">Windows_Server</span></span>

<span data-ttu-id="3a3f1-155">此值無法更新。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-155">This value cannot be updated.</span></span>
<span data-ttu-id="3a3f1-156">如果您指定此參數進行更新，則此值必須符合虛擬機器的初始值。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="3a3f1-157">-Linux</span></span>
<span data-ttu-id="3a3f1-158">指出磁片檔案是否適用于 Linux VM （如果已指定的話）;如果未指定預設，則為 Windows。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-159">-位置</span><span class="sxs-lookup"><span data-stu-id="3a3f1-159">-Location</span></span>
<span data-ttu-id="3a3f1-160">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-161">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a3f1-161">-Name</span></span>
<span data-ttu-id="3a3f1-162">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="3a3f1-163">-OpenPorts</span></span>
<span data-ttu-id="3a3f1-164">在已建立的 VM 的網路安全性群組 (NSG) 上開啟的埠清單。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="3a3f1-165">預設值取決於您所選取的影像類型 (亦即 Windows：3389、5985和 Linux： 22) 。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-166">-PublicIpAddressName</span></span>
<span data-ttu-id="3a3f1-167">已建立之 VM 要使用的新 (或現有) 公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="3a3f1-168">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-169">-ResourceGroupName</span></span>
<span data-ttu-id="3a3f1-170">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-171">-SecurityGroupName</span></span>
<span data-ttu-id="3a3f1-172">已建立的要使用之 VM (NSG) 的新 (或現有) 網路安全群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="3a3f1-173">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-174">-大小</span><span class="sxs-lookup"><span data-stu-id="3a3f1-174">-Size</span></span>
<span data-ttu-id="3a3f1-175">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="3a3f1-176">預設值為： Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3a3f1-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="3a3f1-178">將針對 VM 建立之子網上的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-179">-SubnetName</span></span>
<span data-ttu-id="3a3f1-180">已建立的 VM 要使用的新 (或現有) 子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="3a3f1-181">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a3f1-182">-Tag</span></span>
<span data-ttu-id="3a3f1-183">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3a3f1-184">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3a3f1-185">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3a3f1-186">-VirtualNetworkName</span></span>
<span data-ttu-id="3a3f1-187">已建立的 VM 要使用的新 (或現有) 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="3a3f1-188">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-189">-VM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-189">-VM</span></span>
<span data-ttu-id="3a3f1-190">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="3a3f1-191">若要取得虛擬機器物件，請使用 New-AzureRmVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="3a3f1-192">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage 和 Add AzureRmVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="3a3f1-193">-Zone</span></span>
<span data-ttu-id="3a3f1-194">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f1-195">-確認</span><span class="sxs-lookup"><span data-stu-id="3a3f1-195">-Confirm</span></span>
<span data-ttu-id="3a3f1-196">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3f1-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3f1-197">-WhatIf</span></span>
<span data-ttu-id="3a3f1-198">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3a3f1-199">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3f1-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3f1-200">CommonParameters</span></span>
<span data-ttu-id="3a3f1-201">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3f1-202">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a3f1-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3f1-203">輸入</span><span class="sxs-lookup"><span data-stu-id="3a3f1-203">INPUTS</span></span>

### <span data-ttu-id="3a3f1-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3a3f1-204">PSVirtualMachine</span></span>
<span data-ttu-id="3a3f1-205">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="3a3f1-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3a3f1-206">輸出</span><span class="sxs-lookup"><span data-stu-id="3a3f1-206">OUTPUTS</span></span>

### <span data-ttu-id="3a3f1-207">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3a3f1-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3a3f1-208">筆記</span><span class="sxs-lookup"><span data-stu-id="3a3f1-208">NOTES</span></span>

## <span data-ttu-id="3a3f1-209">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a3f1-209">RELATED LINKS</span></span>

[<span data-ttu-id="3a3f1-210">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3a3f1-211">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="3a3f1-212">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="3a3f1-213">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="3a3f1-214">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="3a3f1-215">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a3f1-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="3a3f1-216">附加 AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a3f1-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="3a3f1-217">附加 AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a3f1-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="3a3f1-218">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="3a3f1-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="3a3f1-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3a3f1-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="3a3f1-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="3a3f1-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="3a3f1-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3a3f1-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


