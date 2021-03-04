---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: e6da084f13d85f8c4f5a8934cd5fd4f05882c251
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917002"
---
# <span data-ttu-id="1485c-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1485c-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="1485c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1485c-102">SYNOPSIS</span></span>
<span data-ttu-id="1485c-103">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="1485c-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="1485c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1485c-104">SYNTAX</span></span>

### <span data-ttu-id="1485c-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1485c-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1485c-106">更新</span><span class="sxs-lookup"><span data-stu-id="1485c-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1485c-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1485c-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1485c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1485c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1485c-109">描述</span><span class="sxs-lookup"><span data-stu-id="1485c-109">DESCRIPTION</span></span>
<span data-ttu-id="1485c-110">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="1485c-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="1485c-111">例子</span><span class="sxs-lookup"><span data-stu-id="1485c-111">EXAMPLES</span></span>

### <span data-ttu-id="1485c-112">範例 1：更新擴充功能</span><span class="sxs-lookup"><span data-stu-id="1485c-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="1485c-113">更新特定電腦上擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1485c-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="1485c-114">範例 2：使用透過管線指定的位置更新延伸模組</span><span class="sxs-lookup"><span data-stu-id="1485c-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="1485c-115">更新透過管線傳遞的特定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1485c-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="1485c-116">在此，我們將使用透過管線傳遞的擴充功能，協助我們識別要操作哪一個擴充功能，並透過像) 一般參數指定要變更 `-Settings` (專案) </span><span class="sxs-lookup"><span data-stu-id="1485c-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="1485c-117">範例 3：使用透過管線指定的擴充功能參數更新擴充功能</span><span class="sxs-lookup"><span data-stu-id="1485c-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="1485c-118">更新透過管線傳遞的特定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1485c-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="1485c-119">在此，我們將使用透過管道傳遞的擴充功能，提供我們在擴充功能上進行變更。</span><span class="sxs-lookup"><span data-stu-id="1485c-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="1485c-120">擴充功能的位置不會透過管線來取取，而是透過由 splat 參數或 (指定) 。</span><span class="sxs-lookup"><span data-stu-id="1485c-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="1485c-121">範例 4：使用擴充功能物件做為更新的位置和參數</span><span class="sxs-lookup"><span data-stu-id="1485c-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="1485c-122">更新透過管線傳遞的特定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1485c-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="1485c-123">在此，我們將使用透過管線傳遞的擴充功能，協助我們識別要執行哪一個擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1485c-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="1485c-124">除此之外，我們還使用擴充物件的參數來指定更新專案。</span><span class="sxs-lookup"><span data-stu-id="1485c-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="1485c-125">參數</span><span class="sxs-lookup"><span data-stu-id="1485c-125">PARAMETERS</span></span>

### <span data-ttu-id="1485c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1485c-126">-AsJob</span></span>
<span data-ttu-id="1485c-127">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="1485c-127">Run the command as a job</span></span>

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

### <span data-ttu-id="1485c-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1485c-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1485c-129">指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用該次要版本。</span><span class="sxs-lookup"><span data-stu-id="1485c-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="1485c-130">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="1485c-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1485c-131">-DefaultProfile</span></span>
<span data-ttu-id="1485c-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1485c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1485c-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="1485c-133">-ExtensionParameter</span></span>
<span data-ttu-id="1485c-134">說明電腦擴充功能更新。</span><span class="sxs-lookup"><span data-stu-id="1485c-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="1485c-135">若要建構，請參閱 EXTENSIONPARAMETER 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1485c-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1485c-136">-ForceRerun</span></span>
<span data-ttu-id="1485c-137">延伸處理常式如何強制更新，即使擴充功能組沒有變更。</span><span class="sxs-lookup"><span data-stu-id="1485c-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1485c-138">-InputObject</span></span>
<span data-ttu-id="1485c-139">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1485c-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="1485c-140">-MachineName</span></span>
<span data-ttu-id="1485c-141">應該建立或更新擴充功能的機器名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="1485c-142">-Name</span></span>
<span data-ttu-id="1485c-143">電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="1485c-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1485c-144">-NoWait</span></span>
<span data-ttu-id="1485c-145">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="1485c-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1485c-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="1485c-146">-ProtectedSetting</span></span>
<span data-ttu-id="1485c-147">擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="1485c-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1485c-148">-Publisher</span></span>
<span data-ttu-id="1485c-149">擴充處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1485c-150">-ResourceGroupName</span></span>
<span data-ttu-id="1485c-151">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-152">-設定</span><span class="sxs-lookup"><span data-stu-id="1485c-152">-Setting</span></span>
<span data-ttu-id="1485c-153">Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="1485c-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1485c-154">-SubscriptionId</span></span>
<span data-ttu-id="1485c-155">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1485c-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1485c-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1485c-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-157">-標記</span><span class="sxs-lookup"><span data-stu-id="1485c-157">-Tag</span></span>
<span data-ttu-id="1485c-158">資源標記</span><span class="sxs-lookup"><span data-stu-id="1485c-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-159">-類型</span><span class="sxs-lookup"><span data-stu-id="1485c-159">-Type</span></span>
<span data-ttu-id="1485c-160">指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="1485c-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1485c-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="1485c-162">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="1485c-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485c-163">-確認</span><span class="sxs-lookup"><span data-stu-id="1485c-163">-Confirm</span></span>
<span data-ttu-id="1485c-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1485c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1485c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1485c-165">-WhatIf</span></span>
<span data-ttu-id="1485c-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1485c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1485c-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1485c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1485c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1485c-168">CommonParameters</span></span>
<span data-ttu-id="1485c-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1485c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1485c-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1485c-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1485c-171">輸入</span><span class="sxs-lookup"><span data-stu-id="1485c-171">INPUTS</span></span>

### <span data-ttu-id="1485c-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="1485c-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="1485c-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="1485c-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="1485c-174">輸出</span><span class="sxs-lookup"><span data-stu-id="1485c-174">OUTPUTS</span></span>

### <span data-ttu-id="1485c-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1485c-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="1485c-176">筆記</span><span class="sxs-lookup"><span data-stu-id="1485c-176">NOTES</span></span>

<span data-ttu-id="1485c-177">別名</span><span class="sxs-lookup"><span data-stu-id="1485c-177">ALIASES</span></span>

<span data-ttu-id="1485c-178">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1485c-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1485c-179">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1485c-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1485c-180">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1485c-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1485c-181">EXTENSIONPARAMETER： <IMachineExtensionUpdate> 說明電腦擴充功能更新。</span><span class="sxs-lookup"><span data-stu-id="1485c-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="1485c-182">`[Tag <IUpdateResourceTags>]`：資源標記</span><span class="sxs-lookup"><span data-stu-id="1485c-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="1485c-183">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="1485c-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1485c-184">`[AutoUpgradeMinorVersion <Boolean?>]`：指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用。</span><span class="sxs-lookup"><span data-stu-id="1485c-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="1485c-185">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="1485c-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="1485c-186">`[ForceUpdateTag <String>]`：即使擴充功能組配置沒有變更，擴充處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="1485c-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="1485c-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`：擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="1485c-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="1485c-188">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="1485c-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`：Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="1485c-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="1485c-190">`[Type <String>]`：指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="1485c-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="1485c-191">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="1485c-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="1485c-192">INPUTOBJECT： <IConnectedMachineIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1485c-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1485c-193">`[ExtensionName <String>]`：電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="1485c-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="1485c-194">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="1485c-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1485c-195">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="1485c-196">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1485c-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1485c-197">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1485c-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1485c-198">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1485c-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1485c-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="1485c-199">RELATED LINKS</span></span>

