---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: df2e1de102143f227178b45ea14264f9e61d86a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917021"
---
# <span data-ttu-id="daba3-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="daba3-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="daba3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="daba3-102">SYNOPSIS</span></span>
<span data-ttu-id="daba3-103">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="daba3-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="daba3-104">語法</span><span class="sxs-lookup"><span data-stu-id="daba3-104">SYNTAX</span></span>

### <span data-ttu-id="daba3-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="daba3-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="daba3-106">創建</span><span class="sxs-lookup"><span data-stu-id="daba3-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="daba3-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="daba3-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="daba3-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="daba3-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="daba3-109">描述</span><span class="sxs-lookup"><span data-stu-id="daba3-109">DESCRIPTION</span></span>
<span data-ttu-id="daba3-110">建立或更新擴充功能的操作。</span><span class="sxs-lookup"><span data-stu-id="daba3-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="daba3-111">例子</span><span class="sxs-lookup"><span data-stu-id="daba3-111">EXAMPLES</span></span>

### <span data-ttu-id="daba3-112">範例 1：在電腦中新增擴充功能</span><span class="sxs-lookup"><span data-stu-id="daba3-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="daba3-113">設定電腦上延伸模組。</span><span class="sxs-lookup"><span data-stu-id="daba3-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="daba3-114">範例 2：使用透過管線指定的擴充參數新增擴充功能</span><span class="sxs-lookup"><span data-stu-id="daba3-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="daba3-115">這會使用透過管線傳遞的物件所提供的擴充參數，來建立新的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="daba3-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="daba3-116">如果您想要抓取一部電腦的參數，然後將參數應用至另一部電腦，這是很棒的方法。</span><span class="sxs-lookup"><span data-stu-id="daba3-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="daba3-117">範例 3：新增透過管線指定位置的新擴充功能</span><span class="sxs-lookup"><span data-stu-id="daba3-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="daba3-118">這會使用透過管線提供的身分識別建立新電腦擴充功能。</span><span class="sxs-lookup"><span data-stu-id="daba3-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="daba3-119">您很可能不會這麼做，但有可能。</span><span class="sxs-lookup"><span data-stu-id="daba3-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="daba3-120">範例 4：使用副檔名物件新增副檔名做為更新的位置和參數</span><span class="sxs-lookup"><span data-stu-id="daba3-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="daba3-121">這會使用透過管線提供的身分識別，以及延伸物件所傳遞的擴充詳細資料，來建立新電腦擴充功能。</span><span class="sxs-lookup"><span data-stu-id="daba3-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="daba3-122">您很可能不會這麼做，但有可能。</span><span class="sxs-lookup"><span data-stu-id="daba3-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="daba3-123">參數</span><span class="sxs-lookup"><span data-stu-id="daba3-123">PARAMETERS</span></span>

### <span data-ttu-id="daba3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daba3-124">-AsJob</span></span>
<span data-ttu-id="daba3-125">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="daba3-125">Run the command as a job</span></span>

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

