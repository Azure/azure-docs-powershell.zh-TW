---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: a6894765d4da1e0582adc4f22fe0a0e572f000d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790393"
---
# <span data-ttu-id="65454-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65454-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="65454-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65454-102">SYNOPSIS</span></span>
<span data-ttu-id="65454-103">建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="65454-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="65454-104">句法</span><span class="sxs-lookup"><span data-stu-id="65454-104">SYNTAX</span></span>

### <span data-ttu-id="65454-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="65454-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65454-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65454-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65454-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="65454-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65454-108">說明</span><span class="sxs-lookup"><span data-stu-id="65454-108">DESCRIPTION</span></span>
<span data-ttu-id="65454-109">**AzActivityLogAlert** Cmdlet 會建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="65454-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="65454-110">針對標記、條件及動作，您必須事先建立物件，並以逗號分隔的方式將物件作為參數傳遞， (請參閱以下範例) 。</span><span class="sxs-lookup"><span data-stu-id="65454-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="65454-111">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立/修改資源前，可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="65454-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="65454-112">**注意** ：這個 Cmdlet 及其相關的 **AzLogAlertRule** 會取代2017年11月) 的已過時的 (。</span><span class="sxs-lookup"><span data-stu-id="65454-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="65454-113">示例</span><span class="sxs-lookup"><span data-stu-id="65454-113">EXAMPLES</span></span>

### <span data-ttu-id="65454-114">範例1：建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="65454-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="65454-115">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="65454-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="65454-116">最終命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="65454-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="65454-117">範例2：建立活動記錄通知已停用</span><span class="sxs-lookup"><span data-stu-id="65454-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="65454-118">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="65454-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="65454-119">最後一個命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒，但會建立 [已停用] 通知。</span><span class="sxs-lookup"><span data-stu-id="65454-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="65454-120">範例3：根據管道或 InputObject 參數中的值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="65454-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="65454-121">第一個命令與 nop 類似，它會使用與其他命令相同的值來設定通知，以取得警報規則、變更描述並停用，然後使用 InputObject 參數保留這些變更</span><span class="sxs-lookup"><span data-stu-id="65454-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="65454-122">範例4：使用管道中的 ResourceId 值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="65454-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="65454-123">如果有指定的記錄警示規則，這個命令會停用。</span><span class="sxs-lookup"><span data-stu-id="65454-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="65454-124">參數</span><span class="sxs-lookup"><span data-stu-id="65454-124">PARAMETERS</span></span>

### <span data-ttu-id="65454-125">-動作</span><span class="sxs-lookup"><span data-stu-id="65454-125">-Action</span></span>
<span data-ttu-id="65454-126">活動記錄通知的動作群組清單。</span><span class="sxs-lookup"><span data-stu-id="65454-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="65454-127">-條件</span><span class="sxs-lookup"><span data-stu-id="65454-127">-Condition</span></span>
<span data-ttu-id="65454-128">活動記錄通知的條件清單。</span><span class="sxs-lookup"><span data-stu-id="65454-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="65454-129">**注意** ：在條件清單中，至少必須有一個欄位等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="65454-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="65454-130">如果此條件不存在，後端會以 400 (BadRequest) 回應。</span><span class="sxs-lookup"><span data-stu-id="65454-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="65454-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65454-131">-DefaultProfile</span></span>
<span data-ttu-id="65454-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="65454-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65454-133">-描述</span><span class="sxs-lookup"><span data-stu-id="65454-133">-Description</span></span>
<span data-ttu-id="65454-134">警報資源的描述。</span><span class="sxs-lookup"><span data-stu-id="65454-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="65454-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="65454-135">-DisableAlert</span></span>
<span data-ttu-id="65454-136">允許使用者建立停用的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="65454-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="65454-137">如果未指定，即會啟用通知。</span><span class="sxs-lookup"><span data-stu-id="65454-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="65454-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65454-138">-InputObject</span></span>
<span data-ttu-id="65454-139">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="65454-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="65454-140">-位置</span><span class="sxs-lookup"><span data-stu-id="65454-140">-Location</span></span>
<span data-ttu-id="65454-141">活動記錄通知存在的位置。</span><span class="sxs-lookup"><span data-stu-id="65454-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="65454-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="65454-142">-Name</span></span>
<span data-ttu-id="65454-143">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="65454-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="65454-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65454-144">-ResourceGroupName</span></span>
<span data-ttu-id="65454-145">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65454-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="65454-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65454-146">-ResourceId</span></span>
<span data-ttu-id="65454-147">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="65454-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="65454-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="65454-148">-Scope</span></span>
<span data-ttu-id="65454-149">活動記錄通知的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="65454-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="65454-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="65454-150">-Tag</span></span>
<span data-ttu-id="65454-151">設定活動記錄通知資源的 tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="65454-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="65454-152">-確認</span><span class="sxs-lookup"><span data-stu-id="65454-152">-Confirm</span></span>
<span data-ttu-id="65454-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65454-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65454-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65454-154">-WhatIf</span></span>
<span data-ttu-id="65454-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65454-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65454-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65454-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65454-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65454-157">CommonParameters</span></span>
<span data-ttu-id="65454-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65454-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65454-159">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="65454-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65454-160">輸入</span><span class="sxs-lookup"><span data-stu-id="65454-160">INPUTS</span></span>

### <span data-ttu-id="65454-161">System.object</span><span class="sxs-lookup"><span data-stu-id="65454-161">System.String</span></span>

### <span data-ttu-id="65454-162">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65454-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65454-163">[System.object]。清單 ' 1 [ActivityLogAlertLeafCondition，，Marvell. PowerShell. Monitor，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="65454-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="65454-164">[System.object]。清單 ' 1 [ActivityLogAlertActionGroup，，Marvell. PowerShell. Monitor，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="65454-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="65454-165">[System.object]。字典 ' 2 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]，[System.object，，Culture = 中立，PublicKeyToken = 4.0.0.0]」）。））中的 "</span><span class="sxs-lookup"><span data-stu-id="65454-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65454-166">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="65454-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="65454-167">輸出</span><span class="sxs-lookup"><span data-stu-id="65454-167">OUTPUTS</span></span>

### <span data-ttu-id="65454-168">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="65454-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="65454-169">筆記</span><span class="sxs-lookup"><span data-stu-id="65454-169">NOTES</span></span>

## <span data-ttu-id="65454-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="65454-170">RELATED LINKS</span></span>

[<span data-ttu-id="65454-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65454-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="65454-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65454-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="65454-173">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65454-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="65454-174">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65454-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="65454-175">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="65454-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="65454-176">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="65454-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
