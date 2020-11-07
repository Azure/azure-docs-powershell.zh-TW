---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796125"
---
# <span data-ttu-id="633b5-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-101">New-AzVM</span></span>

## <span data-ttu-id="633b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="633b5-102">SYNOPSIS</span></span>
<span data-ttu-id="633b5-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="633b5-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="633b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="633b5-104">SYNTAX</span></span>

### <span data-ttu-id="633b5-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="633b5-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633b5-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="633b5-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633b5-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="633b5-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="633b5-108">說明</span><span class="sxs-lookup"><span data-stu-id="633b5-108">DESCRIPTION</span></span>
<span data-ttu-id="633b5-109">**新的-AzVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="633b5-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="633b5-110">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="633b5-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="633b5-111">使用 New-AzVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="633b5-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="633b5-112">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="633b5-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="633b5-113">您可以透過將 `SimpleParameterSet` 常見的 VM 建立引數設為選用，提供一種便利的方法來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="633b5-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="633b5-114">示例</span><span class="sxs-lookup"><span data-stu-id="633b5-114">EXAMPLES</span></span>

### <span data-ttu-id="633b5-115">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="633b5-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="633b5-116">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="633b5-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="633b5-117">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="633b5-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="633b5-118">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="633b5-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="633b5-119">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="633b5-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="633b5-120">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="633b5-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="633b5-121">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="633b5-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="633b5-122">您可以使用 **AzureSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="633b5-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="633b5-123">參數</span><span class="sxs-lookup"><span data-stu-id="633b5-123">PARAMETERS</span></span>

