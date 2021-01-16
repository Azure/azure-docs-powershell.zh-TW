---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276640"
---
# <span data-ttu-id="dfc3d-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dfc3d-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="dfc3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfc3d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc3d-103">設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="dfc3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfc3d-104">SYNTAX</span></span>

### <span data-ttu-id="dfc3d-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="dfc3d-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfc3d-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="dfc3d-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfc3d-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="dfc3d-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfc3d-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="dfc3d-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfc3d-109">Linux</span><span class="sxs-lookup"><span data-stu-id="dfc3d-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc3d-110">說明</span><span class="sxs-lookup"><span data-stu-id="dfc3d-110">DESCRIPTION</span></span>
<span data-ttu-id="dfc3d-111">**AzVMOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="dfc3d-112">您可以指定登入認證、電腦名稱稱及作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="dfc3d-113">示例</span><span class="sxs-lookup"><span data-stu-id="dfc3d-113">EXAMPLES</span></span>

### <span data-ttu-id="dfc3d-114">範例1：為新的虛擬機器設定作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="dfc3d-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="dfc3d-115">第一個命令會將密碼轉換成安全字串，然後將密碼儲存在 $SecurePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="dfc3d-116">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="dfc3d-117">第二個命令會為使用者 FullerP 及儲存在 $SecurePassword 中的密碼建立認證，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="dfc3d-118">如需詳細資訊，請輸入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="dfc3d-119">第三個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dfc3d-120">第四個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dfc3d-121">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dfc3d-122">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="dfc3d-123">接下來的四個命令會將值指派給要在下列命令中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="dfc3d-124">因為您可以直接在 **AzVMOperatingSystem** 命令中指定這些字串，所以這個方法只適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="dfc3d-125">不過，您可能會在腳本中使用這種方法。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="dfc3d-126">最終命令會針對儲存在 $VirtualMachine 中的虛擬機器設定作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="dfc3d-127">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="dfc3d-128">此命令會使用在先前命令中為某些參數指定的變數。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="dfc3d-129">參數</span><span class="sxs-lookup"><span data-stu-id="dfc3d-129">PARAMETERS</span></span>

### <span data-ttu-id="dfc3d-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="dfc3d-130">-ComputerName</span></span>
<span data-ttu-id="dfc3d-131">指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="dfc3d-132">-認證</span><span class="sxs-lookup"><span data-stu-id="dfc3d-132">-Credential</span></span>
<span data-ttu-id="dfc3d-133">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="dfc3d-134">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="dfc3d-135">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="dfc3d-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="dfc3d-136">-CustomData</span></span>
<span data-ttu-id="dfc3d-137">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="dfc3d-138">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="dfc3d-139">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="dfc3d-140">**注意：請勿在 customData 屬性中傳遞任何機密或密碼**</span><span class="sxs-lookup"><span data-stu-id="dfc3d-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="dfc3d-141">建立 VM 之後，就無法更新此屬性。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="dfc3d-142">customData 會傳送至 VM 以儲存為檔案，如需詳細資訊，請參閱 [Azure vm 上的自訂資料](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="dfc3d-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="dfc3d-143">若要針對您的 Linux VM 使用雲端初始化，請參閱 [在建立期間使用雲端初始化自訂 LINUX vm](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span><span class="sxs-lookup"><span data-stu-id="dfc3d-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="dfc3d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc3d-144">-DefaultProfile</span></span>
<span data-ttu-id="dfc3d-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfc3d-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="dfc3d-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="dfc3d-147">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-147">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="dfc3d-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="dfc3d-148">-DisableVMAgent</span></span>
<span data-ttu-id="dfc3d-149">停用 [預配 VM 代理程式]。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-149">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="dfc3d-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="dfc3d-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="dfc3d-151">表示此 Cmdlet 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-151">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="dfc3d-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="dfc3d-152">-Linux</span></span>
<span data-ttu-id="dfc3d-153">表示作業系統類型是 Linux。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-153">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="dfc3d-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="dfc3d-154">-PatchMode</span></span>
<span data-ttu-id="dfc3d-155">指定訪客內修補到 IaaS 虛擬機器的模式。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="dfc3d-156">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="dfc3d-156">Possible values are:</span></span><br>
<span data-ttu-id="dfc3d-157">**手動** -將修補程式的應用程式控制至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="dfc3d-158">您可以在 VM 中手動套用修補程式來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="dfc3d-159">在此模式中，會停用自動更新;屬性 WindowsConfiguration 的 enableAutomaticUpdates 必須是 false</span><span class="sxs-lookup"><span data-stu-id="dfc3d-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="dfc3d-160">**AutomaticByOS** -虛擬機器將自動由作業系統更新。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="dfc3d-161">WindowsConfiguration 屬性必須為 true。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="dfc3d-162">**AutomaticByPlatform** -虛擬機器將由 OS 自動更新。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="dfc3d-163">[屬性 provisionVMAgent] 和 WindowsConfiguration enableAutomaticUpdates 必須為 true</span><span class="sxs-lookup"><span data-stu-id="dfc3d-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3d-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="dfc3d-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="dfc3d-165">指示設定需要在虛擬機器上安裝虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="dfc3d-166">-時區</span><span class="sxs-lookup"><span data-stu-id="dfc3d-166">-TimeZone</span></span>
<span data-ttu-id="dfc3d-167">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="dfc3d-168">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="dfc3d-169">可能的值可以是 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 從 [TimeZoneInfo](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)傳回的時區值。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="dfc3d-170">-VM</span><span class="sxs-lookup"><span data-stu-id="dfc3d-170">-VM</span></span>
<span data-ttu-id="dfc3d-171">指定要設定作業系統屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="dfc3d-172">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="dfc3d-173">使用 New-AzVMConfig Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="dfc3d-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="dfc3d-174">-Windows</span></span>
<span data-ttu-id="dfc3d-175">表示作業系統類型是 Windows。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-175">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="dfc3d-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="dfc3d-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="dfc3d-177">指定 WinRM 憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="dfc3d-178">這需要儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-178">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="dfc3d-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="dfc3d-179">-WinRMHttp</span></span>
<span data-ttu-id="dfc3d-180">表示此作業系統使用 HTTP WinRM。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-180">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="dfc3d-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="dfc3d-181">-WinRMHttps</span></span>
<span data-ttu-id="dfc3d-182">表示此作業系統使用 HTTPS WinRM。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="dfc3d-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc3d-183">CommonParameters</span></span>
<span data-ttu-id="dfc3d-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc3d-185">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfc3d-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc3d-186">輸入</span><span class="sxs-lookup"><span data-stu-id="dfc3d-186">INPUTS</span></span>

### <span data-ttu-id="dfc3d-187">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="dfc3d-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dfc3d-188">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="dfc3d-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dfc3d-189">System.object</span><span class="sxs-lookup"><span data-stu-id="dfc3d-189">System.String</span></span>

### <span data-ttu-id="dfc3d-190">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="dfc3d-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="dfc3d-191">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="dfc3d-191">System.Uri</span></span>

## <span data-ttu-id="dfc3d-192">輸出</span><span class="sxs-lookup"><span data-stu-id="dfc3d-192">OUTPUTS</span></span>

### <span data-ttu-id="dfc3d-193">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="dfc3d-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dfc3d-194">筆記</span><span class="sxs-lookup"><span data-stu-id="dfc3d-194">NOTES</span></span>

## <span data-ttu-id="dfc3d-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfc3d-195">RELATED LINKS</span></span>

[<span data-ttu-id="dfc3d-196">AzVM</span><span class="sxs-lookup"><span data-stu-id="dfc3d-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dfc3d-197">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dfc3d-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


