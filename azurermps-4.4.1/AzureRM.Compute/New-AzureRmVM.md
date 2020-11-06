---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456824"
---
# <span data-ttu-id="758b4-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-101">New-AzureRmVM</span></span>

## <span data-ttu-id="758b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="758b4-102">SYNOPSIS</span></span>
<span data-ttu-id="758b4-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="758b4-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="758b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="758b4-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="758b4-105">DESCRIPTION</span></span>
<span data-ttu-id="758b4-106">**新的-AzureRmVM** Cmdlet 會在 Azure 中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="758b4-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="758b4-107">這個 Cmdlet 會採用虛擬電腦物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="758b4-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="758b4-108">使用 New-AzureRmVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="758b4-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="758b4-109">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="758b4-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="758b4-110">示例</span><span class="sxs-lookup"><span data-stu-id="758b4-110">EXAMPLES</span></span>

### <span data-ttu-id="758b4-111">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="758b4-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="758b4-112">這個範例腳本說明如何建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="758b4-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="758b4-113">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="758b4-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="758b4-114">範例2：從自訂使用者影像建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="758b4-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="758b4-115">這個範例會採用現有的 sys prepped、通用的自訂作業系統影像，並將資料磁片附加至它、置備新的網路、部署 VHD 並執行。</span><span class="sxs-lookup"><span data-stu-id="758b4-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="758b4-116">此腳本可用於自動進行預配，因為它會使用本機虛擬機器管理員認證（而不是呼叫需要使用者互動的 **取得認證）** 。</span><span class="sxs-lookup"><span data-stu-id="758b4-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="758b4-117">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="758b4-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="758b4-118">您可以使用 **AzureSubscription** Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="758b4-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="758b4-119">參數</span><span class="sxs-lookup"><span data-stu-id="758b4-119">PARAMETERS</span></span>

### <span data-ttu-id="758b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758b4-120">-DefaultProfile</span></span>
<span data-ttu-id="758b4-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="758b4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="758b4-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="758b4-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="758b4-123">表示此 Cmdlet 不會在虛擬機器上安裝 **BG 資訊** 延伸。</span><span class="sxs-lookup"><span data-stu-id="758b4-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="758b4-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="758b4-124">-LicenseType</span></span>
<span data-ttu-id="758b4-125">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="758b4-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="758b4-126">這個值只適用于包含 Windows Server 作業系統的影像。</span><span class="sxs-lookup"><span data-stu-id="758b4-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="758b4-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="758b4-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="758b4-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="758b4-128">Windows_Client</span></span> 
- <span data-ttu-id="758b4-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="758b4-129">Windows_Server</span></span>

<span data-ttu-id="758b4-130">此值無法更新。</span><span class="sxs-lookup"><span data-stu-id="758b4-130">This value cannot be updated.</span></span>
<span data-ttu-id="758b4-131">如果您指定此參數進行更新，則此值必須符合虛擬機器的初始值。</span><span class="sxs-lookup"><span data-stu-id="758b4-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-132">-位置</span><span class="sxs-lookup"><span data-stu-id="758b4-132">-Location</span></span>
<span data-ttu-id="758b4-133">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="758b4-133">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758b4-134">-ResourceGroupName</span></span>
<span data-ttu-id="758b4-135">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="758b4-135">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-136">-標記</span><span class="sxs-lookup"><span data-stu-id="758b4-136">-Tags</span></span>
<span data-ttu-id="758b4-137">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="758b4-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="758b4-138">新增標籤至資源之後，您就可以將資源群組集中在不同的資源群組中，以及建立您自己的視圖。</span><span class="sxs-lookup"><span data-stu-id="758b4-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="758b4-139">每個資源或資源群組最多可以有15個標籤。</span><span class="sxs-lookup"><span data-stu-id="758b4-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-140">-VM</span><span class="sxs-lookup"><span data-stu-id="758b4-140">-VM</span></span>
<span data-ttu-id="758b4-141">指定要建立的本機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="758b4-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="758b4-142">若要取得虛擬機器物件，請使用 New-AzureRmVMConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="758b4-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="758b4-143">您可以使用其他 Cmdlet 來設定虛擬機器，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage 和 Add AzureRmVMNetworkInterface。</span><span class="sxs-lookup"><span data-stu-id="758b4-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="758b4-144">-Zone</span></span>
<span data-ttu-id="758b4-145">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="758b4-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758b4-146">-確認</span><span class="sxs-lookup"><span data-stu-id="758b4-146">-Confirm</span></span>
<span data-ttu-id="758b4-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="758b4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758b4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758b4-148">-WhatIf</span></span>
<span data-ttu-id="758b4-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="758b4-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="758b4-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="758b4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758b4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758b4-151">CommonParameters</span></span>
<span data-ttu-id="758b4-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="758b4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758b4-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="758b4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758b4-154">輸入</span><span class="sxs-lookup"><span data-stu-id="758b4-154">INPUTS</span></span>

## <span data-ttu-id="758b4-155">輸出</span><span class="sxs-lookup"><span data-stu-id="758b4-155">OUTPUTS</span></span>

## <span data-ttu-id="758b4-156">筆記</span><span class="sxs-lookup"><span data-stu-id="758b4-156">NOTES</span></span>

## <span data-ttu-id="758b4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="758b4-157">RELATED LINKS</span></span>

[<span data-ttu-id="758b4-158">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="758b4-159">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="758b4-160">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="758b4-161">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="758b4-162">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="758b4-163">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="758b4-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="758b4-164">附加 AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="758b4-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="758b4-165">附加 AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="758b4-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="758b4-166">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="758b4-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="758b4-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="758b4-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="758b4-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="758b4-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="758b4-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="758b4-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


