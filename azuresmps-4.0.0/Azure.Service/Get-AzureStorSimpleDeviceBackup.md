---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967736"
---
# <span data-ttu-id="b0cae-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="b0cae-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="b0cae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0cae-102">SYNOPSIS</span></span>
<span data-ttu-id="b0cae-103">從裝置中取得備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-103">Gets backups from a device.</span></span>

## <span data-ttu-id="b0cae-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0cae-104">SYNTAX</span></span>

### <span data-ttu-id="b0cae-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="b0cae-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0cae-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="b0cae-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0cae-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="b0cae-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0cae-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="b0cae-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0cae-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="b0cae-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b0cae-110">說明</span><span class="sxs-lookup"><span data-stu-id="b0cae-110">DESCRIPTION</span></span>
<span data-ttu-id="b0cae-111">**AzureStorSimpleDeviceBackup** Cmdlet 會從裝置進行備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="b0cae-112">您可以指定備份的備份原則、量及建立時間。</span><span class="sxs-lookup"><span data-stu-id="b0cae-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="b0cae-113">這個 Cmdlet 最多可以在第一頁中傳回100備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="b0cae-114">如果有超過100的備份，請使用 *第一個* 和 [ *略過* ] 參數來檢索後續頁面。</span><span class="sxs-lookup"><span data-stu-id="b0cae-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="b0cae-115">如果您為 *Skip* 指定的值是100，而 *第一次* 則是50，則此 Cmdlet 不會傳回第一個100結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="b0cae-116">它會在跳過的100之後傳回接下來的50結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="b0cae-117">示例</span><span class="sxs-lookup"><span data-stu-id="b0cae-117">EXAMPLES</span></span>

### <span data-ttu-id="b0cae-118">範例1：取得裝置上的所有備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="b0cae-119">這個命令會取得位於名為 Contoso63-AppVm 的裝置上的所有備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="b0cae-120">如果有超過第一頁所允許的最大100備份數，請使用 *第一個* 和 [ *略過* ] 參數來查看其他結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="b0cae-121">範例2：取得在兩個日期之間建立的備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="b0cae-122">這個命令會在名為 Contoso63-AppVm 的裝置上，或在10/7/2014 或之後或之前（10/8/2014）之後所建立的裝置上取得備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="b0cae-123">這個 Cmdlet 會跳過第一個結果，並傳回第一個結果之後的前兩個結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="b0cae-124">修改 *第一個* 和 [ *略過* ] 的值，以查看其他結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="b0cae-125">範例3：取得備份原則識別碼的備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="b0cae-126">這個命令會在指定日期之前或之前建立的 Contoso63-AppVm 裝置上取得備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="b0cae-127">命令會使用具有指定識別碼的備份策略來取得所建立的備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="b0cae-128">這個命令會指定 *第一個* 參數，因此只會傳回前10個結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="b0cae-129">範例4：取得備份原則物件的備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="b0cae-130">這個命令會使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet 取得 **BackupPolicyDetails** 物件，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0cae-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0cae-131">這個 Cmdlet 會從命令的第一個部分使用備份原則，為從 Contoso63-AppVm 建立的裝置取得備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="b0cae-132">這個命令會在指定的日期或之前（就像先前的範例所示）建立備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="b0cae-133">這個命令只會傳回前10個結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="b0cae-134">範例5：取得大量 ID 的備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="b0cae-135">這個命令會在擁有指定實例識別碼的卷上，取得已建立的裝置上的備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="b0cae-136">這個命令會指定 *第* 一個參數，因此它只會傳回第一個結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="b0cae-137">範例6：取得卷名的備份</span><span class="sxs-lookup"><span data-stu-id="b0cae-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="b0cae-138">這個命令會使用 **AzureStorSimpleDeviceVolume** Cmdlet 取得 **VirtualDisk** 物件，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0cae-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0cae-139">這個 Cmdlet 會從命令的第一個部分開始，為從該卷上建立的裝置（名為 Contoso63-AppVm）取得備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="b0cae-140">這個命令只會傳回第一個結果。</span><span class="sxs-lookup"><span data-stu-id="b0cae-140">This command returns only the first result.</span></span>

