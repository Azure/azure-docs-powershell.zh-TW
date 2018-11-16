---
title: 開始使用 Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 7eb5e3fad31b5a92be1cfb36aefdaa7b920bae5f
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575955"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="8ca9c-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ca9c-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="8ca9c-103">Azure PowerShell 的設計是為了讓您從命令列管理 Azure 資源，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="8ca9c-104">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或可將它安裝在本機電腦上，並在任何 PowerShell 工作階段中使用它。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="8ca9c-105">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="8ca9c-106">連線</span><span class="sxs-lookup"><span data-stu-id="8ca9c-106">Connect</span></span>

<span data-ttu-id="8ca9c-107">若要開始使用，最簡單的方式就是[啟動 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="8ca9c-108">從 Azure 入口網站的頂端導覽啟動 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 圖示](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="8ca9c-110">選擇您想使用的訂用帳戶，並建立儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![建立儲存體帳戶](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="8ca9c-112">一旦您建立儲存體之後，Cloud Shell 會在瀏覽器中開啟 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![適用於 PowerShell 的 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="8ca9c-114">您也可以安裝 Azure PowerShell，並在本機 PowerShell 工作階段中使用。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="8ca9c-115">安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ca9c-115">Install Azure PowerShell</span></span>

<span data-ttu-id="8ca9c-116">第一步是確定您已安裝最新版的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="8ca9c-117">如需最新版本的相關資訊，請參閱[版本資訊](./release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="8ca9c-118">[安裝 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="8ca9c-119">若要確認安裝是否成功，請從命令列執行 `Get-Module AzureRM -ListAvailable`。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-119">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="8ca9c-120">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="8ca9c-120">Sign in to Azure</span></span>

<span data-ttu-id="8ca9c-121">以互動方式登入︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-121">Sign on interactively:</span></span>

1. <span data-ttu-id="8ca9c-122">輸入 `Login-AzureRmAccount`。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="8ca9c-123">您會看到對話方塊，裡面會要求您提供 Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="8ca9c-124">選項 [-EnvironmentName] 可讓您驗證 Azure China 或 Azure Germany。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-124">Option '-EnvironmentName' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="8ca9c-125">例如 Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="8ca9c-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="8ca9c-126">輸入與您帳戶相關聯的電子郵件地址和密碼。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="8ca9c-127">Azure 會驗證並儲存認證資訊，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="8ca9c-128">在登入 Azure 帳戶後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="8ca9c-129">建立資源群組</span><span class="sxs-lookup"><span data-stu-id="8ca9c-129">Create a resource group</span></span>

<span data-ttu-id="8ca9c-130">一切都已準備就緒，接下來我們要使用 Azure PowerShell 在 Azure 中建立資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="8ca9c-131">首先，建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-131">First, create a Resource Group.</span></span> <span data-ttu-id="8ca9c-132">對於您想要以邏輯方式群組在一起的多個資源，Azure 的資源群組可讓您有辦法管理這些資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="8ca9c-133">例如，您可以為應用程式或專案建立資源群組，並在該群組中新增虛擬機器、資料庫和 CDN 服務。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="8ca9c-134">讓我們建立一個名為「MyResourceGroup」的資源群組，位置則定在 Azure 的 westeurope 區域。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="8ca9c-135">若要這麼做，請輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="8ca9c-135">To do so type the following command:</span></span>

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="8ca9c-136">建立 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8ca9c-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="8ca9c-137">我們已擁有資源群組，接著我們要在其中建立 Windows VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="8ca9c-138">若要建立新的 VM，我們必須先建立其他必要資源，並將它們指派至某組態。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="8ca9c-139">然後，我們可以使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="8ca9c-140">建立必要的網路資源</span><span class="sxs-lookup"><span data-stu-id="8ca9c-140">Create the required network resources</span></span>

<span data-ttu-id="8ca9c-141">首先，我們需要建立一個子網路組態，以用於虛擬網路的建立程序。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="8ca9c-142">我們也會建立公用 IP 位址，以便可以連線到此 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="8ca9c-143">我們會建立網路安全性群組，來保護對於公用位址的存取。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="8ca9c-144">最後，我們會使用前面的所有資源來建立虛擬 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="8ca9c-145">建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8ca9c-145">Create the virtual machine</span></span>

<span data-ttu-id="8ca9c-146">首先，我們需要一組作業系統認證。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-146">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="8ca9c-147">我們已擁有所需的資源，因此可以建立 VM 了。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="8ca9c-148">在此步驟中，我們會建立 VM 組態物件，然後使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="8ca9c-149">在 VM 整個建立好並可供使用之後，`New-AzureRmVM` 命令會輸出結果。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="8ca9c-150">現在，使用遠端桌面和 VM 的公用 IP 位址來登入新建立的 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-150">Now sign in to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="8ca9c-151">下列命令會顯示前面的指令碼所建立的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="8ca9c-152">如果您所在的系統是 Windows 架構，您可以從命令列使用 mstsc 命令來執行此作業︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="8ca9c-153">提供您在建立 VM 時所使用的相同使用者名稱/密碼組合來進行登入。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-153">Supply the same username/password combination you used when creating the VM to sign in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="8ca9c-154">建立 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8ca9c-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="8ca9c-155">若要建立新的 Linux VM，我們必須先建立其他必要資源，並將它們指派至某組態。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="8ca9c-156">然後，我們可以使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="8ca9c-157">其假設前提是您已如先前所示方式建立了資源群組。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="8ca9c-158">此外，您在使用者設定檔的 .ssh 目錄中需要有一個名為 `id_rsa.pub` 的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="8ca9c-159">建立必要的網路資源</span><span class="sxs-lookup"><span data-stu-id="8ca9c-159">Create the required network resources</span></span>

<span data-ttu-id="8ca9c-160">首先，我們需要建立一個子網路組態，以用於虛擬網路的建立程序。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="8ca9c-161">我們也會建立公用 IP 位址，以便可以連線到此 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="8ca9c-162">我們會建立網路安全性群組，來保護對於公用位址的存取。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="8ca9c-163">最後，我們會使用前面的所有資源來建立虛擬 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="8ca9c-164">建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8ca9c-164">Create the virtual machine</span></span>

<span data-ttu-id="8ca9c-165">我們已擁有所需的資源，因此可以建立 VM 了。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="8ca9c-166">在此步驟中，我們會建立 VM 組態物件，然後使用該組態來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="8ca9c-167">VM 已經建立好，因此您可以搭配使用 SSH 與您所建立之 VM 的公用 IP 位址，來登入新的 Linux VM︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="8ca9c-168">在 Azure 中建立其他資源</span><span class="sxs-lookup"><span data-stu-id="8ca9c-168">Creating other resources in Azure</span></span>

<span data-ttu-id="8ca9c-169">我們已逐步瀏覽過如何建立資源群組、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="8ca9c-170">您也可以建立其他許多類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="8ca9c-171">例如，若要建立 Azure 網路負載平衡器，然後與我們新建立的 VM 相關聯，我們可以使用下列建立命令︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="8ca9c-172">我們也可以使用下列命令，為我們的基礎結構建立新的私人虛擬網路 (此網路在 Azure 中通常稱為「VNet」)︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="8ca9c-173">Azure 和 Azure PowerShell 的功能之所以強大，是因為它們不只能用來獲得雲端架構的基礎結構，還能用來建立受控平台服務。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="8ca9c-174">受控平台服務也可以結合基礎結構來建置更強大的解決方案。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="8ca9c-175">例如，您可以使用 Azure PowerShell 來建立 Azure AppService。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="8ca9c-176">Azure AppService 是一種受控平台服務，它可讓您裝載 Web 應用程式，而不必擔心基礎結構的問題。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="8ca9c-177">在建立 Azure AppService 之後，您可以使用下列命令在 AppService 內建立兩個新的 Azure Web Apps︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="8ca9c-178">列出已部署的資源</span><span class="sxs-lookup"><span data-stu-id="8ca9c-178">Listing deployed resources</span></span>

<span data-ttu-id="8ca9c-179">您可以使用 `Get-AzureRmResource` Cmdlet 來列出 Azure 內所執行的資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="8ca9c-180">下列範例顯示我們剛才在新的資源群組中所建立的資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-180">The following example shows the resources we just created in the new resource group.</span></span>

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="8ca9c-181">刪除資源</span><span class="sxs-lookup"><span data-stu-id="8ca9c-181">Deleting resources</span></span>

<span data-ttu-id="8ca9c-182">為了清除 Azure 帳戶，您想要移除我們已在此範例中建立的資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="8ca9c-183">您可以使用 `Remove-AzureRm*` Cmdlet 來刪除您不再需要的資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="8ca9c-184">若要移除我們已建立的 Windows VM，請使用下列命令︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="8ca9c-185">系統會提示您確認您想要移除資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8ca9c-186">您也可以一次刪除許多資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="8ca9c-187">例如，下列命令會將資源群組「MyResourceGroup」整個刪除，之前我們將這個群組用於此快速入門教學課程中的所有範例。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="8ca9c-188">這會移除資源群組和其中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-188">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8ca9c-189">這可能需要數分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="8ca9c-190">取得範例</span><span class="sxs-lookup"><span data-stu-id="8ca9c-190">Get samples</span></span>

<span data-ttu-id="8ca9c-191">若要深入了解如何使用 Azure PowerShell，請參閱我們針對 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 和 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 所提供的最常見指令碼。</span><span class="sxs-lookup"><span data-stu-id="8ca9c-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8ca9c-192">後續步驟</span><span class="sxs-lookup"><span data-stu-id="8ca9c-192">Next steps</span></span>

* [<span data-ttu-id="8ca9c-193">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="8ca9c-193">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="8ca9c-194">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="8ca9c-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="8ca9c-195">使用 Azure PowerShell 在 Azure 中建立服務主體</span><span class="sxs-lookup"><span data-stu-id="8ca9c-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="8ca9c-196">參閱從較舊版本進行移轉的相關版本資訊：[https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="8ca9c-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="8ca9c-197">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="8ca9c-197">Get help from the community:</span></span>
  * [<span data-ttu-id="8ca9c-198">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="8ca9c-198">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="8ca9c-199">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="8ca9c-199">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
