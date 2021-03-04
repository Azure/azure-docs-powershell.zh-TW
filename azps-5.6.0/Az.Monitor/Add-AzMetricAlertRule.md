---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: a38dbb3e608390369a31d9376923328d9550cbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908990"
---
# <span data-ttu-id="af477-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="af477-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="af477-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af477-102">SYNOPSIS</span></span>
<span data-ttu-id="af477-103">新增或更新公制提醒規則。</span><span class="sxs-lookup"><span data-stu-id="af477-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="af477-104">語法</span><span class="sxs-lookup"><span data-stu-id="af477-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af477-105">描述</span><span class="sxs-lookup"><span data-stu-id="af477-105">DESCRIPTION</span></span>
<span data-ttu-id="af477-106">**Add-AzMetricAlertRule** Cmdlet 會新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="af477-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="af477-107">新增的規則與資源群組相關聯，而且有名稱。</span><span class="sxs-lookup"><span data-stu-id="af477-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="af477-108">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="af477-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="af477-109">例子</span><span class="sxs-lookup"><span data-stu-id="af477-109">EXAMPLES</span></span>

### <span data-ttu-id="af477-110">範例 1：新增計量警示規則至網站</span><span class="sxs-lookup"><span data-stu-id="af477-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="af477-111">此命令會為網站建立公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="af477-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="af477-112">範例 2：停用規則</span><span class="sxs-lookup"><span data-stu-id="af477-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="af477-113">此命令會停用規則。</span><span class="sxs-lookup"><span data-stu-id="af477-113">This command disables a rule.</span></span>
<span data-ttu-id="af477-114">如果規則不存在，會建立已停用的規則。</span><span class="sxs-lookup"><span data-stu-id="af477-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="af477-115">如果規則存在，則它只要將其停用。</span><span class="sxs-lookup"><span data-stu-id="af477-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="af477-116">範例 3：使用動作新增規則</span><span class="sxs-lookup"><span data-stu-id="af477-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="af477-117">此命令會為網站建立公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="af477-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="af477-118">參數</span><span class="sxs-lookup"><span data-stu-id="af477-118">PARAMETERS</span></span>

### <span data-ttu-id="af477-119">-動作</span><span class="sxs-lookup"><span data-stu-id="af477-119">-Action</span></span>
<span data-ttu-id="af477-120">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="af477-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af477-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af477-121">-DefaultProfile</span></span>
<span data-ttu-id="af477-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="af477-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af477-123">-描述</span><span class="sxs-lookup"><span data-stu-id="af477-123">-Description</span></span>
<span data-ttu-id="af477-124">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="af477-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="af477-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="af477-125">-DisableRule</span></span>
<span data-ttu-id="af477-126">停用規則。</span><span class="sxs-lookup"><span data-stu-id="af477-126">Disables the rule.</span></span>
<span data-ttu-id="af477-127">如果您未指定此參數，則規則會啟用。</span><span class="sxs-lookup"><span data-stu-id="af477-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="af477-128">-位置</span><span class="sxs-lookup"><span data-stu-id="af477-128">-Location</span></span>
<span data-ttu-id="af477-129">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="af477-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="af477-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="af477-130">-MetricName</span></span>
<span data-ttu-id="af477-131">指定規則監控的度量名稱。</span><span class="sxs-lookup"><span data-stu-id="af477-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="af477-132">僅針對公制規則指定此參數。</span><span class="sxs-lookup"><span data-stu-id="af477-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="af477-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="af477-133">-Name</span></span>
<span data-ttu-id="af477-134">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="af477-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="af477-135">-運算子</span><span class="sxs-lookup"><span data-stu-id="af477-135">-Operator</span></span>
<span data-ttu-id="af477-136">指定規則條件的關係運算子。</span><span class="sxs-lookup"><span data-stu-id="af477-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="af477-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="af477-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af477-138">Greater用</span><span class="sxs-lookup"><span data-stu-id="af477-138">GreaterThan</span></span>
- <span data-ttu-id="af477-139">GreaterQualOrEqual</span><span class="sxs-lookup"><span data-stu-id="af477-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="af477-140">Less一維</span><span class="sxs-lookup"><span data-stu-id="af477-140">LessThan</span></span>
- <span data-ttu-id="af477-141">LessQualOrEqual</span><span class="sxs-lookup"><span data-stu-id="af477-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af477-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af477-142">-ResourceGroupName</span></span>
<span data-ttu-id="af477-143">指定規則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="af477-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="af477-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="af477-144">-TargetResourceId</span></span>
<span data-ttu-id="af477-145">指定規則監視之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="af477-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="af477-146">注意：無法針對現有的警示規則更新此屬性。</span><span class="sxs-lookup"><span data-stu-id="af477-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="af477-147">-閾值</span><span class="sxs-lookup"><span data-stu-id="af477-147">-Threshold</span></span>
<span data-ttu-id="af477-148">指定規則的閾值。</span><span class="sxs-lookup"><span data-stu-id="af477-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af477-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="af477-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="af477-150">指定評估規則時要適用于時間視窗的匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="af477-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af477-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="af477-151">-WindowSize</span></span>
<span data-ttu-id="af477-152">指定規則計算其資料的時段大小。</span><span class="sxs-lookup"><span data-stu-id="af477-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="af477-153">-確認</span><span class="sxs-lookup"><span data-stu-id="af477-153">-Confirm</span></span>
<span data-ttu-id="af477-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af477-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af477-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af477-155">-WhatIf</span></span>
<span data-ttu-id="af477-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af477-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af477-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af477-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af477-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af477-158">CommonParameters</span></span>
<span data-ttu-id="af477-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af477-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af477-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af477-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af477-161">輸入</span><span class="sxs-lookup"><span data-stu-id="af477-161">INPUTS</span></span>

### <span data-ttu-id="af477-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="af477-162">System.TimeSpan</span></span>

### <span data-ttu-id="af477-163">Microsoft.Azure.management.Monitor.management.models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="af477-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="af477-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="af477-164">System.Double</span></span>

### <span data-ttu-id="af477-165">System.String</span><span class="sxs-lookup"><span data-stu-id="af477-165">System.String</span></span>

### <span data-ttu-id="af477-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af477-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="af477-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af477-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="af477-168">System.Collections.generic.List'1[[Microsoft.Azure.management.Monitor.management.models.RuleAction，Microsoft.Azure.PowerShell.Cmdlets.Monitor， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af477-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="af477-169">輸出</span><span class="sxs-lookup"><span data-stu-id="af477-169">OUTPUTS</span></span>

### <span data-ttu-id="af477-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af477-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="af477-171">筆記</span><span class="sxs-lookup"><span data-stu-id="af477-171">NOTES</span></span>

## <span data-ttu-id="af477-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="af477-172">RELATED LINKS</span></span>

[<span data-ttu-id="af477-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af477-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="af477-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="af477-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="af477-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="af477-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="af477-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="af477-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="af477-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="af477-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="af477-178">New-AzAlertRuleWeb一體式</span><span class="sxs-lookup"><span data-stu-id="af477-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="af477-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="af477-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


