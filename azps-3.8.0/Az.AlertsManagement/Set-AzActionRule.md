---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: f2f8d4d17f9cce30f5101a5ae5a90c20c50e3f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957135"
---
# <span data-ttu-id="dfcf9-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="dfcf9-101">Set-AzActionRule</span></span>

## <span data-ttu-id="dfcf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcf9-103">建立或更新行動規則。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-103">Create or update an action rule.</span></span>

## <span data-ttu-id="dfcf9-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfcf9-104">SYNTAX</span></span>

### <span data-ttu-id="dfcf9-105">BySimplifiedFormatDiagnosticsActionRule (預設) </span><span class="sxs-lookup"><span data-stu-id="dfcf9-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcf9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dfcf9-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfcf9-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="dfcf9-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcf9-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="dfcf9-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcf9-109">說明</span><span class="sxs-lookup"><span data-stu-id="dfcf9-109">DESCRIPTION</span></span>
<span data-ttu-id="dfcf9-110">[ **設定] AzActionRule** 會建立或更新動作規則。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="dfcf9-111">示例</span><span class="sxs-lookup"><span data-stu-id="dfcf9-111">EXAMPLES</span></span>

### <span data-ttu-id="dfcf9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dfcf9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="dfcf9-113">這個 Cmdlet 會建立 supression 的動作規則。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="dfcf9-114">範例2</span><span class="sxs-lookup"><span data-stu-id="dfcf9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="dfcf9-115">這個 Cmdlet 會建立動作群組的動作規則。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="dfcf9-116">範例3</span><span class="sxs-lookup"><span data-stu-id="dfcf9-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="dfcf9-117">這個 Cmdlet 會為診斷設定建立動作規則。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="dfcf9-118">參數</span><span class="sxs-lookup"><span data-stu-id="dfcf9-118">PARAMETERS</span></span>

### <span data-ttu-id="dfcf9-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="dfcf9-119">-ActionGroupId</span></span>
<span data-ttu-id="dfcf9-120">要通知的動作群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="dfcf9-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="dfcf9-121">-ActionRuleType</span></span>
<span data-ttu-id="dfcf9-122">動作規則 Json 格式</span><span class="sxs-lookup"><span data-stu-id="dfcf9-122">Action rule Json format</span></span>

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

### <span data-ttu-id="dfcf9-123">-AlertCoNtextCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-123">-AlertContextCondition</span></span>
<span data-ttu-id="dfcf9-124">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-125">包含： smartgroups</span><span class="sxs-lookup"><span data-stu-id="dfcf9-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="dfcf9-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="dfcf9-127">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-128">Equals：/訂閱/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers//metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="dfcf9-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="dfcf9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcf9-129">-DefaultProfile</span></span>
<span data-ttu-id="dfcf9-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfcf9-131">-描述</span><span class="sxs-lookup"><span data-stu-id="dfcf9-131">-Description</span></span>
<span data-ttu-id="dfcf9-132">行動規則的描述</span><span class="sxs-lookup"><span data-stu-id="dfcf9-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="dfcf9-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-133">-DescriptionCondition</span></span>
<span data-ttu-id="dfcf9-134">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-135">包含：測試警示</span><span class="sxs-lookup"><span data-stu-id="dfcf9-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="dfcf9-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfcf9-136">-InputObject</span></span>
<span data-ttu-id="dfcf9-137">[動作規則] 資源</span><span class="sxs-lookup"><span data-stu-id="dfcf9-137">The action rule resource</span></span>

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

### <span data-ttu-id="dfcf9-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-138">-MonitorCondition</span></span>
<span data-ttu-id="dfcf9-139">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-140">NotEquals：已解決</span><span class="sxs-lookup"><span data-stu-id="dfcf9-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="dfcf9-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="dfcf9-142">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-143">Equals：平臺、記錄分析</span><span class="sxs-lookup"><span data-stu-id="dfcf9-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="dfcf9-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfcf9-144">-Name</span></span>
<span data-ttu-id="dfcf9-145">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="dfcf9-145">Action rule Name</span></span>

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

### <span data-ttu-id="dfcf9-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="dfcf9-146">-ReccurenceType</span></span>
<span data-ttu-id="dfcf9-147">指定應該套用抑制的持續時間。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="dfcf9-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="dfcf9-148">-ReccurentValue</span></span>
<span data-ttu-id="dfcf9-149">Reccurent 值（如果適用的話）。在每週更新- \[ 1、 \] \[ 3、5、30年的情況下，按2\]</span><span class="sxs-lookup"><span data-stu-id="dfcf9-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="dfcf9-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcf9-150">-ResourceGroupName</span></span>
<span data-ttu-id="dfcf9-151">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="dfcf9-151">Resource Group Name</span></span>

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

### <span data-ttu-id="dfcf9-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="dfcf9-152">-Scope</span></span>
<span data-ttu-id="dfcf9-153">以逗號分隔的值清單</span><span class="sxs-lookup"><span data-stu-id="dfcf9-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="dfcf9-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-154">-SeverityCondition</span></span>
<span data-ttu-id="dfcf9-155">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-156">等於： Sev0、Sev1</span><span class="sxs-lookup"><span data-stu-id="dfcf9-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="dfcf9-157">-狀態</span><span class="sxs-lookup"><span data-stu-id="dfcf9-157">-Status</span></span>
<span data-ttu-id="dfcf9-158">行動規則的狀態。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="dfcf9-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="dfcf9-159">-SuppressionEndTime</span></span>
<span data-ttu-id="dfcf9-160">抑制結束時間。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-160">Suppression End Time.</span></span>
<span data-ttu-id="dfcf9-161">如果 Reccurent Supression 排程-一次、每天、每週或每月，則應提及 12/09/2018 06:00:00 + 格式。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="dfcf9-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="dfcf9-162">-SuppressionStartTime</span></span>
<span data-ttu-id="dfcf9-163">抑制開始時間。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-163">Suppression Start Time.</span></span>
<span data-ttu-id="dfcf9-164">如果 Reccurent Supression 排程-一次、每天、每週或每月，則應提及 12/09/2018 06:00:00 + 格式。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="dfcf9-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="dfcf9-166">預期的格式-{ \< 運算 \> ： \< 以逗號分隔的值清單，如所示 \> 。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="dfcf9-167">包含：虛擬機器、儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="dfcf9-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="dfcf9-168">-確認</span><span class="sxs-lookup"><span data-stu-id="dfcf9-168">-Confirm</span></span>
<span data-ttu-id="dfcf9-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcf9-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcf9-170">-WhatIf</span></span>
<span data-ttu-id="dfcf9-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfcf9-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcf9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcf9-173">CommonParameters</span></span>
<span data-ttu-id="dfcf9-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcf9-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfcf9-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcf9-176">輸入</span><span class="sxs-lookup"><span data-stu-id="dfcf9-176">INPUTS</span></span>

### <span data-ttu-id="dfcf9-177">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="dfcf9-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="dfcf9-178">輸出</span><span class="sxs-lookup"><span data-stu-id="dfcf9-178">OUTPUTS</span></span>

### <span data-ttu-id="dfcf9-179">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="dfcf9-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="dfcf9-180">筆記</span><span class="sxs-lookup"><span data-stu-id="dfcf9-180">NOTES</span></span>

## <span data-ttu-id="dfcf9-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfcf9-181">RELATED LINKS</span></span>
