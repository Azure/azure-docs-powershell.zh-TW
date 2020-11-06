---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449931"
---
# <span data-ttu-id="2cb7f-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2cb7f-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="2cb7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cb7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb7f-103">設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cb7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cb7f-104">SYNTAX</span></span>

### <span data-ttu-id="2cb7f-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="2cb7f-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="2cb7f-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="2cb7f-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="2cb7f-107">Linux</span><span class="sxs-lookup"><span data-stu-id="2cb7f-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="2cb7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="2cb7f-108">DESCRIPTION</span></span>
<span data-ttu-id="2cb7f-109">**AzureRmVMOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="2cb7f-110">您可以指定登入認證、電腦名稱稱及作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="2cb7f-111">示例</span><span class="sxs-lookup"><span data-stu-id="2cb7f-111">EXAMPLES</span></span>

### <span data-ttu-id="2cb7f-112">範例1：為新的虛擬機器設定作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="2cb7f-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="2cb7f-113">第一個命令會將密碼轉換成安全字串，然後將密碼儲存在 $SecurePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="2cb7f-114">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="2cb7f-115">第二個命令會為使用者 FullerP 及儲存在 $SecurePassword 中的密碼建立認證，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="2cb7f-116">如需詳細資訊，請輸入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="2cb7f-117">第三個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="2cb7f-118">第四個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2cb7f-119">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2cb7f-120">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="2cb7f-121">接下來的四個命令會將值指派給要在下列命令中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="2cb7f-122">因為您可以直接在 **AzureRmVMOperatingSystem** 命令中指定這些字串，所以這個方法只適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="2cb7f-123">不過，您可能會在腳本中使用這種方法。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="2cb7f-124">最終命令會針對儲存在 $VirtualMachine 中的虛擬機器設定作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2cb7f-125">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="2cb7f-126">此命令會使用在先前命令中為某些參數指定的變數。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="2cb7f-127">參數</span><span class="sxs-lookup"><span data-stu-id="2cb7f-127">PARAMETERS</span></span>

### <span data-ttu-id="2cb7f-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="2cb7f-128">-ComputerName</span></span>
<span data-ttu-id="2cb7f-129">指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-130">-認證</span><span class="sxs-lookup"><span data-stu-id="2cb7f-130">-Credential</span></span>
<span data-ttu-id="2cb7f-131">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="2cb7f-132">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="2cb7f-133">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="2cb7f-134">-CustomData</span></span>
<span data-ttu-id="2cb7f-135">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="2cb7f-136">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="2cb7f-137">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-137">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="2cb7f-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="2cb7f-139">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-139">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-140">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="2cb7f-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="2cb7f-141">表示此 Cmdlet 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-141">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="2cb7f-142">-Linux</span></span>
<span data-ttu-id="2cb7f-143">表示作業系統類型是 Linux。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-143">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="2cb7f-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="2cb7f-145">指示設定需要在虛擬機器上安裝虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-146">-時區</span><span class="sxs-lookup"><span data-stu-id="2cb7f-146">-TimeZone</span></span>
<span data-ttu-id="2cb7f-147">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-147">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-148">-VM</span><span class="sxs-lookup"><span data-stu-id="2cb7f-148">-VM</span></span>
<span data-ttu-id="2cb7f-149">指定要設定作業系統屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="2cb7f-150">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="2cb7f-151">使用 New-AzureRmVMConfig Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="2cb7f-152">-Windows</span></span>
<span data-ttu-id="2cb7f-153">表示作業系統類型是 Windows。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-153">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-154">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="2cb7f-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="2cb7f-155">指定 WinRM 憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="2cb7f-156">這需要儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-156">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="2cb7f-157">-WinRMHttp</span></span>
<span data-ttu-id="2cb7f-158">表示此作業系統使用 HTTP WinRM。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-158">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="2cb7f-159">-WinRMHttps</span></span>
<span data-ttu-id="2cb7f-160">表示此作業系統使用 HTTPS WinRM。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb7f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb7f-161">CommonParameters</span></span>
<span data-ttu-id="2cb7f-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb7f-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb7f-164">輸入</span><span class="sxs-lookup"><span data-stu-id="2cb7f-164">INPUTS</span></span>

### <span data-ttu-id="2cb7f-165">所有</span><span class="sxs-lookup"><span data-stu-id="2cb7f-165">None</span></span>
<span data-ttu-id="2cb7f-166">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2cb7f-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2cb7f-167">輸出</span><span class="sxs-lookup"><span data-stu-id="2cb7f-167">OUTPUTS</span></span>

## <span data-ttu-id="2cb7f-168">筆記</span><span class="sxs-lookup"><span data-stu-id="2cb7f-168">NOTES</span></span>

## <span data-ttu-id="2cb7f-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cb7f-169">RELATED LINKS</span></span>

[<span data-ttu-id="2cb7f-170">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2cb7f-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2cb7f-171">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2cb7f-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


