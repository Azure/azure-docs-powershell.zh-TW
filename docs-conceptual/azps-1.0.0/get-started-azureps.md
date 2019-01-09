---
title: 開始使用 Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982904"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="75f61-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="75f61-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="75f61-103">Azure PowerShell 的設計是為了讓您從命令列管理 Azure 資源，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。</span><span class="sxs-lookup"><span data-stu-id="75f61-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="75f61-104">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或者將它安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="75f61-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="75f61-105">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="75f61-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="75f61-106">安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="75f61-106">Install Azure PowerShell</span></span>

<span data-ttu-id="75f61-107">第一步是確定您已安裝最新版的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="75f61-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="75f61-108">如需最新版本的相關資訊，請參閱[版本資訊](./release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="75f61-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="75f61-109">[安裝 Azure PowerShell](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="75f61-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="75f61-110">若要確認安裝是否成功，請從命令列執行 `Get-InstalledModule Az -AllVersions`。</span><span class="sxs-lookup"><span data-stu-id="75f61-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="75f61-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="75f61-111">Azure Cloud Shell</span></span>

<span data-ttu-id="75f61-112">若要開始使用，最簡單的方式就是[啟動 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="75f61-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="75f61-113">從 Azure 入口網站的頂端導覽啟動 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="75f61-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 圖示](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="75f61-115">選擇您想使用的訂用帳戶，並建立儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="75f61-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![建立儲存體帳戶](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="75f61-117">一旦您建立儲存體之後，Cloud Shell 會在瀏覽器中開啟 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="75f61-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![適用於 PowerShell 的 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="75f61-119">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="75f61-119">Sign in to Azure</span></span>

<span data-ttu-id="75f61-120">以互動方式登入︰</span><span class="sxs-lookup"><span data-stu-id="75f61-120">Sign on interactively:</span></span>

1. <span data-ttu-id="75f61-121">輸入 `Connect-AzAccount`。</span><span class="sxs-lookup"><span data-stu-id="75f61-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="75f61-122">`-Environment` 引數可讓您針對不同區域或雲端進行驗證。</span><span class="sxs-lookup"><span data-stu-id="75f61-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="75f61-123">例如，若要連線至 Azure China：</span><span class="sxs-lookup"><span data-stu-id="75f61-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="75f61-124">您會獲得在 https://microsoft.com/devicelogin 上使用的權杖。</span><span class="sxs-lookup"><span data-stu-id="75f61-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="75f61-125">在瀏覽器中開啟此頁面，並輸入權杖以使用 Azure 認證來登入，然後授權 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="75f61-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="75f61-126">在登入 Azure 帳戶後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="75f61-127">若要深入了解登入程序和可用的驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="75f61-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="75f61-128">使用簡單的預設值建立 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="75f61-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="75f61-129">`New-AzVM` Cmdlet 提供簡化的語法，讓您能輕鬆地建立新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="75f61-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="75f61-130">您只需提供兩個參數值，分別是 VM 的名稱，以及一組 VM 上本機系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="75f61-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="75f61-131">首先，建立認證物件。</span><span class="sxs-lookup"><span data-stu-id="75f61-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="75f61-132">接著，建立 VM。</span><span class="sxs-lookup"><span data-stu-id="75f61-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="75f61-133">您可能會好奇是不是還建立了其他項目，以及 VM 是如何設定的。</span><span class="sxs-lookup"><span data-stu-id="75f61-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="75f61-134">先來看看我們的資源群組。</span><span class="sxs-lookup"><span data-stu-id="75f61-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="75f61-135">您第一次使用 Cloud Shell 時會建立 **cloud-shell-storage-westus** 資源群組。</span><span class="sxs-lookup"><span data-stu-id="75f61-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="75f61-136">**SampleVM** 資源群組是由 `New-AzVM` Cmdlet 建立。</span><span class="sxs-lookup"><span data-stu-id="75f61-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="75f61-137">現在，在這個新的資源群組中還建立了哪些其他的資源？</span><span class="sxs-lookup"><span data-stu-id="75f61-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="75f61-138">讓我們取得更多關於 VM 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="75f61-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="75f61-139">此範例說明如何擷取用來建立 VM 的 OS 映像相關資訊。</span><span class="sxs-lookup"><span data-stu-id="75f61-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="75f61-140">建立設定完整的 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="75f61-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="75f61-141">前面的範例使用簡化的語法和預設參數值來建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="75f61-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="75f61-142">在這個範例中，我們為虛擬機器提供所有選項的值。</span><span class="sxs-lookup"><span data-stu-id="75f61-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="75f61-143">建立資源群組</span><span class="sxs-lookup"><span data-stu-id="75f61-143">Create a resource group</span></span>

<span data-ttu-id="75f61-144">在此範例中，我們要建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="75f61-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="75f61-145">對於您想要以邏輯方式群組在一起的多個資源，Azure 的資源群組可讓您有辦法管理這些資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="75f61-146">例如，您可以為應用程式或專案建立資源群組，並在該群組中新增虛擬機器、資料庫和 CDN 服務。</span><span class="sxs-lookup"><span data-stu-id="75f61-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="75f61-147">讓我們建立一個名為「MyResourceGroup」的資源群組，位置則定在 Azure 的 uswest2 區域。</span><span class="sxs-lookup"><span data-stu-id="75f61-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="75f61-148">若要這麼做，請輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="75f61-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="75f61-149">這個新的資源群組將會納入建立新 VM 所需的所有資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="75f61-150">若要建立新的 Linux VM，我們必須先建立其他必要資源，並將它們指派至某組態。</span><span class="sxs-lookup"><span data-stu-id="75f61-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="75f61-151">然後，我們可以使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="75f61-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="75f61-152">此外，您在使用者設定檔的 `.ssh` 目錄中需要有一個名為 `id_rsa.pub` 的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="75f61-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="75f61-153">建立必要的網路資源</span><span class="sxs-lookup"><span data-stu-id="75f61-153">Create the required network resources</span></span>

<span data-ttu-id="75f61-154">首先，我們需要建立一個子網路組態，以用於虛擬網路的建立程序。</span><span class="sxs-lookup"><span data-stu-id="75f61-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="75f61-155">我們也會建立公用 IP 位址，以便可以連線到此 VM。</span><span class="sxs-lookup"><span data-stu-id="75f61-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="75f61-156">我們會建立網路安全性群組，來保護對於公用位址的存取。</span><span class="sxs-lookup"><span data-stu-id="75f61-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="75f61-157">最後，我們會使用前面的所有資源來建立虛擬 NIC。</span><span class="sxs-lookup"><span data-stu-id="75f61-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="75f61-158">建立 VM 組態</span><span class="sxs-lookup"><span data-stu-id="75f61-158">Create the VM configuration</span></span>

<span data-ttu-id="75f61-159">我們已擁有所需的資源，可以建立 VM 組態物件了。</span><span class="sxs-lookup"><span data-stu-id="75f61-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="75f61-160">建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="75f61-160">Create the virtual machine</span></span>

<span data-ttu-id="75f61-161">現在，我們可以使用 VM 組態物件來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="75f61-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="75f61-162">VM 已建立完成，現在您可以搭配使用 SSH 與您所建立之 VM 的公用 IP 位址，來登入新的 Linux VM︰</span><span class="sxs-lookup"><span data-stu-id="75f61-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="75f61-163">在 Azure 中建立其他資源</span><span class="sxs-lookup"><span data-stu-id="75f61-163">Creating other resources in Azure</span></span>

<span data-ttu-id="75f61-164">我們已逐步瀏覽過如何建立資源群組、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="75f61-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="75f61-165">您也可以建立其他許多類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="75f61-166">例如，若要建立 Azure 網路負載平衡器，然後與我們新建立的 VM 相關聯，我們可以使用下列建立命令︰</span><span class="sxs-lookup"><span data-stu-id="75f61-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="75f61-167">我們也可以使用下列命令，為我們的基礎結構建立新的私人虛擬網路 (此網路在 Azure 中通常稱為「VNet」)︰</span><span class="sxs-lookup"><span data-stu-id="75f61-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="75f61-168">Azure 和 Azure PowerShell 的功能之所以強大，是因為它們不只能用來獲得雲端架構的基礎結構，還能用來建立受控平台服務。</span><span class="sxs-lookup"><span data-stu-id="75f61-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="75f61-169">受控平台服務也可以結合基礎結構來建置更強大的解決方案。</span><span class="sxs-lookup"><span data-stu-id="75f61-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="75f61-170">例如，您可以使用 Azure PowerShell 來建立 Azure AppService。</span><span class="sxs-lookup"><span data-stu-id="75f61-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="75f61-171">Azure AppService 是一種受控平台服務，它可讓您裝載 Web 應用程式，而不必擔心基礎結構的問題。</span><span class="sxs-lookup"><span data-stu-id="75f61-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="75f61-172">在建立 Azure AppService 之後，您可以使用下列命令在 AppService 內建立兩個新的 Azure Web Apps︰</span><span class="sxs-lookup"><span data-stu-id="75f61-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="75f61-173">列出已部署的資源</span><span class="sxs-lookup"><span data-stu-id="75f61-173">Listing deployed resources</span></span>

<span data-ttu-id="75f61-174">您可以使用 `Get-AzResource` Cmdlet 來列出 Azure 內所執行的資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="75f61-175">下列範例顯示我們在新的資源群組中建立的資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="75f61-176">刪除資源</span><span class="sxs-lookup"><span data-stu-id="75f61-176">Deleting resources</span></span>

<span data-ttu-id="75f61-177">為了清除 Azure 帳戶，您想要移除我們已在此範例中建立的資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="75f61-178">您可以使用 `Remove-Az*` Cmdlet 來刪除您不再需要的資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="75f61-179">若要移除我們已建立的 Windows VM，請使用下列命令︰</span><span class="sxs-lookup"><span data-stu-id="75f61-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="75f61-180">系統會提示您確認您想要移除資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="75f61-181">您也可以一次刪除許多資源。</span><span class="sxs-lookup"><span data-stu-id="75f61-181">You can also delete many resources at once.</span></span> <span data-ttu-id="75f61-182">例如，下列命令會刪除我們在目前為止的所有範例中使用的資源群組 "MyResourceGroup"。</span><span class="sxs-lookup"><span data-stu-id="75f61-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="75f61-183">該群組中的所有資源也會一併刪除。</span><span class="sxs-lookup"><span data-stu-id="75f61-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="75f61-184">此工作可能需要幾分鐘才能完成，視資源的數量和類型而定。</span><span class="sxs-lookup"><span data-stu-id="75f61-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="75f61-185">取得範例</span><span class="sxs-lookup"><span data-stu-id="75f61-185">Get samples</span></span>

<span data-ttu-id="75f61-186">若要深入了解如何使用 Azure PowerShell，請參閱我們針對 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 和 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 所提供的最常見指令碼。</span><span class="sxs-lookup"><span data-stu-id="75f61-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="75f61-187">後續步驟</span><span class="sxs-lookup"><span data-stu-id="75f61-187">Next steps</span></span>

* [<span data-ttu-id="75f61-188">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="75f61-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="75f61-189">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="75f61-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="75f61-190">使用 Azure PowerShell 在 Azure 中建立服務主體</span><span class="sxs-lookup"><span data-stu-id="75f61-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="75f61-191">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="75f61-191">Get help from the community:</span></span>
  * [<span data-ttu-id="75f61-192">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="75f61-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="75f61-193">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="75f61-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
