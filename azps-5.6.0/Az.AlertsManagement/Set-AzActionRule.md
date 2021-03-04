---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 65d402f06770542265bd9b0a6e9e50cd943114f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917821"
---
# <span data-ttu-id="ef6fe-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="ef6fe-101">Set-AzActionRule</span></span>

## <span data-ttu-id="ef6fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6fe-103">建立或更新動作規則。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-103">Create or update an action rule.</span></span>

## <span data-ttu-id="ef6fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef6fe-104">SYNTAX</span></span>

### <span data-ttu-id="ef6fe-105">BySifiedFormatDiagnosticsActionRule (預設) </span><span class="sxs-lookup"><span data-stu-id="ef6fe-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6fe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef6fe-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6fe-107">BySifiedifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="ef6fe-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6fe-108">BySifiedifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="ef6fe-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6fe-109">描述</span><span class="sxs-lookup"><span data-stu-id="ef6fe-109">DESCRIPTION</span></span>
<span data-ttu-id="ef6fe-110">**Set-AzActionRule** 會建立或更新動作規則。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="ef6fe-111">例子</span><span class="sxs-lookup"><span data-stu-id="ef6fe-111">EXAMPLES</span></span>

### <span data-ttu-id="ef6fe-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef6fe-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="ef6fe-113">此 Cmdlet 會建立一個具有訂閱範圍的運算式動作規則。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="ef6fe-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="ef6fe-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="ef6fe-115">此 Cmdlet 會建立動作群組的動作規則，並包含資源群組範圍清單。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="ef6fe-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="ef6fe-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="ef6fe-117">此 Cmdlet 會針對具有資源範圍的診斷設定建立動作規則。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="ef6fe-118">參數</span><span class="sxs-lookup"><span data-stu-id="ef6fe-118">PARAMETERS</span></span>

### <span data-ttu-id="ef6fe-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="ef6fe-119">-ActionGroupId</span></span>
<span data-ttu-id="ef6fe-120">要通知的動作群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="ef6fe-121">-ActionRuleType</span></span>
<span data-ttu-id="ef6fe-122">動作規則 Json 格式</span><span class="sxs-lookup"><span data-stu-id="ef6fe-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-123">-AlertCoNtextCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-123">-AlertContextCondition</span></span>
<span data-ttu-id="ef6fe-124">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-125">包含：smartgroups</span><span class="sxs-lookup"><span data-stu-id="ef6fe-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="ef6fe-127">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-128">等於：/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="ef6fe-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6fe-129">-DefaultProfile</span></span>
<span data-ttu-id="ef6fe-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef6fe-131">-描述</span><span class="sxs-lookup"><span data-stu-id="ef6fe-131">-Description</span></span>
<span data-ttu-id="ef6fe-132">動作規則的描述</span><span class="sxs-lookup"><span data-stu-id="ef6fe-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-133">-DescriptionCondition</span></span>
<span data-ttu-id="ef6fe-134">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-135">包含：測試通知</span><span class="sxs-lookup"><span data-stu-id="ef6fe-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6fe-136">-InputObject</span></span>
<span data-ttu-id="ef6fe-137">動作規則資源</span><span class="sxs-lookup"><span data-stu-id="ef6fe-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-138">-MonitorCondition</span></span>
<span data-ttu-id="ef6fe-139">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-140">NotEquals：已解決</span><span class="sxs-lookup"><span data-stu-id="ef6fe-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="ef6fe-142">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-143">等於：平臺、記錄分析</span><span class="sxs-lookup"><span data-stu-id="ef6fe-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef6fe-144">-Name</span></span>
<span data-ttu-id="ef6fe-145">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="ef6fe-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="ef6fe-146">-ReccurenceType</span></span>
<span data-ttu-id="ef6fe-147">指定應該使用干擾的持續時間。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="ef6fe-148">-ReccurentValue</span></span>
<span data-ttu-id="ef6fe-149">遞迴值 ，如果適用。以每週 - \[ 1，2 \] 為每月 - \[ 1，3，5，30\]</span><span class="sxs-lookup"><span data-stu-id="ef6fe-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6fe-150">-ResourceGroupName</span></span>
<span data-ttu-id="ef6fe-151">資源組名</span><span class="sxs-lookup"><span data-stu-id="ef6fe-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="ef6fe-152">-Scope</span></span>
<span data-ttu-id="ef6fe-153">以逗號分隔的值清單</span><span class="sxs-lookup"><span data-stu-id="ef6fe-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-154">-嚴重性Condition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-154">-SeverityCondition</span></span>
<span data-ttu-id="ef6fe-155">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-156">等於：Sev0，Sev1</span><span class="sxs-lookup"><span data-stu-id="ef6fe-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-157">-狀態</span><span class="sxs-lookup"><span data-stu-id="ef6fe-157">-Status</span></span>
<span data-ttu-id="ef6fe-158">動作規則的狀態。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-159">-EndEndTime</span><span class="sxs-lookup"><span data-stu-id="ef6fe-159">-SuppressionEndTime</span></span>
<span data-ttu-id="ef6fe-160">干擾結束時間。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-160">Suppression End Time.</span></span>
<span data-ttu-id="ef6fe-161">格式 12/09/2018 06：00：00 +在 Reccurent Supression Schedule 中應提及 - 一次、每天、每週或每月。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-162">-StartTime -StartTime</span><span class="sxs-lookup"><span data-stu-id="ef6fe-162">-SuppressionStartTime</span></span>
<span data-ttu-id="ef6fe-163">干擾開始時間。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-163">Suppression Start Time.</span></span>
<span data-ttu-id="ef6fe-164">格式 12/09/2018 06：00：00 +在 Reccurent Supression Schedule 中應提及 - 一次、每天、每週或每月。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="ef6fe-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="ef6fe-166">預期格式 - { \<operation\> ： \<comma separated list of values\> } for 例如。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ef6fe-167">包含：虛擬機器、儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ef6fe-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6fe-168">-確認</span><span class="sxs-lookup"><span data-stu-id="ef6fe-168">-Confirm</span></span>
<span data-ttu-id="ef6fe-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6fe-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6fe-170">-WhatIf</span></span>
<span data-ttu-id="ef6fe-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef6fe-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6fe-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6fe-173">CommonParameters</span></span>
<span data-ttu-id="ef6fe-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef6fe-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6fe-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef6fe-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6fe-176">輸入</span><span class="sxs-lookup"><span data-stu-id="ef6fe-176">INPUTS</span></span>

### <span data-ttu-id="ef6fe-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ef6fe-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ef6fe-178">輸出</span><span class="sxs-lookup"><span data-stu-id="ef6fe-178">OUTPUTS</span></span>

### <span data-ttu-id="ef6fe-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ef6fe-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ef6fe-180">筆記</span><span class="sxs-lookup"><span data-stu-id="ef6fe-180">NOTES</span></span>

## <span data-ttu-id="ef6fe-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef6fe-181">RELATED LINKS</span></span>