### <span data-ttu-id="633b5-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="633b5-124">-AddressPrefix</span></span>
<span data-ttu-id="633b5-125">將針對 VM 建立之虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="633b5-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="633b5-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="633b5-126">-AllocationMethod</span></span>
<span data-ttu-id="633b5-127">將針對 VM 建立之公用 IP 的 IP 配置方法。</span><span class="sxs-lookup"><span data-stu-id="633b5-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="633b5-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="633b5-128">-AsJob</span></span>
<span data-ttu-id="633b5-129">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="633b5-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="633b5-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="633b5-130">-AvailabilitySetName</span></span>
<span data-ttu-id="633b5-131">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="633b5-132">-認證</span><span class="sxs-lookup"><span data-stu-id="633b5-132">-Credential</span></span>
<span data-ttu-id="633b5-133">VM 的管理員認證。</span><span class="sxs-lookup"><span data-stu-id="633b5-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="633b5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633b5-134">-DefaultProfile</span></span>
<span data-ttu-id="633b5-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="633b5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="633b5-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="633b5-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="633b5-137">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="633b5-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="633b5-138">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="633b5-138">-DiskFile</span></span>
<span data-ttu-id="633b5-139">要上傳到雲端及建立 VM 的虛擬硬碟檔案的本機路徑，其後綴必須是 ".vhd"。</span><span class="sxs-lookup"><span data-stu-id="633b5-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="633b5-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="633b5-140">-DomainNameLabel</span></span>
<span data-ttu-id="633b5-141">[完全合格的功能變數名稱] 的子域標籤 (VM 的 FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="633b5-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="633b5-142">這將會採用該表單 `{domainNameLabel}.{location}.cloudapp.azure.com` 。</span><span class="sxs-lookup"><span data-stu-id="633b5-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="633b5-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="633b5-143">-ImageName</span></span>
<span data-ttu-id="633b5-144">可在其上建立 VM 的友好影像名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="633b5-145">這些包括： Win2016Datacenter、Win2012R2Datacenter、Win2012Datacenter、Win2008R2SP1、UbuntuLTS、CentOS、CoreOS、Debian、openSUSE、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="633b5-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="633b5-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="633b5-146">-LicenseType</span></span>
<span data-ttu-id="633b5-147">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="633b5-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="633b5-148">這個值只適用于包含 Windows Server 作業系統的影像。</span><span class="sxs-lookup"><span data-stu-id="633b5-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="633b5-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="633b5-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="633b5-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="633b5-150">Windows_Client</span></span> 
- <span data-ttu-id="633b5-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="633b5-151">Windows_Server</span></span>

<span data-ttu-id="633b5-152">此值無法更新。</span><span class="sxs-lookup"><span data-stu-id="633b5-152">This value cannot be updated.</span></span>
<span data-ttu-id="633b5-153">如果您指定此參數進行更新，則此值必須符合虛擬機器的初始值。</span><span class="sxs-lookup"><span data-stu-id="633b5-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="633b5-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="633b5-154">-Linux</span></span>
<span data-ttu-id="633b5-155">指出磁片檔案是否適用于 Linux VM （如果已指定的話）;如果未指定預設，則為 Windows。</span><span class="sxs-lookup"><span data-stu-id="633b5-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="633b5-156">-位置</span><span class="sxs-lookup"><span data-stu-id="633b5-156">-Location</span></span>
<span data-ttu-id="633b5-157">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="633b5-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="633b5-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="633b5-158">-Name</span></span>
<span data-ttu-id="633b5-159">VM 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="633b5-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="633b5-160">-OpenPorts</span></span>
<span data-ttu-id="633b5-161">在已建立的 VM 的網路安全性群組 (NSG) 上開啟的埠清單。</span><span class="sxs-lookup"><span data-stu-id="633b5-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="633b5-162">預設值取決於您所選取的影像類型 (亦即 Windows：3389、5985和 Linux： 22) 。</span><span class="sxs-lookup"><span data-stu-id="633b5-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="633b5-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="633b5-163">-PublicIpAddressName</span></span>
<span data-ttu-id="633b5-164">已建立之 VM 要使用的新 (或現有) 公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="633b5-165">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="633b5-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633b5-166">-ResourceGroupName</span></span>
<span data-ttu-id="633b5-167">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="633b5-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="633b5-168">-SecurityGroupName</span></span>
<span data-ttu-id="633b5-169">已建立的要使用之 VM (NSG) 的新 (或現有) 網路安全群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="633b5-170">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="633b5-171">-大小</span><span class="sxs-lookup"><span data-stu-id="633b5-171">-Size</span></span>
<span data-ttu-id="633b5-172">虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="633b5-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="633b5-173">預設值為： Standard_DS1_v2。</span><span class="sxs-lookup"><span data-stu-id="633b5-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="633b5-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="633b5-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="633b5-175">將針對 VM 建立之子網上的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="633b5-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="633b5-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="633b5-176">-SubnetName</span></span>
<span data-ttu-id="633b5-177">已建立的 VM 要使用的新 (或現有) 子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="633b5-178">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="633b5-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="633b5-179">-Tag</span></span>
<span data-ttu-id="633b5-180">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="633b5-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="633b5-181">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="633b5-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="633b5-182">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="633b5-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="633b5-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="633b5-183">-VirtualNetworkName</span></span>
<span data-ttu-id="633b5-184">已建立的 VM 要使用的新 (或現有) 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="633b5-185">如果未指定，將會產生名稱。</span><span class="sxs-lookup"><span data-stu-id="633b5-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="633b5-186">-VM</span><span class="sxs-lookup"><span data-stu-id="633b5-186">-VM</span></span>
<span data-ttu-id="633b5-187">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="633b5-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="633b5-188">若要取得虛擬機器物件，請使用 New-AzVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="633b5-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="633b5-189">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzVMOperatingSystem、AzVMSourceImage 和 Add AzVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="633b5-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="633b5-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="633b5-190">-Zone</span></span>
<span data-ttu-id="633b5-191">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="633b5-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="633b5-192">-確認</span><span class="sxs-lookup"><span data-stu-id="633b5-192">-Confirm</span></span>
<span data-ttu-id="633b5-193">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="633b5-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="633b5-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="633b5-194">-WhatIf</span></span>
<span data-ttu-id="633b5-195">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="633b5-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="633b5-196">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="633b5-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="633b5-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633b5-197">CommonParameters</span></span>
<span data-ttu-id="633b5-198">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="633b5-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633b5-199">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="633b5-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633b5-200">輸入</span><span class="sxs-lookup"><span data-stu-id="633b5-200">INPUTS</span></span>

### <span data-ttu-id="633b5-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="633b5-201">PSVirtualMachine</span></span>
<span data-ttu-id="633b5-202">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="633b5-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="633b5-203">輸出</span><span class="sxs-lookup"><span data-stu-id="633b5-203">OUTPUTS</span></span>

### <span data-ttu-id="633b5-204">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="633b5-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="633b5-205">筆記</span><span class="sxs-lookup"><span data-stu-id="633b5-205">NOTES</span></span>

## <span data-ttu-id="633b5-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="633b5-206">RELATED LINKS</span></span>

[<span data-ttu-id="633b5-207">AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="633b5-208">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="633b5-209">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="633b5-210">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="633b5-211">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="633b5-212">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="633b5-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="633b5-213">附加 AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="633b5-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="633b5-214">附加 AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="633b5-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="633b5-215">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="633b5-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="633b5-216">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="633b5-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="633b5-217">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="633b5-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="633b5-218">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="633b5-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


