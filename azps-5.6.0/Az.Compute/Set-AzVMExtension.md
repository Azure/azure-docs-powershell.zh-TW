---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: b1c7a45f538c10c2ef6c2f03809a127a21237fc9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909137"
---
# <span data-ttu-id="72249-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="72249-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="72249-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72249-102">SYNOPSIS</span></span>
<span data-ttu-id="72249-103">更新擴充功能屬性或將擴充功能新增加到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="72249-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="72249-104">語法</span><span class="sxs-lookup"><span data-stu-id="72249-104">SYNTAX</span></span>

### <span data-ttu-id="72249-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="72249-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72249-106">設定字串</span><span class="sxs-lookup"><span data-stu-id="72249-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72249-107">描述</span><span class="sxs-lookup"><span data-stu-id="72249-107">DESCRIPTION</span></span>
<span data-ttu-id="72249-108">**Set-Az VIRTUALExtension** Cmdlet 會更新現有虛擬機器擴充功能的屬性，或新增擴充功能至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="72249-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="72249-109">例子</span><span class="sxs-lookup"><span data-stu-id="72249-109">EXAMPLES</span></span>

### <span data-ttu-id="72249-110">範例 1：使用雜湊表修改設定</span><span class="sxs-lookup"><span data-stu-id="72249-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="72249-111">前兩個命令會使用標準 Windows PowerShell 語法來建立雜湊表，然後將這些雜湊表儲存在 $Settings 中$ProtectedSettings變數。</span><span class="sxs-lookup"><span data-stu-id="72249-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="72249-112">如需要詳細資訊，請鍵入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="72249-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="72249-113">第二個命令包含先前建立並儲存在變數中的兩個值。</span><span class="sxs-lookup"><span data-stu-id="72249-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="72249-114">最後一個命令會修改 ResourceGroup11 中 VirtualMachine22 的擴充功能，$Settings$ProtectedSettings。</span><span class="sxs-lookup"><span data-stu-id="72249-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="72249-115">命令會指定包括發行者與擴充功能類型的其他所需資訊。</span><span class="sxs-lookup"><span data-stu-id="72249-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="72249-116">範例 2：使用字串修改設定</span><span class="sxs-lookup"><span data-stu-id="72249-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="72249-117">前兩個命令會建立包含設定的字串，然後將這些字串儲存在$SettingsString$ProtectedSettingsString變數。</span><span class="sxs-lookup"><span data-stu-id="72249-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="72249-118">最後一個命令會修改 ResourceGroup11 中 VirtualMachine22 的擴充功能，$SettingsString$ProtectedSettingsString。</span><span class="sxs-lookup"><span data-stu-id="72249-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="72249-119">命令會指定包括發行者與擴充功能類型的其他所需資訊。</span><span class="sxs-lookup"><span data-stu-id="72249-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="72249-120">參數</span><span class="sxs-lookup"><span data-stu-id="72249-120">PARAMETERS</span></span>

### <span data-ttu-id="72249-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72249-121">-AsJob</span></span>
<span data-ttu-id="72249-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="72249-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72249-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72249-123">-DefaultProfile</span></span>
<span data-ttu-id="72249-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72249-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72249-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="72249-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="72249-126">表示此 Cmdlet 會防止 Azure 來賓代理程式自動更新擴充功能至較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="72249-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="72249-127">根據預設，此 Cmdlet 可讓來賓代理程式更新擴充功能。</span><span class="sxs-lookup"><span data-stu-id="72249-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="72249-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="72249-129">指出如果有較新版本的擴充功能可用，該擴充功能是否應該由平臺自動升級。</span><span class="sxs-lookup"><span data-stu-id="72249-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72249-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="72249-130">-ExtensionType</span></span>
<span data-ttu-id="72249-131">指定擴充功能類型。</span><span class="sxs-lookup"><span data-stu-id="72249-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="72249-132">-ForceRerun</span></span>
<span data-ttu-id="72249-133">表示此 Cmdlet 強制在虛擬機器上重新進行相同的擴充功能組配置，而不需要卸載並重新安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="72249-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="72249-134">該值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="72249-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="72249-135">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="72249-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="72249-136">-位置</span><span class="sxs-lookup"><span data-stu-id="72249-136">-Location</span></span>
<span data-ttu-id="72249-137">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="72249-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="72249-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="72249-138">-Name</span></span>
<span data-ttu-id="72249-139">指定副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="72249-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72249-140">-NoWait</span></span>
<span data-ttu-id="72249-141">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="72249-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="72249-142">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="72249-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72249-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="72249-143">-ProtectedSettings</span></span>
<span data-ttu-id="72249-144">指定副檔名的私人群組原則，做為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="72249-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="72249-145">此 Cmdlet 會加密私人組配置。</span><span class="sxs-lookup"><span data-stu-id="72249-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="72249-146">-ProtectedSettingString</span></span>
<span data-ttu-id="72249-147">指定副檔名的私人群組原則，做為字串。</span><span class="sxs-lookup"><span data-stu-id="72249-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="72249-148">此 Cmdlet 會加密私人組配置。</span><span class="sxs-lookup"><span data-stu-id="72249-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="72249-149">-Publisher</span></span>
<span data-ttu-id="72249-150">指定擴充功能發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="72249-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="72249-151">發行者在發行者註冊擴充功能時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="72249-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72249-152">-ResourceGroupName</span></span>
<span data-ttu-id="72249-153">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="72249-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-154">-設定</span><span class="sxs-lookup"><span data-stu-id="72249-154">-Settings</span></span>
<span data-ttu-id="72249-155">指定副檔名的公用群組原則，做為雜湊表。</span><span class="sxs-lookup"><span data-stu-id="72249-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="72249-156">此 Cmdlet 不會加密公用組配置。</span><span class="sxs-lookup"><span data-stu-id="72249-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="72249-157">-SettingString</span></span>
<span data-ttu-id="72249-158">指定副檔名的公用組組，做為字串。</span><span class="sxs-lookup"><span data-stu-id="72249-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="72249-159">此 Cmdlet 不會加密公用組配置。</span><span class="sxs-lookup"><span data-stu-id="72249-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="72249-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="72249-161">指定要用於此虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="72249-161">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="72249-162">-VMName</span></span>
<span data-ttu-id="72249-163">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="72249-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="72249-164">此 Cmdlet 會修改此參數指定的虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="72249-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72249-165">-確認</span><span class="sxs-lookup"><span data-stu-id="72249-165">-Confirm</span></span>
<span data-ttu-id="72249-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="72249-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72249-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72249-167">-WhatIf</span></span>
<span data-ttu-id="72249-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72249-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72249-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72249-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72249-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72249-170">CommonParameters</span></span>
<span data-ttu-id="72249-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72249-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72249-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72249-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72249-173">輸入</span><span class="sxs-lookup"><span data-stu-id="72249-173">INPUTS</span></span>

### <span data-ttu-id="72249-174">System.String</span><span class="sxs-lookup"><span data-stu-id="72249-174">System.String</span></span>

### <span data-ttu-id="72249-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="72249-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="72249-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72249-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72249-177">輸出</span><span class="sxs-lookup"><span data-stu-id="72249-177">OUTPUTS</span></span>

### <span data-ttu-id="72249-178">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72249-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72249-179">筆記</span><span class="sxs-lookup"><span data-stu-id="72249-179">NOTES</span></span>

## <span data-ttu-id="72249-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="72249-180">RELATED LINKS</span></span>

[<span data-ttu-id="72249-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="72249-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="72249-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="72249-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


