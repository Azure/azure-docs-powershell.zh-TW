---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286156"
---
# <span data-ttu-id="6f491-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6f491-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="6f491-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f491-102">SYNOPSIS</span></span>
<span data-ttu-id="6f491-103">還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-103">Restores a SQL database.</span></span>

## <span data-ttu-id="6f491-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f491-104">SYNTAX</span></span>

### <span data-ttu-id="6f491-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f491-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="6f491-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f491-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f491-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="6f491-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f491-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f491-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="6f491-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f491-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f491-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="6f491-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f491-113">說明</span><span class="sxs-lookup"><span data-stu-id="6f491-113">DESCRIPTION</span></span>
<span data-ttu-id="6f491-114">**Restore-AzSqlDatabase** Cmdlet 會從地域冗余備份、備份已刪除的資料庫、長時間保留備份或即時資料庫中的時間點，復原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="6f491-115">已還原的資料庫會建立為新資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="6f491-116">您可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="6f491-117">示例</span><span class="sxs-lookup"><span data-stu-id="6f491-117">EXAMPLES</span></span>

### <span data-ttu-id="6f491-118">範例1：從某個時間點還原資料庫</span><span class="sxs-lookup"><span data-stu-id="6f491-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="6f491-119">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f491-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="6f491-120">第二個命令會從指定的時間點備份將 $Database 中的資料庫還原到名為 RestoredDatabase 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="6f491-121">範例2：從某個時間點將資料庫還原到彈性池</span><span class="sxs-lookup"><span data-stu-id="6f491-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6f491-122">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f491-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="6f491-123">第二個命令會將 $Database 中的資料庫從指定的時間點備份還原到名為 elasticpool01 的彈性池中名為 RestoredDatabase 的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="6f491-124">範例3：還原已刪除的資料庫</span><span class="sxs-lookup"><span data-stu-id="6f491-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="6f491-125">第一個命令會使用 [AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="6f491-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="6f491-126">第二個命令會使用 [Restore AzSqlDatabase](./Restore-AzSqlDatabase.md) Cmdlet，從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="6f491-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="6f491-127">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="6f491-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="6f491-128">範例4：將已刪除的資料庫還原成彈性池</span><span class="sxs-lookup"><span data-stu-id="6f491-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="6f491-129">第一個命令會使用 [AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="6f491-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="6f491-130">第二個命令會使用 [restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="6f491-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="6f491-131">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="6f491-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="6f491-132">範例5： Geo-Restore 資料庫</span><span class="sxs-lookup"><span data-stu-id="6f491-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="6f491-133">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f491-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="6f491-134">第二個命令會在 $GeoBackup 到名為 RestoredDatabase 的 SQL 資料庫時還原備份。</span><span class="sxs-lookup"><span data-stu-id="6f491-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="6f491-135">參數</span><span class="sxs-lookup"><span data-stu-id="6f491-135">PARAMETERS</span></span>

