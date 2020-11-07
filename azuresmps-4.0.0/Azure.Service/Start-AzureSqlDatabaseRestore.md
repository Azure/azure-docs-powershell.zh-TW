---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966872"
---
# <span data-ttu-id="e2878-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="e2878-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="e2878-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2878-102">SYNOPSIS</span></span>
<span data-ttu-id="e2878-103">執行資料庫的時間點還原。</span><span class="sxs-lookup"><span data-stu-id="e2878-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="e2878-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2878-104">SYNTAX</span></span>

### <span data-ttu-id="e2878-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e2878-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2878-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e2878-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2878-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2878-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2878-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2878-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2878-109">說明</span><span class="sxs-lookup"><span data-stu-id="e2878-109">DESCRIPTION</span></span>
<span data-ttu-id="e2878-110">**AzureSqlDatabaseRestore** Cmdlet 會執行基本、標準或 Premium 資料庫的時間點還原。</span><span class="sxs-lookup"><span data-stu-id="e2878-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="e2878-111">Azure SQL 資料庫會保留基本的資料庫備份7天、標準的14天，以及35天的 Premium。</span><span class="sxs-lookup"><span data-stu-id="e2878-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="e2878-112">[還原] 作業會建立新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2878-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="e2878-113">如果源資料庫未刪除， *SourceDatabaseName* 和 *TargetDatabaseName* 參數必須具有不同的值。</span><span class="sxs-lookup"><span data-stu-id="e2878-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="e2878-114">Azure SQL Database 目前不支援跨伺服器還原。</span><span class="sxs-lookup"><span data-stu-id="e2878-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="e2878-115">來源和目標伺服器名稱必須相同。</span><span class="sxs-lookup"><span data-stu-id="e2878-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="e2878-116">示例</span><span class="sxs-lookup"><span data-stu-id="e2878-116">EXAMPLES</span></span>

### <span data-ttu-id="e2878-117">範例1：將指定為物件的資料庫還原到某個時間點</span><span class="sxs-lookup"><span data-stu-id="e2878-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="e2878-118">第一個命令會在名為 Server01 的伺服器上取得名為 Database17 的資料庫物件，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2878-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="e2878-119">第二個命令會將資料庫還原至特定的時間點。</span><span class="sxs-lookup"><span data-stu-id="e2878-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="e2878-120">該命令會指定新資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="e2878-121">範例2：將名稱指定的資料庫還原到某個時間點</span><span class="sxs-lookup"><span data-stu-id="e2878-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="e2878-122">這個命令會將名為 Database17 的資料庫還原至特定時間點。</span><span class="sxs-lookup"><span data-stu-id="e2878-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="e2878-123">該命令會指定新資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="e2878-124">範例3：將已刪除的資料庫指定為物件至某個時間點</span><span class="sxs-lookup"><span data-stu-id="e2878-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="e2878-125">第一個命令會在名為 Server01 的伺服器上，為名為 Database01 的資料庫取得資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="e2878-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="e2878-126">命令會指定 *RestorableDropped* 參數。</span><span class="sxs-lookup"><span data-stu-id="e2878-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="e2878-127">因此，此 Cmdlet 會取得可復原的中斷資料庫，並將指定的還原點。</span><span class="sxs-lookup"><span data-stu-id="e2878-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="e2878-128">該命令會將該資料庫物件儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2878-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="e2878-129">第二個命令會還原 $Database 指定的刪除的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2878-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="e2878-130">該命令會指定新資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="e2878-131">參數</span><span class="sxs-lookup"><span data-stu-id="e2878-131">PARAMETERS</span></span>

### <span data-ttu-id="e2878-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e2878-132">-PointInTime</span></span>
<span data-ttu-id="e2878-133">指定要還原資料庫的還原點。</span><span class="sxs-lookup"><span data-stu-id="e2878-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="e2878-134">當還原作業完成時，資料庫會還原為此參數指定之日期和時間的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2878-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="e2878-135">根據預設，針對此設定為目前時間的即時資料庫，而針對刪除的資料庫，此 Cmdlet 會使用刪除資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="e2878-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e2878-136">-Profile</span></span>
<span data-ttu-id="e2878-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e2878-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2878-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e2878-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2878-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="e2878-139">-RestorableDropped</span></span>
<span data-ttu-id="e2878-140">表示此 Cmdlet 會還原可復原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="e2878-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2878-141">-SourceDatabase</span></span>
<span data-ttu-id="e2878-142">指定此 Cmdlet 所還原之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="e2878-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="e2878-144">指定刪除資料庫的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e2878-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="e2878-145">當您指定時間來符合實際資料庫刪除時間時，您必須包含毫秒數。</span><span class="sxs-lookup"><span data-stu-id="e2878-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2878-146">-SourceDatabaseName</span></span>
<span data-ttu-id="e2878-147">指定此 Cmdlet 還原之實際資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e2878-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="e2878-149">指定代表此 Cmdlet 還原之可復原的已刪除資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="e2878-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="e2878-150">若要取得 **RestorableDroppedDatabase** 物件，請使用 Get-AzureSqlDatabase Cmdlet，並指定 *RestorableDropped* 參數。</span><span class="sxs-lookup"><span data-stu-id="e2878-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="e2878-151">-SourceServerName</span></span>
<span data-ttu-id="e2878-152">指定源資料庫處於即時及正在執行的伺服器名稱，或在刪除之前執行源資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2878-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2878-153">-TargetDatabaseName</span></span>
<span data-ttu-id="e2878-154">指定還原作業所建立之新資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-154">Specifies the name of the new database that the restore operation creates.</span></span>

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

### <span data-ttu-id="e2878-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="e2878-155">-TargetServerName</span></span>
<span data-ttu-id="e2878-156">指定此 Cmdlet 要還原資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e2878-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="e2878-157">Azure SQL Database 目前不支援跨伺服器還原。</span><span class="sxs-lookup"><span data-stu-id="e2878-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="e2878-158">來源和目標伺服器名稱必須相同。</span><span class="sxs-lookup"><span data-stu-id="e2878-158">The source and target server names must be the same.</span></span>

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

### <span data-ttu-id="e2878-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2878-159">CommonParameters</span></span>
<span data-ttu-id="e2878-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2878-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2878-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2878-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2878-162">輸入</span><span class="sxs-lookup"><span data-stu-id="e2878-162">INPUTS</span></span>

### <span data-ttu-id="e2878-163">SqlDatabase. RestorableDroppedDatabase （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="e2878-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="e2878-164">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="e2878-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="e2878-165">輸出</span><span class="sxs-lookup"><span data-stu-id="e2878-165">OUTPUTS</span></span>

### <span data-ttu-id="e2878-166">SqlDatabase. RestoreDatabaseOperation （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="e2878-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="e2878-167">筆記</span><span class="sxs-lookup"><span data-stu-id="e2878-167">NOTES</span></span>
* <span data-ttu-id="e2878-168">您必須使用 [以認證為基礎的驗證] 才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2878-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="e2878-169">在執行此 Cmdlet 的電腦上執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="e2878-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="e2878-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2878-170">RELATED LINKS</span></span>

[<span data-ttu-id="e2878-171">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="e2878-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e2878-172">建立資料庫還原要求</span><span class="sxs-lookup"><span data-stu-id="e2878-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="e2878-173">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="e2878-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e2878-174">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2878-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


