---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: d96ccfb2160d7121ffda4802a0fd8afa43ea4589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910922"
---
# <span data-ttu-id="fe041-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="fe041-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="fe041-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fe041-102">SYNOPSIS</span></span>
<span data-ttu-id="fe041-103">建立排程專案。</span><span class="sxs-lookup"><span data-stu-id="fe041-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="fe041-104">語法</span><span class="sxs-lookup"><span data-stu-id="fe041-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe041-105">描述</span><span class="sxs-lookup"><span data-stu-id="fe041-105">DESCRIPTION</span></span>
<span data-ttu-id="fe041-106">**New-AzRedisCacheScheduleEntry Cmdlet** 會建立 **PSScheduleEntry** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe041-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="fe041-107">Azure Redis Cache 修補程式排程 Cmdlet ，例如 New-AzRedisCachePatchSchedule Cmdlet，需要排程專案物件。</span><span class="sxs-lookup"><span data-stu-id="fe041-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="fe041-108">例子</span><span class="sxs-lookup"><span data-stu-id="fe041-108">EXAMPLES</span></span>

### <span data-ttu-id="fe041-109">範例 1：建立週末排程專案</span><span class="sxs-lookup"><span data-stu-id="fe041-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="fe041-110">此命令會建立 **一個 PSScheduleEntry** 物件，代表具有指定開始時間和視窗的週末排程。</span><span class="sxs-lookup"><span data-stu-id="fe041-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="fe041-111">參數</span><span class="sxs-lookup"><span data-stu-id="fe041-111">PARAMETERS</span></span>

### <span data-ttu-id="fe041-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="fe041-112">-DayOfWeek</span></span>
<span data-ttu-id="fe041-113">指定排程專案一周中的日期。</span><span class="sxs-lookup"><span data-stu-id="fe041-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="fe041-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe041-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe041-115">每天</span><span class="sxs-lookup"><span data-stu-id="fe041-115">Everyday</span></span> 
- <span data-ttu-id="fe041-116">週末</span><span class="sxs-lookup"><span data-stu-id="fe041-116">Weekend</span></span> 
- <span data-ttu-id="fe041-117">星期一</span><span class="sxs-lookup"><span data-stu-id="fe041-117">Monday</span></span> 
- <span data-ttu-id="fe041-118">星期二</span><span class="sxs-lookup"><span data-stu-id="fe041-118">Tuesday</span></span> 
- <span data-ttu-id="fe041-119">星期三</span><span class="sxs-lookup"><span data-stu-id="fe041-119">Wednesday</span></span> 
- <span data-ttu-id="fe041-120">星期四</span><span class="sxs-lookup"><span data-stu-id="fe041-120">Thursday</span></span> 
- <span data-ttu-id="fe041-121">星期五</span><span class="sxs-lookup"><span data-stu-id="fe041-121">Friday</span></span> 
- <span data-ttu-id="fe041-122">星期六</span><span class="sxs-lookup"><span data-stu-id="fe041-122">Saturday</span></span> 
- <span data-ttu-id="fe041-123">星期天</span><span class="sxs-lookup"><span data-stu-id="fe041-123">Sunday</span></span>

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

### <span data-ttu-id="fe041-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe041-124">-DefaultProfile</span></span>
<span data-ttu-id="fe041-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe041-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe041-126">-維護視窗</span><span class="sxs-lookup"><span data-stu-id="fe041-126">-MaintenanceWindow</span></span>
<span data-ttu-id="fe041-127">指定允許更新的時段。</span><span class="sxs-lookup"><span data-stu-id="fe041-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="fe041-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="fe041-128">-StartHourUtc</span></span>
<span data-ttu-id="fe041-129">指定排程開始時的一小時。</span><span class="sxs-lookup"><span data-stu-id="fe041-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="fe041-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe041-130">CommonParameters</span></span>
<span data-ttu-id="fe041-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fe041-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe041-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fe041-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe041-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fe041-133">INPUTS</span></span>

### <span data-ttu-id="fe041-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fe041-134">System.String</span></span>

### <span data-ttu-id="fe041-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fe041-135">System.Int32</span></span>

### <span data-ttu-id="fe041-136">System.Nullable'1[[System.TimeSpan， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe041-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fe041-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fe041-137">OUTPUTS</span></span>

### <span data-ttu-id="fe041-138">Microsoft.Azure.Commands.RedisCache.models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="fe041-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="fe041-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fe041-139">NOTES</span></span>
* <span data-ttu-id="fe041-140">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="fe041-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="fe041-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe041-141">RELATED LINKS</span></span>

[<span data-ttu-id="fe041-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fe041-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="fe041-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fe041-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="fe041-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fe041-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


