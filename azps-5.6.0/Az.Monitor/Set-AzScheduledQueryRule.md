---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: eefcebbcf1544205fd37201574ed0c3394123bcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904030"
---
# <span data-ttu-id="bff82-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bff82-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="bff82-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bff82-102">SYNOPSIS</span></span>
<span data-ttu-id="bff82-103">更新記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="bff82-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="bff82-104">語法</span><span class="sxs-lookup"><span data-stu-id="bff82-104">SYNTAX</span></span>

### <span data-ttu-id="bff82-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="bff82-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff82-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bff82-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff82-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bff82-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff82-108">描述</span><span class="sxs-lookup"><span data-stu-id="bff82-108">DESCRIPTION</span></span>
<span data-ttu-id="bff82-109">使用 PUT 語性更新記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="bff82-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="bff82-110">例子</span><span class="sxs-lookup"><span data-stu-id="bff82-110">EXAMPLES</span></span>

### <span data-ttu-id="bff82-111">範例 1：依規則名稱設定</span><span class="sxs-lookup"><span data-stu-id="bff82-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="bff82-112">範例 2：按輸入物件設定</span><span class="sxs-lookup"><span data-stu-id="bff82-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="bff82-113">範例 3：根據資源識別碼設定</span><span class="sxs-lookup"><span data-stu-id="bff82-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="bff82-114">參數</span><span class="sxs-lookup"><span data-stu-id="bff82-114">PARAMETERS</span></span>

### <span data-ttu-id="bff82-115">-動作</span><span class="sxs-lookup"><span data-stu-id="bff82-115">-Action</span></span>
<span data-ttu-id="bff82-116">已排程查詢規則警示動作</span><span class="sxs-lookup"><span data-stu-id="bff82-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bff82-117">-AsJob</span></span>
<span data-ttu-id="bff82-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bff82-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bff82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff82-119">-DefaultProfile</span></span>
<span data-ttu-id="bff82-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bff82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff82-121">-描述</span><span class="sxs-lookup"><span data-stu-id="bff82-121">-Description</span></span>
<span data-ttu-id="bff82-122">此通知的描述</span><span class="sxs-lookup"><span data-stu-id="bff82-122">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-123">-已啟用</span><span class="sxs-lookup"><span data-stu-id="bff82-123">-Enabled</span></span>
<span data-ttu-id="bff82-124">Azure 警示狀態 - 有效的值 - $true、$false</span><span class="sxs-lookup"><span data-stu-id="bff82-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bff82-125">-InputObject</span></span>
<span data-ttu-id="bff82-126">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="bff82-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-127">-位置</span><span class="sxs-lookup"><span data-stu-id="bff82-127">-Location</span></span>
<span data-ttu-id="bff82-128">此通知的位置</span><span class="sxs-lookup"><span data-stu-id="bff82-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="bff82-129">-Name</span></span>
<span data-ttu-id="bff82-130">警示名稱</span><span class="sxs-lookup"><span data-stu-id="bff82-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff82-131">-ResourceGroupName</span></span>
<span data-ttu-id="bff82-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="bff82-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bff82-133">-ResourceId</span></span>
<span data-ttu-id="bff82-134">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bff82-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-135">-排程</span><span class="sxs-lookup"><span data-stu-id="bff82-135">-Schedule</span></span>
<span data-ttu-id="bff82-136">已排程的查詢規則排程</span><span class="sxs-lookup"><span data-stu-id="bff82-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-137">-來源</span><span class="sxs-lookup"><span data-stu-id="bff82-137">-Source</span></span>
<span data-ttu-id="bff82-138">已排程查詢規則來源</span><span class="sxs-lookup"><span data-stu-id="bff82-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-139">-標記</span><span class="sxs-lookup"><span data-stu-id="bff82-139">-Tag</span></span>
<span data-ttu-id="bff82-140">資源標記</span><span class="sxs-lookup"><span data-stu-id="bff82-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-141">-確認</span><span class="sxs-lookup"><span data-stu-id="bff82-141">-Confirm</span></span>
<span data-ttu-id="bff82-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bff82-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff82-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff82-143">-WhatIf</span></span>
<span data-ttu-id="bff82-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bff82-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff82-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bff82-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff82-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff82-146">CommonParameters</span></span>
<span data-ttu-id="bff82-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bff82-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff82-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bff82-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff82-149">輸入</span><span class="sxs-lookup"><span data-stu-id="bff82-149">INPUTS</span></span>

### <span data-ttu-id="bff82-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="bff82-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="bff82-151">System.String</span><span class="sxs-lookup"><span data-stu-id="bff82-151">System.String</span></span>

### <span data-ttu-id="bff82-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bff82-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="bff82-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="bff82-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="bff82-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bff82-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bff82-155">輸出</span><span class="sxs-lookup"><span data-stu-id="bff82-155">OUTPUTS</span></span>

### <span data-ttu-id="bff82-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="bff82-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="bff82-157">筆記</span><span class="sxs-lookup"><span data-stu-id="bff82-157">NOTES</span></span>

## <span data-ttu-id="bff82-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bff82-158">RELATED LINKS</span></span>
