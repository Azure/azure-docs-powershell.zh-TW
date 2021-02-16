---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141214"
---
# <span data-ttu-id="a7867-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7867-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="a7867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7867-102">SYNOPSIS</span></span>
<span data-ttu-id="a7867-103">更新擴充屬性或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7867-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a7867-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7867-104">SYNTAX</span></span>

### <span data-ttu-id="a7867-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="a7867-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7867-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="a7867-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7867-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7867-107">DESCRIPTION</span></span>
<span data-ttu-id="a7867-108">**AzVMExtension** Cmdlet 會更新現有虛擬機器延伸的屬性，或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7867-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="a7867-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7867-109">EXAMPLES</span></span>

### <span data-ttu-id="a7867-110">範例1：使用雜湊資料表修改設定</span><span class="sxs-lookup"><span data-stu-id="a7867-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="a7867-111">前兩個命令使用標準的 Windows PowerShell 語法來建立雜湊資料表，然後將這些雜湊資料表儲存在 $Settings 並 $ProtectedSettings 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7867-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="a7867-112">如需詳細資訊，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="a7867-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a7867-113">第二個命令包含先前建立並儲存在變數中的兩個值。</span><span class="sxs-lookup"><span data-stu-id="a7867-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="a7867-114">最後一個命令會根據 $Settings 和 $ProtectedSettings 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="a7867-115">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="a7867-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="a7867-116">範例2：使用字串修改設定</span><span class="sxs-lookup"><span data-stu-id="a7867-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="a7867-117">前兩個命令會建立包含設定的字串，然後將它們儲存在 $SettingsString 並 $ProtectedSettingsString 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7867-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="a7867-118">最後一個命令會根據 $SettingsString 和 $ProtectedSettingsString 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="a7867-119">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="a7867-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="a7867-120">參數</span><span class="sxs-lookup"><span data-stu-id="a7867-120">PARAMETERS</span></span>

### <span data-ttu-id="a7867-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7867-121">-AsJob</span></span>
<span data-ttu-id="a7867-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a7867-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7867-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7867-123">-DefaultProfile</span></span>
<span data-ttu-id="a7867-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7867-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7867-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a7867-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a7867-126">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="a7867-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="a7867-127">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="a7867-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7867-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="a7867-129">指示如果有更新版本的擴充功能，平臺是否應自動升級延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

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

### <span data-ttu-id="a7867-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a7867-130">-ExtensionType</span></span>
<span data-ttu-id="a7867-131">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="a7867-131">Specifies the extension type.</span></span>

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

### <span data-ttu-id="a7867-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a7867-132">-ForceRerun</span></span>
<span data-ttu-id="a7867-133">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a7867-134">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="a7867-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="a7867-135">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="a7867-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a7867-136">-位置</span><span class="sxs-lookup"><span data-stu-id="a7867-136">-Location</span></span>
<span data-ttu-id="a7867-137">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="a7867-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a7867-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7867-138">-Name</span></span>
<span data-ttu-id="a7867-139">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7867-139">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="a7867-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7867-140">-NoWait</span></span>
<span data-ttu-id="a7867-141">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="a7867-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a7867-142">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="a7867-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a7867-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="a7867-143">-ProtectedSettings</span></span>
<span data-ttu-id="a7867-144">以雜湊資料表的方式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a7867-145">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-145">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="a7867-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="a7867-146">-ProtectedSettingString</span></span>
<span data-ttu-id="a7867-147">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a7867-148">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-148">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="a7867-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a7867-149">-Publisher</span></span>
<span data-ttu-id="a7867-150">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7867-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a7867-151">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="a7867-151">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="a7867-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7867-152">-ResourceGroupName</span></span>
<span data-ttu-id="a7867-153">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7867-153">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a7867-154">-設定</span><span class="sxs-lookup"><span data-stu-id="a7867-154">-Settings</span></span>
<span data-ttu-id="a7867-155">以雜湊資料表的方式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="a7867-156">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-156">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="a7867-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="a7867-157">-SettingString</span></span>
<span data-ttu-id="a7867-158">以字串形式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="a7867-159">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="a7867-159">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="a7867-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a7867-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="a7867-161">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="a7867-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="a7867-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="a7867-162">-VMName</span></span>
<span data-ttu-id="a7867-163">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7867-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a7867-164">這個 Cmdlet 會修改此參數指定之虛擬機器的延伸。</span><span class="sxs-lookup"><span data-stu-id="a7867-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7867-165">-確認</span><span class="sxs-lookup"><span data-stu-id="a7867-165">-Confirm</span></span>
<span data-ttu-id="a7867-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7867-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7867-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7867-167">-WhatIf</span></span>
<span data-ttu-id="a7867-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7867-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7867-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7867-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7867-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7867-170">CommonParameters</span></span>
<span data-ttu-id="a7867-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7867-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7867-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7867-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7867-173">輸入</span><span class="sxs-lookup"><span data-stu-id="a7867-173">INPUTS</span></span>

### <span data-ttu-id="a7867-174">System.object</span><span class="sxs-lookup"><span data-stu-id="a7867-174">System.String</span></span>

### <span data-ttu-id="a7867-175">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7867-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a7867-176">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a7867-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7867-177">輸出</span><span class="sxs-lookup"><span data-stu-id="a7867-177">OUTPUTS</span></span>

### <span data-ttu-id="a7867-178">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a7867-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a7867-179">筆記</span><span class="sxs-lookup"><span data-stu-id="a7867-179">NOTES</span></span>

## <span data-ttu-id="a7867-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7867-180">RELATED LINKS</span></span>

[<span data-ttu-id="a7867-181">AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7867-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="a7867-182">移除-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7867-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