## <span data-ttu-id="b0cae-141">參數</span><span class="sxs-lookup"><span data-stu-id="b0cae-141">PARAMETERS</span></span>

### <span data-ttu-id="b0cae-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b0cae-142">-BackupPolicy</span></span>
<span data-ttu-id="b0cae-143">指定 **BackupPolicyDetails** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0cae-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="b0cae-144">這個 Cmdlet 使用這個物件的 **InstanceId** 來決定要取得哪些備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="b0cae-145">若要取得 **BackupPolicyDetails** 物件，請使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0cae-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="b0cae-146">-BackupPolicyId</span></span>
<span data-ttu-id="b0cae-147">指定備份原則的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0cae-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="b0cae-148">這個 Cmdlet 會針對此參數指定的原則取得裝置備份。</span><span class="sxs-lookup"><span data-stu-id="b0cae-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b0cae-149">-DeviceName</span></span>
<span data-ttu-id="b0cae-150">指定要取得備份之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0cae-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="b0cae-151">-優先</span><span class="sxs-lookup"><span data-stu-id="b0cae-151">-First</span></span>
<span data-ttu-id="b0cae-152">只取得指定數目的物件。</span><span class="sxs-lookup"><span data-stu-id="b0cae-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="b0cae-153">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="b0cae-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-154">-從</span><span class="sxs-lookup"><span data-stu-id="b0cae-154">-From</span></span>
<span data-ttu-id="b0cae-155">指定此 Cmdlet 取得之備份的開始日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b0cae-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0cae-156">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b0cae-156">-Profile</span></span>
<span data-ttu-id="b0cae-157">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b0cae-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b0cae-158">-略過</span><span class="sxs-lookup"><span data-stu-id="b0cae-158">-Skip</span></span>
<span data-ttu-id="b0cae-159">忽略指定的物件數目，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="b0cae-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="b0cae-160">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="b0cae-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-161">-To</span><span class="sxs-lookup"><span data-stu-id="b0cae-161">-To</span></span>
<span data-ttu-id="b0cae-162">指定此 Cmdlet 取得之備份的結束日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b0cae-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0cae-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="b0cae-163">-Volume</span></span>
<span data-ttu-id="b0cae-164">指定 **VirtualDisk** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0cae-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="b0cae-165">這個 Cmdlet 使用這個物件的 **InstanceId** 來判斷備份存在的磁片卷。</span><span class="sxs-lookup"><span data-stu-id="b0cae-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="b0cae-166">若要取得 **VirtualDisk** 物件，請使用 **AzureStorSimpleDeviceVolume** 參數。</span><span class="sxs-lookup"><span data-stu-id="b0cae-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="b0cae-167">-VolumeId</span></span>
<span data-ttu-id="b0cae-168">指定在其中存在備份之卷的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0cae-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0cae-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0cae-169">CommonParameters</span></span>
<span data-ttu-id="b0cae-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0cae-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0cae-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0cae-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0cae-172">輸入</span><span class="sxs-lookup"><span data-stu-id="b0cae-172">INPUTS</span></span>

### <span data-ttu-id="b0cae-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="b0cae-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="b0cae-174">這個 Cmdlet 接受 **BackupPolicyDetails** 和 **VirtualDisk** 物件。</span><span class="sxs-lookup"><span data-stu-id="b0cae-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="b0cae-175">輸出</span><span class="sxs-lookup"><span data-stu-id="b0cae-175">OUTPUTS</span></span>

### <span data-ttu-id="b0cae-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="b0cae-176">IList\<Backup\></span></span>
<span data-ttu-id="b0cae-177">這個 Cmdlet 會傳回 **備份** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="b0cae-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="b0cae-178">筆記</span><span class="sxs-lookup"><span data-stu-id="b0cae-178">NOTES</span></span>

## <span data-ttu-id="b0cae-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0cae-179">RELATED LINKS</span></span>

[<span data-ttu-id="b0cae-180">移除-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="b0cae-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="b0cae-181">AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b0cae-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b0cae-182">AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="b0cae-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


