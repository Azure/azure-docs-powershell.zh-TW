---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 5a335aaed12a39653d57c5a72e54d6a3caa53828
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796737"
---
# <span data-ttu-id="d94e0-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d94e0-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="d94e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d94e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d94e0-103">更新記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="d94e0-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="d94e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d94e0-104">SYNTAX</span></span>

### <span data-ttu-id="d94e0-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="d94e0-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d94e0-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94e0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d94e0-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="d94e0-108">DESCRIPTION</span></span>
<span data-ttu-id="d94e0-109">透過 PUT 語義來更新記錄警報規則</span><span class="sxs-lookup"><span data-stu-id="d94e0-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="d94e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="d94e0-110">EXAMPLES</span></span>

### <span data-ttu-id="d94e0-111">範例 1-依規則名稱設定</span><span class="sxs-lookup"><span data-stu-id="d94e0-111">Example 1 - Set by rule name</span></span>
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

### <span data-ttu-id="d94e0-112">範例 2-由輸入物件設定</span><span class="sxs-lookup"><span data-stu-id="d94e0-112">Example 2 - Set by Input Object</span></span>
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

### <span data-ttu-id="d94e0-113">範例 3-依資源識別碼設定</span><span class="sxs-lookup"><span data-stu-id="d94e0-113">Example 3 - Set by resource Id</span></span>
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

## <span data-ttu-id="d94e0-114">參數</span><span class="sxs-lookup"><span data-stu-id="d94e0-114">PARAMETERS</span></span>

### <span data-ttu-id="d94e0-115">-動作</span><span class="sxs-lookup"><span data-stu-id="d94e0-115">-Action</span></span>
<span data-ttu-id="d94e0-116">[排程查詢規則] 警示動作</span><span class="sxs-lookup"><span data-stu-id="d94e0-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="d94e0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d94e0-117">-AsJob</span></span>
<span data-ttu-id="d94e0-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d94e0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d94e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94e0-119">-DefaultProfile</span></span>
<span data-ttu-id="d94e0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d94e0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94e0-121">-描述</span><span class="sxs-lookup"><span data-stu-id="d94e0-121">-Description</span></span>
<span data-ttu-id="d94e0-122">此提醒的描述</span><span class="sxs-lookup"><span data-stu-id="d94e0-122">The description for this alert</span></span>

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

### <span data-ttu-id="d94e0-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="d94e0-123">-Enabled</span></span>
<span data-ttu-id="d94e0-124">Azure 警示狀態-有效的值-$true、$false</span><span class="sxs-lookup"><span data-stu-id="d94e0-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="d94e0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d94e0-125">-InputObject</span></span>
<span data-ttu-id="d94e0-126">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="d94e0-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="d94e0-127">-位置</span><span class="sxs-lookup"><span data-stu-id="d94e0-127">-Location</span></span>
<span data-ttu-id="d94e0-128">此提醒的位置</span><span class="sxs-lookup"><span data-stu-id="d94e0-128">The location for this alert</span></span>

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

### <span data-ttu-id="d94e0-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="d94e0-129">-Name</span></span>
<span data-ttu-id="d94e0-130">警示名稱</span><span class="sxs-lookup"><span data-stu-id="d94e0-130">The alert name</span></span>

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

### <span data-ttu-id="d94e0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94e0-131">-ResourceGroupName</span></span>
<span data-ttu-id="d94e0-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d94e0-132">The resource group name</span></span>

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

### <span data-ttu-id="d94e0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d94e0-133">-ResourceId</span></span>
<span data-ttu-id="d94e0-134">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d94e0-134">The resource Id</span></span>

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

### <span data-ttu-id="d94e0-135">-排程</span><span class="sxs-lookup"><span data-stu-id="d94e0-135">-Schedule</span></span>
<span data-ttu-id="d94e0-136">排程查詢規則排程</span><span class="sxs-lookup"><span data-stu-id="d94e0-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="d94e0-137">-來源</span><span class="sxs-lookup"><span data-stu-id="d94e0-137">-Source</span></span>
<span data-ttu-id="d94e0-138">排程查詢規則來源</span><span class="sxs-lookup"><span data-stu-id="d94e0-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="d94e0-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d94e0-139">-Tag</span></span>
<span data-ttu-id="d94e0-140">資源標記</span><span class="sxs-lookup"><span data-stu-id="d94e0-140">Resource tags</span></span>

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

### <span data-ttu-id="d94e0-141">-確認</span><span class="sxs-lookup"><span data-stu-id="d94e0-141">-Confirm</span></span>
<span data-ttu-id="d94e0-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d94e0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94e0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94e0-143">-WhatIf</span></span>
<span data-ttu-id="d94e0-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d94e0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94e0-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d94e0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94e0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94e0-146">CommonParameters</span></span>
<span data-ttu-id="d94e0-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d94e0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94e0-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d94e0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94e0-149">輸入</span><span class="sxs-lookup"><span data-stu-id="d94e0-149">INPUTS</span></span>

### <span data-ttu-id="d94e0-150">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d94e0-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="d94e0-151">System.object</span><span class="sxs-lookup"><span data-stu-id="d94e0-151">System.String</span></span>

### <span data-ttu-id="d94e0-152">PSScheduledQueryRuleSource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d94e0-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="d94e0-153">PSScheduledQueryRuleSchedule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d94e0-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="d94e0-154">PSScheduledQueryRuleAlertingAction 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d94e0-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="d94e0-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d94e0-155">OUTPUTS</span></span>

### <span data-ttu-id="d94e0-156">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d94e0-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="d94e0-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d94e0-157">NOTES</span></span>

## <span data-ttu-id="d94e0-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="d94e0-158">RELATED LINKS</span></span>