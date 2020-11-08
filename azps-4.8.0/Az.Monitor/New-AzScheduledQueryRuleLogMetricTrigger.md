---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127741"
---
# <span data-ttu-id="59447-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="59447-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="59447-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59447-102">SYNOPSIS</span></span>
<span data-ttu-id="59447-103">建立類型記錄度量觸發程式的物件。</span><span class="sxs-lookup"><span data-stu-id="59447-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="59447-104">句法</span><span class="sxs-lookup"><span data-stu-id="59447-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59447-105">說明</span><span class="sxs-lookup"><span data-stu-id="59447-105">DESCRIPTION</span></span>
<span data-ttu-id="59447-106">建立類型記錄度量觸發程式的物件，且它是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="59447-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="59447-107">這是公制查詢規則的觸發條件，可在您需要 [警示] 的狀態度量類型時使用。</span><span class="sxs-lookup"><span data-stu-id="59447-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="59447-108">示例</span><span class="sxs-lookup"><span data-stu-id="59447-108">EXAMPLES</span></span>

### <span data-ttu-id="59447-109">範例1</span><span class="sxs-lookup"><span data-stu-id="59447-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="59447-110">參數</span><span class="sxs-lookup"><span data-stu-id="59447-110">PARAMETERS</span></span>

### <span data-ttu-id="59447-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59447-111">-DefaultProfile</span></span>
<span data-ttu-id="59447-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59447-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59447-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="59447-113">-MetricColumn</span></span>
<span data-ttu-id="59447-114">要匯總之公制值的欄。</span><span class="sxs-lookup"><span data-stu-id="59447-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="59447-115">未驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="59447-115">The input is not validated.</span></span> <span data-ttu-id="59447-116">在最終呼叫 New-AzScheduledQueryRule 時，會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="59447-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="59447-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="59447-117">-MetricTriggerType</span></span>
<span data-ttu-id="59447-118">公制觸發類型。</span><span class="sxs-lookup"><span data-stu-id="59447-118">The metric trigger type.</span></span>
<span data-ttu-id="59447-119">未驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="59447-119">The input is not validated.</span></span> <span data-ttu-id="59447-120">在最終呼叫 New-AzScheduledQueryRule 時，會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="59447-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="59447-121">-閾值</span><span class="sxs-lookup"><span data-stu-id="59447-121">-Threshold</span></span>
<span data-ttu-id="59447-122">[公制] 閾值： [連續]、[總計]。</span><span class="sxs-lookup"><span data-stu-id="59447-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="59447-123">未驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="59447-123">The input is not validated.</span></span> <span data-ttu-id="59447-124">在最終呼叫 New-AzScheduledQueryRule 時，會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="59447-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="59447-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="59447-125">-ThresholdOperator</span></span>
<span data-ttu-id="59447-126">公制閾值運算子： GreaterThan、小於、相等。</span><span class="sxs-lookup"><span data-stu-id="59447-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="59447-127">未驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="59447-127">The input is not validated.</span></span> <span data-ttu-id="59447-128">在最終呼叫 New-AzScheduledQueryRule 時，會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="59447-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="59447-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59447-129">CommonParameters</span></span>
<span data-ttu-id="59447-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59447-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59447-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59447-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59447-132">輸入</span><span class="sxs-lookup"><span data-stu-id="59447-132">INPUTS</span></span>

### <span data-ttu-id="59447-133">所有</span><span class="sxs-lookup"><span data-stu-id="59447-133">None</span></span>

## <span data-ttu-id="59447-134">輸出</span><span class="sxs-lookup"><span data-stu-id="59447-134">OUTPUTS</span></span>

### <span data-ttu-id="59447-135">PSScheduledQueryRuleLogMetricTrigger 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="59447-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="59447-136">筆記</span><span class="sxs-lookup"><span data-stu-id="59447-136">NOTES</span></span>

## <span data-ttu-id="59447-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="59447-137">RELATED LINKS</span></span>
