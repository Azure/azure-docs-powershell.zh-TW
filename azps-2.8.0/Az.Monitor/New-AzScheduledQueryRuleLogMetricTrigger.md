---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790449"
---
# <span data-ttu-id="2a973-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2a973-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="2a973-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a973-102">SYNOPSIS</span></span>
<span data-ttu-id="2a973-103">建立類型記錄度量觸發程式的物件</span><span class="sxs-lookup"><span data-stu-id="2a973-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="2a973-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a973-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a973-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a973-105">DESCRIPTION</span></span>
<span data-ttu-id="2a973-106">建立類型記錄度量觸發程式的物件，且它是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2a973-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="2a973-107">這是公制查詢規則的觸發條件，可在您需要 [警示] 的狀態度量類型時使用。</span><span class="sxs-lookup"><span data-stu-id="2a973-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="2a973-108">示例</span><span class="sxs-lookup"><span data-stu-id="2a973-108">EXAMPLES</span></span>

### <span data-ttu-id="2a973-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2a973-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="2a973-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a973-110">PARAMETERS</span></span>

### <span data-ttu-id="2a973-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a973-111">-DefaultProfile</span></span>
<span data-ttu-id="2a973-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a973-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a973-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="2a973-113">-MetricColumn</span></span>
<span data-ttu-id="2a973-114">要匯總之公制值的欄</span><span class="sxs-lookup"><span data-stu-id="2a973-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="2a973-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="2a973-115">-MetricTriggerType</span></span>
<span data-ttu-id="2a973-116">公制觸發類型</span><span class="sxs-lookup"><span data-stu-id="2a973-116">The metric trigger type</span></span>

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

### <span data-ttu-id="2a973-117">-閾值</span><span class="sxs-lookup"><span data-stu-id="2a973-117">-Threshold</span></span>
<span data-ttu-id="2a973-118">[公制閾值] 值</span><span class="sxs-lookup"><span data-stu-id="2a973-118">The metric threshold value</span></span>

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

### <span data-ttu-id="2a973-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="2a973-119">-ThresholdOperator</span></span>
<span data-ttu-id="2a973-120">公制閾值運算子： GreaterThan、小於、等於</span><span class="sxs-lookup"><span data-stu-id="2a973-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="2a973-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a973-121">CommonParameters</span></span>
<span data-ttu-id="2a973-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a973-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a973-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a973-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a973-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2a973-124">INPUTS</span></span>

### <span data-ttu-id="2a973-125">所有</span><span class="sxs-lookup"><span data-stu-id="2a973-125">None</span></span>

## <span data-ttu-id="2a973-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2a973-126">OUTPUTS</span></span>

### <span data-ttu-id="2a973-127">PSScheduledQueryRuleLogMetricTrigger 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="2a973-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="2a973-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2a973-128">NOTES</span></span>

## <span data-ttu-id="2a973-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a973-129">RELATED LINKS</span></span>
