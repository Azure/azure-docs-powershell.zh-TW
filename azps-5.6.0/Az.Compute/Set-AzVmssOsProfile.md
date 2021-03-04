---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903645"
---
# <span data-ttu-id="3685f-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="3685f-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="3685f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3685f-102">SYNOPSIS</span></span>
<span data-ttu-id="3685f-103">設定 VMSS 作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3685f-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="3685f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3685f-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3685f-105">描述</span><span class="sxs-lookup"><span data-stu-id="3685f-105">DESCRIPTION</span></span>
<span data-ttu-id="3685f-106">**Set-AzEvssOsProfile** Cmdlet 會設定虛擬機器縮放集作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3685f-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="3685f-107">例子</span><span class="sxs-lookup"><span data-stu-id="3685f-107">EXAMPLES</span></span>

### <span data-ttu-id="3685f-108">範例 1：設定 VMSS 的作業系統配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="3685f-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="3685f-109">此命令會針對名稱為 Contoso VMSS 的虛擬機器設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3685f-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="3685f-110">該命令會設定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼，以進行測試，並提供給系統管理員使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="3685f-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="3685f-111">參數</span><span class="sxs-lookup"><span data-stu-id="3685f-111">PARAMETERS</span></span>

### <span data-ttu-id="3685f-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3685f-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="3685f-113">指定自動執行的內容物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="3685f-114">您可以使用Add-AzVMAdditionalUnattendContent建立物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3685f-115">-AdminPassword</span></span>
<span data-ttu-id="3685f-116">指定要用於 VMSS 中所有虛擬機器實例的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="3685f-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="3685f-117">-AdminUsername</span></span>
<span data-ttu-id="3685f-118">指定要用於 VMSS 中所有虛擬機器實例的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3685f-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="3685f-119">**Windows 限制：** 無法以 \" 結尾。\"</span><span class="sxs-lookup"><span data-stu-id="3685f-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="3685f-120">**不允許的值：** \"系統管理員 \" ， \" 系統管理員 \" ， \" 使用者， \" \" \" user1， \" \" test， \" \" user2， \" \" \" test， user3， \" \" \" admin1， \" \" 1， \" 1， 123， \" \" \" a， \" actuser， \" \" \" adm， \" \" admin2， \" aspnet， \" \" \" backup， \" \" console， \" \" david， \" \" guest， \" \" john， \" \" owner， \" \" root， \" \" server， \" \" sql， \" \" support， \" \" support_388945a0， \" sys， \" \" \" test2， \" \" test3， \" \" user4， \" user5. \"</span><span class="sxs-lookup"><span data-stu-id="3685f-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="3685f-121">**Linux 版 (長度) ：1** 個字元</span><span class="sxs-lookup"><span data-stu-id="3685f-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="3685f-122">**Linux (長度) ：64** 個字元</span><span class="sxs-lookup"><span data-stu-id="3685f-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="3685f-123">**Windows (長度) ：20** 個字元</span><span class="sxs-lookup"><span data-stu-id="3685f-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="3685f-124">若要取得 Linux VM 的根存取權，請參閱在 Azure 的 Linux 虛擬機器 [上使用根許可權](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="3685f-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="3685f-125">有關 Linux 上不應在此欄位中使用的內建系統使用者清單，請參閱選取 Azure 上的 [Linux 使用者名稱](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="3685f-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="3685f-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="3685f-127">指定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼。</span><span class="sxs-lookup"><span data-stu-id="3685f-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="3685f-128">電腦名稱稱必須長 1 到 15 個字元。</span><span class="sxs-lookup"><span data-stu-id="3685f-128">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="3685f-129">-CustomData</span></span>
<span data-ttu-id="3685f-130">指定自訂資料的底數為 64 的編碼字串。</span><span class="sxs-lookup"><span data-stu-id="3685f-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="3685f-131">這會解碼為二進位陣列，該陣列會儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="3685f-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="3685f-132">二進位陣列的長度上限為 65535 位元組。</span><span class="sxs-lookup"><span data-stu-id="3685f-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="3685f-133">若要針對您的 VM 使用雲端 init，請參閱在建立期間使用[雲端 init 自訂 Linux VM。](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="3685f-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="3685f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3685f-134">-DefaultProfile</span></span>
<span data-ttu-id="3685f-135">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3685f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3685f-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="3685f-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="3685f-137">表示此 Cmdlet 會停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="3685f-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-138">-聆聽者</span><span class="sxs-lookup"><span data-stu-id="3685f-138">-Listener</span></span>
<span data-ttu-id="3685f-139">指定 Windows Remote Management (WinRM) 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="3685f-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="3685f-140">這會啟用遠端 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="3685f-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="3685f-141">您可以使用 Add-AzVmssWinRMListener Cmdlet 來建立聆聽者。</span><span class="sxs-lookup"><span data-stu-id="3685f-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="3685f-142">-PublicKey</span></span>
<span data-ttu-id="3685f-143">指定安全命令命令 (SSH) 鍵物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="3685f-144">您可以使用 Add-AzVMSshPublicKey Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-145">-機密</span><span class="sxs-lookup"><span data-stu-id="3685f-145">-Secret</span></span>
<span data-ttu-id="3685f-146">指定密碼物件，其中包含要放在虛擬機器上的憑證參照。</span><span class="sxs-lookup"><span data-stu-id="3685f-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="3685f-147">您可以使用 Add-AzVmssSecret Cmdlet 來建立機密物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-148">-時區</span><span class="sxs-lookup"><span data-stu-id="3685f-148">-TimeZone</span></span>
<span data-ttu-id="3685f-149">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="3685f-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="3685f-150">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="3685f-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="3685f-151">可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)</span><span class="sxs-lookup"><span data-stu-id="3685f-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3685f-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3685f-153">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="3685f-154">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="3685f-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="3685f-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="3685f-156">指出 VMSS 中的虛擬機器是否已啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="3685f-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-157">-WindowsConfigurationProvisionMSAGEnt</span><span class="sxs-lookup"><span data-stu-id="3685f-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="3685f-158">指出是否應該在 VMSS 的虛擬機器上部署虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="3685f-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-159">-確認</span><span class="sxs-lookup"><span data-stu-id="3685f-159">-Confirm</span></span>
<span data-ttu-id="3685f-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3685f-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3685f-161">-WhatIf</span></span>
<span data-ttu-id="3685f-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3685f-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3685f-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3685f-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3685f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3685f-164">CommonParameters</span></span>
<span data-ttu-id="3685f-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3685f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3685f-166">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3685f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3685f-167">輸入</span><span class="sxs-lookup"><span data-stu-id="3685f-167">INPUTS</span></span>

