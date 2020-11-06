---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 60c5d9326b99c8349554f8b3eff2a432382c018e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613141"
---
# <span data-ttu-id="23f5d-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="23f5d-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="23f5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="23f5d-103">設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="23f5d-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="23f5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="23f5d-104">SYNTAX</span></span>

### <span data-ttu-id="23f5d-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="23f5d-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f5d-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="23f5d-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f5d-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="23f5d-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f5d-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="23f5d-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f5d-109">Linux</span><span class="sxs-lookup"><span data-stu-id="23f5d-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23f5d-110">說明</span><span class="sxs-lookup"><span data-stu-id="23f5d-110">DESCRIPTION</span></span>
<span data-ttu-id="23f5d-111">**AzVMOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="23f5d-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="23f5d-112">您可以指定登入認證、電腦名稱稱及作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="23f5d-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="23f5d-113">示例</span><span class="sxs-lookup"><span data-stu-id="23f5d-113">EXAMPLES</span></span>

### <span data-ttu-id="23f5d-114">範例1：為新的虛擬機器設定作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="23f5d-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="23f5d-115">第一個命令會將密碼轉換成安全字串，然後將密碼儲存在 $SecurePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="23f5d-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="23f5d-116">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="23f5d-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="23f5d-117">第二個命令會為使用者 FullerP 及儲存在 $SecurePassword 中的密碼建立認證，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="23f5d-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="23f5d-118">如需詳細資訊，請輸入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="23f5d-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="23f5d-119">第三個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="23f5d-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="23f5d-120">第四個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="23f5d-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="23f5d-121">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="23f5d-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="23f5d-122">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="23f5d-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="23f5d-123">接下來的四個命令會將值指派給要在下列命令中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="23f5d-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="23f5d-124">因為您可以直接在 **AzVMOperatingSystem** 命令中指定這些字串，所以這個方法只適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="23f5d-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="23f5d-125">不過，您可能會在腳本中使用這種方法。</span><span class="sxs-lookup"><span data-stu-id="23f5d-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="23f5d-126">最終命令會針對儲存在 $VirtualMachine 中的虛擬機器設定作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="23f5d-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="23f5d-127">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="23f5d-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="23f5d-128">此命令會使用在先前命令中為某些參數指定的變數。</span><span class="sxs-lookup"><span data-stu-id="23f5d-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="23f5d-129">參數</span><span class="sxs-lookup"><span data-stu-id="23f5d-129">PARAMETERS</span></span>

### <span data-ttu-id="23f5d-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="23f5d-130">-ComputerName</span></span>
<span data-ttu-id="23f5d-131">指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="23f5d-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="23f5d-132">-認證</span><span class="sxs-lookup"><span data-stu-id="23f5d-132">-Credential</span></span>
<span data-ttu-id="23f5d-133">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="23f5d-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="23f5d-134">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23f5d-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="23f5d-135">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="23f5d-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="23f5d-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="23f5d-136">-CustomData</span></span>
<span data-ttu-id="23f5d-137">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="23f5d-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="23f5d-138">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="23f5d-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="23f5d-139">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="23f5d-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="23f5d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f5d-140">-DefaultProfile</span></span>
<span data-ttu-id="23f5d-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23f5d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f5d-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="23f5d-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="23f5d-143">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="23f5d-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="23f5d-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="23f5d-144">-DisableVMAgent</span></span>
<span data-ttu-id="23f5d-145">停用 [預配 VM 代理程式]。</span><span class="sxs-lookup"><span data-stu-id="23f5d-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="23f5d-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="23f5d-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="23f5d-147">表示此 Cmdlet 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="23f5d-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="23f5d-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="23f5d-148">-Linux</span></span>
<span data-ttu-id="23f5d-149">表示作業系統類型是 Linux。</span><span class="sxs-lookup"><span data-stu-id="23f5d-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="23f5d-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="23f5d-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="23f5d-151">指示設定需要在虛擬機器上安裝虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="23f5d-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="23f5d-152">-時區</span><span class="sxs-lookup"><span data-stu-id="23f5d-152">-TimeZone</span></span>
<span data-ttu-id="23f5d-153">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="23f5d-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="23f5d-154">-VM</span><span class="sxs-lookup"><span data-stu-id="23f5d-154">-VM</span></span>
<span data-ttu-id="23f5d-155">指定要設定作業系統屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="23f5d-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="23f5d-156">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23f5d-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="23f5d-157">使用 New-AzVMConfig Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="23f5d-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="23f5d-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="23f5d-158">-Windows</span></span>
<span data-ttu-id="23f5d-159">表示作業系統類型是 Windows。</span><span class="sxs-lookup"><span data-stu-id="23f5d-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="23f5d-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="23f5d-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="23f5d-161">指定 WinRM 憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="23f5d-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="23f5d-162">這需要儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="23f5d-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="23f5d-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="23f5d-163">-WinRMHttp</span></span>
<span data-ttu-id="23f5d-164">表示此作業系統使用 HTTP WinRM。</span><span class="sxs-lookup"><span data-stu-id="23f5d-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="23f5d-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="23f5d-165">-WinRMHttps</span></span>
<span data-ttu-id="23f5d-166">表示此作業系統使用 HTTPS WinRM。</span><span class="sxs-lookup"><span data-stu-id="23f5d-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="23f5d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f5d-167">CommonParameters</span></span>
<span data-ttu-id="23f5d-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23f5d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f5d-169">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23f5d-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f5d-170">輸入</span><span class="sxs-lookup"><span data-stu-id="23f5d-170">INPUTS</span></span>

### <span data-ttu-id="23f5d-171">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="23f5d-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="23f5d-172">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="23f5d-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="23f5d-173">System.object</span><span class="sxs-lookup"><span data-stu-id="23f5d-173">System.String</span></span>

### <span data-ttu-id="23f5d-174">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="23f5d-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="23f5d-175">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="23f5d-175">System.Uri</span></span>

## <span data-ttu-id="23f5d-176">輸出</span><span class="sxs-lookup"><span data-stu-id="23f5d-176">OUTPUTS</span></span>

### <span data-ttu-id="23f5d-177">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="23f5d-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="23f5d-178">筆記</span><span class="sxs-lookup"><span data-stu-id="23f5d-178">NOTES</span></span>

## <span data-ttu-id="23f5d-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="23f5d-179">RELATED LINKS</span></span>

[<span data-ttu-id="23f5d-180">AzVM</span><span class="sxs-lookup"><span data-stu-id="23f5d-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="23f5d-181">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="23f5d-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


