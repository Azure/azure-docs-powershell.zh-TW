---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 1fcafb0eb9e4bd1cfb0cf5b3f5ec770c35ea92d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913506"
---
# <span data-ttu-id="d6417-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d6417-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="d6417-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6417-102">SYNOPSIS</span></span>
<span data-ttu-id="d6417-103">建立類型為觸發條件的物件</span><span class="sxs-lookup"><span data-stu-id="d6417-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="d6417-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6417-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6417-105">描述</span><span class="sxs-lookup"><span data-stu-id="d6417-105">DESCRIPTION</span></span>
<span data-ttu-id="d6417-106">建立類型為觸發條件的物件。</span><span class="sxs-lookup"><span data-stu-id="d6417-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="d6417-107">這個物件會傳遞至建立警示動作物件的命令</span><span class="sxs-lookup"><span data-stu-id="d6417-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="d6417-108">例子</span><span class="sxs-lookup"><span data-stu-id="d6417-108">EXAMPLES</span></span>

### <span data-ttu-id="d6417-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6417-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="d6417-110">參數</span><span class="sxs-lookup"><span data-stu-id="d6417-110">PARAMETERS</span></span>

### <span data-ttu-id="d6417-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6417-111">-DefaultProfile</span></span>
<span data-ttu-id="d6417-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6417-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6417-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d6417-113">-MetricTrigger</span></span>
<span data-ttu-id="d6417-114">公制查詢規則的觸發條件</span><span class="sxs-lookup"><span data-stu-id="d6417-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6417-115">-閾值</span><span class="sxs-lookup"><span data-stu-id="d6417-115">-Threshold</span></span>
<span data-ttu-id="d6417-116">警示獲得警示的臨界值上方</span><span class="sxs-lookup"><span data-stu-id="d6417-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="d6417-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="d6417-117">-ThresholdOperator</span></span>
<span data-ttu-id="d6417-118">臨界值運算子：Greater用、Less用或等號</span><span class="sxs-lookup"><span data-stu-id="d6417-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="d6417-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6417-119">CommonParameters</span></span>
<span data-ttu-id="d6417-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6417-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6417-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6417-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6417-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d6417-122">INPUTS</span></span>

### <span data-ttu-id="d6417-123">沒有</span><span class="sxs-lookup"><span data-stu-id="d6417-123">None</span></span>

## <span data-ttu-id="d6417-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d6417-124">OUTPUTS</span></span>

### <span data-ttu-id="d6417-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d6417-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="d6417-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d6417-126">NOTES</span></span>

## <span data-ttu-id="d6417-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6417-127">RELATED LINKS</span></span>
