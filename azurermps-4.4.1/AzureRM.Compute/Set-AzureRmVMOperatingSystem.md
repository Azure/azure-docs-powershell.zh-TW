---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 2d742a70f1ae95d362d5ceafcc117f1296dc2cb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457268"
---
# <span data-ttu-id="67564-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67564-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="67564-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67564-102">SYNOPSIS</span></span>
<span data-ttu-id="67564-103">設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="67564-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67564-104">句法</span><span class="sxs-lookup"><span data-stu-id="67564-104">SYNTAX</span></span>

### <span data-ttu-id="67564-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="67564-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67564-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="67564-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67564-107">Linux</span><span class="sxs-lookup"><span data-stu-id="67564-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67564-108">說明</span><span class="sxs-lookup"><span data-stu-id="67564-108">DESCRIPTION</span></span>
<span data-ttu-id="67564-109">**AzureRmVMOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="67564-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="67564-110">您可以指定登入認證、電腦名稱稱及作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="67564-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="67564-111">示例</span><span class="sxs-lookup"><span data-stu-id="67564-111">EXAMPLES</span></span>

### <span data-ttu-id="67564-112">範例1：為新的虛擬機器設定作業系統屬性</span><span class="sxs-lookup"><span data-stu-id="67564-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="67564-113">第一個命令會將密碼轉換成安全字串，然後將密碼儲存在 $SecurePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="67564-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="67564-114">如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="67564-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="67564-115">第二個命令會為使用者 FullerP 及儲存在 $SecurePassword 中的密碼建立認證，然後將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="67564-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="67564-116">如需詳細資訊，請輸入 `Get-Help New-Object` 。</span><span class="sxs-lookup"><span data-stu-id="67564-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="67564-117">第三個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="67564-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="67564-118">第四個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="67564-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="67564-119">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="67564-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="67564-120">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="67564-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="67564-121">接下來的四個命令會將值指派給要在下列命令中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="67564-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="67564-122">因為您可以直接在 **AzureRmVMOperatingSystem** 命令中指定這些字串，所以這個方法只適用于可讀性。</span><span class="sxs-lookup"><span data-stu-id="67564-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="67564-123">不過，您可能會在腳本中使用這種方法。</span><span class="sxs-lookup"><span data-stu-id="67564-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="67564-124">最終命令會針對儲存在 $VirtualMachine 中的虛擬機器設定作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="67564-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="67564-125">命令會使用儲存在 $Credential 中的認證。</span><span class="sxs-lookup"><span data-stu-id="67564-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="67564-126">此命令會使用在先前命令中為某些參數指定的變數。</span><span class="sxs-lookup"><span data-stu-id="67564-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="67564-127">參數</span><span class="sxs-lookup"><span data-stu-id="67564-127">PARAMETERS</span></span>

### <span data-ttu-id="67564-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="67564-128">-ComputerName</span></span>
<span data-ttu-id="67564-129">指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="67564-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="67564-130">-認證</span><span class="sxs-lookup"><span data-stu-id="67564-130">-Credential</span></span>
<span data-ttu-id="67564-131">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="67564-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="67564-132">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67564-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="67564-133">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="67564-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="67564-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="67564-134">-CustomData</span></span>
<span data-ttu-id="67564-135">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="67564-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="67564-136">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="67564-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="67564-137">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="67564-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="67564-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67564-138">-DefaultProfile</span></span>
<span data-ttu-id="67564-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67564-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67564-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="67564-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="67564-141">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="67564-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="67564-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="67564-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="67564-143">表示此 Cmdlet 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="67564-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="67564-144">-Linux</span></span>
<span data-ttu-id="67564-145">表示作業系統類型是 Linux。</span><span class="sxs-lookup"><span data-stu-id="67564-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="67564-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="67564-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="67564-147">指示設定需要在虛擬機器上安裝虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="67564-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="67564-148">-時區</span><span class="sxs-lookup"><span data-stu-id="67564-148">-TimeZone</span></span>
<span data-ttu-id="67564-149">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="67564-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-150">-VM</span><span class="sxs-lookup"><span data-stu-id="67564-150">-VM</span></span>
<span data-ttu-id="67564-151">指定要設定作業系統屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="67564-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="67564-152">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67564-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="67564-153">使用 New-AzureRmVMConfig Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="67564-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="67564-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="67564-154">-Windows</span></span>
<span data-ttu-id="67564-155">表示作業系統類型是 Windows。</span><span class="sxs-lookup"><span data-stu-id="67564-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="67564-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="67564-157">指定 WinRM 憑證的 URI。</span><span class="sxs-lookup"><span data-stu-id="67564-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="67564-158">這需要儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="67564-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="67564-159">-WinRMHttp</span></span>
<span data-ttu-id="67564-160">表示此作業系統使用 HTTP WinRM。</span><span class="sxs-lookup"><span data-stu-id="67564-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="67564-161">-WinRMHttps</span></span>
<span data-ttu-id="67564-162">表示此作業系統使用 HTTPS WinRM。</span><span class="sxs-lookup"><span data-stu-id="67564-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67564-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67564-163">CommonParameters</span></span>
<span data-ttu-id="67564-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67564-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67564-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67564-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67564-166">輸入</span><span class="sxs-lookup"><span data-stu-id="67564-166">INPUTS</span></span>

## <span data-ttu-id="67564-167">輸出</span><span class="sxs-lookup"><span data-stu-id="67564-167">OUTPUTS</span></span>

## <span data-ttu-id="67564-168">筆記</span><span class="sxs-lookup"><span data-stu-id="67564-168">NOTES</span></span>

## <span data-ttu-id="67564-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="67564-169">RELATED LINKS</span></span>

[<span data-ttu-id="67564-170">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67564-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="67564-171">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="67564-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


