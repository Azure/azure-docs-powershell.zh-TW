---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141914"
---
# <span data-ttu-id="db123-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="db123-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="db123-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db123-102">SYNOPSIS</span></span>
<span data-ttu-id="db123-103">建立排程專案。</span><span class="sxs-lookup"><span data-stu-id="db123-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="db123-104">句法</span><span class="sxs-lookup"><span data-stu-id="db123-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db123-105">說明</span><span class="sxs-lookup"><span data-stu-id="db123-105">DESCRIPTION</span></span>
<span data-ttu-id="db123-106">**新的-AzRedisCacheScheduleEntry** Cmdlet 會建立 **PSScheduleEntry** 物件。</span><span class="sxs-lookup"><span data-stu-id="db123-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="db123-107">Azure Redis Cache 修補程式排程 Cmdlet （例如 New-AzRedisCachePatchSchedule Cmdlet）需要排程專案物件。</span><span class="sxs-lookup"><span data-stu-id="db123-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="db123-108">示例</span><span class="sxs-lookup"><span data-stu-id="db123-108">EXAMPLES</span></span>

### <span data-ttu-id="db123-109">範例1：建立週末的排程專案</span><span class="sxs-lookup"><span data-stu-id="db123-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="db123-110">這個命令會建立一個代表有指定開始時間和視窗之週末排程的 **PSScheduleEntry** 物件。</span><span class="sxs-lookup"><span data-stu-id="db123-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="db123-111">參數</span><span class="sxs-lookup"><span data-stu-id="db123-111">PARAMETERS</span></span>

### <span data-ttu-id="db123-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="db123-112">-DayOfWeek</span></span>
<span data-ttu-id="db123-113">指定 [排程] 專案在周中的日期。</span><span class="sxs-lookup"><span data-stu-id="db123-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="db123-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="db123-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db123-115">生活</span><span class="sxs-lookup"><span data-stu-id="db123-115">Everyday</span></span> 
- <span data-ttu-id="db123-116">版</span><span class="sxs-lookup"><span data-stu-id="db123-116">Weekend</span></span> 
- <span data-ttu-id="db123-117">從</span><span class="sxs-lookup"><span data-stu-id="db123-117">Monday</span></span> 
- <span data-ttu-id="db123-118">星期二</span><span class="sxs-lookup"><span data-stu-id="db123-118">Tuesday</span></span> 
- <span data-ttu-id="db123-119">星期三</span><span class="sxs-lookup"><span data-stu-id="db123-119">Wednesday</span></span> 
- <span data-ttu-id="db123-120">星期四</span><span class="sxs-lookup"><span data-stu-id="db123-120">Thursday</span></span> 
- <span data-ttu-id="db123-121">日</span><span class="sxs-lookup"><span data-stu-id="db123-121">Friday</span></span> 
- <span data-ttu-id="db123-122">星期六</span><span class="sxs-lookup"><span data-stu-id="db123-122">Saturday</span></span> 
- <span data-ttu-id="db123-123">日</span><span class="sxs-lookup"><span data-stu-id="db123-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db123-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db123-124">-DefaultProfile</span></span>
<span data-ttu-id="db123-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db123-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db123-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="db123-126">-MaintenanceWindow</span></span>
<span data-ttu-id="db123-127">指定更新所允許的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="db123-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db123-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="db123-128">-StartHourUtc</span></span>
<span data-ttu-id="db123-129">指定排程開始日的一個小時。</span><span class="sxs-lookup"><span data-stu-id="db123-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db123-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db123-130">CommonParameters</span></span>
<span data-ttu-id="db123-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db123-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db123-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db123-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db123-133">輸入</span><span class="sxs-lookup"><span data-stu-id="db123-133">INPUTS</span></span>

### <span data-ttu-id="db123-134">System.object</span><span class="sxs-lookup"><span data-stu-id="db123-134">System.String</span></span>

### <span data-ttu-id="db123-135">System.object</span><span class="sxs-lookup"><span data-stu-id="db123-135">System.Int32</span></span>

### <span data-ttu-id="db123-136">CoreLib "1 [System. Timespan.zero，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db123-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="db123-137">輸出</span><span class="sxs-lookup"><span data-stu-id="db123-137">OUTPUTS</span></span>

### <span data-ttu-id="db123-138">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="db123-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="db123-139">筆記</span><span class="sxs-lookup"><span data-stu-id="db123-139">NOTES</span></span>
* <span data-ttu-id="db123-140">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="db123-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="db123-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="db123-141">RELATED LINKS</span></span>

[<span data-ttu-id="db123-142">AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="db123-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="db123-143">新-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="db123-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="db123-144">移除-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="db123-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


