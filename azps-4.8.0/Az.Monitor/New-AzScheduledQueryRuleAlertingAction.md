---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127560"
---
# <span data-ttu-id="a092c-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a092c-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="a092c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a092c-102">SYNOPSIS</span></span>
<span data-ttu-id="a092c-103">建立 [警示動作] 類型的物件</span><span class="sxs-lookup"><span data-stu-id="a092c-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="a092c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a092c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a092c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a092c-105">DESCRIPTION</span></span>
<span data-ttu-id="a092c-106">建立 [警示動作] 類型的物件這個物件將會傳遞到建立記錄提醒規則的命令</span><span class="sxs-lookup"><span data-stu-id="a092c-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="a092c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a092c-107">EXAMPLES</span></span>

### <span data-ttu-id="a092c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a092c-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="a092c-109">參數</span><span class="sxs-lookup"><span data-stu-id="a092c-109">PARAMETERS</span></span>

### <span data-ttu-id="a092c-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="a092c-110">-AznsAction</span></span>
<span data-ttu-id="a092c-111">AzNS 動作詳細資料</span><span class="sxs-lookup"><span data-stu-id="a092c-111">The AzNS action details</span></span>

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

### <span data-ttu-id="a092c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a092c-112">-DefaultProfile</span></span>
<span data-ttu-id="a092c-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a092c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a092c-114">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="a092c-114">-Severity</span></span>
<span data-ttu-id="a092c-115">此提醒的嚴重性</span><span class="sxs-lookup"><span data-stu-id="a092c-115">The severity for this alert</span></span>

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

### <span data-ttu-id="a092c-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="a092c-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="a092c-117">應如何限制提醒的持續時間（分鐘）</span><span class="sxs-lookup"><span data-stu-id="a092c-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="a092c-118">-觸發程式</span><span class="sxs-lookup"><span data-stu-id="a092c-118">-Trigger</span></span>
<span data-ttu-id="a092c-119">警示觸發條件</span><span class="sxs-lookup"><span data-stu-id="a092c-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="a092c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a092c-120">CommonParameters</span></span>
<span data-ttu-id="a092c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a092c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a092c-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a092c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a092c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a092c-123">INPUTS</span></span>

### <span data-ttu-id="a092c-124">所有</span><span class="sxs-lookup"><span data-stu-id="a092c-124">None</span></span>

## <span data-ttu-id="a092c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a092c-125">OUTPUTS</span></span>

### <span data-ttu-id="a092c-126">PSScheduledQueryRuleAlertingAction 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a092c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="a092c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a092c-127">NOTES</span></span>

## <span data-ttu-id="a092c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a092c-128">RELATED LINKS</span></span>
