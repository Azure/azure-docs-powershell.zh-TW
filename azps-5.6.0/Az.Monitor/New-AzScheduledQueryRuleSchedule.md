---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908526"
---
# <span data-ttu-id="e84ad-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e84ad-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e84ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e84ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e84ad-103">建立排程類型的物件</span><span class="sxs-lookup"><span data-stu-id="e84ad-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="e84ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="e84ad-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e84ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="e84ad-105">DESCRIPTION</span></span>
<span data-ttu-id="e84ad-106">建立類型為 Schedule 的物件。</span><span class="sxs-lookup"><span data-stu-id="e84ad-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="e84ad-107">這個物件會傳遞至建立記錄提醒規則的命令。</span><span class="sxs-lookup"><span data-stu-id="e84ad-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="e84ad-108">例子</span><span class="sxs-lookup"><span data-stu-id="e84ad-108">EXAMPLES</span></span>

### <span data-ttu-id="e84ad-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e84ad-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="e84ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="e84ad-110">PARAMETERS</span></span>

### <span data-ttu-id="e84ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84ad-111">-DefaultProfile</span></span>
<span data-ttu-id="e84ad-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e84ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e84ad-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e84ad-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="e84ad-114">警示頻率</span><span class="sxs-lookup"><span data-stu-id="e84ad-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e84ad-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="e84ad-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="e84ad-116">警示時間視窗</span><span class="sxs-lookup"><span data-stu-id="e84ad-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e84ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84ad-117">CommonParameters</span></span>
<span data-ttu-id="e84ad-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e84ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84ad-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e84ad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84ad-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e84ad-120">INPUTS</span></span>

### <span data-ttu-id="e84ad-121">沒有</span><span class="sxs-lookup"><span data-stu-id="e84ad-121">None</span></span>

## <span data-ttu-id="e84ad-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e84ad-122">OUTPUTS</span></span>

### <span data-ttu-id="e84ad-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e84ad-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e84ad-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e84ad-124">NOTES</span></span>

## <span data-ttu-id="e84ad-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e84ad-125">RELATED LINKS</span></span>
