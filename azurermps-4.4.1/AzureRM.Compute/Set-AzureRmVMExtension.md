---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449635"
---
# <span data-ttu-id="2f167-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2f167-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="2f167-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f167-102">SYNOPSIS</span></span>
<span data-ttu-id="2f167-103">更新擴充屬性或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f167-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f167-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f167-104">SYNTAX</span></span>

### <span data-ttu-id="2f167-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="2f167-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f167-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="2f167-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f167-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f167-107">DESCRIPTION</span></span>
<span data-ttu-id="2f167-108">**AzureRmVMExtension** Cmdlet 會更新現有虛擬機器延伸的屬性，或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f167-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="2f167-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f167-109">EXAMPLES</span></span>

### <span data-ttu-id="2f167-110">範例1：使用雜湊資料表修改設定</span><span class="sxs-lookup"><span data-stu-id="2f167-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="2f167-111">前兩個命令使用標準的 Windows PowerShell 語法來建立雜湊資料表，然後將這些雜湊資料表儲存在 $Settings 並 $ProtectedSettings 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f167-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="2f167-112">如需詳細資訊，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="2f167-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2f167-113">第二個命令包含先前建立並儲存在變數中的兩個值。</span><span class="sxs-lookup"><span data-stu-id="2f167-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="2f167-114">最後一個命令會根據 $Settings 和 $ProtectedSettings 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="2f167-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="2f167-115">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="2f167-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="2f167-116">範例2：使用字串修改設定</span><span class="sxs-lookup"><span data-stu-id="2f167-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="2f167-117">前兩個命令會建立包含設定的字串，然後將它們儲存在 $SettingsString 並 $ProtectedSettingsString 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f167-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="2f167-118">最後一個命令會根據 $SettingsString 和 $ProtectedSettingsString 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="2f167-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="2f167-119">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="2f167-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="2f167-120">參數</span><span class="sxs-lookup"><span data-stu-id="2f167-120">PARAMETERS</span></span>

### <span data-ttu-id="2f167-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f167-121">-DefaultProfile</span></span>
<span data-ttu-id="2f167-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f167-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f167-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2f167-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2f167-124">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="2f167-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="2f167-125">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="2f167-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="2f167-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2f167-126">-ExtensionType</span></span>
<span data-ttu-id="2f167-127">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="2f167-127">Specifies the extension type.</span></span>

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

### <span data-ttu-id="2f167-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2f167-128">-ForceRerun</span></span>
<span data-ttu-id="2f167-129">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="2f167-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2f167-130">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="2f167-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="2f167-131">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="2f167-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2f167-132">-位置</span><span class="sxs-lookup"><span data-stu-id="2f167-132">-Location</span></span>
<span data-ttu-id="2f167-133">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="2f167-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2f167-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f167-134">-Name</span></span>
<span data-ttu-id="2f167-135">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f167-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="2f167-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="2f167-136">-ProtectedSettings</span></span>
<span data-ttu-id="2f167-137">以雜湊資料表的方式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="2f167-138">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-138">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="2f167-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="2f167-139">-ProtectedSettingString</span></span>
<span data-ttu-id="2f167-140">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="2f167-141">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-141">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="2f167-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2f167-142">-Publisher</span></span>
<span data-ttu-id="2f167-143">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f167-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="2f167-144">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="2f167-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="2f167-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f167-145">-ResourceGroupName</span></span>
<span data-ttu-id="2f167-146">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f167-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2f167-147">-設定</span><span class="sxs-lookup"><span data-stu-id="2f167-147">-Settings</span></span>
<span data-ttu-id="2f167-148">以雜湊資料表的方式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="2f167-149">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-149">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="2f167-150">-SettingString</span><span class="sxs-lookup"><span data-stu-id="2f167-150">-SettingString</span></span>
<span data-ttu-id="2f167-151">以字串形式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="2f167-152">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="2f167-152">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="2f167-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2f167-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="2f167-154">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2f167-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="2f167-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="2f167-155">-VMName</span></span>
<span data-ttu-id="2f167-156">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f167-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2f167-157">這個 Cmdlet 會修改此參數指定之虛擬機器的延伸。</span><span class="sxs-lookup"><span data-stu-id="2f167-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f167-158">-確認</span><span class="sxs-lookup"><span data-stu-id="2f167-158">-Confirm</span></span>
<span data-ttu-id="2f167-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f167-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f167-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f167-160">-WhatIf</span></span>
<span data-ttu-id="2f167-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f167-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2f167-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f167-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f167-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f167-163">CommonParameters</span></span>
<span data-ttu-id="2f167-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f167-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f167-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f167-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f167-166">輸入</span><span class="sxs-lookup"><span data-stu-id="2f167-166">INPUTS</span></span>

## <span data-ttu-id="2f167-167">輸出</span><span class="sxs-lookup"><span data-stu-id="2f167-167">OUTPUTS</span></span>

## <span data-ttu-id="2f167-168">筆記</span><span class="sxs-lookup"><span data-stu-id="2f167-168">NOTES</span></span>

## <span data-ttu-id="2f167-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f167-169">RELATED LINKS</span></span>

[<span data-ttu-id="2f167-170">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2f167-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="2f167-171">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2f167-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


