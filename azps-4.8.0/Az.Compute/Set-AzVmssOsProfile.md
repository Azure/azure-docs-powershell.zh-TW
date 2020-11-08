---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971452"
---
# <span data-ttu-id="3c019-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="3c019-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="3c019-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c019-102">SYNOPSIS</span></span>
<span data-ttu-id="3c019-103">設定 VMSS 作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3c019-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="3c019-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c019-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c019-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c019-105">DESCRIPTION</span></span>
<span data-ttu-id="3c019-106">**AzVmssOsProfile** Cmdlet 會設定虛擬機器縮放設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3c019-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="3c019-107">示例</span><span class="sxs-lookup"><span data-stu-id="3c019-107">EXAMPLES</span></span>

### <span data-ttu-id="3c019-108">範例1：設定 VMSS 的作業系統配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="3c019-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="3c019-109">這個命令會為屬於名為 ContosoVMSS 之 VMSS 的虛擬機器設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="3c019-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="3c019-110">此命令會為 VMSS 中的所有虛擬機器實例設定電腦名稱稱首碼，以測試並提供系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="3c019-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="3c019-111">參數</span><span class="sxs-lookup"><span data-stu-id="3c019-111">PARAMETERS</span></span>

### <span data-ttu-id="3c019-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3c019-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="3c019-113">指定無人參與的內容物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="3c019-114">您可以使用 Add-AzVMAdditionalUnattendContent 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="3c019-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3c019-115">-AdminPassword</span></span>
<span data-ttu-id="3c019-116">指定要用於 VMSS 中所有虛擬機器實例的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="3c019-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="3c019-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="3c019-117">-AdminUsername</span></span>
<span data-ttu-id="3c019-118">指定要用於 VMSS 中所有虛擬機器實例的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3c019-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="3c019-119">**僅限 Windows 的限制：** 無法結束 \" 。\"</span><span class="sxs-lookup"><span data-stu-id="3c019-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="3c019-120">不 **允許的值：** \"administrator \" 、 \" admin \" 、 \" user \" 、 \" user1 \" 、 \" test \" 、 \" 使用者 \" \" 2、 \" \" \" 123、user3、 \" admin1 \" 、 \" 1 \" 、 \" \" 、 \" a \" 、 \" actuser、、 \" \" \" \" admin2 \" 、 \" aspnet \" 、 \" 備份 \" support_388945a0、 \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" 主機、test2、test3、、user4、user5、、、、、、、、、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="3c019-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="3c019-121">**最小長度 (Linux) ：** 1 個字元</span><span class="sxs-lookup"><span data-stu-id="3c019-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="3c019-122">**最大長度 (Linux) ：** 64 字元</span><span class="sxs-lookup"><span data-stu-id="3c019-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="3c019-123">**(Windows) 的最大長度：** 20 個字元</span><span class="sxs-lookup"><span data-stu-id="3c019-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="3c019-124">如需 Linux VM 的根目錄存取權，請參閱在 [Azure 中使用 linux 虛擬機器上的根許可權](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="3c019-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="3c019-125">如需 Linux 上不應在這個欄位中使用之內建系統使用者的清單，請參閱 [在 Azure 上選取 [Linux 的使用者名稱](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)]。</span><span class="sxs-lookup"><span data-stu-id="3c019-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="3c019-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="3c019-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="3c019-127">指定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼。</span><span class="sxs-lookup"><span data-stu-id="3c019-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="3c019-128">電腦名稱稱的長度必須是1到15個字元。</span><span class="sxs-lookup"><span data-stu-id="3c019-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="3c019-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="3c019-129">-CustomData</span></span>
<span data-ttu-id="3c019-130">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="3c019-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="3c019-131">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="3c019-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="3c019-132">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="3c019-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="3c019-133">若要針對您的 VM 使用雲端初始化，請參閱 [在建立期間使用雲端初始化自訂 LINUX VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="3c019-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="3c019-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c019-134">-DefaultProfile</span></span>
<span data-ttu-id="3c019-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c019-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c019-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c019-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="3c019-137">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="3c019-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="3c019-138">-監聽器</span><span class="sxs-lookup"><span data-stu-id="3c019-138">-Listener</span></span>
<span data-ttu-id="3c019-139">指定 Windows 遠端系統管理 (WinRM) 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="3c019-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="3c019-140">這會啟用遠端 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="3c019-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="3c019-141">您可以使用 Add-AzVmssWinRMListener Cmdlet 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="3c019-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="3c019-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="3c019-142">-PublicKey</span></span>
<span data-ttu-id="3c019-143">指定 SSH) 公用金鑰組象 (的安全 Shell。</span><span class="sxs-lookup"><span data-stu-id="3c019-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="3c019-144">您可以使用 Add-AzVMSshPublicKey Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3c019-145">密碼</span><span class="sxs-lookup"><span data-stu-id="3c019-145">-Secret</span></span>
<span data-ttu-id="3c019-146">指定包含要放在虛擬機器上之憑證參照的機密物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="3c019-147">您可以使用 Add-AzVmssSecret Cmdlet 來建立機密物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="3c019-148">-時區</span><span class="sxs-lookup"><span data-stu-id="3c019-148">-TimeZone</span></span>
<span data-ttu-id="3c019-149">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="3c019-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="3c019-150">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="3c019-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="3c019-151">可能的值可以是 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 從 [TimeZoneInfo](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)傳回的時區值。</span><span class="sxs-lookup"><span data-stu-id="3c019-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="3c019-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3c019-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3c019-153">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="3c019-154">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="3c019-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3c019-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="3c019-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="3c019-156">指出是否已針對自動更新啟用 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3c019-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="3c019-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="3c019-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="3c019-158">指出是否應該在 VMSS 的虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="3c019-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="3c019-159">-確認</span><span class="sxs-lookup"><span data-stu-id="3c019-159">-Confirm</span></span>
<span data-ttu-id="3c019-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c019-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c019-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c019-161">-WhatIf</span></span>
<span data-ttu-id="3c019-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c019-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c019-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c019-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c019-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c019-164">CommonParameters</span></span>
<span data-ttu-id="3c019-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c019-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c019-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3c019-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c019-167">輸入</span><span class="sxs-lookup"><span data-stu-id="3c019-167">INPUTS</span></span>

### <span data-ttu-id="3c019-168">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3c019-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3c019-169">System.object</span><span class="sxs-lookup"><span data-stu-id="3c019-169">System.String</span></span>

### <span data-ttu-id="3c019-170">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c019-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3c019-171">AdditionalUnattendContent [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="3c019-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="3c019-172">WinRMListener [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="3c019-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="3c019-173">SshPublicKey [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="3c019-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="3c019-174">VaultSecretGroup [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="3c019-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="3c019-175">輸出</span><span class="sxs-lookup"><span data-stu-id="3c019-175">OUTPUTS</span></span>

### <span data-ttu-id="3c019-176">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3c019-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3c019-177">筆記</span><span class="sxs-lookup"><span data-stu-id="3c019-177">NOTES</span></span>

## <span data-ttu-id="3c019-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c019-178">RELATED LINKS</span></span>

[<span data-ttu-id="3c019-179">附加 AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3c019-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="3c019-180">附加 AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="3c019-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="3c019-181">附加 AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3c019-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="3c019-182">附加 AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="3c019-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="3c019-183">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3c019-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


