---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970441"
---
# <span data-ttu-id="b6900-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b6900-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="b6900-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6900-102">SYNOPSIS</span></span>
<span data-ttu-id="b6900-103">建立排程類型的物件</span><span class="sxs-lookup"><span data-stu-id="b6900-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="b6900-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6900-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6900-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6900-105">DESCRIPTION</span></span>
<span data-ttu-id="b6900-106">建立 [排程] 類型的物件。</span><span class="sxs-lookup"><span data-stu-id="b6900-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="b6900-107">這個物件會傳遞到建立記錄提醒規則的命令。</span><span class="sxs-lookup"><span data-stu-id="b6900-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="b6900-108">示例</span><span class="sxs-lookup"><span data-stu-id="b6900-108">EXAMPLES</span></span>

### <span data-ttu-id="b6900-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b6900-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="b6900-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6900-110">PARAMETERS</span></span>

### <span data-ttu-id="b6900-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6900-111">-DefaultProfile</span></span>
<span data-ttu-id="b6900-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6900-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6900-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6900-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="b6900-114">警報頻率</span><span class="sxs-lookup"><span data-stu-id="b6900-114">The alert frequency</span></span>

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

### <span data-ttu-id="b6900-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6900-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="b6900-116">[警示時間] 視窗</span><span class="sxs-lookup"><span data-stu-id="b6900-116">The alert time window</span></span>

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

### <span data-ttu-id="b6900-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6900-117">CommonParameters</span></span>
<span data-ttu-id="b6900-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6900-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6900-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6900-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6900-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b6900-120">INPUTS</span></span>

### <span data-ttu-id="b6900-121">所有</span><span class="sxs-lookup"><span data-stu-id="b6900-121">None</span></span>

## <span data-ttu-id="b6900-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b6900-122">OUTPUTS</span></span>

### <span data-ttu-id="b6900-123">PSScheduledQueryRuleSchedule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="b6900-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="b6900-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b6900-124">NOTES</span></span>

## <span data-ttu-id="b6900-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6900-125">RELATED LINKS</span></span>
