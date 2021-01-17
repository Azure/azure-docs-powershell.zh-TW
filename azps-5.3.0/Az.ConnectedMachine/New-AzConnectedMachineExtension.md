---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449646"
---
# <span data-ttu-id="1efc1-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1efc1-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="1efc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1efc1-102">SYNOPSIS</span></span>
<span data-ttu-id="1efc1-103">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="1efc1-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="1efc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="1efc1-104">SYNTAX</span></span>

### <span data-ttu-id="1efc1-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1efc1-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1efc1-106">建立</span><span class="sxs-lookup"><span data-stu-id="1efc1-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1efc1-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1efc1-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1efc1-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1efc1-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1efc1-109">說明</span><span class="sxs-lookup"><span data-stu-id="1efc1-109">DESCRIPTION</span></span>
<span data-ttu-id="1efc1-110">建立或更新延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="1efc1-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="1efc1-111">示例</span><span class="sxs-lookup"><span data-stu-id="1efc1-111">EXAMPLES</span></span>

### <span data-ttu-id="1efc1-112">範例1：將新的延伸功能新增至電腦</span><span class="sxs-lookup"><span data-stu-id="1efc1-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="1efc1-113">在電腦上設定延伸。</span><span class="sxs-lookup"><span data-stu-id="1efc1-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="1efc1-114">範例2：使用透過管線指定的延伸參數新增副檔名</span><span class="sxs-lookup"><span data-stu-id="1efc1-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="1efc1-115">這會使用透過管線傳入的物件所提供的延伸參數，來建立新的副檔名。</span><span class="sxs-lookup"><span data-stu-id="1efc1-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="1efc1-116">如果您想要抓取一台電腦的參數，並將它套用至另一部電腦，這是很好的方式。</span><span class="sxs-lookup"><span data-stu-id="1efc1-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="1efc1-117">範例3：使用透過管線指定的位置來新增副檔名</span><span class="sxs-lookup"><span data-stu-id="1efc1-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="1efc1-118">這會使用透過管線提供的身分識別來建立新的電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="1efc1-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="1efc1-119">您可能無法這樣做，但可能會這麼做。</span><span class="sxs-lookup"><span data-stu-id="1efc1-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="1efc1-120">範例4：使用延伸物件新增副檔名作為更新的位置和參數</span><span class="sxs-lookup"><span data-stu-id="1efc1-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="1efc1-121">這會使用透過管線提供的身分識別，以及傳入延伸物件所提供的延伸詳細資料，來建立新的電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="1efc1-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="1efc1-122">您可能無法這樣做，但可能會這麼做。</span><span class="sxs-lookup"><span data-stu-id="1efc1-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="1efc1-123">參數</span><span class="sxs-lookup"><span data-stu-id="1efc1-123">PARAMETERS</span></span>

### <span data-ttu-id="1efc1-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1efc1-124">-AsJob</span></span>
<span data-ttu-id="1efc1-125">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="1efc1-125">Run the command as a job</span></span>

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

### <span data-ttu-id="1efc1-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1efc1-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1efc1-127">指示在部署時間，延伸時是否應使用較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="1efc1-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="1efc1-128">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="1efc1-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="1efc1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efc1-129">-DefaultProfile</span></span>
<span data-ttu-id="1efc1-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1efc1-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="1efc1-131">-ExtensionParameter</span></span>
<span data-ttu-id="1efc1-132">描述電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="1efc1-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="1efc1-133">若要建立，請參閱 EXTENSIONPARAMETER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="1efc1-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="1efc1-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1efc1-134">-ExtensionType</span></span>
<span data-ttu-id="1efc1-135">指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="1efc1-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="1efc1-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1efc1-136">-ForceRerun</span></span>
<span data-ttu-id="1efc1-137">即使延伸設定尚未變更，延伸處理常式應該如何強制更新。</span><span class="sxs-lookup"><span data-stu-id="1efc1-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="1efc1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1efc1-138">-InputObject</span></span>
<span data-ttu-id="1efc1-139">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1efc1-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1efc1-140">-位置</span><span class="sxs-lookup"><span data-stu-id="1efc1-140">-Location</span></span>
<span data-ttu-id="1efc1-141">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="1efc1-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="1efc1-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="1efc1-142">-MachineName</span></span>
<span data-ttu-id="1efc1-143">應該在其中建立或更新延伸的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="1efc1-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="1efc1-144">-Name</span></span>
<span data-ttu-id="1efc1-145">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="1efc1-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1efc1-146">-NoWait</span></span>
<span data-ttu-id="1efc1-147">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="1efc1-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1efc1-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="1efc1-148">-ProtectedSetting</span></span>
<span data-ttu-id="1efc1-149">副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="1efc1-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="1efc1-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1efc1-150">-Publisher</span></span>
<span data-ttu-id="1efc1-151">延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="1efc1-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1efc1-152">-ResourceGroupName</span></span>
<span data-ttu-id="1efc1-153">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="1efc1-154">-設定</span><span class="sxs-lookup"><span data-stu-id="1efc1-154">-Setting</span></span>
<span data-ttu-id="1efc1-155">副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="1efc1-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="1efc1-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1efc1-156">-SubscriptionId</span></span>
<span data-ttu-id="1efc1-157">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1efc1-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1efc1-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1efc1-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1efc1-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="1efc1-159">-Tag</span></span>
<span data-ttu-id="1efc1-160">資源標記。</span><span class="sxs-lookup"><span data-stu-id="1efc1-160">Resource tags.</span></span>

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

