---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: 262d4266a41cd9072ff9109819a2268999d26d7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792396"
---
# <span data-ttu-id="df218-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="df218-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="df218-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df218-102">SYNOPSIS</span></span>
<span data-ttu-id="df218-103">還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-103">Restores a SQL database.</span></span>

## <span data-ttu-id="df218-104">句法</span><span class="sxs-lookup"><span data-stu-id="df218-104">SYNTAX</span></span>

### <span data-ttu-id="df218-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="df218-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df218-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="df218-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df218-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="df218-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df218-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="df218-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df218-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="df218-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df218-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="df218-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df218-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="df218-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df218-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="df218-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df218-113">說明</span><span class="sxs-lookup"><span data-stu-id="df218-113">DESCRIPTION</span></span>
<span data-ttu-id="df218-114">**Restore-AzSqlDatabase** Cmdlet 會從地域冗余備份、備份已刪除的資料庫、長時間保留備份或即時資料庫中的時間點，復原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="df218-115">已還原的資料庫會建立為新資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="df218-116">您可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="df218-117">示例</span><span class="sxs-lookup"><span data-stu-id="df218-117">EXAMPLES</span></span>

### <span data-ttu-id="df218-118">範例1：從某個時間點還原資料庫</span><span class="sxs-lookup"><span data-stu-id="df218-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="df218-119">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="df218-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="df218-120">第二個命令會從指定的時間點備份將 $Database 中的資料庫還原到名為 RestoredDatabase 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="df218-121">範例2：從某個時間點將資料庫還原到彈性池</span><span class="sxs-lookup"><span data-stu-id="df218-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="df218-122">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="df218-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="df218-123">第二個命令會將 $Database 中的資料庫從指定的時間點備份還原到名為 elasticpool01 的彈性池中名為 RestoredDatabase 的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="df218-124">範例3：還原已刪除的資料庫</span><span class="sxs-lookup"><span data-stu-id="df218-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="df218-125">第一個命令會使用 [AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="df218-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="df218-126">第二個命令會使用 [Restore AzSqlDatabase](./Restore-AzSqlDatabase.md) Cmdlet，從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="df218-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="df218-127">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="df218-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="df218-128">範例4：將已刪除的資料庫還原成彈性池</span><span class="sxs-lookup"><span data-stu-id="df218-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="df218-129">第一個命令會使用 [AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="df218-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="df218-130">第二個命令會使用 [restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="df218-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="df218-131">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="df218-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="df218-132">範例5： Geo-Restore 資料庫</span><span class="sxs-lookup"><span data-stu-id="df218-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="df218-133">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="df218-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="df218-134">第二個命令會在 $GeoBackup 到名為 RestoredDatabase 的 SQL 資料庫時還原備份。</span><span class="sxs-lookup"><span data-stu-id="df218-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="df218-135">參數</span><span class="sxs-lookup"><span data-stu-id="df218-135">PARAMETERS</span></span>

### <span data-ttu-id="df218-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df218-136">-AsJob</span></span>
<span data-ttu-id="df218-137">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df218-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df218-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="df218-138">-ComputeGeneration</span></span>
<span data-ttu-id="df218-139">要指派給已還原資料庫的計算產生</span><span class="sxs-lookup"><span data-stu-id="df218-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="df218-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df218-140">-DefaultProfile</span></span>
<span data-ttu-id="df218-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df218-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df218-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="df218-142">-DeletionDate</span></span>
<span data-ttu-id="df218-143">將刪除日期指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="df218-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="df218-144">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df218-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="df218-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="df218-145">-Edition</span></span>
<span data-ttu-id="df218-146">指定 SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="df218-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="df218-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="df218-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df218-148">所有</span><span class="sxs-lookup"><span data-stu-id="df218-148">None</span></span>
- <span data-ttu-id="df218-149">空白</span><span class="sxs-lookup"><span data-stu-id="df218-149">Basic</span></span>
- <span data-ttu-id="df218-150">標準</span><span class="sxs-lookup"><span data-stu-id="df218-150">Standard</span></span>
- <span data-ttu-id="df218-151">佳</span><span class="sxs-lookup"><span data-stu-id="df218-151">Premium</span></span>
- <span data-ttu-id="df218-152">倉庫</span><span class="sxs-lookup"><span data-stu-id="df218-152">DataWarehouse</span></span>
- <span data-ttu-id="df218-153">空閒</span><span class="sxs-lookup"><span data-stu-id="df218-153">Free</span></span>
- <span data-ttu-id="df218-154">伸縮</span><span class="sxs-lookup"><span data-stu-id="df218-154">Stretch</span></span>
- <span data-ttu-id="df218-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="df218-155">GeneralPurpose</span></span>
- <span data-ttu-id="df218-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="df218-156">BusinessCritical</span></span>

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

