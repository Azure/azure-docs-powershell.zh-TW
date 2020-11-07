---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790457"
---
# <span data-ttu-id="4ff7f-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4ff7f-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4ff7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ff7f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff7f-103">建立 [警示動作] 類型的物件</span><span class="sxs-lookup"><span data-stu-id="4ff7f-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="4ff7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ff7f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ff7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ff7f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff7f-106">建立 [警示動作] 類型的物件這個物件將會傳遞到建立記錄提醒規則的命令</span><span class="sxs-lookup"><span data-stu-id="4ff7f-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="4ff7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ff7f-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff7f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ff7f-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="4ff7f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ff7f-109">PARAMETERS</span></span>

### <span data-ttu-id="4ff7f-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="4ff7f-110">-AznsAction</span></span>
<span data-ttu-id="4ff7f-111">AzNS 動作詳細資料</span><span class="sxs-lookup"><span data-stu-id="4ff7f-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff7f-112">-DefaultProfile</span></span>
<span data-ttu-id="4ff7f-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ff7f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ff7f-114">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="4ff7f-114">-Severity</span></span>
<span data-ttu-id="4ff7f-115">此提醒的嚴重性</span><span class="sxs-lookup"><span data-stu-id="4ff7f-115">The severity for this alert</span></span>

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

### <span data-ttu-id="4ff7f-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="4ff7f-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="4ff7f-117">應如何限制提醒的持續時間（分鐘）</span><span class="sxs-lookup"><span data-stu-id="4ff7f-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff7f-118">-觸發程式</span><span class="sxs-lookup"><span data-stu-id="4ff7f-118">-Trigger</span></span>
<span data-ttu-id="4ff7f-119">警示觸發條件</span><span class="sxs-lookup"><span data-stu-id="4ff7f-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff7f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff7f-120">CommonParameters</span></span>
<span data-ttu-id="4ff7f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ff7f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff7f-122">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ff7f-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff7f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4ff7f-123">INPUTS</span></span>

### <span data-ttu-id="4ff7f-124">所有</span><span class="sxs-lookup"><span data-stu-id="4ff7f-124">None</span></span>

## <span data-ttu-id="4ff7f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4ff7f-125">OUTPUTS</span></span>

### <span data-ttu-id="4ff7f-126">PSScheduledQueryRuleAlertingAction 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="4ff7f-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4ff7f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4ff7f-127">NOTES</span></span>

## <span data-ttu-id="4ff7f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ff7f-128">RELATED LINKS</span></span>
