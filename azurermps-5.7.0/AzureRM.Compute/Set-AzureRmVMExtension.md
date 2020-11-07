---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623476"
---
# <span data-ttu-id="c96e3-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c96e3-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="c96e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c96e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c96e3-103">更新擴充屬性或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c96e3-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c96e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c96e3-104">SYNTAX</span></span>

### <span data-ttu-id="c96e3-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="c96e3-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c96e3-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="c96e3-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c96e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="c96e3-107">DESCRIPTION</span></span>
<span data-ttu-id="c96e3-108">**AzureRmVMExtension** Cmdlet 會更新現有虛擬機器延伸的屬性，或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c96e3-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="c96e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="c96e3-109">EXAMPLES</span></span>

### <span data-ttu-id="c96e3-110">範例1：使用雜湊資料表修改設定</span><span class="sxs-lookup"><span data-stu-id="c96e3-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="c96e3-111">前兩個命令使用標準的 Windows PowerShell 語法來建立雜湊資料表，然後將這些雜湊資料表儲存在 $Settings 並 $ProtectedSettings 變數中。</span><span class="sxs-lookup"><span data-stu-id="c96e3-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="c96e3-112">如需詳細資訊，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="c96e3-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="c96e3-113">第二個命令包含先前建立並儲存在變數中的兩個值。</span><span class="sxs-lookup"><span data-stu-id="c96e3-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="c96e3-114">最後一個命令會根據 $Settings 和 $ProtectedSettings 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="c96e3-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="c96e3-115">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="c96e3-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="c96e3-116">範例2：使用字串修改設定</span><span class="sxs-lookup"><span data-stu-id="c96e3-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="c96e3-117">前兩個命令會建立包含設定的字串，然後將它們儲存在 $SettingsString 並 $ProtectedSettingsString 變數中。</span><span class="sxs-lookup"><span data-stu-id="c96e3-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="c96e3-118">最後一個命令會根據 $SettingsString 和 $ProtectedSettingsString 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="c96e3-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="c96e3-119">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="c96e3-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="c96e3-120">參數</span><span class="sxs-lookup"><span data-stu-id="c96e3-120">PARAMETERS</span></span>

### <span data-ttu-id="c96e3-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c96e3-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c96e3-122">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="c96e3-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="c96e3-123">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="c96e3-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c96e3-124">-ExtensionType</span></span>
<span data-ttu-id="c96e3-125">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="c96e3-125">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="c96e3-126">-ForceRerun</span></span>
<span data-ttu-id="c96e3-127">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="c96e3-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="c96e3-128">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="c96e3-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="c96e3-129">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="c96e3-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="c96e3-130">-Location</span></span>
<span data-ttu-id="c96e3-131">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-131">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="c96e3-132">-Name</span></span>
<span data-ttu-id="c96e3-133">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e3-133">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="c96e3-134">-ProtectedSettings</span></span>
<span data-ttu-id="c96e3-135">以雜湊資料表的方式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="c96e3-136">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-136">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="c96e3-137">-ProtectedSettingString</span></span>
<span data-ttu-id="c96e3-138">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="c96e3-139">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-139">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c96e3-140">-Publisher</span></span>
<span data-ttu-id="c96e3-141">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e3-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="c96e3-142">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e3-142">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96e3-143">-ResourceGroupName</span></span>
<span data-ttu-id="c96e3-144">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e3-144">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-145">-設定</span><span class="sxs-lookup"><span data-stu-id="c96e3-145">-Settings</span></span>
<span data-ttu-id="c96e3-146">以雜湊資料表的方式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="c96e3-147">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-147">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-148">-SettingString</span><span class="sxs-lookup"><span data-stu-id="c96e3-148">-SettingString</span></span>
<span data-ttu-id="c96e3-149">以字串形式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="c96e3-150">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="c96e3-150">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c96e3-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="c96e3-152">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="c96e3-152">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="c96e3-153">-VMName</span></span>
<span data-ttu-id="c96e3-154">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e3-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c96e3-155">這個 Cmdlet 會修改此參數指定之虛擬機器的延伸。</span><span class="sxs-lookup"><span data-stu-id="c96e3-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-156">-確認</span><span class="sxs-lookup"><span data-stu-id="c96e3-156">-Confirm</span></span>
<span data-ttu-id="c96e3-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c96e3-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c96e3-158">-WhatIf</span></span>
<span data-ttu-id="c96e3-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c96e3-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c96e3-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c96e3-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96e3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96e3-161">CommonParameters</span></span>
<span data-ttu-id="c96e3-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c96e3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96e3-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c96e3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96e3-164">輸入</span><span class="sxs-lookup"><span data-stu-id="c96e3-164">INPUTS</span></span>

### <span data-ttu-id="c96e3-165">所有</span><span class="sxs-lookup"><span data-stu-id="c96e3-165">None</span></span>
<span data-ttu-id="c96e3-166">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c96e3-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c96e3-167">輸出</span><span class="sxs-lookup"><span data-stu-id="c96e3-167">OUTPUTS</span></span>

## <span data-ttu-id="c96e3-168">筆記</span><span class="sxs-lookup"><span data-stu-id="c96e3-168">NOTES</span></span>

## <span data-ttu-id="c96e3-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="c96e3-169">RELATED LINKS</span></span>

[<span data-ttu-id="c96e3-170">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c96e3-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="c96e3-171">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c96e3-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


