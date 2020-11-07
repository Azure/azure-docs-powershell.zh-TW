---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 17be83253d452b4c347154f8c0e392277287d0b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786781"
---
# <span data-ttu-id="548a3-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="548a3-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="548a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="548a3-102">SYNOPSIS</span></span>
<span data-ttu-id="548a3-103">新增或更新基 (非傳統) 公制規則。</span><span class="sxs-lookup"><span data-stu-id="548a3-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="548a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="548a3-104">SYNTAX</span></span>

### <span data-ttu-id="548a3-105">CreateAlertByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="548a3-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548a3-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="548a3-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548a3-107">說明</span><span class="sxs-lookup"><span data-stu-id="548a3-107">DESCRIPTION</span></span>
<span data-ttu-id="548a3-108">新增或更新 **基 (非傳統) 公制規則** 。</span><span class="sxs-lookup"><span data-stu-id="548a3-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="548a3-109">新增的規則與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="548a3-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="548a3-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="548a3-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="548a3-111">示例</span><span class="sxs-lookup"><span data-stu-id="548a3-111">EXAMPLES</span></span>

### <span data-ttu-id="548a3-112">範例1：將度量警報規則新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="548a3-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="548a3-113">這個命令會建立虛擬機器的度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="548a3-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="548a3-114">$condition 是 New-AzMetricAlertRuleV2Criteria Cmdlet 的輸出，而 $act 是 New-AzActionGroup Cmdlet 的輸出</span><span class="sxs-lookup"><span data-stu-id="548a3-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="548a3-115">範例2：為訂閱中的所有虛擬機器新增公制警報規則</span><span class="sxs-lookup"><span data-stu-id="548a3-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="548a3-116">這個命令會針對 eastus 中的訂閱中的所有虛擬機器建立公制警報規則</span><span class="sxs-lookup"><span data-stu-id="548a3-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="548a3-117">範例3：停用度量警示規則</span><span class="sxs-lookup"><span data-stu-id="548a3-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="548a3-118">這個命令會停用度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="548a3-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="548a3-119">在這裡，我們會將 Get-AzMetricAlertRuleV2 的輸出管道到 Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="548a3-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="548a3-120">範例4：新增含維度的度量警示規則</span><span class="sxs-lookup"><span data-stu-id="548a3-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="548a3-121">若要建立更複雜的度量警報規則，例如選取維度值或有多個準則，您可以使用協助程式 Cmdlet New-AzMetricAlertRuleV2DimensionSelection 與 AzMetricAlertRuleV2Criteria。</span><span class="sxs-lookup"><span data-stu-id="548a3-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="548a3-122">上方的一組 Cmdlet 會建立含維度的度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="548a3-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>
## <span data-ttu-id="548a3-123">參數</span><span class="sxs-lookup"><span data-stu-id="548a3-123">PARAMETERS</span></span>

### <span data-ttu-id="548a3-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="548a3-124">-ActionGroup</span></span>
<span data-ttu-id="548a3-125">規則的 [動作] 群組</span><span class="sxs-lookup"><span data-stu-id="548a3-125">The Action Group for rule</span></span>