### <span data-ttu-id="df218-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="df218-157">-ElasticPoolName</span></span>
<span data-ttu-id="df218-158">指定要放入 SQL 資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="df218-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="df218-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="df218-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="df218-160">表示此 Cmdlet 會從已刪除的 SQL 資料庫備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="df218-161">您可以使用 Get-AzSqlDeletedDatabaseBackup Cmdlet 來取得已刪除之 SQL 資料庫的備份。</span><span class="sxs-lookup"><span data-stu-id="df218-161">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="df218-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="df218-162">-FromGeoBackup</span></span>
<span data-ttu-id="df218-163">表示此 Cmdlet 會從地域冗余備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="df218-164">您可以使用 Get-AzSqlDatabaseGeoBackup Cmdlet 來取得地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="df218-164">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="df218-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="df218-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="df218-166">表示此 Cmdlet 會從長期保留備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="df218-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="df218-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="df218-168">表示此 Cmdlet 會從時間點備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="df218-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="df218-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="df218-169">-LicenseType</span></span>
<span data-ttu-id="df218-170">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="df218-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="df218-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="df218-171">-PointInTime</span></span>
<span data-ttu-id="df218-172">指定要將 SQL 資料庫還原至其中的時間點（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="df218-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="df218-173">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df218-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="df218-174">將此參數與 *FromPointInTimeBackup* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="df218-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="df218-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df218-175">-ResourceGroupName</span></span>
<span data-ttu-id="df218-176">指定此 Cmdlet 指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df218-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="df218-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df218-177">-ResourceId</span></span>
<span data-ttu-id="df218-178">指定要還原的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="df218-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="df218-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df218-179">-ServerName</span></span>
<span data-ttu-id="df218-180">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="df218-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="df218-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="df218-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="df218-182">指定服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="df218-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="df218-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="df218-183">-TargetDatabaseName</span></span>
<span data-ttu-id="df218-184">指定要還原到的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="df218-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="df218-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="df218-185">-VCore</span></span>
<span data-ttu-id="df218-186">已還原之 Azure Sql 資料庫的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="df218-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="df218-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df218-187">CommonParameters</span></span>
<span data-ttu-id="df218-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df218-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df218-189">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df218-189">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df218-190">輸入</span><span class="sxs-lookup"><span data-stu-id="df218-190">INPUTS</span></span>

### <span data-ttu-id="df218-191">System.object</span><span class="sxs-lookup"><span data-stu-id="df218-191">System.DateTime</span></span>

### <span data-ttu-id="df218-192">System.object</span><span class="sxs-lookup"><span data-stu-id="df218-192">System.String</span></span>

## <span data-ttu-id="df218-193">輸出</span><span class="sxs-lookup"><span data-stu-id="df218-193">OUTPUTS</span></span>

### <span data-ttu-id="df218-194">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="df218-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="df218-195">筆記</span><span class="sxs-lookup"><span data-stu-id="df218-195">NOTES</span></span>

## <span data-ttu-id="df218-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="df218-196">RELATED LINKS</span></span>

[<span data-ttu-id="df218-197">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="df218-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="df218-198">從使用者錯誤復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="df218-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="df218-199">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="df218-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="df218-200">AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="df218-200">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="df218-201">AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="df218-201">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="df218-202">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="df218-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

