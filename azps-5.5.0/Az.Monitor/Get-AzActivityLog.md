---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132714"
---
# <span data-ttu-id="51b5a-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="51b5a-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="51b5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="51b5a-103">檢索活動記錄事件。</span><span class="sxs-lookup"><span data-stu-id="51b5a-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="51b5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="51b5a-104">SYNTAX</span></span>

### <span data-ttu-id="51b5a-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="51b5a-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51b5a-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51b5a-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51b5a-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51b5a-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b5a-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="51b5a-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51b5a-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="51b5a-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51b5a-110">說明</span><span class="sxs-lookup"><span data-stu-id="51b5a-110">DESCRIPTION</span></span>
<span data-ttu-id="51b5a-111">Get-AzActivityLog Cmdlet 會檢索活動記錄事件。</span><span class="sxs-lookup"><span data-stu-id="51b5a-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="51b5a-112">事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。</span><span class="sxs-lookup"><span data-stu-id="51b5a-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="51b5a-113">示例</span><span class="sxs-lookup"><span data-stu-id="51b5a-113">EXAMPLES</span></span>

### <span data-ttu-id="51b5a-114">範例1：依訂閱識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="51b5a-115">這個命令會列出與使用者訂閱識別碼相關聯的1000事件，這些事件是在目前日期/時間之前的7天內發生。</span><span class="sxs-lookup"><span data-stu-id="51b5a-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-116">範例2：依訂閱識別碼（含最大事件數）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="51b5a-117">這個命令會列出與使用者訂閱識別碼相關聯的100事件，這些事件是在目前日期/時間之前的7天內發生。</span><span class="sxs-lookup"><span data-stu-id="51b5a-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-118">範例3：依訂閱識別碼（含開始時間）取得事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="51b5a-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="51b5a-119">這個命令會列出與在2017年或2017之後所發生的使用者訂閱識別碼相關聯的1000事件（最大01T10：30個當地時間），如果該日期/時間不是從目前日期/時間的90天之前。</span><span class="sxs-lookup"><span data-stu-id="51b5a-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-120">範例4：按照訂閱識別碼，以開始時間和結束時間來取得事件記錄。</span><span class="sxs-lookup"><span data-stu-id="51b5a-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="51b5a-121">這個命令最多可列出與在2017年或2017年之後所發生的使用者訂閱 ID 相關的事件 1000 01T10：30個當地時間，以及2017年-14T11：30（當地時間）如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="51b5a-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="51b5a-122">範例5：依相關識別碼取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="51b5a-123">這個命令會列出與指定的相關識別碼相關聯的1000事件，這些事件會從目前的日期/時間開始，發生7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="51b5a-124">**注意**：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="51b5a-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="51b5a-125">範例6：使用最大事件數的相關識別碼來取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="51b5a-126">這個命令會列出與指定的相關識別碼相關聯的100事件，這些事件會從目前的日期/時間開始，發生7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="51b5a-127">**注意**：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="51b5a-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="51b5a-128">範例7：依相關識別碼和開始時間取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="51b5a-129">這個命令最多可列出與2017年或2017之後所發生的指定相關識別碼相關聯的1000事件，22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。</span><span class="sxs-lookup"><span data-stu-id="51b5a-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="51b5a-130">**注意**：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="51b5a-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="51b5a-131">範例8：依 [開始時間] 和 [結束時間] 的相關識別碼來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="51b5a-132">這個命令會列出與在2017年或2017年15T04：30個當地時間，但在2017年到 04-25T12：30個當地時間為止，如果整個日期/時間範圍不是從目前日期/時間開始的90天內，就會列出與此設定相關聯的1000事件（例如： [保留期間]）。</span><span class="sxs-lookup"><span data-stu-id="51b5a-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="51b5a-133">範例9：取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="51b5a-134">這個命令1000最多可列出與指定資源群組相關聯的事件，這些事件是從目前的日期/時間開始7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-135">範例10：取得含有最大事件數之資源群組的事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="51b5a-136">這個命令會列出與特定資源群組相關聯的100事件，這些事件是從目前的日期/時間開始7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-137">範例11：依開始時間取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="51b5a-138">這個命令會列出與在2017年或之後發生的特定資源群組相關聯的1000事件（最大值），22T04：30：00當地時間（如果開始時間不早于目前日期/時間的90天）。</span><span class="sxs-lookup"><span data-stu-id="51b5a-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-139">範例12：取得具有開始時間和結束時間之資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="51b5a-140">這個命令會列出與在2017年或2017之後所發生的特定資源群組相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="51b5a-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="51b5a-141">範例13：透過資源識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="51b5a-142">這個命令會列出與指定的資源識別碼相關聯的1000事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-143">範例14：以資源識別碼（含最大事件數）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="51b5a-144">這個命令會列出與指定的資源識別碼相關聯的100事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-145">範例15：透過資源識別碼取得開始時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="51b5a-146">這個命令最多可列出與2017年或2017之後所發生的指定資源識別碼相關聯的1000事件（22T04：30：00當地時間），如果開始時間不是從目前日期/時間的90天之前。</span><span class="sxs-lookup"><span data-stu-id="51b5a-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-147">範例16：以資源識別碼（含開始時間和結束時間）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="51b5a-148">這個命令會列出與在2017年或2017年之後所發生的指定資源識別碼相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不是從目前日期/時間的90天之前，即為 [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="51b5a-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="51b5a-149">範例17：透過資源提供者取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="51b5a-150">這個命令會列出與指定資源提供者相關的1000事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-151">範例18：以資源提供者取得最大事件數的事件記錄</span><span class="sxs-lookup"><span data-stu-id="51b5a-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="51b5a-152">這個命令會列出與指定資源提供者相關的100事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="51b5a-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-153">範例19：由資源提供者使用啟動時間來取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="51b5a-154">這個命令會列出與在2017年或之後所發生的指定資源提供者相關聯的1000事件（最多個），22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。</span><span class="sxs-lookup"><span data-stu-id="51b5a-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="51b5a-155">範例20：透過資源提供者取得開始時間和結束時間的事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="51b5a-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="51b5a-156">這個命令會列出與在2017年或2017之後所發生的指定資源提供者所產生的1000事件（15T04：30個當地時間），但在2017年之前的25T12：30個當地時間（如果整個日期/時間範圍不是從目前日期/時間起的90天以內），亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="51b5a-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="51b5a-157">參數</span><span class="sxs-lookup"><span data-stu-id="51b5a-157">PARAMETERS</span></span>