### <span data-ttu-id="daba3-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="daba3-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="daba3-127">指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用該次要版本。</span><span class="sxs-lookup"><span data-stu-id="daba3-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="daba3-128">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="daba3-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daba3-129">-DefaultProfile</span></span>
<span data-ttu-id="daba3-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="daba3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daba3-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="daba3-131">-ExtensionParameter</span></span>
<span data-ttu-id="daba3-132">說明機器延伸模組。</span><span class="sxs-lookup"><span data-stu-id="daba3-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="daba3-133">若要建構，請參閱 EXTENSIONPARAMETER 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="daba3-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="daba3-134">-ExtensionType</span></span>
<span data-ttu-id="daba3-135">指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="daba3-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="daba3-136">-ForceRerun</span></span>
<span data-ttu-id="daba3-137">延伸處理常式如何強制更新，即使擴充功能組沒有變更。</span><span class="sxs-lookup"><span data-stu-id="daba3-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daba3-138">-InputObject</span></span>
<span data-ttu-id="daba3-139">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="daba3-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-140">-位置</span><span class="sxs-lookup"><span data-stu-id="daba3-140">-Location</span></span>
<span data-ttu-id="daba3-141">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="daba3-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="daba3-142">-MachineName</span></span>
<span data-ttu-id="daba3-143">應該建立或更新擴充功能的機器名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="daba3-144">-Name</span></span>
<span data-ttu-id="daba3-145">電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="daba3-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="daba3-146">-NoWait</span></span>
<span data-ttu-id="daba3-147">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="daba3-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="daba3-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="daba3-148">-ProtectedSetting</span></span>
<span data-ttu-id="daba3-149">擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="daba3-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="daba3-150">-Publisher</span></span>
<span data-ttu-id="daba3-151">擴充處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daba3-152">-ResourceGroupName</span></span>
<span data-ttu-id="daba3-153">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-154">-設定</span><span class="sxs-lookup"><span data-stu-id="daba3-154">-Setting</span></span>
<span data-ttu-id="daba3-155">Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="daba3-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="daba3-156">-SubscriptionId</span></span>
<span data-ttu-id="daba3-157">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="daba3-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="daba3-158">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="daba3-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-159">-標記</span><span class="sxs-lookup"><span data-stu-id="daba3-159">-Tag</span></span>
<span data-ttu-id="daba3-160">資源標記。</span><span class="sxs-lookup"><span data-stu-id="daba3-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="daba3-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="daba3-162">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="daba3-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daba3-163">-確認</span><span class="sxs-lookup"><span data-stu-id="daba3-163">-Confirm</span></span>
<span data-ttu-id="daba3-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="daba3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daba3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daba3-165">-WhatIf</span></span>
<span data-ttu-id="daba3-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="daba3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daba3-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daba3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daba3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daba3-168">CommonParameters</span></span>
<span data-ttu-id="daba3-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="daba3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daba3-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daba3-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daba3-171">輸入</span><span class="sxs-lookup"><span data-stu-id="daba3-171">INPUTS</span></span>

### <span data-ttu-id="daba3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="daba3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="daba3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="daba3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="daba3-174">輸出</span><span class="sxs-lookup"><span data-stu-id="daba3-174">OUTPUTS</span></span>

### <span data-ttu-id="daba3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="daba3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="daba3-176">筆記</span><span class="sxs-lookup"><span data-stu-id="daba3-176">NOTES</span></span>

<span data-ttu-id="daba3-177">別名</span><span class="sxs-lookup"><span data-stu-id="daba3-177">ALIASES</span></span>

<span data-ttu-id="daba3-178">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="daba3-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="daba3-179">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="daba3-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="daba3-180">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="daba3-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="daba3-181">EXTENSIONPARAMETER： <IMachineExtension> 說明機器延伸模組。</span><span class="sxs-lookup"><span data-stu-id="daba3-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="daba3-182">`Location <String>`：資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="daba3-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="daba3-183">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="daba3-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="daba3-184">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="daba3-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="daba3-185">`[AutoUpgradeMinorVersion <Boolean?>]`：指出擴充功能是否應該使用較新的次要版本 ，如果部署時可以使用。</span><span class="sxs-lookup"><span data-stu-id="daba3-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="daba3-186">不過，部署後，除非重新部署，即使此屬性設為 True，擴充功能不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="daba3-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="daba3-187">`[ForceUpdateTag <String>]`：即使擴充功能組配置沒有變更，擴充處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="daba3-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="daba3-188">`[MachineExtensionType <String>]`：指定擴充功能的類型;範例為 「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="daba3-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="daba3-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`：擴充功能可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或完全不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="daba3-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="daba3-190">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="daba3-191">`[Setting <IMachineExtensionPropertiesSettings>]`：Json 格式化的擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="daba3-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="daba3-192">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="daba3-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="daba3-193">INPUTOBJECT： <IConnectedMachineIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="daba3-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="daba3-194">`[ExtensionName <String>]`：電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="daba3-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="daba3-195">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="daba3-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="daba3-196">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="daba3-197">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daba3-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="daba3-198">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="daba3-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="daba3-199">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="daba3-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="daba3-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="daba3-200">RELATED LINKS</span></span>

