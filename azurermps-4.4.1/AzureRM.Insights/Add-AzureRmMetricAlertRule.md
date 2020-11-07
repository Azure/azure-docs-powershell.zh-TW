---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626277"
---
# <span data-ttu-id="e418b-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e418b-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="e418b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e418b-102">SYNOPSIS</span></span>
<span data-ttu-id="e418b-103">新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e418b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e418b-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e418b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e418b-105">DESCRIPTION</span></span>
<span data-ttu-id="e418b-106">**AzureRmMetricAlertRule** Cmdlet 會新增或更新以公制為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="e418b-107">新增的規則與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="e418b-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="e418b-108">示例</span><span class="sxs-lookup"><span data-stu-id="e418b-108">EXAMPLES</span></span>

### <span data-ttu-id="e418b-109">範例1：將度量警示規則新增至網站</span><span class="sxs-lookup"><span data-stu-id="e418b-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="e418b-110">這個命令會建立網站的度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="e418b-111">範例2：停用規則</span><span class="sxs-lookup"><span data-stu-id="e418b-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="e418b-112">這個命令會停用規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-112">This command disables a rule.</span></span>
<span data-ttu-id="e418b-113">如果規則不存在，則會將它建立為停用。</span><span class="sxs-lookup"><span data-stu-id="e418b-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="e418b-114">如果規則存在，則它只是停用它。</span><span class="sxs-lookup"><span data-stu-id="e418b-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="e418b-115">範例3：使用動作新增規則</span><span class="sxs-lookup"><span data-stu-id="e418b-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e418b-116">這個命令會建立網站的度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="e418b-117">參數</span><span class="sxs-lookup"><span data-stu-id="e418b-117">PARAMETERS</span></span>

### <span data-ttu-id="e418b-118">-動作</span><span class="sxs-lookup"><span data-stu-id="e418b-118">-Actions</span></span>
<span data-ttu-id="e418b-119">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="e418b-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="e418b-120">-描述</span><span class="sxs-lookup"><span data-stu-id="e418b-120">-Description</span></span>
<span data-ttu-id="e418b-121">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="e418b-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e418b-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e418b-122">-DisableRule</span></span>
<span data-ttu-id="e418b-123">停用規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-123">Disables the rule.</span></span>
<span data-ttu-id="e418b-124">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="e418b-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e418b-125">-位置</span><span class="sxs-lookup"><span data-stu-id="e418b-125">-Location</span></span>
<span data-ttu-id="e418b-126">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="e418b-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e418b-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e418b-127">-MetricName</span></span>
<span data-ttu-id="e418b-128">指定規則監視的度量名稱。</span><span class="sxs-lookup"><span data-stu-id="e418b-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="e418b-129">請僅針對公制規則指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e418b-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="e418b-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e418b-130">-Name</span></span>
<span data-ttu-id="e418b-131">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e418b-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e418b-132">-運算子</span><span class="sxs-lookup"><span data-stu-id="e418b-132">-Operator</span></span>
<span data-ttu-id="e418b-133">針對規則的條件指定關聯式運算子。</span><span class="sxs-lookup"><span data-stu-id="e418b-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="e418b-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e418b-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e418b-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="e418b-135">GreaterThan</span></span>
- <span data-ttu-id="e418b-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e418b-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="e418b-137">小於</span><span class="sxs-lookup"><span data-stu-id="e418b-137">LessThan</span></span>
- <span data-ttu-id="e418b-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e418b-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="e418b-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e418b-139">-ResourceGroup</span></span>
<span data-ttu-id="e418b-140">指定規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e418b-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="e418b-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e418b-141">-TargetResourceId</span></span>
<span data-ttu-id="e418b-142">指定規則所監視之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e418b-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="e418b-143">注意：此屬性無法針對現有的警示規則進行更新。</span><span class="sxs-lookup"><span data-stu-id="e418b-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="e418b-144">-閾值</span><span class="sxs-lookup"><span data-stu-id="e418b-144">-Threshold</span></span>
<span data-ttu-id="e418b-145">指定規則的閥值。</span><span class="sxs-lookup"><span data-stu-id="e418b-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="e418b-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="e418b-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="e418b-147">指定評估規則時，要套用至時間範圍的匯總運算子。</span><span class="sxs-lookup"><span data-stu-id="e418b-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="e418b-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="e418b-148">-WindowSize</span></span>
<span data-ttu-id="e418b-149">指定規則計算其資料的時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="e418b-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e418b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e418b-150">-DefaultProfile</span></span>
<span data-ttu-id="e418b-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e418b-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e418b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e418b-152">CommonParameters</span></span>
<span data-ttu-id="e418b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e418b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e418b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e418b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e418b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="e418b-155">INPUTS</span></span>

## <span data-ttu-id="e418b-156">輸出</span><span class="sxs-lookup"><span data-stu-id="e418b-156">OUTPUTS</span></span>

### <span data-ttu-id="e418b-157">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e418b-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e418b-158">筆記</span><span class="sxs-lookup"><span data-stu-id="e418b-158">NOTES</span></span>

## <span data-ttu-id="e418b-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="e418b-159">RELATED LINKS</span></span>

[<span data-ttu-id="e418b-160">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e418b-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e418b-161">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e418b-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e418b-162">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e418b-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e418b-163">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e418b-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="e418b-164">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e418b-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="e418b-165">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e418b-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="e418b-166">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e418b-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


