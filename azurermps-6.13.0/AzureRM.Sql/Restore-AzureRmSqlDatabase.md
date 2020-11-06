---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: b4c444233701a6ecfe66eb77f90dade618c9e08f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449703"
---
# <span data-ttu-id="27e21-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27e21-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="27e21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27e21-102">SYNOPSIS</span></span>
<span data-ttu-id="27e21-103">還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27e21-104">句法</span><span class="sxs-lookup"><span data-stu-id="27e21-104">SYNTAX</span></span>

### <span data-ttu-id="27e21-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e21-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="27e21-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e21-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e21-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="27e21-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e21-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-109">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27e21-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="27e21-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27e21-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27e21-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="27e21-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27e21-113">說明</span><span class="sxs-lookup"><span data-stu-id="27e21-113">DESCRIPTION</span></span>
<span data-ttu-id="27e21-114">**Restore-AzureRmSqlDatabase** Cmdlet 會從地域冗余備份、備份已刪除的資料庫、長時間保留備份或即時資料庫中的時間點，復原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-114">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="27e21-115">已還原的資料庫會建立為新資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="27e21-116">您可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="27e21-117">示例</span><span class="sxs-lookup"><span data-stu-id="27e21-117">EXAMPLES</span></span>

### <span data-ttu-id="27e21-118">範例1：從某個時間點還原資料庫</span><span class="sxs-lookup"><span data-stu-id="27e21-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="27e21-119">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="27e21-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="27e21-120">第二個命令會從指定的時間點備份將 $Database 中的資料庫還原到名為 RestoredDatabase 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="27e21-121">範例2：從某個時間點將資料庫還原到彈性池</span><span class="sxs-lookup"><span data-stu-id="27e21-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="27e21-122">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="27e21-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="27e21-123">第二個命令會將 $Database 中的資料庫從指定的時間點備份還原到名為 elasticpool01 的彈性池中名為 RestoredDatabase 的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="27e21-124">範例3：還原已刪除的資料庫</span><span class="sxs-lookup"><span data-stu-id="27e21-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="27e21-125">第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="27e21-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="27e21-126">第二個命令會使用 [Restore AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) Cmdlet，從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="27e21-126">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="27e21-127">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="27e21-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="27e21-128">範例4：將已刪除的資料庫還原成彈性池</span><span class="sxs-lookup"><span data-stu-id="27e21-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="27e21-129">第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="27e21-129">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="27e21-130">第二個命令會使用 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="27e21-130">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="27e21-131">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="27e21-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="27e21-132">範例5： Geo-Restore 資料庫</span><span class="sxs-lookup"><span data-stu-id="27e21-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="27e21-133">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="27e21-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="27e21-134">第二個命令會在 $GeoBackup 到名為 RestoredDatabase 的 SQL 資料庫時還原備份。</span><span class="sxs-lookup"><span data-stu-id="27e21-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="27e21-135">參數</span><span class="sxs-lookup"><span data-stu-id="27e21-135">PARAMETERS</span></span>

### <span data-ttu-id="27e21-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27e21-136">-AsJob</span></span>
<span data-ttu-id="27e21-137">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="27e21-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27e21-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="27e21-138">-ComputeGeneration</span></span>
<span data-ttu-id="27e21-139">要指派給已還原資料庫的計算產生</span><span class="sxs-lookup"><span data-stu-id="27e21-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="27e21-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e21-140">-DefaultProfile</span></span>
<span data-ttu-id="27e21-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="27e21-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e21-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="27e21-142">-DeletionDate</span></span>
<span data-ttu-id="27e21-143">將刪除日期指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="27e21-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="27e21-144">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27e21-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="27e21-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="27e21-145">-Edition</span></span>
<span data-ttu-id="27e21-146">指定 SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="27e21-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="27e21-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="27e21-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27e21-148">所有</span><span class="sxs-lookup"><span data-stu-id="27e21-148">None</span></span>
- <span data-ttu-id="27e21-149">空白</span><span class="sxs-lookup"><span data-stu-id="27e21-149">Basic</span></span>
- <span data-ttu-id="27e21-150">標準</span><span class="sxs-lookup"><span data-stu-id="27e21-150">Standard</span></span>
- <span data-ttu-id="27e21-151">佳</span><span class="sxs-lookup"><span data-stu-id="27e21-151">Premium</span></span>
- <span data-ttu-id="27e21-152">倉庫</span><span class="sxs-lookup"><span data-stu-id="27e21-152">DataWarehouse</span></span>
- <span data-ttu-id="27e21-153">空閒</span><span class="sxs-lookup"><span data-stu-id="27e21-153">Free</span></span>
- <span data-ttu-id="27e21-154">伸縮</span><span class="sxs-lookup"><span data-stu-id="27e21-154">Stretch</span></span>
- <span data-ttu-id="27e21-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="27e21-155">GeneralPurpose</span></span>
- <span data-ttu-id="27e21-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="27e21-156">BusinessCritical</span></span>

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

