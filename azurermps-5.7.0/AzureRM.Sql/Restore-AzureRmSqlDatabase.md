---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623789"
---
# <span data-ttu-id="b3f1d-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3f1d-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="b3f1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f1d-103">還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3f1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3f1d-104">SYNTAX</span></span>

### <span data-ttu-id="b3f1d-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f1d-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f1d-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3f1d-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f1d-109">說明</span><span class="sxs-lookup"><span data-stu-id="b3f1d-109">DESCRIPTION</span></span>
<span data-ttu-id="b3f1d-110">**Restore-AzureRmSqlDatabase** Cmdlet 會從地域冗余備份、備份已刪除的資料庫、長時間保留備份或即時資料庫中的時間點，復原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="b3f1d-111">已還原的資料庫會建立為新資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="b3f1d-112">您可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="b3f1d-113">示例</span><span class="sxs-lookup"><span data-stu-id="b3f1d-113">EXAMPLES</span></span>

### <span data-ttu-id="b3f1d-114">範例1：從某個時間點還原資料庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="b3f1d-115">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="b3f1d-116">第二個命令會從指定的時間點備份將 $Database 中的資料庫還原到名為 RestoredDatabase 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="b3f1d-117">範例2：從某個時間點將資料庫還原到彈性池</span><span class="sxs-lookup"><span data-stu-id="b3f1d-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b3f1d-118">第一個命令會取得名為 Database01 的 SQL 資料庫，然後將它儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="b3f1d-119">第二個命令會將 $Database 中的資料庫從指定的時間點備份還原到名為 elasticpool01 的彈性池中名為 RestoredDatabase 的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="b3f1d-120">範例3：還原已刪除的資料庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="b3f1d-121">第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b3f1d-122">第二個命令會使用 [Restore AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) Cmdlet，從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="b3f1d-123">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b3f1d-124">範例4：將已刪除的資料庫還原成彈性池</span><span class="sxs-lookup"><span data-stu-id="b3f1d-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="b3f1d-125">第一個命令會使用 [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)來取得您想要還原的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b3f1d-126">第二個命令會使用 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)從已刪除的資料庫備份開始還原。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="b3f1d-127">如果未指定-PointInTime 參數，資料庫將會還原到刪除時間。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b3f1d-128">範例5： Geo-Restore 資料庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="b3f1d-129">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="b3f1d-130">第二個命令會在 $GeoBackup 到名為 RestoredDatabase 的 SQL 資料庫時還原備份。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="b3f1d-131">參數</span><span class="sxs-lookup"><span data-stu-id="b3f1d-131">PARAMETERS</span></span>

### <span data-ttu-id="b3f1d-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3f1d-132">-AsJob</span></span>
<span data-ttu-id="b3f1d-133">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3f1d-133">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f1d-134">-DefaultProfile</span></span>
<span data-ttu-id="b3f1d-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b3f1d-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3f1d-136">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b3f1d-136">-DeletionDate</span></span>
<span data-ttu-id="b3f1d-137">將刪除日期指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-137">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="b3f1d-138">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-138">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="b3f1d-139">-Edition</span></span>
<span data-ttu-id="b3f1d-140">指定 SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-140">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="b3f1d-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b3f1d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3f1d-142">所有</span><span class="sxs-lookup"><span data-stu-id="b3f1d-142">None</span></span>
- <span data-ttu-id="b3f1d-143">佳</span><span class="sxs-lookup"><span data-stu-id="b3f1d-143">Premium</span></span>
- <span data-ttu-id="b3f1d-144">空白</span><span class="sxs-lookup"><span data-stu-id="b3f1d-144">Basic</span></span>
- <span data-ttu-id="b3f1d-145">標準</span><span class="sxs-lookup"><span data-stu-id="b3f1d-145">Standard</span></span>
- <span data-ttu-id="b3f1d-146">倉庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-146">DataWarehouse</span></span>
- <span data-ttu-id="b3f1d-147">空閒</span><span class="sxs-lookup"><span data-stu-id="b3f1d-147">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-148">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b3f1d-148">-ElasticPoolName</span></span>
<span data-ttu-id="b3f1d-149">指定要放入 SQL 資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-149">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-150">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-150">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="b3f1d-151">表示此 Cmdlet 會從已刪除的 SQL 資料庫備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-151">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="b3f1d-152">您可以使用 Get-AzureRMSqlDeletedDatabaseBackup Cmdlet 來取得已刪除之 SQL 資料庫的備份。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-152">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-153">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-153">-FromGeoBackup</span></span>
<span data-ttu-id="b3f1d-154">表示此 Cmdlet 會從地域冗余備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-154">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="b3f1d-155">您可以使用 Get-AzureRMSqlDatabaseGeoBackup Cmdlet 來取得地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-155">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-156">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-156">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="b3f1d-157">表示此 Cmdlet 會從長期保留備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-157">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-158">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-158">-FromPointInTimeBackup</span></span>
<span data-ttu-id="b3f1d-159">表示此 Cmdlet 會從時間點備份還原 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-159">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-160">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="b3f1d-160">-PointInTime</span></span>
<span data-ttu-id="b3f1d-161">指定要將 SQL 資料庫還原至其中的時間點（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-161">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="b3f1d-162">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-162">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="b3f1d-163">將此參數與 *FromPointInTimeBackup* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-163">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f1d-164">-ResourceGroupName</span></span>
<span data-ttu-id="b3f1d-165">指定此 Cmdlet 指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-165">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f1d-166">-ResourceId</span></span>
<span data-ttu-id="b3f1d-167">指定要還原的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-167">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3f1d-168">-ServerName</span></span>
<span data-ttu-id="b3f1d-169">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-169">Specifies the name of the SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-170">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b3f1d-170">-ServiceObjectiveName</span></span>
<span data-ttu-id="b3f1d-171">指定服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-171">Specifies the name of the service objective.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f1d-172">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3f1d-172">-TargetDatabaseName</span></span>
<span data-ttu-id="b3f1d-173">指定要還原到的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-173">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="b3f1d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f1d-174">CommonParameters</span></span>
<span data-ttu-id="b3f1d-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f1d-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f1d-177">輸入</span><span class="sxs-lookup"><span data-stu-id="b3f1d-177">INPUTS</span></span>

### <span data-ttu-id="b3f1d-178">所有</span><span class="sxs-lookup"><span data-stu-id="b3f1d-178">None</span></span>
<span data-ttu-id="b3f1d-179">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3f1d-180">輸出</span><span class="sxs-lookup"><span data-stu-id="b3f1d-180">OUTPUTS</span></span>

### <span data-ttu-id="b3f1d-181">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="b3f1d-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b3f1d-182">筆記</span><span class="sxs-lookup"><span data-stu-id="b3f1d-182">NOTES</span></span>

## <span data-ttu-id="b3f1d-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3f1d-183">RELATED LINKS</span></span>

[<span data-ttu-id="b3f1d-184">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-184">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="b3f1d-185">從使用者錯誤復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="b3f1d-185">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="b3f1d-186">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3f1d-186">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="b3f1d-187">AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-187">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="b3f1d-188">AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b3f1d-188">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="b3f1d-189">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b3f1d-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

