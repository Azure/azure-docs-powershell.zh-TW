---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: f679b674de8ed2f860278cb3a384f73ed17e5f54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908989"
---
# <span data-ttu-id="77e60-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="77e60-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="77e60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77e60-102">SYNOPSIS</span></span>
<span data-ttu-id="77e60-103">新增或更新 V2 (非傳統) 公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="77e60-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="77e60-104">語法</span><span class="sxs-lookup"><span data-stu-id="77e60-104">SYNTAX</span></span>

### <span data-ttu-id="77e60-105">CreateAlertByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="77e60-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77e60-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="77e60-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77e60-107">描述</span><span class="sxs-lookup"><span data-stu-id="77e60-107">DESCRIPTION</span></span>
<span data-ttu-id="77e60-108">新增或更新 **V2 (非傳統) 公制警示規則**。</span><span class="sxs-lookup"><span data-stu-id="77e60-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="77e60-109">新增的規則與資源群組相關聯，而且有名稱。</span><span class="sxs-lookup"><span data-stu-id="77e60-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="77e60-110">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="77e60-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="77e60-111">例子</span><span class="sxs-lookup"><span data-stu-id="77e60-111">EXAMPLES</span></span>

### <span data-ttu-id="77e60-112">範例 1：在虛擬機器中新增公制警示規則</span><span class="sxs-lookup"><span data-stu-id="77e60-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="77e60-113">此命令會為虛擬機器建立公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="77e60-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="77e60-114">$condition [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) Cmdlet 的輸出結果，而 $act 是 [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) Cmdlet 的輸出結果</span><span class="sxs-lookup"><span data-stu-id="77e60-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="77e60-115">範例 2：新增訂閱中所有虛擬機器的公制警示規則</span><span class="sxs-lookup"><span data-stu-id="77e60-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="77e60-116">此命令會針對訂閱中東部的所有虛擬機器建立公制警示規則</span><span class="sxs-lookup"><span data-stu-id="77e60-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="77e60-117">範例 3：停用公制警示規則</span><span class="sxs-lookup"><span data-stu-id="77e60-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="77e60-118">此命令會停用公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="77e60-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="77e60-119">這裡提供 [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) 到 [Add-AzMetricAlertRuleV2 的管線輸出](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="77e60-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="77e60-120">範例 4：新增維度的公制警示規則</span><span class="sxs-lookup"><span data-stu-id="77e60-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="77e60-121">若要建立更複雜的公制警示規則，例如需要選取維度值或有多個準則的警示規則，您可以使用協助程式 Cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection)和[New-AzMetricAlertRuleV2Criteria。](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="77e60-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="77e60-122">上述一組 Cmdlet 會建立具有維度的公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="77e60-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="77e60-123">參數</span><span class="sxs-lookup"><span data-stu-id="77e60-123">PARAMETERS</span></span>

### <span data-ttu-id="77e60-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="77e60-124">-ActionGroup</span></span>
<span data-ttu-id="77e60-125">規則的動作群組</span><span class="sxs-lookup"><span data-stu-id="77e60-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="77e60-126">-ActionGroupId</span></span>
<span data-ttu-id="77e60-127">規則的動作群組識別碼</span><span class="sxs-lookup"><span data-stu-id="77e60-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-128">-條件</span><span class="sxs-lookup"><span data-stu-id="77e60-128">-Condition</span></span>
<span data-ttu-id="77e60-129">規則的條件</span><span class="sxs-lookup"><span data-stu-id="77e60-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e60-130">-DefaultProfile</span></span>
<span data-ttu-id="77e60-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77e60-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e60-132">-描述</span><span class="sxs-lookup"><span data-stu-id="77e60-132">-Description</span></span>
<span data-ttu-id="77e60-133">公制警示規則的描述</span><span class="sxs-lookup"><span data-stu-id="77e60-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="77e60-134">-DisableRule</span></span>
<span data-ttu-id="77e60-135">停用規則會 (狀態) 標</span><span class="sxs-lookup"><span data-stu-id="77e60-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-136">-Frequency</span><span class="sxs-lookup"><span data-stu-id="77e60-136">-Frequency</span></span>
<span data-ttu-id="77e60-137">規則的評估頻率</span><span class="sxs-lookup"><span data-stu-id="77e60-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="77e60-138">-Name</span></span>
<span data-ttu-id="77e60-139">公制警示規則的名稱</span><span class="sxs-lookup"><span data-stu-id="77e60-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e60-140">-ResourceGroupName</span></span>
<span data-ttu-id="77e60-141">資源組名</span><span class="sxs-lookup"><span data-stu-id="77e60-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-142">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="77e60-142">-Severity</span></span>
<span data-ttu-id="77e60-143">公制警示規則的嚴重性</span><span class="sxs-lookup"><span data-stu-id="77e60-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="77e60-144">-TargetResourceId</span></span>
<span data-ttu-id="77e60-145">規則的目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="77e60-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="77e60-146">-TargetResourceRegion</span></span>
<span data-ttu-id="77e60-147">規則的目標資源區域</span><span class="sxs-lookup"><span data-stu-id="77e60-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="77e60-148">-TargetResourceScope</span></span>
<span data-ttu-id="77e60-149">規則的目標資源範圍</span><span class="sxs-lookup"><span data-stu-id="77e60-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="77e60-150">-TargetResourceType</span></span>
<span data-ttu-id="77e60-151">規則的目標資源類型</span><span class="sxs-lookup"><span data-stu-id="77e60-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="77e60-152">-WindowSize</span></span>
<span data-ttu-id="77e60-153">規則的視窗大小</span><span class="sxs-lookup"><span data-stu-id="77e60-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e60-154">-確認</span><span class="sxs-lookup"><span data-stu-id="77e60-154">-Confirm</span></span>
<span data-ttu-id="77e60-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="77e60-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e60-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e60-156">-WhatIf</span></span>
<span data-ttu-id="77e60-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77e60-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e60-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77e60-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e60-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e60-159">CommonParameters</span></span>
<span data-ttu-id="77e60-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77e60-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e60-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77e60-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e60-162">輸入</span><span class="sxs-lookup"><span data-stu-id="77e60-162">INPUTS</span></span>

### <span data-ttu-id="77e60-163">System.String</span><span class="sxs-lookup"><span data-stu-id="77e60-163">System.String</span></span>

### <span data-ttu-id="77e60-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="77e60-164">System.TimeSpan</span></span>

### <span data-ttu-id="77e60-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="77e60-165">System.String[]</span></span>

### <span data-ttu-id="77e60-166">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="77e60-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="77e60-167">Microsoft.Azure.management.monitor.models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="77e60-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="77e60-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77e60-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="77e60-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="77e60-169">System.Int32</span></span>

## <span data-ttu-id="77e60-170">輸出</span><span class="sxs-lookup"><span data-stu-id="77e60-170">OUTPUTS</span></span>

### <span data-ttu-id="77e60-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="77e60-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="77e60-172">筆記</span><span class="sxs-lookup"><span data-stu-id="77e60-172">NOTES</span></span>

## <span data-ttu-id="77e60-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="77e60-173">RELATED LINKS</span></span>
