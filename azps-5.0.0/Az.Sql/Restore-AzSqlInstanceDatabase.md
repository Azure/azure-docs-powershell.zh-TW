---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4d8ece03cc5c1a96d73bcde79aef76c8f329b38a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138414"
---
# <span data-ttu-id="cf48e-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cf48e-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="cf48e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf48e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf48e-103">還原 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="cf48e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf48e-104">SYNTAX</span></span>

### <span data-ttu-id="cf48e-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="cf48e-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cf48e-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="cf48e-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf48e-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="cf48e-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cf48e-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf48e-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="cf48e-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="cf48e-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf48e-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="cf48e-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="cf48e-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="cf48e-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf48e-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="cf48e-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf48e-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="cf48e-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf48e-117">說明</span><span class="sxs-lookup"><span data-stu-id="cf48e-117">DESCRIPTION</span></span>
<span data-ttu-id="cf48e-118">**Restore-AzSqlInstanceDatabase** Cmdlet 會從地域冗余備份、即時資料庫中的時間點或長期保留備份中還原實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="cf48e-119">已還原的資料庫會建立為新的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="cf48e-120">示例</span><span class="sxs-lookup"><span data-stu-id="cf48e-120">EXAMPLES</span></span>

### <span data-ttu-id="cf48e-121">範例1：從某個時間點還原實例資料庫</span><span class="sxs-lookup"><span data-stu-id="cf48e-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="cf48e-122">該命令會將實例資料庫 Database01 從指定的時間點備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="cf48e-123">範例2：從某個時間點將實例資料庫還原到不同資源群組上的另一個實例</span><span class="sxs-lookup"><span data-stu-id="cf48e-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="cf48e-124">該命令會將 [資源群組] ResourceGroup01 上的實例 managedInstance1 的實例資料庫 Database01 還原至資源群組 ResourceGroup02 上實例 managedInstance2 上名為 [Database01_restored] 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="cf48e-125">範例3： Geo-Restore 實例資料庫</span><span class="sxs-lookup"><span data-stu-id="cf48e-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="cf48e-126">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="cf48e-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="cf48e-127">第二個命令會將 $GeoBackup 中的備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="cf48e-128">範例4：從某個時間點還原已刪除的實例資料庫</span><span class="sxs-lookup"><span data-stu-id="cf48e-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="cf48e-129">第一個命令會取得實例 "managedInstance1" 上名為 "DB1" 的已刪除實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="cf48e-130">第二個命令會將回遷的資料庫從指定的時間點備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="cf48e-131">範例5：從某個時間點還原已刪除的實例資料庫</span><span class="sxs-lookup"><span data-stu-id="cf48e-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="cf48e-132">第一個命令會取得實例 "managedInstance1" 上名為 "DB1" 的已刪除實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="cf48e-133">第二個命令會從指定的時間點備份將取得的資料庫還原到名為 Database01_restored 使用輸入物件的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="cf48e-134">範例6：從 LTR 備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="cf48e-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="cf48e-135">透過執行 AzSqlInstanceDatabaseLongTermRetentionBackup) ，以指定的資源識別碼還原 LTR 備份， (可找到。</span><span class="sxs-lookup"><span data-stu-id="cf48e-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="cf48e-136">參數</span><span class="sxs-lookup"><span data-stu-id="cf48e-136">PARAMETERS</span></span>

### <span data-ttu-id="cf48e-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf48e-137">-AsJob</span></span>
<span data-ttu-id="cf48e-138">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf48e-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf48e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf48e-139">-DefaultProfile</span></span>
<span data-ttu-id="cf48e-140">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf48e-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="cf48e-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cf48e-141">-DeletionDate</span></span>
<span data-ttu-id="cf48e-142">已刪除資料庫的刪除日期。</span><span class="sxs-lookup"><span data-stu-id="cf48e-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="cf48e-143">-FromGeoBackup</span></span>
<span data-ttu-id="cf48e-144">從 geo 備份還原。</span><span class="sxs-lookup"><span data-stu-id="cf48e-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cf48e-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="cf48e-146">從長期保留備份中還原。</span><span class="sxs-lookup"><span data-stu-id="cf48e-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="cf48e-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="cf48e-148">從時間點備份中還原。</span><span class="sxs-lookup"><span data-stu-id="cf48e-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="cf48e-149">-GeoBackupObject</span></span>
<span data-ttu-id="cf48e-150">要還原的可復原實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="cf48e-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf48e-151">-InputObject</span></span>
<span data-ttu-id="cf48e-152">要還原的實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="cf48e-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cf48e-153">-InstanceName</span></span>
<span data-ttu-id="cf48e-154">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf48e-155">-Name</span></span>
<span data-ttu-id="cf48e-156">要還原的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="cf48e-157">-PointInTime</span></span>
<span data-ttu-id="cf48e-158">要還原資料庫的時間點。</span><span class="sxs-lookup"><span data-stu-id="cf48e-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf48e-159">-ResourceGroupName</span></span>
<span data-ttu-id="cf48e-160">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf48e-161">-ResourceId</span></span>
<span data-ttu-id="cf48e-162">要還原之實例資料庫物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cf48e-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf48e-163">-SubscriptionId</span></span>
<span data-ttu-id="cf48e-164">來源訂閱 id。</span><span class="sxs-lookup"><span data-stu-id="cf48e-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf48e-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="cf48e-166">要還原到的目標實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="cf48e-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="cf48e-167">-TargetInstanceName</span></span>
<span data-ttu-id="cf48e-168">要還原到的目標實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="cf48e-169">如果未指定，目標實例就會與源實例相同。</span><span class="sxs-lookup"><span data-stu-id="cf48e-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf48e-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="cf48e-171">要還原到的目標資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf48e-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="cf48e-172">如果未指定，[目標資源] 群組就會與 [來源資源] 群組相同。</span><span class="sxs-lookup"><span data-stu-id="cf48e-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf48e-173">-確認</span><span class="sxs-lookup"><span data-stu-id="cf48e-173">-Confirm</span></span>
<span data-ttu-id="cf48e-174">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf48e-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf48e-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf48e-175">-WhatIf</span></span>
<span data-ttu-id="cf48e-176">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf48e-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf48e-177">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf48e-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf48e-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf48e-178">CommonParameters</span></span>
<span data-ttu-id="cf48e-179">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf48e-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf48e-180">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf48e-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf48e-181">輸入</span><span class="sxs-lookup"><span data-stu-id="cf48e-181">INPUTS</span></span>

### <span data-ttu-id="cf48e-182">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="cf48e-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="cf48e-183">AzureSqlRecoverableManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="cf48e-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="cf48e-184">System.object</span><span class="sxs-lookup"><span data-stu-id="cf48e-184">System.String</span></span>

## <span data-ttu-id="cf48e-185">輸出</span><span class="sxs-lookup"><span data-stu-id="cf48e-185">OUTPUTS</span></span>

### <span data-ttu-id="cf48e-186">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="cf48e-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cf48e-187">筆記</span><span class="sxs-lookup"><span data-stu-id="cf48e-187">NOTES</span></span>

## <span data-ttu-id="cf48e-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf48e-188">RELATED LINKS</span></span>
