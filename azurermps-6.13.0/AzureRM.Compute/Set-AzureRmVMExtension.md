---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: bdd502a90840201560bb9a6a4ea5411b4ccc1a6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449234"
---
# <span data-ttu-id="f8625-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8625-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="f8625-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8625-102">SYNOPSIS</span></span>
<span data-ttu-id="f8625-103">更新擴充屬性或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f8625-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8625-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8625-104">SYNTAX</span></span>

### <span data-ttu-id="f8625-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="f8625-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8625-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="f8625-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8625-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8625-107">DESCRIPTION</span></span>
<span data-ttu-id="f8625-108">**AzureRmVMExtension** Cmdlet 會更新現有虛擬機器延伸的屬性，或將延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f8625-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="f8625-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8625-109">EXAMPLES</span></span>

### <span data-ttu-id="f8625-110">範例1：使用雜湊資料表修改設定</span><span class="sxs-lookup"><span data-stu-id="f8625-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="f8625-111">前兩個命令使用標準的 Windows PowerShell 語法來建立雜湊資料表，然後將這些雜湊資料表儲存在 $Settings 並 $ProtectedSettings 變數中。</span><span class="sxs-lookup"><span data-stu-id="f8625-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="f8625-112">如需詳細資訊，請輸入 `Get-Help about_Hash_Tables` 。</span><span class="sxs-lookup"><span data-stu-id="f8625-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f8625-113">第二個命令包含先前建立並儲存在變數中的兩個值。</span><span class="sxs-lookup"><span data-stu-id="f8625-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="f8625-114">最後一個命令會根據 $Settings 和 $ProtectedSettings 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="f8625-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="f8625-115">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="f8625-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="f8625-116">範例2：使用字串修改設定</span><span class="sxs-lookup"><span data-stu-id="f8625-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="f8625-117">前兩個命令會建立包含設定的字串，然後將它們儲存在 $SettingsString 並 $ProtectedSettingsString 變數中。</span><span class="sxs-lookup"><span data-stu-id="f8625-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="f8625-118">最後一個命令會根據 $SettingsString 和 $ProtectedSettingsString 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="f8625-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="f8625-119">此命令會指定包含發行者及延伸類型的其他必要資訊。</span><span class="sxs-lookup"><span data-stu-id="f8625-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="f8625-120">參數</span><span class="sxs-lookup"><span data-stu-id="f8625-120">PARAMETERS</span></span>

### <span data-ttu-id="f8625-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8625-121">-AsJob</span></span>
<span data-ttu-id="f8625-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8625-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8625-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8625-123">-DefaultProfile</span></span>
<span data-ttu-id="f8625-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8625-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8625-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f8625-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f8625-126">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="f8625-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="f8625-127">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="f8625-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="f8625-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f8625-128">-ExtensionType</span></span>
<span data-ttu-id="f8625-129">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="f8625-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="f8625-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f8625-130">-ForceRerun</span></span>
<span data-ttu-id="f8625-131">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="f8625-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f8625-132">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="f8625-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="f8625-133">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="f8625-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f8625-134">-位置</span><span class="sxs-lookup"><span data-stu-id="f8625-134">-Location</span></span>
<span data-ttu-id="f8625-135">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="f8625-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f8625-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8625-136">-Name</span></span>
<span data-ttu-id="f8625-137">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8625-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="f8625-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="f8625-138">-ProtectedSettings</span></span>
<span data-ttu-id="f8625-139">以雜湊資料表的方式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f8625-140">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-140">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="f8625-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="f8625-141">-ProtectedSettingString</span></span>
<span data-ttu-id="f8625-142">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f8625-143">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="f8625-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f8625-144">-Publisher</span></span>
<span data-ttu-id="f8625-145">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8625-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f8625-146">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="f8625-146">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="f8625-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8625-147">-ResourceGroupName</span></span>
<span data-ttu-id="f8625-148">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8625-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f8625-149">-設定</span><span class="sxs-lookup"><span data-stu-id="f8625-149">-Settings</span></span>
<span data-ttu-id="f8625-150">以雜湊資料表的方式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f8625-151">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-151">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="f8625-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="f8625-152">-SettingString</span></span>
<span data-ttu-id="f8625-153">以字串形式指定延伸的公用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="f8625-154">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="f8625-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="f8625-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f8625-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="f8625-156">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="f8625-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="f8625-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="f8625-157">-VMName</span></span>
<span data-ttu-id="f8625-158">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8625-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f8625-159">這個 Cmdlet 會修改此參數指定之虛擬機器的延伸。</span><span class="sxs-lookup"><span data-stu-id="f8625-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8625-160">-確認</span><span class="sxs-lookup"><span data-stu-id="f8625-160">-Confirm</span></span>
<span data-ttu-id="f8625-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8625-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8625-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8625-162">-WhatIf</span></span>
<span data-ttu-id="f8625-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8625-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8625-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8625-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8625-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8625-165">CommonParameters</span></span>
<span data-ttu-id="f8625-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8625-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8625-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8625-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8625-168">輸入</span><span class="sxs-lookup"><span data-stu-id="f8625-168">INPUTS</span></span>

### <span data-ttu-id="f8625-169">System.object</span><span class="sxs-lookup"><span data-stu-id="f8625-169">System.String</span></span>

### <span data-ttu-id="f8625-170">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8625-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f8625-171">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f8625-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8625-172">輸出</span><span class="sxs-lookup"><span data-stu-id="f8625-172">OUTPUTS</span></span>

### <span data-ttu-id="f8625-173">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f8625-173">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f8625-174">筆記</span><span class="sxs-lookup"><span data-stu-id="f8625-174">NOTES</span></span>

## <span data-ttu-id="f8625-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8625-175">RELATED LINKS</span></span>

[<span data-ttu-id="f8625-176">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8625-176">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="f8625-177">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8625-177">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