### <span data-ttu-id="51b5a-158">-來電者</span><span class="sxs-lookup"><span data-stu-id="51b5a-158">-Caller</span></span>
<span data-ttu-id="51b5a-159">要提取事件的來電者</span><span class="sxs-lookup"><span data-stu-id="51b5a-159">The caller of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="51b5a-160">-CorrelationId</span></span>
<span data-ttu-id="51b5a-161">CorrelationId</span><span class="sxs-lookup"><span data-stu-id="51b5a-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b5a-162">-DefaultProfile</span></span>
<span data-ttu-id="51b5a-163">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51b5a-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b5a-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="51b5a-164">-DetailedOutput</span></span>
<span data-ttu-id="51b5a-165">傳回包含事件之所有詳細資料的物件 (預設值是只傳回部分屬性，亦即傳回詳細資料) </span><span class="sxs-lookup"><span data-stu-id="51b5a-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="51b5a-166">-EndTime</span></span>
<span data-ttu-id="51b5a-167">查詢的 endTime</span><span class="sxs-lookup"><span data-stu-id="51b5a-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="51b5a-168">-MaxRecord</span></span>
<span data-ttu-id="51b5a-169">要提取的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="51b5a-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="51b5a-170">別名： MaxRecords、MaxEvents</span><span class="sxs-lookup"><span data-stu-id="51b5a-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b5a-171">-ResourceGroupName</span></span>
<span data-ttu-id="51b5a-172">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="51b5a-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b5a-173">-ResourceId</span></span>
<span data-ttu-id="51b5a-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b5a-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="51b5a-175">-ResourceProvider</span></span>
<span data-ttu-id="51b5a-176">ResourceProvider 名稱</span><span class="sxs-lookup"><span data-stu-id="51b5a-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="51b5a-177">-StartTime</span></span>
<span data-ttu-id="51b5a-178">查詢的 correlationId</span><span class="sxs-lookup"><span data-stu-id="51b5a-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-179">-狀態</span><span class="sxs-lookup"><span data-stu-id="51b5a-179">-Status</span></span>
<span data-ttu-id="51b5a-180">要提取事件的狀態</span><span class="sxs-lookup"><span data-stu-id="51b5a-180">The status of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b5a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b5a-181">CommonParameters</span></span>
<span data-ttu-id="51b5a-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51b5a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b5a-183">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="51b5a-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b5a-184">輸入</span><span class="sxs-lookup"><span data-stu-id="51b5a-184">INPUTS</span></span>

### <span data-ttu-id="51b5a-185">System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="51b5a-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="51b5a-186">System.object</span><span class="sxs-lookup"><span data-stu-id="51b5a-186">System.String</span></span>

### <span data-ttu-id="51b5a-187">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="51b5a-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="51b5a-188">System.object</span><span class="sxs-lookup"><span data-stu-id="51b5a-188">System.Int32</span></span>

## <span data-ttu-id="51b5a-189">輸出</span><span class="sxs-lookup"><span data-stu-id="51b5a-189">OUTPUTS</span></span>

### <span data-ttu-id="51b5a-190">PSEventData 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="51b5a-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="51b5a-191">筆記</span><span class="sxs-lookup"><span data-stu-id="51b5a-191">NOTES</span></span>

## <span data-ttu-id="51b5a-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="51b5a-192">RELATED LINKS</span></span>