### <span data-ttu-id="1efc1-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1efc1-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="1efc1-162">指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="1efc1-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="1efc1-163">-確認</span><span class="sxs-lookup"><span data-stu-id="1efc1-163">-Confirm</span></span>
<span data-ttu-id="1efc1-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1efc1-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1efc1-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1efc1-165">-WhatIf</span></span>
<span data-ttu-id="1efc1-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1efc1-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1efc1-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1efc1-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1efc1-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efc1-168">CommonParameters</span></span>
<span data-ttu-id="1efc1-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1efc1-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efc1-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1efc1-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efc1-171">輸入</span><span class="sxs-lookup"><span data-stu-id="1efc1-171">INPUTS</span></span>

### <span data-ttu-id="1efc1-172">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="1efc1-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="1efc1-173">IConnectedMachineIdentity （ConnectedMachine）的</span><span class="sxs-lookup"><span data-stu-id="1efc1-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="1efc1-174">輸出</span><span class="sxs-lookup"><span data-stu-id="1efc1-174">OUTPUTS</span></span>

### <span data-ttu-id="1efc1-175">IMachineExtension （ConnectedMachine）。 Api20200802。</span><span class="sxs-lookup"><span data-stu-id="1efc1-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="1efc1-176">筆記</span><span class="sxs-lookup"><span data-stu-id="1efc1-176">NOTES</span></span>

<span data-ttu-id="1efc1-177">別名</span><span class="sxs-lookup"><span data-stu-id="1efc1-177">ALIASES</span></span>

<span data-ttu-id="1efc1-178">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1efc1-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1efc1-179">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1efc1-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1efc1-180">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1efc1-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1efc1-181">EXTENSIONPARAMETER <IMachineExtension> ：說明電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="1efc1-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="1efc1-182">`Location <String>`：資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="1efc1-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="1efc1-183">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="1efc1-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="1efc1-184">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="1efc1-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1efc1-185">`[AutoUpgradeMinorVersion <Boolean?>]`：指示延伸時，如果部署時間可使用較新的次要版本，則應使用此功能。</span><span class="sxs-lookup"><span data-stu-id="1efc1-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="1efc1-186">不過，除非將此屬性設為 true，否則延伸之後就不會升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="1efc1-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="1efc1-187">`[ForceUpdateTag <String>]`：即使延伸設定尚未變更，延伸處理常式也應強制更新。</span><span class="sxs-lookup"><span data-stu-id="1efc1-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="1efc1-188">`[MachineExtensionType <String>]`：指定延伸類型;範例是「CustomScriptExtension」。</span><span class="sxs-lookup"><span data-stu-id="1efc1-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="1efc1-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`[延伸]：副檔名可以包含 protectedSettings 或 protectedSettingsFromKeyVault，或是根本不包含受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="1efc1-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="1efc1-190">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="1efc1-191">`[Setting <IMachineExtensionPropertiesSettings>]`：副檔名的 Json 格式公開設定。</span><span class="sxs-lookup"><span data-stu-id="1efc1-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="1efc1-192">`[TypeHandlerVersion <String>]`：指定腳本處理常式的版本。</span><span class="sxs-lookup"><span data-stu-id="1efc1-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="1efc1-193">INPUTOBJECT <IConnectedMachineIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1efc1-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1efc1-194">`[ExtensionName <String>]`：電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="1efc1-195">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1efc1-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1efc1-196">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="1efc1-197">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1efc1-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1efc1-198">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1efc1-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1efc1-199">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1efc1-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1efc1-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="1efc1-200">RELATED LINKS</span></span>

