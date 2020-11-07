---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966970"
---
# <span data-ttu-id="01fdb-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="01fdb-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="01fdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="01fdb-103">建立備份排程更新設定物件。</span><span class="sxs-lookup"><span data-stu-id="01fdb-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="01fdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="01fdb-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01fdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="01fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="01fdb-106">**新的-AzureStorSimpleDeviceBackupScheduleUpdateConfig** Cmdlet 會建立 **BackupScheduleUpdateRequest** 設定物件。</span><span class="sxs-lookup"><span data-stu-id="01fdb-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="01fdb-107">使用此設定物件來使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet 來更新備份原則。</span><span class="sxs-lookup"><span data-stu-id="01fdb-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="01fdb-108">示例</span><span class="sxs-lookup"><span data-stu-id="01fdb-108">EXAMPLES</span></span>

### <span data-ttu-id="01fdb-109">範例1：建立排程更新要求</span><span class="sxs-lookup"><span data-stu-id="01fdb-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="01fdb-110">這個命令會為具有指定識別碼的排程建立備份排程更新要求。</span><span class="sxs-lookup"><span data-stu-id="01fdb-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="01fdb-111">要求是將每小時產生一個雲端快照備份。</span><span class="sxs-lookup"><span data-stu-id="01fdb-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="01fdb-112">備份會保留50天。</span><span class="sxs-lookup"><span data-stu-id="01fdb-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="01fdb-113">此排程是從預設時間啟用，也就是目前的時間。</span><span class="sxs-lookup"><span data-stu-id="01fdb-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="01fdb-114">參數</span><span class="sxs-lookup"><span data-stu-id="01fdb-114">PARAMETERS</span></span>

### <span data-ttu-id="01fdb-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="01fdb-115">-BackupType</span></span>
<span data-ttu-id="01fdb-116">指定備份類型。</span><span class="sxs-lookup"><span data-stu-id="01fdb-116">Specifies the backup type.</span></span>
<span data-ttu-id="01fdb-117">有效值為： LocalSnapshot 和 CloudSnapshot。</span><span class="sxs-lookup"><span data-stu-id="01fdb-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="01fdb-118">-Enabled</span></span>
<span data-ttu-id="01fdb-119">指出是否要啟用備份排程。</span><span class="sxs-lookup"><span data-stu-id="01fdb-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="01fdb-120">-Id</span></span>
<span data-ttu-id="01fdb-121">指定要更新之備份排程的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="01fdb-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="01fdb-122">-Profile</span></span>
<span data-ttu-id="01fdb-123">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="01fdb-123">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="01fdb-124">-RecurrenceType</span></span>
<span data-ttu-id="01fdb-125">指定此備份排程的週期類型。</span><span class="sxs-lookup"><span data-stu-id="01fdb-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="01fdb-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="01fdb-126">Valid values are:</span></span> 

- <span data-ttu-id="01fdb-127">持續</span><span class="sxs-lookup"><span data-stu-id="01fdb-127">Minutes</span></span>
- <span data-ttu-id="01fdb-128">工資</span><span class="sxs-lookup"><span data-stu-id="01fdb-128">Hourly</span></span>
- <span data-ttu-id="01fdb-129">日常</span><span class="sxs-lookup"><span data-stu-id="01fdb-129">Daily</span></span>
- <span data-ttu-id="01fdb-130">周更新</span><span class="sxs-lookup"><span data-stu-id="01fdb-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="01fdb-131">-RecurrenceValue</span></span>
<span data-ttu-id="01fdb-132">指定備份的頻率。</span><span class="sxs-lookup"><span data-stu-id="01fdb-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="01fdb-133">這個參數使用 *RecurrenceType* 參數所指定的單位。</span><span class="sxs-lookup"><span data-stu-id="01fdb-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="01fdb-134">-RetentionCount</span></span>
<span data-ttu-id="01fdb-135">指定保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="01fdb-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="01fdb-136">-StartFromDateTime</span></span>
<span data-ttu-id="01fdb-137">指定開始進行備份的日期。</span><span class="sxs-lookup"><span data-stu-id="01fdb-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="01fdb-138">預設值是目前的時間。</span><span class="sxs-lookup"><span data-stu-id="01fdb-138">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fdb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fdb-139">CommonParameters</span></span>
<span data-ttu-id="01fdb-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01fdb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fdb-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01fdb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fdb-142">輸入</span><span class="sxs-lookup"><span data-stu-id="01fdb-142">INPUTS</span></span>

### <span data-ttu-id="01fdb-143">所有</span><span class="sxs-lookup"><span data-stu-id="01fdb-143">None</span></span>

## <span data-ttu-id="01fdb-144">輸出</span><span class="sxs-lookup"><span data-stu-id="01fdb-144">OUTPUTS</span></span>

### <span data-ttu-id="01fdb-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="01fdb-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="01fdb-146">這個 Cmdlet 會傳回 **BackupScheduleUpdateRequest** 物件，其中包含更新備份排程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01fdb-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="01fdb-147">筆記</span><span class="sxs-lookup"><span data-stu-id="01fdb-147">NOTES</span></span>

## <span data-ttu-id="01fdb-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="01fdb-148">RELATED LINKS</span></span>

[<span data-ttu-id="01fdb-149">新-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="01fdb-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="01fdb-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="01fdb-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