### <span data-ttu-id="27e21-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="27e21-157">-ElasticPoolName</span></span>
<span data-ttu-id="27e21-158">指定要放入 SQL 資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e21-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="27e21-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="27e21-160">表示此 Cmdlet 會從已刪除的 SQL 資料庫備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="27e21-161">您可以使用 Get-AzureRMSqlDeletedDatabaseBackup Cmdlet 來取得已刪除之 SQL 資料庫的備份。</span><span class="sxs-lookup"><span data-stu-id="27e21-161">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="27e21-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-162">-FromGeoBackup</span></span>
<span data-ttu-id="27e21-163">表示此 Cmdlet 會從地域冗余備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="27e21-164">您可以使用 Get-AzureRMSqlDatabaseGeoBackup Cmdlet 來取得地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="27e21-164">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="27e21-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="27e21-166">表示此 Cmdlet 會從長期保留備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="27e21-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="27e21-168">表示此 Cmdlet 會從時間點備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="27e21-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="27e21-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="27e21-169">-LicenseType</span></span>
<span data-ttu-id="27e21-170">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="27e21-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="27e21-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="27e21-171">-PointInTime</span></span>
<span data-ttu-id="27e21-172">指定要將 SQL 資料庫還原至其中的時間點（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="27e21-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="27e21-173">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27e21-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="27e21-174">將此參數與 *FromPointInTimeBackup* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="27e21-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="27e21-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e21-175">-ResourceGroupName</span></span>
<span data-ttu-id="27e21-176">指定此 Cmdlet 指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e21-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="27e21-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e21-177">-ResourceId</span></span>
<span data-ttu-id="27e21-178">指定要還原的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="27e21-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="27e21-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27e21-179">-ServerName</span></span>
<span data-ttu-id="27e21-180">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e21-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="27e21-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="27e21-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="27e21-182">指定服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e21-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="27e21-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="27e21-183">-TargetDatabaseName</span></span>
<span data-ttu-id="27e21-184">指定要還原到的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e21-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="27e21-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="27e21-185">-VCore</span></span>
<span data-ttu-id="27e21-186">已還原之 Azure Sql 資料庫的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="27e21-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="27e21-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e21-187">CommonParameters</span></span>
<span data-ttu-id="27e21-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27e21-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e21-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27e21-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e21-190">輸入</span><span class="sxs-lookup"><span data-stu-id="27e21-190">INPUTS</span></span>

### <span data-ttu-id="27e21-191">System.object</span><span class="sxs-lookup"><span data-stu-id="27e21-191">System.DateTime</span></span>

### <span data-ttu-id="27e21-192">System.object</span><span class="sxs-lookup"><span data-stu-id="27e21-192">System.String</span></span>

## <span data-ttu-id="27e21-193">輸出</span><span class="sxs-lookup"><span data-stu-id="27e21-193">OUTPUTS</span></span>

### <span data-ttu-id="27e21-194">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="27e21-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="27e21-195">筆記</span><span class="sxs-lookup"><span data-stu-id="27e21-195">NOTES</span></span>

## <span data-ttu-id="27e21-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="27e21-196">RELATED LINKS</span></span>

[<span data-ttu-id="27e21-197">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="27e21-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="27e21-198">從使用者錯誤復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="27e21-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="27e21-199">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27e21-199">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="27e21-200">AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-200">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="27e21-201">AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="27e21-201">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="27e21-202">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="27e21-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

