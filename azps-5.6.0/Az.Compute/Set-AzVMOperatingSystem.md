---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911750"
---
# <span data-ttu-id="1dc0d-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1dc0d-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="1dc0d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc0d-103">設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="1dc0d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dc0d-104">SYNTAX</span></span>

### <span data-ttu-id="1dc0d-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="1dc0d-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc0d-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="1dc0d-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc0d-107">WindowsDisableMSAGEnt</span><span class="sxs-lookup"><span data-stu-id="1dc0d-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc0d-108">WindowsDisableWINAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="1dc0d-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc0d-109">Linux</span><span class="sxs-lookup"><span data-stu-id="1dc0d-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc0d-110">描述</span><span class="sxs-lookup"><span data-stu-id="1dc0d-110">DESCRIPTION</span></span>
<span data-ttu-id="1dc0d-111">**Set-Az VIRTUALOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="1dc0d-112">您可以指定登入認證、電腦名稱稱和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="1dc0d-113">例子</span><span class="sxs-lookup"><span data-stu-id="1dc0d-113">EXAMPLES</span></span>

### <span data-ttu-id="1dc0d-114">範例 1：設定新虛擬機器的作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="1dc0d-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="1dc0d-115">第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="1dc0d-116">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1dc0d-117">第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="1dc0d-118">如需要詳細資訊，請鍵入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="1dc0d-119">第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1dc0d-120">第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1dc0d-121">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1dc0d-122">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1dc0d-123">接下來四個命令會指派值給變數，以用於下列命令。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="1dc0d-124">由於您可以直接在 **Set-Az%。OPeratingSystem** 命令中指定這些字串，因此此方法僅適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="1dc0d-125">不過，您可能會在腳本中使用這類方法。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="1dc0d-126">最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1dc0d-127">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="1dc0d-128">該命令會針對某些參數使用先前命令中指派的變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="1dc0d-129">範例 2：設定已啟用熱修補功能的新虛擬機器的作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="1dc0d-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="1dc0d-130">第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="1dc0d-131">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1dc0d-132">第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="1dc0d-133">如需要詳細資訊，請鍵入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="1dc0d-134">第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1dc0d-135">第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1dc0d-136">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1dc0d-137">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1dc0d-138">接下來四個命令會指派值給變數，以用於下列命令。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="1dc0d-139">由於您可以直接在 **Set-Az%。OPeratingSystem** 命令中指定這些字串，因此此方法僅適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="1dc0d-140">不過，您可能會在腳本中使用這類方法。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="1dc0d-141">最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1dc0d-142">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="1dc0d-143">該命令會針對某些參數使用先前命令中指派的變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="1dc0d-144">此命令可在虛擬機器上啟用 Hotpatching。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="1dc0d-145">範例 3：設定新 Linux 虛擬機器的作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="1dc0d-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="1dc0d-146">第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="1dc0d-147">如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1dc0d-148">第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="1dc0d-149">如需要詳細資訊，請鍵入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="1dc0d-150">第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1dc0d-151">第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1dc0d-152">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1dc0d-153">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1dc0d-154">接下來兩個命令會指派值給變數，以用於下列命令。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="1dc0d-155">最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1dc0d-156">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="1dc0d-157">該命令會針對某些參數使用先前命令中指派的變數。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="1dc0d-158">該命令將虛擬機器上的修補模式值設定為「AutomaticByPlatform」。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="1dc0d-159">參數</span><span class="sxs-lookup"><span data-stu-id="1dc0d-159">PARAMETERS</span></span>

