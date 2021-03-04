---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904374"
---
# <span data-ttu-id="9a6c1-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9a6c1-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9a6c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6c1-103">建立類型為警示動作的物件</span><span class="sxs-lookup"><span data-stu-id="9a6c1-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="9a6c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a6c1-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a6c1-105">描述</span><span class="sxs-lookup"><span data-stu-id="9a6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6c1-106">建立類型為警示動作的物件 這個物件會傳遞至建立記錄提醒規則的命令</span><span class="sxs-lookup"><span data-stu-id="9a6c1-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="9a6c1-107">例子</span><span class="sxs-lookup"><span data-stu-id="9a6c1-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6c1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9a6c1-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="9a6c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="9a6c1-109">PARAMETERS</span></span>

### <span data-ttu-id="9a6c1-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="9a6c1-110">-AznsAction</span></span>
<span data-ttu-id="9a6c1-111">AzNS 動作詳細資料</span><span class="sxs-lookup"><span data-stu-id="9a6c1-111">The AzNS action details</span></span>

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

### <span data-ttu-id="9a6c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6c1-112">-DefaultProfile</span></span>
<span data-ttu-id="9a6c1-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a6c1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a6c1-114">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="9a6c1-114">-Severity</span></span>
<span data-ttu-id="9a6c1-115">此警示的嚴重性</span><span class="sxs-lookup"><span data-stu-id="9a6c1-115">The severity for this alert</span></span>

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

### <span data-ttu-id="9a6c1-116">-節流LingInMinutes</span><span class="sxs-lookup"><span data-stu-id="9a6c1-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="9a6c1-117">應該節流警示的持續時間 ，以分鐘為分</span><span class="sxs-lookup"><span data-stu-id="9a6c1-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="9a6c1-118">-觸發</span><span class="sxs-lookup"><span data-stu-id="9a6c1-118">-Trigger</span></span>
<span data-ttu-id="9a6c1-119">警示觸發條件</span><span class="sxs-lookup"><span data-stu-id="9a6c1-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="9a6c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6c1-120">CommonParameters</span></span>
<span data-ttu-id="9a6c1-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a6c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6c1-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a6c1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6c1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9a6c1-123">INPUTS</span></span>

### <span data-ttu-id="9a6c1-124">沒有</span><span class="sxs-lookup"><span data-stu-id="9a6c1-124">None</span></span>

## <span data-ttu-id="9a6c1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9a6c1-125">OUTPUTS</span></span>

### <span data-ttu-id="9a6c1-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9a6c1-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9a6c1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9a6c1-127">NOTES</span></span>

## <span data-ttu-id="9a6c1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a6c1-128">RELATED LINKS</span></span>
