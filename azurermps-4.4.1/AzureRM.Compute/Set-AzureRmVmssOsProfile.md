---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: 59a50a9138cec99aae8c9f999bf1fa7415655d2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444972"
---
# <span data-ttu-id="80710-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="80710-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="80710-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80710-102">SYNOPSIS</span></span>
<span data-ttu-id="80710-103">設定 VMSS 作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="80710-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80710-104">句法</span><span class="sxs-lookup"><span data-stu-id="80710-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80710-105">說明</span><span class="sxs-lookup"><span data-stu-id="80710-105">DESCRIPTION</span></span>
<span data-ttu-id="80710-106">**AzureRmVmssOsProfile** Cmdlet 會設定虛擬機器縮放設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="80710-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="80710-107">示例</span><span class="sxs-lookup"><span data-stu-id="80710-107">EXAMPLES</span></span>

### <span data-ttu-id="80710-108">範例1：設定 VMSS 的作業系統配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="80710-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="80710-109">這個命令會為屬於名為 ContosoVMSS 之 VMSS 的虛擬機器設定作業系統配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="80710-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="80710-110">此命令會為 VMSS 中的所有虛擬機器實例設定電腦名稱稱首碼，以測試並提供系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="80710-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="80710-111">參數</span><span class="sxs-lookup"><span data-stu-id="80710-111">PARAMETERS</span></span>

### <span data-ttu-id="80710-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="80710-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="80710-113">指定無人參與的內容物件。</span><span class="sxs-lookup"><span data-stu-id="80710-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="80710-114">您可以使用 Add-AzureRmVMAdditionalUnattendContent 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="80710-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="80710-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="80710-115">-AdminPassword</span></span>
<span data-ttu-id="80710-116">指定要用於 VMSS 中所有虛擬機器實例的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="80710-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="80710-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="80710-117">-AdminUsername</span></span>
<span data-ttu-id="80710-118">指定要用於 VMSS 中所有虛擬機器實例的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="80710-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="80710-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="80710-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="80710-120">指定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼。</span><span class="sxs-lookup"><span data-stu-id="80710-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="80710-121">電腦名稱稱的長度必須是1到15個字元。</span><span class="sxs-lookup"><span data-stu-id="80710-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="80710-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="80710-122">-CustomData</span></span>
<span data-ttu-id="80710-123">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="80710-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="80710-124">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="80710-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="80710-125">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="80710-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="80710-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80710-126">-DefaultProfile</span></span>
<span data-ttu-id="80710-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80710-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80710-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="80710-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="80710-129">表示這個 Cmdlet 停用密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="80710-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="80710-130">-監聽器</span><span class="sxs-lookup"><span data-stu-id="80710-130">-Listener</span></span>
<span data-ttu-id="80710-131">指定 Windows 遠端系統管理 (WinRM) 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="80710-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="80710-132">這會啟用遠端 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="80710-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="80710-133">您可以使用 Add-AzureRmVmssWinRMListener Cmdlet 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="80710-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="80710-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="80710-134">-PublicKey</span></span>
<span data-ttu-id="80710-135">指定 SSH) 公用金鑰組象 (的安全 Shell。</span><span class="sxs-lookup"><span data-stu-id="80710-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="80710-136">您可以使用 Add-AzureRmVMSshPublicKey Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="80710-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="80710-137">密碼</span><span class="sxs-lookup"><span data-stu-id="80710-137">-Secret</span></span>
<span data-ttu-id="80710-138">指定包含要放在虛擬機器上之憑證參照的機密物件。</span><span class="sxs-lookup"><span data-stu-id="80710-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="80710-139">您可以使用 Add-AzureRmVmssSecret Cmdlet 來建立機密物件。</span><span class="sxs-lookup"><span data-stu-id="80710-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="80710-140">-時區</span><span class="sxs-lookup"><span data-stu-id="80710-140">-TimeZone</span></span>
<span data-ttu-id="80710-141">指定虛擬機器的時區。</span><span class="sxs-lookup"><span data-stu-id="80710-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="80710-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="80710-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="80710-143">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="80710-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="80710-144">您可以使用 New-AzureRmVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="80710-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="80710-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="80710-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="80710-146">指出是否已針對自動更新啟用 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="80710-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="80710-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="80710-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="80710-148">指出是否應該在 VMSS 的虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="80710-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="80710-149">-確認</span><span class="sxs-lookup"><span data-stu-id="80710-149">-Confirm</span></span>
<span data-ttu-id="80710-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80710-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80710-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80710-151">-WhatIf</span></span>
<span data-ttu-id="80710-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80710-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80710-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80710-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80710-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80710-154">CommonParameters</span></span>
<span data-ttu-id="80710-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80710-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80710-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80710-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80710-157">輸入</span><span class="sxs-lookup"><span data-stu-id="80710-157">INPUTS</span></span>

## <span data-ttu-id="80710-158">輸出</span><span class="sxs-lookup"><span data-stu-id="80710-158">OUTPUTS</span></span>

### <span data-ttu-id="80710-159">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="80710-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="80710-160">筆記</span><span class="sxs-lookup"><span data-stu-id="80710-160">NOTES</span></span>

## <span data-ttu-id="80710-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="80710-161">RELATED LINKS</span></span>

[<span data-ttu-id="80710-162">附加 AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="80710-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="80710-163">附加 AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="80710-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="80710-164">附加 AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="80710-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="80710-165">附加 AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="80710-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="80710-166">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="80710-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


