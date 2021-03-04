---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: accea82dd6594d71f627d6c3e32943d004fa35e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917009"
---
# <span data-ttu-id="2ee0d-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2ee0d-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="2ee0d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ee0d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee0d-103">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="2ee0d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ee0d-104">SYNTAX</span></span>

### <span data-ttu-id="2ee0d-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="2ee0d-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee0d-106">更新</span><span class="sxs-lookup"><span data-stu-id="2ee0d-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ee0d-107">描述</span><span class="sxs-lookup"><span data-stu-id="2ee0d-107">DESCRIPTION</span></span>
<span data-ttu-id="2ee0d-108">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="2ee0d-109">例子</span><span class="sxs-lookup"><span data-stu-id="2ee0d-109">EXAMPLES</span></span>

### <span data-ttu-id="2ee0d-110">範例 1：在一部電腦上設定延伸模組</span><span class="sxs-lookup"><span data-stu-id="2ee0d-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="2ee0d-111">設定電腦上延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="2ee0d-112">範例 2：使用透過管線指定的擴充參數設定擴充功能</span><span class="sxs-lookup"><span data-stu-id="2ee0d-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="2ee0d-113">這會使用透過管線傳遞的物件所提供的擴充功能參數來設定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="2ee0d-114">如果您想要抓取一部電腦的參數，然後將參數應用至另一部電腦，這是很棒的方法。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="2ee0d-115">參數</span><span class="sxs-lookup"><span data-stu-id="2ee0d-115">PARAMETERS</span></span>

### <span data-ttu-id="2ee0d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ee0d-116">-AsJob</span></span>
<span data-ttu-id="2ee0d-117">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2ee0d-117">Run the command as a job</span></span>

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

### <span data-ttu-id="2ee0d-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2ee0d-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2ee0d-119">指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用該次要版本。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="2ee0d-120">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee0d-121">-DefaultProfile</span></span>
<span data-ttu-id="2ee0d-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="2ee0d-123">-ExtensionParameter</span></span>
<span data-ttu-id="2ee0d-124">說明機器延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="2ee0d-125">若要建構，請參閱 EXTENSIONPARAMETER 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2ee0d-126">-ExtensionType</span></span>
<span data-ttu-id="2ee0d-127">指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2ee0d-128">-ForceRerun</span></span>
<span data-ttu-id="2ee0d-129">延伸處理常式如何強制更新，即使擴充功能組沒有變更。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-130">-位置</span><span class="sxs-lookup"><span data-stu-id="2ee0d-130">-Location</span></span>
<span data-ttu-id="2ee0d-131">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="2ee0d-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="2ee0d-132">-MachineName</span></span>
<span data-ttu-id="2ee0d-133">應該建立或更新擴充功能的機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ee0d-134">-Name</span></span>
<span data-ttu-id="2ee0d-135">電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ee0d-136">-NoWait</span></span>
<span data-ttu-id="2ee0d-137">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2ee0d-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ee0d-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2ee0d-138">-ProtectedSetting</span></span>
<span data-ttu-id="2ee0d-139">擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2ee0d-140">-Publisher</span></span>
<span data-ttu-id="2ee0d-141">擴充處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee0d-142">-ResourceGroupName</span></span>
<span data-ttu-id="2ee0d-143">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-144">-設定</span><span class="sxs-lookup"><span data-stu-id="2ee0d-144">-Setting</span></span>
<span data-ttu-id="2ee0d-145">Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ee0d-146">-SubscriptionId</span></span>
<span data-ttu-id="2ee0d-147">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ee0d-148">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-149">-標記</span><span class="sxs-lookup"><span data-stu-id="2ee0d-149">-Tag</span></span>
<span data-ttu-id="2ee0d-150">資源標記。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2ee0d-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="2ee0d-152">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee0d-153">-確認</span><span class="sxs-lookup"><span data-stu-id="2ee0d-153">-Confirm</span></span>
<span data-ttu-id="2ee0d-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee0d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee0d-155">-WhatIf</span></span>
<span data-ttu-id="2ee0d-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee0d-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee0d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee0d-158">CommonParameters</span></span>
<span data-ttu-id="2ee0d-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee0d-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ee0d-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee0d-161">輸入</span><span class="sxs-lookup"><span data-stu-id="2ee0d-161">INPUTS</span></span>

### <span data-ttu-id="2ee0d-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2ee0d-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="2ee0d-163">輸出</span><span class="sxs-lookup"><span data-stu-id="2ee0d-163">OUTPUTS</span></span>

### <span data-ttu-id="2ee0d-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2ee0d-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="2ee0d-165">筆記</span><span class="sxs-lookup"><span data-stu-id="2ee0d-165">NOTES</span></span>

<span data-ttu-id="2ee0d-166">別名</span><span class="sxs-lookup"><span data-stu-id="2ee0d-166">ALIASES</span></span>

<span data-ttu-id="2ee0d-167">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2ee0d-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ee0d-168">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ee0d-169">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ee0d-170">EXTENSIONPARAMETER： <IMachineExtension> 說明機器延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="2ee0d-171">`Location <String>`：資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="2ee0d-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="2ee0d-172">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2ee0d-173">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2ee0d-174">`[AutoUpgradeMinorVersion <Boolean?>]`：指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="2ee0d-175">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="2ee0d-176">`[ForceUpdateTag <String>]`：即使擴充功能組配置沒有變更，擴充處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="2ee0d-177">`[MachineExtensionType <String>]`：指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="2ee0d-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`：擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="2ee0d-179">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="2ee0d-180">`[Setting <IMachineExtensionPropertiesSettings>]`：Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="2ee0d-181">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="2ee0d-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="2ee0d-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ee0d-182">RELATED LINKS</span></span>

