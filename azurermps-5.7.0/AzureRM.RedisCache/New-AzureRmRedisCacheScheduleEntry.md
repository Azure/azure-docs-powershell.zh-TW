---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623458"
---
# <span data-ttu-id="47353-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="47353-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="47353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47353-102">SYNOPSIS</span></span>
<span data-ttu-id="47353-103">建立排程專案。</span><span class="sxs-lookup"><span data-stu-id="47353-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47353-104">句法</span><span class="sxs-lookup"><span data-stu-id="47353-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47353-105">說明</span><span class="sxs-lookup"><span data-stu-id="47353-105">DESCRIPTION</span></span>
<span data-ttu-id="47353-106">**新的-AzureRmRedisCacheScheduleEntry** Cmdlet 會建立 **PSScheduleEntry** 物件。</span><span class="sxs-lookup"><span data-stu-id="47353-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="47353-107">Azure Redis Cache 修補程式排程 Cmdlet （例如 New-AzureRmRedisCachePatchSchedule Cmdlet）需要排程專案物件。</span><span class="sxs-lookup"><span data-stu-id="47353-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="47353-108">示例</span><span class="sxs-lookup"><span data-stu-id="47353-108">EXAMPLES</span></span>

### <span data-ttu-id="47353-109">範例1：建立週末的排程專案</span><span class="sxs-lookup"><span data-stu-id="47353-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="47353-110">這個命令會建立一個代表有指定開始時間和視窗之週末排程的 **PSScheduleEntry** 物件。</span><span class="sxs-lookup"><span data-stu-id="47353-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="47353-111">參數</span><span class="sxs-lookup"><span data-stu-id="47353-111">PARAMETERS</span></span>

### <span data-ttu-id="47353-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="47353-112">-DayOfWeek</span></span>
<span data-ttu-id="47353-113">指定 [排程] 專案在周中的日期。</span><span class="sxs-lookup"><span data-stu-id="47353-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="47353-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="47353-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47353-115">生活</span><span class="sxs-lookup"><span data-stu-id="47353-115">Everyday</span></span> 
- <span data-ttu-id="47353-116">版</span><span class="sxs-lookup"><span data-stu-id="47353-116">Weekend</span></span> 
- <span data-ttu-id="47353-117">從</span><span class="sxs-lookup"><span data-stu-id="47353-117">Monday</span></span> 
- <span data-ttu-id="47353-118">星期二</span><span class="sxs-lookup"><span data-stu-id="47353-118">Tuesday</span></span> 
- <span data-ttu-id="47353-119">星期三</span><span class="sxs-lookup"><span data-stu-id="47353-119">Wednesday</span></span> 
- <span data-ttu-id="47353-120">星期四</span><span class="sxs-lookup"><span data-stu-id="47353-120">Thursday</span></span> 
- <span data-ttu-id="47353-121">日</span><span class="sxs-lookup"><span data-stu-id="47353-121">Friday</span></span> 
- <span data-ttu-id="47353-122">星期六</span><span class="sxs-lookup"><span data-stu-id="47353-122">Saturday</span></span> 
- <span data-ttu-id="47353-123">日</span><span class="sxs-lookup"><span data-stu-id="47353-123">Sunday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47353-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47353-124">-DefaultProfile</span></span>
<span data-ttu-id="47353-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47353-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47353-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="47353-126">-MaintenanceWindow</span></span>
<span data-ttu-id="47353-127">指定更新所允許的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="47353-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47353-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="47353-128">-StartHourUtc</span></span>
<span data-ttu-id="47353-129">指定排程開始日的一個小時。</span><span class="sxs-lookup"><span data-stu-id="47353-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47353-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47353-130">CommonParameters</span></span>
<span data-ttu-id="47353-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47353-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47353-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47353-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47353-133">輸入</span><span class="sxs-lookup"><span data-stu-id="47353-133">INPUTS</span></span>

### <span data-ttu-id="47353-134">所有</span><span class="sxs-lookup"><span data-stu-id="47353-134">None</span></span>
<span data-ttu-id="47353-135">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47353-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="47353-136">輸出</span><span class="sxs-lookup"><span data-stu-id="47353-136">OUTPUTS</span></span>

### <span data-ttu-id="47353-137">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="47353-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="47353-138">這個 Cmdlet 會傳回排程專案物件。</span><span class="sxs-lookup"><span data-stu-id="47353-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="47353-139">筆記</span><span class="sxs-lookup"><span data-stu-id="47353-139">NOTES</span></span>
* <span data-ttu-id="47353-140">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="47353-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="47353-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="47353-141">RELATED LINKS</span></span>

[<span data-ttu-id="47353-142">AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="47353-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="47353-143">新-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="47353-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="47353-144">移除-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="47353-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


