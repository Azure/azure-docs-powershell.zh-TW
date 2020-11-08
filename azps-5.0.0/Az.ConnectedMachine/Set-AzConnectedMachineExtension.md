---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140178"
---
# <span data-ttu-id="3d178-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3d178-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="3d178-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d178-102">SYNOPSIS</span></span>
<span data-ttu-id="3d178-103">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="3d178-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3d178-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d178-104">SYNTAX</span></span>

### <span data-ttu-id="3d178-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3d178-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3d178-106">時更新</span><span class="sxs-lookup"><span data-stu-id="3d178-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d178-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d178-107">DESCRIPTION</span></span>
<span data-ttu-id="3d178-108">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="3d178-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3d178-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d178-109">EXAMPLES</span></span>

### <span data-ttu-id="3d178-110">範例1：在電腦上設定延伸</span><span class="sxs-lookup"><span data-stu-id="3d178-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="3d178-111">在電腦上設定延伸。</span><span class="sxs-lookup"><span data-stu-id="3d178-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="3d178-112">範例2：使用透過管線指定的延伸參數設定延伸</span><span class="sxs-lookup"><span data-stu-id="3d178-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="3d178-113">這會將延伸設定為透過管線傳入的物件所提供的延伸參數。</span><span class="sxs-lookup"><span data-stu-id="3d178-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="3d178-114">如果您想要抓取一台電腦的參數，並將它套用至另一部電腦，這是很好的方式。</span><span class="sxs-lookup"><span data-stu-id="3d178-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="3d178-115">參數</span><span class="sxs-lookup"><span data-stu-id="3d178-115">PARAMETERS</span></span>

### <span data-ttu-id="3d178-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d178-116">-AsJob</span></span>
<span data-ttu-id="3d178-117">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="3d178-117">Run the command as a job</span></span>

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

### <span data-ttu-id="3d178-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3d178-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3d178-119">指示在部署時間，延伸時是否應使用較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="3d178-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="3d178-120">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="3d178-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="3d178-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d178-121">-DefaultProfile</span></span>
<span data-ttu-id="3d178-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d178-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d178-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="3d178-123">-ExtensionParameter</span></span>
<span data-ttu-id="3d178-124">描述電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="3d178-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="3d178-125">若要建立，請參閱 EXTENSIONPARAMETER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="3d178-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d178-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3d178-126">-ExtensionType</span></span>
<span data-ttu-id="3d178-127">指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="3d178-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="3d178-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3d178-128">-ForceRerun</span></span>
<span data-ttu-id="3d178-129">即使延伸設定尚未變更，延伸處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="3d178-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="3d178-130">-位置</span><span class="sxs-lookup"><span data-stu-id="3d178-130">-Location</span></span>
<span data-ttu-id="3d178-131">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="3d178-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="3d178-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="3d178-132">-MachineName</span></span>
<span data-ttu-id="3d178-133">應該在其中建立或更新延伸的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3d178-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="3d178-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d178-134">-Name</span></span>
<span data-ttu-id="3d178-135">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d178-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="3d178-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d178-136">-NoWait</span></span>
<span data-ttu-id="3d178-137">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="3d178-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d178-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3d178-138">-ProtectedSetting</span></span>
<span data-ttu-id="3d178-139">副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="3d178-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="3d178-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3d178-140">-Publisher</span></span>
<span data-ttu-id="3d178-141">延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d178-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="3d178-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d178-142">-ResourceGroupName</span></span>
<span data-ttu-id="3d178-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d178-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d178-144">-設定</span><span class="sxs-lookup"><span data-stu-id="3d178-144">-Setting</span></span>
<span data-ttu-id="3d178-145">副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="3d178-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="3d178-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d178-146">-SubscriptionId</span></span>
<span data-ttu-id="3d178-147">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3d178-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d178-148">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3d178-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3d178-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d178-149">-Tag</span></span>
<span data-ttu-id="3d178-150">資源標記。</span><span class="sxs-lookup"><span data-stu-id="3d178-150">Resource tags.</span></span>

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

### <span data-ttu-id="3d178-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3d178-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="3d178-152">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="3d178-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="3d178-153">-確認</span><span class="sxs-lookup"><span data-stu-id="3d178-153">-Confirm</span></span>
<span data-ttu-id="3d178-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d178-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d178-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d178-155">-WhatIf</span></span>
<span data-ttu-id="3d178-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d178-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d178-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d178-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d178-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d178-158">CommonParameters</span></span>
<span data-ttu-id="3d178-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d178-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d178-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d178-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d178-161">輸入</span><span class="sxs-lookup"><span data-stu-id="3d178-161">INPUTS</span></span>

### <span data-ttu-id="3d178-162">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="3d178-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="3d178-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3d178-163">OUTPUTS</span></span>

### <span data-ttu-id="3d178-164">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="3d178-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="3d178-165">筆記</span><span class="sxs-lookup"><span data-stu-id="3d178-165">NOTES</span></span>

<span data-ttu-id="3d178-166">別名</span><span class="sxs-lookup"><span data-stu-id="3d178-166">ALIASES</span></span>

<span data-ttu-id="3d178-167">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3d178-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d178-168">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3d178-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d178-169">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3d178-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d178-170">EXTENSIONPARAMETER <IMachineExtension> ：說明電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="3d178-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="3d178-171">`Location <String>`：資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="3d178-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="3d178-172">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="3d178-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="3d178-173">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="3d178-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3d178-174">`[AutoUpgradeMinorVersion <Boolean?>]`：指示延伸時，如果部署時間可使用較新的次要版本，則應使用此功能。</span><span class="sxs-lookup"><span data-stu-id="3d178-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="3d178-175">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="3d178-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="3d178-176">`[ForceUpdateTag <String>]`：即使延伸設定尚未變更，延伸處理常式也應強制更新。</span><span class="sxs-lookup"><span data-stu-id="3d178-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="3d178-177">`[MachineExtensionType <String>]`：指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="3d178-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="3d178-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`[延伸]：副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="3d178-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="3d178-179">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d178-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="3d178-180">`[Setting <IMachineExtensionPropertiesSettings>]`：副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="3d178-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="3d178-181">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="3d178-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="3d178-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d178-182">RELATED LINKS</span></span>