### <span data-ttu-id="3685f-168">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3685f-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3685f-169">System.String</span><span class="sxs-lookup"><span data-stu-id="3685f-169">System.String</span></span>

### <span data-ttu-id="3685f-170">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3685f-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3685f-171">Microsoft.Azure.management.Compute.models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="3685f-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="3685f-172">Microsoft.Azure.management.Compute.models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="3685f-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="3685f-173">Microsoft.Azure.management.Compute.models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="3685f-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="3685f-174">Microsoft.Azure.management.Compute.models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="3685f-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="3685f-175">輸出</span><span class="sxs-lookup"><span data-stu-id="3685f-175">OUTPUTS</span></span>

### <span data-ttu-id="3685f-176">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3685f-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3685f-177">筆記</span><span class="sxs-lookup"><span data-stu-id="3685f-177">NOTES</span></span>

## <span data-ttu-id="3685f-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="3685f-178">RELATED LINKS</span></span>

[<span data-ttu-id="3685f-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3685f-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="3685f-180">Add-AzEvssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="3685f-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="3685f-181">Add-AzMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3685f-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="3685f-182">Add-AzEvssSecret</span><span class="sxs-lookup"><span data-stu-id="3685f-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="3685f-183">New-AzEvssConfig</span><span class="sxs-lookup"><span data-stu-id="3685f-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


