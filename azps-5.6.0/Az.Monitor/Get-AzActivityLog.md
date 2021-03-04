---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908973"
---
# <span data-ttu-id="23edf-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="23edf-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="23edf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23edf-102">SYNOPSIS</span></span>
<span data-ttu-id="23edf-103">取回活動記錄事件。</span><span class="sxs-lookup"><span data-stu-id="23edf-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="23edf-104">語法</span><span class="sxs-lookup"><span data-stu-id="23edf-104">SYNTAX</span></span>

### <span data-ttu-id="23edf-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="23edf-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23edf-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="23edf-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23edf-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23edf-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23edf-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="23edf-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23edf-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="23edf-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23edf-110">描述</span><span class="sxs-lookup"><span data-stu-id="23edf-110">DESCRIPTION</span></span>
<span data-ttu-id="23edf-111">Cmdlet Get-AzActivityLog活動記錄事件。</span><span class="sxs-lookup"><span data-stu-id="23edf-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="23edf-112">事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。</span><span class="sxs-lookup"><span data-stu-id="23edf-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="23edf-113">例子</span><span class="sxs-lookup"><span data-stu-id="23edf-113">EXAMPLES</span></span>

### <span data-ttu-id="23edf-114">範例 1：根據訂閱識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzActivityLog
```

<span data-ttu-id="23edf-115">此命令會列出最多 1000 個與使用者訂閱識別碼相關聯的事件，這些事件從目前日期/時間起 7 天發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-116">範例 2：根據訂閱識別碼取得事件記錄，事件數目上限</span><span class="sxs-lookup"><span data-stu-id="23edf-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="23edf-117">此命令會列出最多 100 個與使用者訂閱識別碼相關聯的事件，這些事件從目前日期/時間起 7 天后發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-118">範例 3：取得具有開始時間之訂閱識別碼的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="23edf-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="23edf-119">此命令會列出最多與 2017-06-01T10：30 當地時間發生或之後之使用者訂閱識別碼相關聯的 1000 個事件，如果日期/時間不大於目前日期/時間 90 天。</span><span class="sxs-lookup"><span data-stu-id="23edf-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-120">範例 4：取得具有開始時間和結束時間之訂閱識別碼的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="23edf-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="23edf-121">此命令會列出最多 1000 個與 2017-04-01T10：30 當地時間，以及 2017-04-14T11：30 當地時間之前發生之使用者訂閱識別碼相關聯的事件，如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間。</span><span class="sxs-lookup"><span data-stu-id="23edf-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="23edf-122">範例 5：根據相關識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="23edf-123">此命令會列出最多 1000 個與指定相關識別碼相關聯的事件，這些事件從目前日期/時間起 7 天發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="23edf-124">**注意**：這通常只有一個事件。</span><span class="sxs-lookup"><span data-stu-id="23edf-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="23edf-125">範例 6：以事件數目上限的關聯識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="23edf-126">此命令會列出最多 100 個與指定相關識別碼相關聯的事件，這些事件自目前日期/時間起 7 天之後發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="23edf-127">**注意**：這通常只有一個事件。</span><span class="sxs-lookup"><span data-stu-id="23edf-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="23edf-128">範例 7：根據相關識別碼和開始時間取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="23edf-129">此命令會列出最多與 2017-05-22T04：30：00 當地時間發生或之後所指定相關識別碼相關聯的 1000 個事件 ，如果開始時間不大於目前日期/時間 90 天。</span><span class="sxs-lookup"><span data-stu-id="23edf-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="23edf-130">**注意**：這通常只有一個事件。</span><span class="sxs-lookup"><span data-stu-id="23edf-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="23edf-131">範例 8：根據相關 ID 取得事件記錄與開始時間和結束時間</span><span class="sxs-lookup"><span data-stu-id="23edf-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="23edf-132">此命令會列出與 2017-04-15T04：30 當地時間當天或之後所發生之指定相關識別碼相關聯的最多 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天 ，即保留期間，則于 2017-04-25T12：30 當地時間之前發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="23edf-133">範例 9：取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="23edf-134">此命令會列出最多 1000 個與指定資源群組相關聯的事件，這些事件會從目前日期/時間起 7 天發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-135">範例 10：取得事件數上限的資源群組事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="23edf-136">此命令會列出最多 100 個與指定資源群組相關聯的事件，這些事件會從目前日期/時間起 7 天發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-137">範例 11：根據開始時間取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="23edf-138">此命令會列出在 2017-05-22T04：30：00 當地時間當天或之後發生與指定資源群組相關聯的最多 1000 個事件，如果開始時間不大於目前日期/時間 90 天。</span><span class="sxs-lookup"><span data-stu-id="23edf-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-139">範例 12：取得具有開始時間和結束時間的資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="23edf-140">此命令會列出最多 1000 個與指定資源群組相關聯的事件，這些事件是在 2017-04-15T04：30 當地時間發生，但如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間，則列于 2017-04-25T12：30 當地時間之前。</span><span class="sxs-lookup"><span data-stu-id="23edf-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="23edf-141">範例 13：根據資源識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="23edf-142">此命令會列出與指定資源識別碼相關聯的最多 1000 個事件，這些事件從目前日期/時間起 7 天后發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-143">範例 14：根據資源識別碼取得事件記錄，事件數目上限</span><span class="sxs-lookup"><span data-stu-id="23edf-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="23edf-144">此命令會列出最多 100 個與指定資源識別碼相關聯的事件，這些事件從目前日期/時間開始 7 天之後發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-145">範例 15：根據資源識別碼取得具有開始時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="23edf-146">此命令會列出最多與 2017-05-22T04：30：00 當地時間發生或之後所指定資源識別碼相關聯的 1000 個事件，如果開始時間不大於目前日期/時間 90 天。</span><span class="sxs-lookup"><span data-stu-id="23edf-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-147">範例 16：根據資源識別碼取得具有開始時間和結束時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="23edf-148">此命令會列出最多與 2017-04-15T04：30 當地時間發生或之後所發生之指定資源識別碼相關聯的 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天，即保留期間，則列于 2017-04-25T12：30 當地時間之前。</span><span class="sxs-lookup"><span data-stu-id="23edf-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="23edf-149">範例 17：根據資源提供者取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="23edf-150">此命令會列出與指定資源提供者相關聯的最多 1000 個事件，這些事件從目前日期/時間起 7 天后發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-151">範例 18：根據資源提供者取得事件記錄，事件數目上限</span><span class="sxs-lookup"><span data-stu-id="23edf-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="23edf-152">此命令會列出最多 100 個與指定資源提供者相關聯的事件，這些事件從目前日期/時間起 7 天發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-153">範例 19：根據資源提供者取得具有開始時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="23edf-154">此命令會列出在 2017-05-22T04：30：00 當地時間當天或之後發生與指定資源提供者相關聯的最多 1000 個事件，如果開始時間不大於目前日期/時間 90 天。</span><span class="sxs-lookup"><span data-stu-id="23edf-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="23edf-155">範例 20：根據資源提供者取得具有開始時間和結束時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="23edf-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="23edf-156">此命令會列出在 2017-04-15T04：30 當地時間當天或之後，與指定資源提供者相關聯的最多 1000 個事件，但如果整個日期/時間範圍不大於目前日期/時間 90 天 ，即保留期間，則于 2017-04-25T12：30 當地時間之前發生。</span><span class="sxs-lookup"><span data-stu-id="23edf-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="23edf-157">參數</span><span class="sxs-lookup"><span data-stu-id="23edf-157">PARAMETERS</span></span>

### <span data-ttu-id="23edf-158">-本機號碼</span><span class="sxs-lookup"><span data-stu-id="23edf-158">-Caller</span></span>
<span data-ttu-id="23edf-159">要抓取之事件的來電者</span><span class="sxs-lookup"><span data-stu-id="23edf-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="23edf-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="23edf-160">-CorrelationId</span></span>
<span data-ttu-id="23edf-161">The CorrelationId</span><span class="sxs-lookup"><span data-stu-id="23edf-161">The CorrelationId</span></span>

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

### <span data-ttu-id="23edf-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23edf-162">-DefaultProfile</span></span>
<span data-ttu-id="23edf-163">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23edf-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23edf-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="23edf-164">-DetailedOutput</span></span>
<span data-ttu-id="23edf-165">包含所有事件詳細資料 (的 Return 物件預設只會返回某些屬性，例如沒有詳細資料) </span><span class="sxs-lookup"><span data-stu-id="23edf-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="23edf-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="23edf-166">-EndTime</span></span>
<span data-ttu-id="23edf-167">查詢的 EndTime</span><span class="sxs-lookup"><span data-stu-id="23edf-167">The endTime of the query</span></span>

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

### <span data-ttu-id="23edf-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="23edf-168">-MaxRecord</span></span>
<span data-ttu-id="23edf-169">要抓取的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="23edf-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="23edf-170">別名：MaxRecords，MaxEvents</span><span class="sxs-lookup"><span data-stu-id="23edf-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="23edf-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23edf-171">-ResourceGroupName</span></span>
<span data-ttu-id="23edf-172">資源組名</span><span class="sxs-lookup"><span data-stu-id="23edf-172">The resource group name</span></span>

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

### <span data-ttu-id="23edf-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23edf-173">-ResourceId</span></span>
<span data-ttu-id="23edf-174">The ResourceId</span><span class="sxs-lookup"><span data-stu-id="23edf-174">The ResourceId</span></span>

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

### <span data-ttu-id="23edf-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="23edf-175">-ResourceProvider</span></span>
<span data-ttu-id="23edf-176">ResourceProvider 名稱</span><span class="sxs-lookup"><span data-stu-id="23edf-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="23edf-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="23edf-177">-StartTime</span></span>
<span data-ttu-id="23edf-178">查詢的相關資料</span><span class="sxs-lookup"><span data-stu-id="23edf-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="23edf-179">-狀態</span><span class="sxs-lookup"><span data-stu-id="23edf-179">-Status</span></span>
<span data-ttu-id="23edf-180">要抓取的事件狀態</span><span class="sxs-lookup"><span data-stu-id="23edf-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="23edf-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23edf-181">CommonParameters</span></span>
<span data-ttu-id="23edf-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23edf-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23edf-183">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23edf-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23edf-184">輸入</span><span class="sxs-lookup"><span data-stu-id="23edf-184">INPUTS</span></span>

### <span data-ttu-id="23edf-185">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23edf-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="23edf-186">System.String</span><span class="sxs-lookup"><span data-stu-id="23edf-186">System.String</span></span>

### <span data-ttu-id="23edf-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23edf-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="23edf-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="23edf-188">System.Int32</span></span>

## <span data-ttu-id="23edf-189">輸出</span><span class="sxs-lookup"><span data-stu-id="23edf-189">OUTPUTS</span></span>

### <span data-ttu-id="23edf-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="23edf-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="23edf-191">筆記</span><span class="sxs-lookup"><span data-stu-id="23edf-191">NOTES</span></span>

## <span data-ttu-id="23edf-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="23edf-192">RELATED LINKS</span></span>
