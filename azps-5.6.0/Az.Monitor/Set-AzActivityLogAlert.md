---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: d01399eeedf3b27bbf74e969876e24180ed571b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905010"
---
# <span data-ttu-id="c842d-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="c842d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c842d-102">SYNOPSIS</span></span>
<span data-ttu-id="c842d-103">建立新活動或設定現有的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c842d-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="c842d-104">語法</span><span class="sxs-lookup"><span data-stu-id="c842d-104">SYNTAX</span></span>

### <span data-ttu-id="c842d-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c842d-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c842d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c842d-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c842d-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c842d-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c842d-108">描述</span><span class="sxs-lookup"><span data-stu-id="c842d-108">DESCRIPTION</span></span>
<span data-ttu-id="c842d-109">**Set-AzActivityLogAlert** Cmdlet 會建立新通知或設定現有的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c842d-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="c842d-110">針對標記、條件和動作，物件必須事先建立，並在此通話中以逗號分隔方式以參數傳遞 (請參閱下列範例) 。</span><span class="sxs-lookup"><span data-stu-id="c842d-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="c842d-111">此 Cmdlet 實做 ShouldProcess 模式，即實際建立/修改資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="c842d-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="c842d-112">**注意**：此 Cmdlet 及其相關 Cmdlet 會取代 2017 年 (2017 年 11 月) **Add-AzLogAlertRule。**</span><span class="sxs-lookup"><span data-stu-id="c842d-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="c842d-113">例子</span><span class="sxs-lookup"><span data-stu-id="c842d-113">EXAMPLES</span></span>

### <span data-ttu-id="c842d-114">範例 1：建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="c842d-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="c842d-115">前四個命令會建立條件及動作群組。</span><span class="sxs-lookup"><span data-stu-id="c842d-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="c842d-116">最後一個命令會使用條件與動作群組建立活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c842d-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="c842d-117">範例 2：已停用建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="c842d-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="c842d-118">前四個命令會建立條件及動作群組。</span><span class="sxs-lookup"><span data-stu-id="c842d-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="c842d-119">最後一個命令會使用條件與動作群組建立活動記錄通知，但會停用警示。</span><span class="sxs-lookup"><span data-stu-id="c842d-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="c842d-120">範例 3：使用來自管道或 InputObject 參數的值設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="c842d-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="c842d-121">第一個命令與 Nop 類似，它會以已包含的相同值設定警示。其他命令會先取回警示規則、變更描述並停用該規則，然後使用 InputObject 參數來保留這些變更</span><span class="sxs-lookup"><span data-stu-id="c842d-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="c842d-122">範例 4：使用來自管道的 ResourceId 值設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="c842d-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="c842d-123">如果特定記錄提醒規則存在，此命令會將其停用。</span><span class="sxs-lookup"><span data-stu-id="c842d-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="c842d-124">參數</span><span class="sxs-lookup"><span data-stu-id="c842d-124">PARAMETERS</span></span>

### <span data-ttu-id="c842d-125">-動作</span><span class="sxs-lookup"><span data-stu-id="c842d-125">-Action</span></span>
<span data-ttu-id="c842d-126">活動記錄提醒的動作群組清單。</span><span class="sxs-lookup"><span data-stu-id="c842d-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-127">-條件</span><span class="sxs-lookup"><span data-stu-id="c842d-127">-Condition</span></span>
<span data-ttu-id="c842d-128">活動記錄提醒的條件清單。</span><span class="sxs-lookup"><span data-stu-id="c842d-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="c842d-129">**注意**：在條件清單中，至少必須有一個欄位等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="c842d-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="c842d-130">如果條件不存在，後端會以 400 (BadRequest) 回應。</span><span class="sxs-lookup"><span data-stu-id="c842d-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c842d-131">-DefaultProfile</span></span>
<span data-ttu-id="c842d-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c842d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c842d-133">-描述</span><span class="sxs-lookup"><span data-stu-id="c842d-133">-Description</span></span>
<span data-ttu-id="c842d-134">警示資源的描述。</span><span class="sxs-lookup"><span data-stu-id="c842d-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-135">-DisableAlert</span></span>
<span data-ttu-id="c842d-136">允許使用者建立已停用的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c842d-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="c842d-137">如果沒有提供通知，系統即會啟用警示。</span><span class="sxs-lookup"><span data-stu-id="c842d-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c842d-138">-InputObject</span></span>
<span data-ttu-id="c842d-139">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱和資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="c842d-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-140">-位置</span><span class="sxs-lookup"><span data-stu-id="c842d-140">-Location</span></span>
<span data-ttu-id="c842d-141">活動記錄警示存在的位置。</span><span class="sxs-lookup"><span data-stu-id="c842d-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="c842d-142">-Name</span></span>
<span data-ttu-id="c842d-143">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="c842d-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c842d-144">-ResourceGroupName</span></span>
<span data-ttu-id="c842d-145">警示資源將存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c842d-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c842d-146">-ResourceId</span></span>
<span data-ttu-id="c842d-147">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="c842d-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="c842d-148">-Scope</span></span>
<span data-ttu-id="c842d-149">活動記錄通知的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="c842d-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-150">-標記</span><span class="sxs-lookup"><span data-stu-id="c842d-150">-Tag</span></span>
<span data-ttu-id="c842d-151">設定活動記錄提醒資源的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="c842d-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c842d-152">-確認</span><span class="sxs-lookup"><span data-stu-id="c842d-152">-Confirm</span></span>
<span data-ttu-id="c842d-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c842d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c842d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c842d-154">-WhatIf</span></span>
<span data-ttu-id="c842d-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c842d-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c842d-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c842d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c842d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c842d-157">CommonParameters</span></span>
<span data-ttu-id="c842d-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c842d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c842d-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c842d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c842d-160">輸入</span><span class="sxs-lookup"><span data-stu-id="c842d-160">INPUTS</span></span>

### <span data-ttu-id="c842d-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c842d-161">System.String</span></span>

### <span data-ttu-id="c842d-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c842d-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c842d-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c842d-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c842d-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c842d-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c842d-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c842d-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c842d-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c842d-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c842d-167">輸出</span><span class="sxs-lookup"><span data-stu-id="c842d-167">OUTPUTS</span></span>

### <span data-ttu-id="c842d-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c842d-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c842d-169">筆記</span><span class="sxs-lookup"><span data-stu-id="c842d-169">NOTES</span></span>

## <span data-ttu-id="c842d-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="c842d-170">RELATED LINKS</span></span>

[<span data-ttu-id="c842d-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="c842d-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="c842d-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="c842d-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c842d-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="c842d-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c842d-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="c842d-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="c842d-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
