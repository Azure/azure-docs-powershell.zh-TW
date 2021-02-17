---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 6c7b867add359edec8379f20e630c9aca5fed00e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402876"
---
# <span data-ttu-id="26926-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="26926-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="26926-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26926-102">SYNOPSIS</span></span>
<span data-ttu-id="26926-103">建立新活動或設定現有的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="26926-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="26926-104">語法</span><span class="sxs-lookup"><span data-stu-id="26926-104">SYNTAX</span></span>

### <span data-ttu-id="26926-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26926-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26926-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26926-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26926-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="26926-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26926-108">描述</span><span class="sxs-lookup"><span data-stu-id="26926-108">DESCRIPTION</span></span>
<span data-ttu-id="26926-109">**Set-AzActivityLogAlert** Cmdlet 會建立新通知或設定現有的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="26926-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="26926-110">針對標記、條件和動作，物件必須事先建立，並在此通話中以逗號分隔方式以參數傳遞 (請參閱下列範例) 。</span><span class="sxs-lookup"><span data-stu-id="26926-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="26926-111">此 Cmdlet 實做 ShouldProcess 模式，即實際建立/修改資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="26926-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="26926-112">**注意**：此 Cmdlet 及其相關專案取代 2017 年 (2017 年 11 月) **Add-AzLogAlertRule。**</span><span class="sxs-lookup"><span data-stu-id="26926-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="26926-113">例子</span><span class="sxs-lookup"><span data-stu-id="26926-113">EXAMPLES</span></span>

### <span data-ttu-id="26926-114">範例 1：建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="26926-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="26926-115">前四個命令會建立條件與動作群組。</span><span class="sxs-lookup"><span data-stu-id="26926-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="26926-116">最後一個命令會使用條件與動作群組建立活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="26926-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="26926-117">範例 2：已停用建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="26926-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="26926-118">前四個命令會建立條件與動作群組。</span><span class="sxs-lookup"><span data-stu-id="26926-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="26926-119">最後一個命令會使用條件與動作群組建立活動記錄通知，但會停用警示。</span><span class="sxs-lookup"><span data-stu-id="26926-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="26926-120">範例 3：使用來自管道或 InputObject 參數的值設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="26926-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="26926-121">第一個命令與 Nop 類似，它會以已包含的相同值設定警示。其他命令會先取回警示規則、變更描述並停用該規則，然後使用 InputObject 參數來保留這些變更</span><span class="sxs-lookup"><span data-stu-id="26926-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="26926-122">範例 4：使用來自管道的 ResourceId 值設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="26926-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="26926-123">如果特定記錄提醒規則存在，此命令會將其停用。</span><span class="sxs-lookup"><span data-stu-id="26926-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="26926-124">參數</span><span class="sxs-lookup"><span data-stu-id="26926-124">PARAMETERS</span></span>

### <span data-ttu-id="26926-125">-動作</span><span class="sxs-lookup"><span data-stu-id="26926-125">-Action</span></span>
<span data-ttu-id="26926-126">活動記錄提醒的動作群組清單。</span><span class="sxs-lookup"><span data-stu-id="26926-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="26926-127">-條件</span><span class="sxs-lookup"><span data-stu-id="26926-127">-Condition</span></span>
<span data-ttu-id="26926-128">活動記錄提醒的條件清單。</span><span class="sxs-lookup"><span data-stu-id="26926-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="26926-129">**注意**：在條件清單中，至少必須有一個欄位等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="26926-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="26926-130">如果條件不存在，後端會以 400 (BadRequest) 回應。</span><span class="sxs-lookup"><span data-stu-id="26926-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="26926-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26926-131">-DefaultProfile</span></span>
<span data-ttu-id="26926-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="26926-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26926-133">-描述</span><span class="sxs-lookup"><span data-stu-id="26926-133">-Description</span></span>
<span data-ttu-id="26926-134">警示資源的描述。</span><span class="sxs-lookup"><span data-stu-id="26926-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="26926-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="26926-135">-DisableAlert</span></span>
<span data-ttu-id="26926-136">允許使用者建立已停用的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="26926-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="26926-137">如果沒有提供，系統即會啟用警示。</span><span class="sxs-lookup"><span data-stu-id="26926-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="26926-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26926-138">-InputObject</span></span>
<span data-ttu-id="26926-139">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱和資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="26926-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="26926-140">-位置</span><span class="sxs-lookup"><span data-stu-id="26926-140">-Location</span></span>
<span data-ttu-id="26926-141">活動記錄警示存在的位置。</span><span class="sxs-lookup"><span data-stu-id="26926-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="26926-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="26926-142">-Name</span></span>
<span data-ttu-id="26926-143">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="26926-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="26926-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26926-144">-ResourceGroupName</span></span>
<span data-ttu-id="26926-145">警示資源將存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26926-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="26926-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26926-146">-ResourceId</span></span>
<span data-ttu-id="26926-147">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="26926-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="26926-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="26926-148">-Scope</span></span>
<span data-ttu-id="26926-149">活動記錄通知的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="26926-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="26926-150">-標記</span><span class="sxs-lookup"><span data-stu-id="26926-150">-Tag</span></span>
<span data-ttu-id="26926-151">設定活動記錄提醒資源的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="26926-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="26926-152">-確認</span><span class="sxs-lookup"><span data-stu-id="26926-152">-Confirm</span></span>
<span data-ttu-id="26926-153">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26926-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26926-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26926-154">-WhatIf</span></span>
<span data-ttu-id="26926-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26926-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26926-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26926-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26926-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26926-157">CommonParameters</span></span>
<span data-ttu-id="26926-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26926-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26926-159">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="26926-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26926-160">輸入</span><span class="sxs-lookup"><span data-stu-id="26926-160">INPUTS</span></span>

### <span data-ttu-id="26926-161">System.String</span><span class="sxs-lookup"><span data-stu-id="26926-161">System.String</span></span>

### <span data-ttu-id="26926-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26926-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26926-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="26926-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="26926-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="26926-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="26926-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26926-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26926-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="26926-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="26926-167">輸出</span><span class="sxs-lookup"><span data-stu-id="26926-167">OUTPUTS</span></span>

### <span data-ttu-id="26926-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="26926-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="26926-169">筆記</span><span class="sxs-lookup"><span data-stu-id="26926-169">NOTES</span></span>

## <span data-ttu-id="26926-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="26926-170">RELATED LINKS</span></span>

[<span data-ttu-id="26926-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="26926-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="26926-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="26926-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="26926-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="26926-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="26926-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="26926-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="26926-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="26926-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
