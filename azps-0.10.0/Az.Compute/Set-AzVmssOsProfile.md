---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795825"
---
# <span data-ttu-id="640af-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="640af-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="640af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="640af-102">SYNOPSIS</span></span>
<span data-ttu-id="640af-103">設定 VMSS 作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="640af-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="640af-104">句法</span><span class="sxs-lookup"><span data-stu-id="640af-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640af-105">說明</span><span class="sxs-lookup"><span data-stu-id="640af-105">DESCRIPTION</span></span>
<span data-ttu-id="640af-106">**AzVmssOsProfile** Cmdlet 會設定虛擬機器縮放設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="640af-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="640af-107">示例</span><span class="sxs-lookup"><span data-stu-id="640af-107">EXAMPLES</span></span>

### <span data-ttu-id="640af-108">範例1：設定 VMSS 的作業系統配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="640af-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="640af-109">這個命令會為屬於名為 ContosoVMSS 之 VMSS 的虛擬機器設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="640af-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="640af-110">此命令會為 VMSS 中的所有虛擬機器實例設定電腦名稱稱首碼，以測試並提供系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="640af-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="640af-111">參數</span><span class="sxs-lookup"><span data-stu-id="640af-111">PARAMETERS</span></span>

### <span data-ttu-id="640af-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="640af-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="640af-113">指定無人參與的內容物件。</span><span class="sxs-lookup"><span data-stu-id="640af-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="640af-114">您可以使用 Add-AzVMAdditionalUnattendContent 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="640af-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="640af-115">-AdminPassword</span></span>
<span data-ttu-id="640af-116">指定要用於 VMSS 中所有虛擬機器實例的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="640af-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="640af-117">-AdminUsername</span></span>
<span data-ttu-id="640af-118">指定要用於 VMSS 中所有虛擬機器實例的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="640af-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="640af-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="640af-120">指定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼。</span><span class="sxs-lookup"><span data-stu-id="640af-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="640af-121">電腦名稱稱的長度必須是1到15個字元。</span><span class="sxs-lookup"><span data-stu-id="640af-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="640af-122">-CustomData</span></span>
<span data-ttu-id="640af-123">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="640af-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="640af-124">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="640af-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="640af-125">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="640af-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="640af-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640af-126">-DefaultProfile</span></span>
<span data-ttu-id="640af-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="640af-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="640af-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="640af-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="640af-129">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="640af-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-130">-監聽器</span><span class="sxs-lookup"><span data-stu-id="640af-130">-Listener</span></span>
<span data-ttu-id="640af-131">指定 Windows 遠端系統管理 (WinRM) 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="640af-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="640af-132">這會啟用遠端 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="640af-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="640af-133">您可以使用 Add-AzVmssWinRMListener Cmdlet 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="640af-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="640af-134">-PublicKey</span></span>
<span data-ttu-id="640af-135">指定 SSH) 公用金鑰組象 (的安全 Shell。</span><span class="sxs-lookup"><span data-stu-id="640af-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="640af-136">您可以使用 Add-AzVMSshPublicKey Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="640af-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-137">密碼</span><span class="sxs-lookup"><span data-stu-id="640af-137">-Secret</span></span>
<span data-ttu-id="640af-138">指定包含要放在虛擬機器上之憑證參照的機密物件。</span><span class="sxs-lookup"><span data-stu-id="640af-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="640af-139">您可以使用 Add-AzVmssSecret Cmdlet 來建立機密物件。</span><span class="sxs-lookup"><span data-stu-id="640af-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-140">-時區</span><span class="sxs-lookup"><span data-stu-id="640af-140">-TimeZone</span></span>
<span data-ttu-id="640af-141">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="640af-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="640af-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="640af-143">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="640af-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="640af-144">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="640af-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="640af-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="640af-146">指出是否已針對自動更新啟用 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="640af-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="640af-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="640af-148">指出是否應該在 VMSS 的虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="640af-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640af-149">-確認</span><span class="sxs-lookup"><span data-stu-id="640af-149">-Confirm</span></span>
<span data-ttu-id="640af-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="640af-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="640af-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640af-151">-WhatIf</span></span>
<span data-ttu-id="640af-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="640af-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="640af-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="640af-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="640af-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640af-154">CommonParameters</span></span>
<span data-ttu-id="640af-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="640af-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640af-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="640af-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640af-157">輸入</span><span class="sxs-lookup"><span data-stu-id="640af-157">INPUTS</span></span>

### <span data-ttu-id="640af-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="640af-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="640af-159">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="640af-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="640af-160">輸出</span><span class="sxs-lookup"><span data-stu-id="640af-160">OUTPUTS</span></span>

### <span data-ttu-id="640af-161">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="640af-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="640af-162">筆記</span><span class="sxs-lookup"><span data-stu-id="640af-162">NOTES</span></span>

## <span data-ttu-id="640af-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="640af-163">RELATED LINKS</span></span>

[<span data-ttu-id="640af-164">附加 AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="640af-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="640af-165">附加 AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="640af-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="640af-166">附加 AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="640af-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="640af-167">附加 AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="640af-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="640af-168">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="640af-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


