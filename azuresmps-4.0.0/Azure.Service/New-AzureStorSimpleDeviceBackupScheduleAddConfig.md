---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966974"
---
# <span data-ttu-id="c05de-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="c05de-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="c05de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c05de-102">SYNOPSIS</span></span>
<span data-ttu-id="c05de-103">建立備份排程設定物件。</span><span class="sxs-lookup"><span data-stu-id="c05de-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="c05de-104">句法</span><span class="sxs-lookup"><span data-stu-id="c05de-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c05de-105">說明</span><span class="sxs-lookup"><span data-stu-id="c05de-105">DESCRIPTION</span></span>
<span data-ttu-id="c05de-106">**新的-AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet 會建立 **BackupScheduleBase** 設定物件。</span><span class="sxs-lookup"><span data-stu-id="c05de-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="c05de-107">使用此設定物件，使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet 來建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="c05de-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="c05de-108">示例</span><span class="sxs-lookup"><span data-stu-id="c05de-108">EXAMPLES</span></span>

### <span data-ttu-id="c05de-109">範例1：建立備份設定物件</span><span class="sxs-lookup"><span data-stu-id="c05de-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="c05de-110">這個命令會建立雲端快照備份的備份排程基底物件。</span><span class="sxs-lookup"><span data-stu-id="c05de-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="c05de-111">每天都會進行備份，備份會保留100天。</span><span class="sxs-lookup"><span data-stu-id="c05de-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="c05de-112">此排程是從預設時間啟用，也就是目前的時間。</span><span class="sxs-lookup"><span data-stu-id="c05de-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="c05de-113">參數</span><span class="sxs-lookup"><span data-stu-id="c05de-113">PARAMETERS</span></span>

### <span data-ttu-id="c05de-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="c05de-114">-BackupType</span></span>
<span data-ttu-id="c05de-115">指定備份類型。</span><span class="sxs-lookup"><span data-stu-id="c05de-115">Specifies the backup type.</span></span>
<span data-ttu-id="c05de-116">有效值為： LocalSnapshot 和 CloudSnapshot。</span><span class="sxs-lookup"><span data-stu-id="c05de-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="c05de-117">-啟用</span><span class="sxs-lookup"><span data-stu-id="c05de-117">-Enabled</span></span>
<span data-ttu-id="c05de-118">指出是否要啟用備份排程。</span><span class="sxs-lookup"><span data-stu-id="c05de-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05de-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c05de-119">-Profile</span></span>
<span data-ttu-id="c05de-120">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c05de-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c05de-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="c05de-121">-RecurrenceType</span></span>
<span data-ttu-id="c05de-122">指定此備份排程的週期類型。</span><span class="sxs-lookup"><span data-stu-id="c05de-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="c05de-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c05de-123">Valid values are:</span></span> 

- <span data-ttu-id="c05de-124">持續</span><span class="sxs-lookup"><span data-stu-id="c05de-124">Minutes</span></span>
- <span data-ttu-id="c05de-125">工資</span><span class="sxs-lookup"><span data-stu-id="c05de-125">Hourly</span></span>
- <span data-ttu-id="c05de-126">日常</span><span class="sxs-lookup"><span data-stu-id="c05de-126">Daily</span></span>
- <span data-ttu-id="c05de-127">周更新</span><span class="sxs-lookup"><span data-stu-id="c05de-127">Weekly</span></span>

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

### <span data-ttu-id="c05de-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="c05de-128">-RecurrenceValue</span></span>
<span data-ttu-id="c05de-129">指定備份的頻率。</span><span class="sxs-lookup"><span data-stu-id="c05de-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="c05de-130">這個參數使用 *RecurrenceType* 參數所指定的單位。</span><span class="sxs-lookup"><span data-stu-id="c05de-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="c05de-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="c05de-131">-RetentionCount</span></span>
<span data-ttu-id="c05de-132">指定保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="c05de-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="c05de-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="c05de-133">-StartFromDateTime</span></span>
<span data-ttu-id="c05de-134">指定開始進行備份的日期。</span><span class="sxs-lookup"><span data-stu-id="c05de-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="c05de-135">預設值是目前的時間。</span><span class="sxs-lookup"><span data-stu-id="c05de-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="c05de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05de-136">CommonParameters</span></span>
<span data-ttu-id="c05de-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c05de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05de-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c05de-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05de-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c05de-139">INPUTS</span></span>

### <span data-ttu-id="c05de-140">所有</span><span class="sxs-lookup"><span data-stu-id="c05de-140">None</span></span>

## <span data-ttu-id="c05de-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c05de-141">OUTPUTS</span></span>

### <span data-ttu-id="c05de-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="c05de-142">BackupScheduleBase</span></span>
<span data-ttu-id="c05de-143">這個 Cmdlet 會傳回 **BackupScheduleBase** 物件。</span><span class="sxs-lookup"><span data-stu-id="c05de-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="c05de-144">使用 **BackupScheduleBase** 建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="c05de-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="c05de-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c05de-145">NOTES</span></span>

## <span data-ttu-id="c05de-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c05de-146">RELATED LINKS</span></span>

[<span data-ttu-id="c05de-147">新-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="c05de-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="c05de-148">新-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c05de-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


