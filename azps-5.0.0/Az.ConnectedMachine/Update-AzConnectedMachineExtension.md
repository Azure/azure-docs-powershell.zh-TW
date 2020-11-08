---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140174"
---
# <span data-ttu-id="b8a72-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b8a72-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="b8a72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8a72-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a72-103">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="b8a72-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="b8a72-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8a72-104">SYNTAX</span></span>

### <span data-ttu-id="b8a72-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b8a72-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b8a72-106">時更新</span><span class="sxs-lookup"><span data-stu-id="b8a72-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8a72-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8a72-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8a72-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b8a72-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8a72-109">說明</span><span class="sxs-lookup"><span data-stu-id="b8a72-109">DESCRIPTION</span></span>
<span data-ttu-id="b8a72-110">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="b8a72-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="b8a72-111">示例</span><span class="sxs-lookup"><span data-stu-id="b8a72-111">EXAMPLES</span></span>

### <span data-ttu-id="b8a72-112">範例1：更新延伸</span><span class="sxs-lookup"><span data-stu-id="b8a72-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="b8a72-113">更新特定電腦上的延伸。</span><span class="sxs-lookup"><span data-stu-id="b8a72-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="b8a72-114">範例2：使用透過管線指定位置來更新延伸</span><span class="sxs-lookup"><span data-stu-id="b8a72-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="b8a72-115">更新透過管線傳入的特定延伸。</span><span class="sxs-lookup"><span data-stu-id="b8a72-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="b8a72-116">在這裡，我們使用透過管線傳入的延伸，協助我們找出我們想要在哪個延伸上操作，並指定我們想要透過一般參數變更的內容 (例如 `-Settings`) </span><span class="sxs-lookup"><span data-stu-id="b8a72-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="b8a72-117">範例3：使用透過管線指定的延伸參數來更新延伸</span><span class="sxs-lookup"><span data-stu-id="b8a72-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="b8a72-118">更新透過管線傳入的特定延伸。</span><span class="sxs-lookup"><span data-stu-id="b8a72-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="b8a72-119">我們在這裡使用透過管線傳入的延伸，以提供我們想要在延伸中進行的變更。</span><span class="sxs-lookup"><span data-stu-id="b8a72-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="b8a72-120">延伸的位置並不透過管線進行檢索，而是透過 splat 參數) 的一般指定參數 (。</span><span class="sxs-lookup"><span data-stu-id="b8a72-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="b8a72-121">範例4：同時使用延伸物件作為更新的位置和參數</span><span class="sxs-lookup"><span data-stu-id="b8a72-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="b8a72-122">更新透過管線傳入的特定延伸。</span><span class="sxs-lookup"><span data-stu-id="b8a72-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="b8a72-123">在這裡，我們使用透過管線傳入的擴充功能，協助我們找出我們想要使用的副檔名。</span><span class="sxs-lookup"><span data-stu-id="b8a72-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="b8a72-124">此外，我們還使用延伸物件的參數來指定要更新的內容。</span><span class="sxs-lookup"><span data-stu-id="b8a72-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="b8a72-125">參數</span><span class="sxs-lookup"><span data-stu-id="b8a72-125">PARAMETERS</span></span>

### <span data-ttu-id="b8a72-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8a72-126">-AsJob</span></span>
<span data-ttu-id="b8a72-127">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b8a72-127">Run the command as a job</span></span>

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