### <span data-ttu-id="6f491-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f491-136">-AsJob</span></span>
<span data-ttu-id="6f491-137">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f491-137">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="6f491-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="6f491-139">儲存 SQL 資料庫備份所用的備份儲存空間冗余。</span><span class="sxs-lookup"><span data-stu-id="6f491-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="6f491-140">選項包括： Local、Zone 和 Geo。</span><span class="sxs-lookup"><span data-stu-id="6f491-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6f491-141">-ComputeGeneration</span></span>
<span data-ttu-id="6f491-142">要指派給已還原資料庫的計算產生</span><span class="sxs-lookup"><span data-stu-id="6f491-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f491-143">-DefaultProfile</span></span>
<span data-ttu-id="6f491-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6f491-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f491-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="6f491-145">-DeletionDate</span></span>
<span data-ttu-id="6f491-146">將刪除日期指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f491-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="6f491-147">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f491-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="6f491-148">-Edition</span></span>
<span data-ttu-id="6f491-149">指定 SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="6f491-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="6f491-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6f491-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f491-151">所有</span><span class="sxs-lookup"><span data-stu-id="6f491-151">None</span></span>
- <span data-ttu-id="6f491-152">空白</span><span class="sxs-lookup"><span data-stu-id="6f491-152">Basic</span></span>
- <span data-ttu-id="6f491-153">標準</span><span class="sxs-lookup"><span data-stu-id="6f491-153">Standard</span></span>
- <span data-ttu-id="6f491-154">佳</span><span class="sxs-lookup"><span data-stu-id="6f491-154">Premium</span></span>
- <span data-ttu-id="6f491-155">倉庫</span><span class="sxs-lookup"><span data-stu-id="6f491-155">DataWarehouse</span></span>
- <span data-ttu-id="6f491-156">空閒</span><span class="sxs-lookup"><span data-stu-id="6f491-156">Free</span></span>
- <span data-ttu-id="6f491-157">伸縮</span><span class="sxs-lookup"><span data-stu-id="6f491-157">Stretch</span></span>
- <span data-ttu-id="6f491-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="6f491-158">GeneralPurpose</span></span>
- <span data-ttu-id="6f491-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="6f491-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6f491-160">-ElasticPoolName</span></span>
<span data-ttu-id="6f491-161">指定要放入 SQL 資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f491-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="6f491-163">表示此 Cmdlet 會從已刪除的 SQL 資料庫備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="6f491-164">您可以使用 Get-AzSqlDeletedDatabaseBackup Cmdlet 來取得已刪除之 SQL 資料庫的備份。</span><span class="sxs-lookup"><span data-stu-id="6f491-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-165">-FromGeoBackup</span></span>
<span data-ttu-id="6f491-166">表示此 Cmdlet 會從地域冗余備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="6f491-167">您可以使用 Get-AzSqlDatabaseGeoBackup Cmdlet 來取得地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="6f491-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="6f491-169">表示此 Cmdlet 會從長期保留備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="6f491-171">表示此 Cmdlet 會從時間點備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6f491-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6f491-172">-LicenseType</span></span>
<span data-ttu-id="6f491-173">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="6f491-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="6f491-174">-PointInTime</span></span>
<span data-ttu-id="6f491-175">指定要將 SQL 資料庫還原至其中的時間點（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="6f491-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="6f491-176">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f491-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="6f491-177">將此參數與 *FromPointInTimeBackup* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6f491-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f491-178">-ResourceGroupName</span></span>
<span data-ttu-id="6f491-179">指定此 Cmdlet 指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f491-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f491-180">-ResourceId</span></span>
<span data-ttu-id="6f491-181">指定要還原的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f491-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f491-182">-ServerName</span></span>
<span data-ttu-id="6f491-183">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f491-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6f491-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="6f491-185">指定服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f491-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f491-186">-TargetDatabaseName</span></span>
<span data-ttu-id="6f491-187">指定要還原到的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f491-187">Specifies the name of the database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="6f491-188">-VCore</span></span>
<span data-ttu-id="6f491-189">已還原之 Azure Sql 資料庫的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="6f491-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-190">-確認</span><span class="sxs-lookup"><span data-stu-id="6f491-190">-Confirm</span></span>
<span data-ttu-id="6f491-191">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f491-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f491-192">-WhatIf</span></span>
<span data-ttu-id="6f491-193">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f491-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f491-194">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f491-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f491-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f491-195">CommonParameters</span></span>
<span data-ttu-id="6f491-196">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f491-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f491-197">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f491-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f491-198">輸入</span><span class="sxs-lookup"><span data-stu-id="6f491-198">INPUTS</span></span>

### <span data-ttu-id="6f491-199">System.object</span><span class="sxs-lookup"><span data-stu-id="6f491-199">System.DateTime</span></span>

### <span data-ttu-id="6f491-200">System.object</span><span class="sxs-lookup"><span data-stu-id="6f491-200">System.String</span></span>

## <span data-ttu-id="6f491-201">輸出</span><span class="sxs-lookup"><span data-stu-id="6f491-201">OUTPUTS</span></span>

### <span data-ttu-id="6f491-202">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="6f491-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6f491-203">筆記</span><span class="sxs-lookup"><span data-stu-id="6f491-203">NOTES</span></span>

## <span data-ttu-id="6f491-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f491-204">RELATED LINKS</span></span>

[<span data-ttu-id="6f491-205">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="6f491-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="6f491-206">從使用者錯誤復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="6f491-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="6f491-207">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6f491-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="6f491-208">AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="6f491-209">AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="6f491-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="6f491-210">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6f491-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

