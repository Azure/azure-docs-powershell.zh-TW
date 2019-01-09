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
# <a name="get-started-with-azure-powershell"></a>開始使用 Azure PowerShell

Azure PowerShell 的設計是為了讓您從命令列管理 Azure 資源，以及讓您建置可對 Azure Resource Manager 起作用的自動化指令碼。 您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或者將它安裝在本機電腦上。 本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。

## <a name="install-azure-powershell"></a>安裝 Azure PowerShell

第一步是確定您已安裝最新版的 Azure PowerShell。 如需最新版本的相關資訊，請參閱[版本資訊](./release-notes-azureps.md)。

1. [安裝 Azure PowerShell](install-az-ps.md)。

2. 若要確認安裝是否成功，請從命令列執行 `Get-InstalledModule Az -AllVersions`。

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

若要開始使用，最簡單的方式就是[啟動 Cloud Shell](/azure/cloud-shell/quickstart)。

1. 從 Azure 入口網站的頂端導覽啟動 Cloud Shell。

   ![Shell 圖示](~/media/get-started-azureps/shell-icon.png)

2. 選擇您想使用的訂用帳戶，並建立儲存體帳戶。

   ![建立儲存體帳戶](~/media/get-started-azureps/storage-prompt.png)

一旦您建立儲存體之後，Cloud Shell 會在瀏覽器中開啟 PowerShell 工作階段。

![適用於 PowerShell 的 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a>登入 Azure

以互動方式登入︰

1. 輸入 `Connect-AzAccount`。 `-Environment` 引數可讓您針對不同區域或雲端進行驗證。 例如，若要連線至 Azure China：

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. 您會獲得在 https://microsoft.com/devicelogin 上使用的權杖。 在瀏覽器中開啟此頁面，並輸入權杖以使用 Azure 認證來登入，然後授權 Azure PowerShell。 

在登入 Azure 帳戶後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。 若要深入了解登入程序和可用的驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>使用簡單的預設值建立 Windows 虛擬機器

`New-AzVM` Cmdlet 提供簡化的語法，讓您能輕鬆地建立新的虛擬機器。 您只需提供兩個參數值，分別是 VM 的名稱，以及一組 VM 上本機系統管理員帳戶的認證。

首先，建立認證物件。

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

接著，建立 VM。

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

您可能會好奇是不是還建立了其他項目，以及 VM 是如何設定的。 先來看看我們的資源群組。

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

您第一次使用 Cloud Shell 時會建立 **cloud-shell-storage-westus** 資源群組。 **SampleVM** 資源群組是由 `New-AzVM` Cmdlet 建立。

現在，在這個新的資源群組中還建立了哪些其他的資源？

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

讓我們取得更多關於 VM 的詳細資料。 此範例說明如何擷取用來建立 VM 的 OS 映像相關資訊。

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a>建立設定完整的 Linux 虛擬機器

前面的範例使用簡化的語法和預設參數值來建立 Windows 虛擬機器。 在這個範例中，我們為虛擬機器提供所有選項的值。

### <a name="create-a-resource-group"></a>建立資源群組

在此範例中，我們要建立資源群組。 對於您想要以邏輯方式群組在一起的多個資源，Azure 的資源群組可讓您有辦法管理這些資源。 例如，您可以為應用程式或專案建立資源群組，並在該群組中新增虛擬機器、資料庫和 CDN 服務。

讓我們建立一個名為「MyResourceGroup」的資源群組，位置則定在 Azure 的 uswest2 區域。 若要這麼做，請輸入下列命令：

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

這個新的資源群組將會納入建立新 VM 所需的所有資源。 若要建立新的 Linux VM，我們必須先建立其他必要資源，並將它們指派至某組態。 然後，我們可以使用該組態來建立 VM。 此外，您在使用者設定檔的 `.ssh` 目錄中需要有一個名為 `id_rsa.pub` 的 SSH 公開金鑰。

#### <a name="create-the-required-network-resources"></a>建立必要的網路資源

首先，我們需要建立一個子網路組態，以用於虛擬網路的建立程序。 我們也會建立公用 IP 位址，以便可以連線到此 VM。 我們會建立網路安全性群組，來保護對於公用位址的存取。 最後，我們會使用前面的所有資源來建立虛擬 NIC。

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

### <a name="create-the-vm-configuration"></a>建立 VM 組態

我們已擁有所需的資源，可以建立 VM 組態物件了。

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

### <a name="create-the-virtual-machine"></a>建立虛擬機器

現在，我們可以使用 VM 組態物件來建立 VM。

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

VM 已建立完成，現在您可以搭配使用 SSH 與您所建立之 VM 的公用 IP 位址，來登入新的 Linux VM︰

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

## <a name="creating-other-resources-in-azure"></a>在 Azure 中建立其他資源

我們已逐步瀏覽過如何建立資源群組、Linux VM 和 Windows Server VM。 您也可以建立其他許多類型的 Azure 資源。

例如，若要建立 Azure 網路負載平衡器，然後與我們新建立的 VM 相關聯，我們可以使用下列建立命令︰

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

我們也可以使用下列命令，為我們的基礎結構建立新的私人虛擬網路 (此網路在 Azure 中通常稱為「VNet」)︰

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Azure 和 Azure PowerShell 的功能之所以強大，是因為它們不只能用來獲得雲端架構的基礎結構，還能用來建立受控平台服務。 受控平台服務也可以結合基礎結構來建置更強大的解決方案。

例如，您可以使用 Azure PowerShell 來建立 Azure AppService。 Azure AppService 是一種受控平台服務，它可讓您裝載 Web 應用程式，而不必擔心基礎結構的問題。 在建立 Azure AppService 之後，您可以使用下列命令在 AppService 內建立兩個新的 Azure Web Apps︰

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a>列出已部署的資源

您可以使用 `Get-AzResource` Cmdlet 來列出 Azure 內所執行的資源。 下列範例顯示我們在新的資源群組中建立的資源。

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

## <a name="deleting-resources"></a>刪除資源

為了清除 Azure 帳戶，您想要移除我們已在此範例中建立的資源。 您可以使用 `Remove-Az*` Cmdlet 來刪除您不再需要的資源。 若要移除我們已建立的 Windows VM，請使用下列命令︰

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

系統會提示您確認您想要移除資源。

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

您也可以一次刪除許多資源。 例如，下列命令會刪除我們在目前為止的所有範例中使用的資源群組 "MyResourceGroup"。
該群組中的所有資源也會一併刪除。

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

此工作可能需要幾分鐘才能完成，視資源的數量和類型而定。

## <a name="get-samples"></a>取得範例

若要深入了解如何使用 Azure PowerShell，請參閱我們針對 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)、[Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 和 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 所提供的最常見指令碼。

## <a name="next-steps"></a>後續步驟

* [使用 Azure PowerShell 登入](authenticate-azureps.md)
* [使用 Azure PowerShell 來管理 Azure 訂用帳戶](manage-subscriptions-azureps.md)
* [使用 Azure PowerShell 在 Azure 中建立服務主體](create-azure-service-principal-azureps.md)
* 從社群獲得協助︰
  * [MSDN 上的 Azure 論壇](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
