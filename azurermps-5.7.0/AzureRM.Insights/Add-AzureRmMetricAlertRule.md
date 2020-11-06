---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448655"
---
# <span data-ttu-id="a6777-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6777-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="a6777-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6777-102">SYNOPSIS</span></span>
<span data-ttu-id="a6777-103">新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6777-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6777-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6777-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6777-105">DESCRIPTION</span></span>
<span data-ttu-id="a6777-106">**AzureRmMetricAlertRule** Cmdlet 會新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="a6777-107">新增的規則與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="a6777-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="a6777-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6777-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a6777-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6777-109">EXAMPLES</span></span>

### <span data-ttu-id="a6777-110">範例1：將度量警示規則新增至網站</span><span class="sxs-lookup"><span data-stu-id="a6777-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="a6777-111">這個命令會建立網站的度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="a6777-112">範例2：停用規則</span><span class="sxs-lookup"><span data-stu-id="a6777-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="a6777-113">這個命令會停用規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-113">This command disables a rule.</span></span>
<span data-ttu-id="a6777-114">如果規則不存在，則會將它建立為停用。</span><span class="sxs-lookup"><span data-stu-id="a6777-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="a6777-115">如果規則存在，則它只是停用它。</span><span class="sxs-lookup"><span data-stu-id="a6777-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="a6777-116">範例3：使用動作新增規則</span><span class="sxs-lookup"><span data-stu-id="a6777-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="a6777-117">這個命令會建立網站的度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="a6777-118">參數</span><span class="sxs-lookup"><span data-stu-id="a6777-118">PARAMETERS</span></span>

### <span data-ttu-id="a6777-119">-動作</span><span class="sxs-lookup"><span data-stu-id="a6777-119">-Action</span></span>
<span data-ttu-id="a6777-120">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="a6777-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6777-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6777-121">-DefaultProfile</span></span>
<span data-ttu-id="a6777-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a6777-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6777-123">-描述</span><span class="sxs-lookup"><span data-stu-id="a6777-123">-Description</span></span>
<span data-ttu-id="a6777-124">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="a6777-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="a6777-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="a6777-125">-DisableRule</span></span>
<span data-ttu-id="a6777-126">停用規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-126">Disables the rule.</span></span>
<span data-ttu-id="a6777-127">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="a6777-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="a6777-128">-位置</span><span class="sxs-lookup"><span data-stu-id="a6777-128">-Location</span></span>
<span data-ttu-id="a6777-129">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="a6777-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="a6777-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="a6777-130">-MetricName</span></span>
<span data-ttu-id="a6777-131">指定規則監視的度量名稱。</span><span class="sxs-lookup"><span data-stu-id="a6777-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="a6777-132">請僅針對公制規則指定此參數。</span><span class="sxs-lookup"><span data-stu-id="a6777-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="a6777-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6777-133">-Name</span></span>
<span data-ttu-id="a6777-134">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6777-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="a6777-135">-運算子</span><span class="sxs-lookup"><span data-stu-id="a6777-135">-Operator</span></span>
<span data-ttu-id="a6777-136">針對規則的條件指定關聯式運算子。</span><span class="sxs-lookup"><span data-stu-id="a6777-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="a6777-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a6777-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6777-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="a6777-138">GreaterThan</span></span>
- <span data-ttu-id="a6777-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="a6777-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="a6777-140">小於</span><span class="sxs-lookup"><span data-stu-id="a6777-140">LessThan</span></span>
- <span data-ttu-id="a6777-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="a6777-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6777-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6777-142">-ResourceGroupName</span></span>
<span data-ttu-id="a6777-143">指定規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6777-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="a6777-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a6777-144">-TargetResourceId</span></span>
<span data-ttu-id="a6777-145">指定規則所監視之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6777-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="a6777-146">注意：此屬性無法針對現有的警示規則進行更新。</span><span class="sxs-lookup"><span data-stu-id="a6777-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="a6777-147">-閾值</span><span class="sxs-lookup"><span data-stu-id="a6777-147">-Threshold</span></span>
<span data-ttu-id="a6777-148">指定規則的閥值。</span><span class="sxs-lookup"><span data-stu-id="a6777-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6777-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="a6777-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="a6777-150">指定評估規則時，要套用至時間範圍的匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="a6777-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6777-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="a6777-151">-WindowSize</span></span>
<span data-ttu-id="a6777-152">指定規則計算其資料的時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="a6777-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="a6777-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6777-153">CommonParameters</span></span>
<span data-ttu-id="a6777-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6777-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6777-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6777-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6777-156">輸入</span><span class="sxs-lookup"><span data-stu-id="a6777-156">INPUTS</span></span>

### <span data-ttu-id="a6777-157">所有</span><span class="sxs-lookup"><span data-stu-id="a6777-157">None</span></span>
<span data-ttu-id="a6777-158">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a6777-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6777-159">輸出</span><span class="sxs-lookup"><span data-stu-id="a6777-159">OUTPUTS</span></span>

### <span data-ttu-id="a6777-160">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a6777-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="a6777-161">筆記</span><span class="sxs-lookup"><span data-stu-id="a6777-161">NOTES</span></span>

## <span data-ttu-id="a6777-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6777-162">RELATED LINKS</span></span>

[<span data-ttu-id="a6777-163">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a6777-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a6777-164">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6777-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="a6777-165">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a6777-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="a6777-166">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6777-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="a6777-167">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a6777-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="a6777-168">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="a6777-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="a6777-169">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6777-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


