---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624446"
---
# <span data-ttu-id="069ab-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-101">New-AzureRmVM</span></span>

## <span data-ttu-id="069ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="069ab-102">SYNOPSIS</span></span>
<span data-ttu-id="069ab-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="069ab-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="069ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="069ab-104">SYNTAX</span></span>

### <span data-ttu-id="069ab-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="069ab-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="069ab-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="069ab-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="069ab-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="069ab-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="069ab-108">說明</span><span class="sxs-lookup"><span data-stu-id="069ab-108">DESCRIPTION</span></span>
<span data-ttu-id="069ab-109">**新的-AzureRmVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="069ab-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="069ab-110">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="069ab-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="069ab-111">使用 New-AzureRmVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="069ab-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="069ab-112">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="069ab-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="069ab-113">您可以透過將 `SimpleParameterSet` 常見的 VM 建立引數設為選用，提供一種便利的方法來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="069ab-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="069ab-114">示例</span><span class="sxs-lookup"><span data-stu-id="069ab-114">EXAMPLES</span></span>

### <span data-ttu-id="069ab-115">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="069ab-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="069ab-116">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="069ab-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="069ab-117">此腳本會要求 VM 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="069ab-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="069ab-118">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="069ab-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="069ab-119">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="069ab-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="069ab-120">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="069ab-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="069ab-121">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="069ab-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="069ab-122">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="069ab-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="069ab-123">您可以使用 **AzureSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="069ab-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="069ab-124">範例3：從不含公用 IP 的 marketplace 影像建立 VM</span><span class="sxs-lookup"><span data-stu-id="069ab-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="069ab-125">這個範例會為您置備新的網路，並從 Marketplace 部署 Windows VM，而不需建立公用 IP 位址或網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="069ab-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="069ab-126">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="069ab-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="069ab-127">參數</span><span class="sxs-lookup"><span data-stu-id="069ab-127">PARAMETERS</span></span>