### <span data-ttu-id="1dc0d-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="1dc0d-160">-ComputerName</span></span>
<span data-ttu-id="1dc0d-161">指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-161">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-162">-認證</span><span class="sxs-lookup"><span data-stu-id="1dc0d-162">-Credential</span></span>
<span data-ttu-id="1dc0d-163">將虛擬機器的使用者名稱和密碼指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1dc0d-164">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1dc0d-165">如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-165">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="1dc0d-166">-CustomData</span></span>
<span data-ttu-id="1dc0d-167">指定要傳遞到虛擬機器的字串。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="1dc0d-168">詳細資訊請參閱 [Azure 虛擬機器上的自訂資料](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="1dc0d-169">**注意：不建議在自訂資料中儲存敏感性資訊。**</span><span class="sxs-lookup"><span data-stu-id="1dc0d-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc0d-170">-DefaultProfile</span></span>
<span data-ttu-id="1dc0d-171">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc0d-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="1dc0d-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="1dc0d-173">表示此 Cmdlet 會停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-173">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="1dc0d-174">-DisableVMAgent</span></span>
<span data-ttu-id="1dc0d-175">停用部署 VM 代理程式。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-175">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="1dc0d-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="1dc0d-177">表示此 Cmdlet 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-177">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="1dc0d-178">-EnableHotpatching</span></span>
<span data-ttu-id="1dc0d-179">讓客戶不需要重新開機，即可修補其 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="1dc0d-180">針對 enableHotpatching，'provisionMSAGEnt' 必須設為 True，而 'patchMode' 必須設為 'AutomaticByPlatform'。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="1dc0d-181">-Linux</span></span>
<span data-ttu-id="1dc0d-182">表示作業系統類型為 Linux。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-182">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="1dc0d-183">-PatchMode</span></span>
<span data-ttu-id="1dc0d-184">指定將來賓內修補模式新修補至IaaS 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="1dc0d-185">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="1dc0d-185">Possible values are:</span></span><br>
<span data-ttu-id="1dc0d-186">**手動** - 您可以控制修補程式對虛擬機器的適用。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="1dc0d-187">您可以手動在 VM 中申請修補程式，以執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="1dc0d-188">在此模式中，自動更新會停用;屬性 WindowsConfiguration.enableAutomaticUpdates 必須為 False</span><span class="sxs-lookup"><span data-stu-id="1dc0d-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="1dc0d-189">**AutomaticByOS** - 作業系統會自動更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="1dc0d-190">WindowsConfiguration.enableAutomaticUpdates 的屬性必須為 True。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="1dc0d-191">**AutomaticByPlatform** - 作業系統會自動更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="1dc0d-192">屬性布布部為 TRUE，且 WindowsConfiguration.enableAutomaticUpdates 必須為 True</span><span class="sxs-lookup"><span data-stu-id="1dc0d-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-193">-ProvisionMSEVAgent</span><span class="sxs-lookup"><span data-stu-id="1dc0d-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="1dc0d-194">表示設定要求虛擬機器代理程式安裝在虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-195">-時區</span><span class="sxs-lookup"><span data-stu-id="1dc0d-195">-TimeZone</span></span>
<span data-ttu-id="1dc0d-196">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="1dc0d-197">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="1dc0d-198">可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)</span><span class="sxs-lookup"><span data-stu-id="1dc0d-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-199">-VM</span><span class="sxs-lookup"><span data-stu-id="1dc0d-199">-VM</span></span>
<span data-ttu-id="1dc0d-200">指定要設定作業系統屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="1dc0d-201">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="1dc0d-202">使用 Cmdlet 建立虛擬機器New-AzVMConfig物件。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="1dc0d-203">-Windows</span></span>
<span data-ttu-id="1dc0d-204">表示作業系統類型為 Windows。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-204">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1dc0d-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="1dc0d-206">指定 WinRM 憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="1dc0d-207">這必須儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-207">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="1dc0d-208">-WinRMHttp</span></span>
<span data-ttu-id="1dc0d-209">表示此作業系統使用 HTTP WinRM。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-209">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="1dc0d-210">-WinRMHttps</span></span>
<span data-ttu-id="1dc0d-211">表示此作業系統使用 HTTPS WinRM。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc0d-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc0d-212">CommonParameters</span></span>
<span data-ttu-id="1dc0d-213">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dc0d-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc0d-214">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dc0d-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc0d-215">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc0d-215">INPUTS</span></span>

### <span data-ttu-id="1dc0d-216">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1dc0d-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1dc0d-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1dc0d-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1dc0d-218">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc0d-218">System.String</span></span>

### <span data-ttu-id="1dc0d-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="1dc0d-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1dc0d-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="1dc0d-220">System.Uri</span></span>

## <span data-ttu-id="1dc0d-221">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc0d-221">OUTPUTS</span></span>

### <span data-ttu-id="1dc0d-222">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1dc0d-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1dc0d-223">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc0d-223">NOTES</span></span>

## <span data-ttu-id="1dc0d-224">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc0d-224">RELATED LINKS</span></span>

[<span data-ttu-id="1dc0d-225">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="1dc0d-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1dc0d-226">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="1dc0d-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