```yaml
Type: ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-126">-條件</span><span class="sxs-lookup"><span data-stu-id="548a3-126">-Condition</span></span>
<span data-ttu-id="548a3-127">規則的條件</span><span class="sxs-lookup"><span data-stu-id="548a3-127">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-128">-確認</span><span class="sxs-lookup"><span data-stu-id="548a3-128">-Confirm</span></span>
<span data-ttu-id="548a3-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="548a3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548a3-130">-DefaultProfile</span></span>
<span data-ttu-id="548a3-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="548a3-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-132">-描述</span><span class="sxs-lookup"><span data-stu-id="548a3-132">-Description</span></span>
<span data-ttu-id="548a3-133">指標警報規則的描述</span><span class="sxs-lookup"><span data-stu-id="548a3-133">The description of the metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="548a3-134">-DisableRule</span></span>
<span data-ttu-id="548a3-135">[停用規則] (狀態) 旗標</span><span class="sxs-lookup"><span data-stu-id="548a3-135">The disable rule (status) flag</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-136">頻率</span><span class="sxs-lookup"><span data-stu-id="548a3-136">-Frequency</span></span>
<span data-ttu-id="548a3-137">規則的評估頻率</span><span class="sxs-lookup"><span data-stu-id="548a3-137">The evaluation frequency for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="548a3-138">-Name</span></span>
<span data-ttu-id="548a3-139">公制警報規則的名稱</span><span class="sxs-lookup"><span data-stu-id="548a3-139">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548a3-140">-ResourceGroupName</span></span>
<span data-ttu-id="548a3-141">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="548a3-141">The Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-142">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="548a3-142">-Severity</span></span>
<span data-ttu-id="548a3-143">公制警報規則的嚴重性</span><span class="sxs-lookup"><span data-stu-id="548a3-143">The severity for the metric alert rule</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="548a3-144">-TargetResourceId</span></span>
<span data-ttu-id="548a3-145">規則的目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="548a3-145">The target resource id for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="548a3-146">-TargetResourceRegion</span></span>
<span data-ttu-id="548a3-147">規則的目標資源區域</span><span class="sxs-lookup"><span data-stu-id="548a3-147">The target resource region for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="548a3-148">-TargetResourceScope</span></span>
<span data-ttu-id="548a3-149">規則的目標資源範圍</span><span class="sxs-lookup"><span data-stu-id="548a3-149">The target resource scope for rule</span></span>

```yaml
Type: String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="548a3-150">-TargetResourceType</span></span>
<span data-ttu-id="548a3-151">規則的目標資源類型</span><span class="sxs-lookup"><span data-stu-id="548a3-151">The target resource type for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548a3-152">-WhatIf</span></span>
<span data-ttu-id="548a3-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="548a3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548a3-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="548a3-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-155">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="548a3-155">-WindowSize</span></span>
<span data-ttu-id="548a3-156">規則的視窗大小</span><span class="sxs-lookup"><span data-stu-id="548a3-156">The window size for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548a3-157">CommonParameters</span></span>
<span data-ttu-id="548a3-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="548a3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="548a3-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="548a3-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548a3-160">輸入</span><span class="sxs-lookup"><span data-stu-id="548a3-160">INPUTS</span></span>

### <span data-ttu-id="548a3-161">System.object</span><span class="sxs-lookup"><span data-stu-id="548a3-161">System.String</span></span>

### <span data-ttu-id="548a3-162">System.object</span><span class="sxs-lookup"><span data-stu-id="548a3-162">System.TimeSpan</span></span>

### <span data-ttu-id="548a3-163">System.object []</span><span class="sxs-lookup"><span data-stu-id="548a3-163">System.String[]</span></span>

### <span data-ttu-id="548a3-164">[System.object]. 清單 ' 1 [OutputClasses. PSMetricCriteria，，1.0.1.0，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="548a3-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="548a3-165">ActivityLogAlertActionGroup [] 中的 [管理模型]</span><span class="sxs-lookup"><span data-stu-id="548a3-165">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="548a3-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="548a3-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="548a3-167">System.object</span><span class="sxs-lookup"><span data-stu-id="548a3-167">System.Int32</span></span>

## <span data-ttu-id="548a3-168">輸出</span><span class="sxs-lookup"><span data-stu-id="548a3-168">OUTPUTS</span></span>

### <span data-ttu-id="548a3-169">PSMetricAlertRuleV2 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="548a3-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="548a3-170">筆記</span><span class="sxs-lookup"><span data-stu-id="548a3-170">NOTES</span></span>

## <span data-ttu-id="548a3-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="548a3-171">RELATED LINKS</span></span>