### <span data-ttu-id="069ab-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="069ab-128">-AddressPrefix</span></span>
<span data-ttu-id="069ab-129">將針對 VM 建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="069ab-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="069ab-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="069ab-130">-AllocationMethod</span></span>
<span data-ttu-id="069ab-131">將針對 VM 建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="069ab-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="069ab-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="069ab-132">-AsJob</span></span>
<span data-ttu-id="069ab-133">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="069ab-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="069ab-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="069ab-134">-AvailabilitySetName</span></span>
<span data-ttu-id="069ab-135">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="069ab-136">-認證</span><span class="sxs-lookup"><span data-stu-id="069ab-136">-Credential</span></span>
<span data-ttu-id="069ab-137">VM 的管理員認證。</span><span class="sxs-lookup"><span data-stu-id="069ab-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="069ab-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="069ab-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="069ab-139">指定資料磁片的大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="069ab-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="069ab-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="069ab-140">-DefaultProfile</span></span>
<span data-ttu-id="069ab-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="069ab-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="069ab-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="069ab-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="069ab-143">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="069ab-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="069ab-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="069ab-144">-DiskFile</span></span>
<span data-ttu-id="069ab-145">要上傳到雲端及建立 VM 的虛擬硬碟檔案的本機路徑，其後綴必須是 ".vhd"。</span><span class="sxs-lookup"><span data-stu-id="069ab-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="069ab-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="069ab-146">-DomainNameLabel</span></span>
<span data-ttu-id="069ab-147">[完全合格的功能變數名稱] 的子域標籤 (VM 的 FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="069ab-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="069ab-148">這將會採用該表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="069ab-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="069ab-149">-影像</span><span class="sxs-lookup"><span data-stu-id="069ab-149">-Image</span></span>
<span data-ttu-id="069ab-150">可在其上建立 VM 的友好影像名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="069ab-151">這些包括： Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="069ab-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="069ab-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="069ab-152">-LicenseType</span></span>
<span data-ttu-id="069ab-153">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="069ab-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="069ab-154">這個值只適用于包含 Windows Server 作業系統的影像。</span><span class="sxs-lookup"><span data-stu-id="069ab-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="069ab-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="069ab-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="069ab-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="069ab-156">Windows_Client</span></span>
- <span data-ttu-id="069ab-157">Windows_Server 此值無法更新。</span><span class="sxs-lookup"><span data-stu-id="069ab-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="069ab-158">如果您指定此參數進行更新，則此值必須符合虛擬機器的初始值。</span><span class="sxs-lookup"><span data-stu-id="069ab-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="069ab-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="069ab-159">-Linux</span></span>
<span data-ttu-id="069ab-160">指出磁片檔案是否適用于 Linux VM （如果已指定的話）;如果未指定預設，則為 Windows。</span><span class="sxs-lookup"><span data-stu-id="069ab-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="069ab-161">-位置</span><span class="sxs-lookup"><span data-stu-id="069ab-161">-Location</span></span>
<span data-ttu-id="069ab-162">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="069ab-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="069ab-163">-名稱</span><span class="sxs-lookup"><span data-stu-id="069ab-163">-Name</span></span>
<span data-ttu-id="069ab-164">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="069ab-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="069ab-165">-OpenPorts</span></span>
<span data-ttu-id="069ab-166">在已建立的 VM 的網路安全性群組 (NSG) 上開啟的埠清單。</span><span class="sxs-lookup"><span data-stu-id="069ab-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="069ab-167">預設值取決於您所選取的影像類型 (亦即 Windows：3389、5985和 Linux： 22) 。</span><span class="sxs-lookup"><span data-stu-id="069ab-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="069ab-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="069ab-168">-PublicIpAddressName</span></span>
<span data-ttu-id="069ab-169">已建立之 VM 要使用的新 (或現有) 公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="069ab-170">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="069ab-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="069ab-171">-ResourceGroupName</span></span>
<span data-ttu-id="069ab-172">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="069ab-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="069ab-173">-SecurityGroupName</span></span>
<span data-ttu-id="069ab-174">已建立的要使用之 VM (NSG) 的新 (或現有) 網路安全群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="069ab-175">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="069ab-176">-大小</span><span class="sxs-lookup"><span data-stu-id="069ab-176">-Size</span></span>
<span data-ttu-id="069ab-177">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="069ab-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="069ab-178">預設值為： Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="069ab-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="069ab-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="069ab-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="069ab-180">將針對 VM 建立之子網上的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="069ab-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="069ab-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="069ab-181">-SubnetName</span></span>
<span data-ttu-id="069ab-182">已建立的 VM 要使用的新 (或現有) 子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="069ab-183">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="069ab-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="069ab-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="069ab-185">如果該參數存在，則會將 VM 指派為自動產生的受管理系統身分識別。</span><span class="sxs-lookup"><span data-stu-id="069ab-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="069ab-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="069ab-186">-Tag</span></span>
<span data-ttu-id="069ab-187">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="069ab-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="069ab-188">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="069ab-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="069ab-189">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="069ab-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="069ab-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="069ab-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="069ab-191">應該指派給 VM 之受管理服務身分識別的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="069ab-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="069ab-192">-VirtualNetworkName</span></span>
<span data-ttu-id="069ab-193">已建立的 VM 要使用的新 (或現有) 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="069ab-194">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="069ab-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="069ab-195">-VM</span><span class="sxs-lookup"><span data-stu-id="069ab-195">-VM</span></span>
<span data-ttu-id="069ab-196">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="069ab-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="069ab-197">若要取得虛擬機器物件，請使用 New-AzureRmVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="069ab-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="069ab-198">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage 和 Add AzureRmVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="069ab-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="069ab-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="069ab-199">-Zone</span></span>
<span data-ttu-id="069ab-200">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="069ab-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="069ab-201">-確認</span><span class="sxs-lookup"><span data-stu-id="069ab-201">-Confirm</span></span>
<span data-ttu-id="069ab-202">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="069ab-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="069ab-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="069ab-203">-WhatIf</span></span>
<span data-ttu-id="069ab-204">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="069ab-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="069ab-205">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="069ab-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="069ab-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069ab-206">CommonParameters</span></span>
<span data-ttu-id="069ab-207">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="069ab-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069ab-208">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="069ab-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069ab-209">輸入</span><span class="sxs-lookup"><span data-stu-id="069ab-209">INPUTS</span></span>

### <span data-ttu-id="069ab-210">System.object</span><span class="sxs-lookup"><span data-stu-id="069ab-210">System.String</span></span>

### <span data-ttu-id="069ab-211">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="069ab-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="069ab-212">System.object []</span><span class="sxs-lookup"><span data-stu-id="069ab-212">System.String[]</span></span>

### <span data-ttu-id="069ab-213">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="069ab-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="069ab-214">輸出</span><span class="sxs-lookup"><span data-stu-id="069ab-214">OUTPUTS</span></span>

### <span data-ttu-id="069ab-215">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="069ab-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="069ab-216">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="069ab-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="069ab-217">筆記</span><span class="sxs-lookup"><span data-stu-id="069ab-217">NOTES</span></span>

## <span data-ttu-id="069ab-218">相關連結</span><span class="sxs-lookup"><span data-stu-id="069ab-218">RELATED LINKS</span></span>

[<span data-ttu-id="069ab-219">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="069ab-220">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="069ab-221">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="069ab-222">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="069ab-223">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="069ab-224">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="069ab-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="069ab-225">附加 AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="069ab-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="069ab-226">附加 AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="069ab-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="069ab-227">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="069ab-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="069ab-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="069ab-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="069ab-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="069ab-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="069ab-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="069ab-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


