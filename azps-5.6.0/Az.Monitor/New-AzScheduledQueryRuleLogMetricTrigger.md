---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908529"
---
# <span data-ttu-id="960c3-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="960c3-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="960c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="960c3-102">SYNOPSIS</span></span>
<span data-ttu-id="960c3-103">建立類型為記錄公制觸發的物件。</span><span class="sxs-lookup"><span data-stu-id="960c3-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="960c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="960c3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="960c3-105">描述</span><span class="sxs-lookup"><span data-stu-id="960c3-105">DESCRIPTION</span></span>
<span data-ttu-id="960c3-106">建立記錄度量觸發類型的物件，而且為選擇性。</span><span class="sxs-lookup"><span data-stu-id="960c3-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="960c3-107">這是公制查詢規則的觸發條件，用於您需要指出警示的公制度量類型。</span><span class="sxs-lookup"><span data-stu-id="960c3-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="960c3-108">例子</span><span class="sxs-lookup"><span data-stu-id="960c3-108">EXAMPLES</span></span>

### <span data-ttu-id="960c3-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="960c3-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="960c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="960c3-110">PARAMETERS</span></span>

### <span data-ttu-id="960c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960c3-111">-DefaultProfile</span></span>
<span data-ttu-id="960c3-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="960c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="960c3-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="960c3-113">-MetricColumn</span></span>
<span data-ttu-id="960c3-114">匯總公制值的欄。</span><span class="sxs-lookup"><span data-stu-id="960c3-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="960c3-115">系統不會驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="960c3-115">The input is not validated.</span></span> <span data-ttu-id="960c3-116">它會先在系統New-AzScheduledQueryRule驗證。</span><span class="sxs-lookup"><span data-stu-id="960c3-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="960c3-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="960c3-117">-MetricTriggerType</span></span>
<span data-ttu-id="960c3-118">公制觸發類型。</span><span class="sxs-lookup"><span data-stu-id="960c3-118">The metric trigger type.</span></span>
<span data-ttu-id="960c3-119">系統不會驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="960c3-119">The input is not validated.</span></span> <span data-ttu-id="960c3-120">它會先在系統New-AzScheduledQueryRule驗證。</span><span class="sxs-lookup"><span data-stu-id="960c3-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="960c3-121">-閾值</span><span class="sxs-lookup"><span data-stu-id="960c3-121">-Threshold</span></span>
<span data-ttu-id="960c3-122">公制閾值：連續、總計。</span><span class="sxs-lookup"><span data-stu-id="960c3-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="960c3-123">系統不會驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="960c3-123">The input is not validated.</span></span> <span data-ttu-id="960c3-124">它會先在系統New-AzScheduledQueryRule驗證。</span><span class="sxs-lookup"><span data-stu-id="960c3-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="960c3-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="960c3-125">-ThresholdOperator</span></span>
<span data-ttu-id="960c3-126">公制閾值運算子：Greater一次、Less一次、等於。</span><span class="sxs-lookup"><span data-stu-id="960c3-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="960c3-127">系統不會驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="960c3-127">The input is not validated.</span></span> <span data-ttu-id="960c3-128">它會先在系統New-AzScheduledQueryRule驗證。</span><span class="sxs-lookup"><span data-stu-id="960c3-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="960c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960c3-129">CommonParameters</span></span>
<span data-ttu-id="960c3-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="960c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960c3-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="960c3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960c3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="960c3-132">INPUTS</span></span>

### <span data-ttu-id="960c3-133">沒有</span><span class="sxs-lookup"><span data-stu-id="960c3-133">None</span></span>

## <span data-ttu-id="960c3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="960c3-134">OUTPUTS</span></span>

### <span data-ttu-id="960c3-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="960c3-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="960c3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="960c3-136">NOTES</span></span>

## <span data-ttu-id="960c3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="960c3-137">RELATED LINKS</span></span>