### <span data-ttu-id="b8a72-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b8a72-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b8a72-129">指示在部署時間，延伸時是否應使用較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="b8a72-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="b8a72-130">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="b8a72-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="b8a72-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a72-131">-DefaultProfile</span></span>
<span data-ttu-id="b8a72-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a72-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="b8a72-133">-ExtensionParameter</span></span>
<span data-ttu-id="b8a72-134">描述電腦延伸更新。</span><span class="sxs-lookup"><span data-stu-id="b8a72-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="b8a72-135">若要建立，請參閱 EXTENSIONPARAMETER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="b8a72-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8a72-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b8a72-136">-ForceRerun</span></span>
<span data-ttu-id="b8a72-137">即使延伸設定尚未變更，延伸處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="b8a72-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="b8a72-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a72-138">-InputObject</span></span>
<span data-ttu-id="b8a72-139">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b8a72-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8a72-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="b8a72-140">-MachineName</span></span>
<span data-ttu-id="b8a72-141">應該在其中建立或更新延伸的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="b8a72-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8a72-142">-Name</span></span>
<span data-ttu-id="b8a72-143">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="b8a72-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b8a72-144">-NoWait</span></span>
<span data-ttu-id="b8a72-145">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b8a72-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b8a72-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b8a72-146">-ProtectedSetting</span></span>
<span data-ttu-id="b8a72-147">副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="b8a72-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="b8a72-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b8a72-148">-Publisher</span></span>
<span data-ttu-id="b8a72-149">延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="b8a72-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a72-150">-ResourceGroupName</span></span>
<span data-ttu-id="b8a72-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8a72-152">-設定</span><span class="sxs-lookup"><span data-stu-id="b8a72-152">-Setting</span></span>
<span data-ttu-id="b8a72-153">副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="b8a72-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="b8a72-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8a72-154">-SubscriptionId</span></span>
<span data-ttu-id="b8a72-155">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b8a72-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b8a72-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b8a72-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b8a72-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8a72-157">-Tag</span></span>
<span data-ttu-id="b8a72-158">資源標記</span><span class="sxs-lookup"><span data-stu-id="b8a72-158">Resource tags</span></span>

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

### <span data-ttu-id="b8a72-159">-類型</span><span class="sxs-lookup"><span data-stu-id="b8a72-159">-Type</span></span>
<span data-ttu-id="b8a72-160">指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="b8a72-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="b8a72-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b8a72-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="b8a72-162">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="b8a72-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="b8a72-163">-確認</span><span class="sxs-lookup"><span data-stu-id="b8a72-163">-Confirm</span></span>
<span data-ttu-id="b8a72-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8a72-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a72-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a72-165">-WhatIf</span></span>
<span data-ttu-id="b8a72-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8a72-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a72-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8a72-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a72-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a72-168">CommonParameters</span></span>
<span data-ttu-id="b8a72-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8a72-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a72-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8a72-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a72-171">輸入</span><span class="sxs-lookup"><span data-stu-id="b8a72-171">INPUTS</span></span>

### <span data-ttu-id="b8a72-172">IMachineExtensionUpdate （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="b8a72-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="b8a72-173">IConnectedMachineIdentity （ConnectedMachine）的</span><span class="sxs-lookup"><span data-stu-id="b8a72-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="b8a72-174">輸出</span><span class="sxs-lookup"><span data-stu-id="b8a72-174">OUTPUTS</span></span>

### <span data-ttu-id="b8a72-175">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="b8a72-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="b8a72-176">筆記</span><span class="sxs-lookup"><span data-stu-id="b8a72-176">NOTES</span></span>

<span data-ttu-id="b8a72-177">別名</span><span class="sxs-lookup"><span data-stu-id="b8a72-177">ALIASES</span></span>

<span data-ttu-id="b8a72-178">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b8a72-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8a72-179">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b8a72-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8a72-180">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b8a72-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8a72-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> ：說明電腦延伸更新。</span><span class="sxs-lookup"><span data-stu-id="b8a72-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="b8a72-182">`[Tag <IUpdateResourceTags>]`：資源標記</span><span class="sxs-lookup"><span data-stu-id="b8a72-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="b8a72-183">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="b8a72-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b8a72-184">`[AutoUpgradeMinorVersion <Boolean?>]`：指示延伸時，如果部署時間可使用較新的次要版本，則應使用此功能。</span><span class="sxs-lookup"><span data-stu-id="b8a72-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="b8a72-185">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="b8a72-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="b8a72-186">`[ForceUpdateTag <String>]`：即使延伸設定尚未變更，延伸處理常式也應強制更新。</span><span class="sxs-lookup"><span data-stu-id="b8a72-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="b8a72-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`[延伸]：副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="b8a72-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="b8a72-188">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="b8a72-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`：副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="b8a72-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="b8a72-190">`[Type <String>]`：指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="b8a72-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="b8a72-191">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="b8a72-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="b8a72-192">INPUTOBJECT <IConnectedMachineIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b8a72-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8a72-193">`[ExtensionName <String>]`：電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="b8a72-194">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b8a72-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8a72-195">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="b8a72-196">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a72-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b8a72-197">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b8a72-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b8a72-198">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b8a72-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b8a72-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8a72-199">RELATED LINKS</span></span>

