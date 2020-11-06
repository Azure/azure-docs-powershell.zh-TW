---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614754"
---
# <span data-ttu-id="82e9c-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82e9c-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="82e9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="82e9c-103">還原 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="82e9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="82e9c-104">SYNTAX</span></span>

### <span data-ttu-id="82e9c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="82e9c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="82e9c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="82e9c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82e9c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="82e9c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="82e9c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82e9c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="82e9c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="82e9c-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="82e9c-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82e9c-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="82e9c-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82e9c-114">說明</span><span class="sxs-lookup"><span data-stu-id="82e9c-114">DESCRIPTION</span></span>
<span data-ttu-id="82e9c-115">**Restore-AzSqlInstanceDatabase** Cmdlet 會從地域冗余備份或即時資料庫中的時間點還原實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="82e9c-116">已還原的資料庫會建立為新的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="82e9c-117">示例</span><span class="sxs-lookup"><span data-stu-id="82e9c-117">EXAMPLES</span></span>

### <span data-ttu-id="82e9c-118">範例1：從某個時間點還原實例資料庫</span><span class="sxs-lookup"><span data-stu-id="82e9c-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="82e9c-119">該命令會將實例資料庫 Database01 從指定的時間點備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="82e9c-120">範例2：從某個時間點將實例資料庫還原到不同資源群組上的另一個實例</span><span class="sxs-lookup"><span data-stu-id="82e9c-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="82e9c-121">該命令會將 [資源群組] ResourceGroup01 上的實例 managedInstance1 的實例資料庫 Database01 還原至資源群組 ResourceGroup02 上實例 managedInstance2 上名為 [Database01_restored] 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="82e9c-122">範例3： Geo-Restore 實例資料庫</span><span class="sxs-lookup"><span data-stu-id="82e9c-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="82e9c-123">第一個命令會針對名為 Database01 的資料庫取得地域冗余備份，然後將其儲存在 $GeoBackup 變數中。</span><span class="sxs-lookup"><span data-stu-id="82e9c-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="82e9c-124">第二個命令會將 $GeoBackup 中的備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="82e9c-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="82e9c-125">參數</span><span class="sxs-lookup"><span data-stu-id="82e9c-125">PARAMETERS</span></span>

### <span data-ttu-id="82e9c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82e9c-126">-AsJob</span></span>
<span data-ttu-id="82e9c-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82e9c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82e9c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e9c-128">-DefaultProfile</span></span>
<span data-ttu-id="82e9c-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="82e9c-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="82e9c-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="82e9c-130">-FromGeoBackup</span></span>
<span data-ttu-id="82e9c-131">從 geo 備份還原。</span><span class="sxs-lookup"><span data-stu-id="82e9c-131">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="82e9c-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="82e9c-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="82e9c-133">從時間點備份中還原。</span><span class="sxs-lookup"><span data-stu-id="82e9c-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="82e9c-134">-GeoBackupObject</span></span>
<span data-ttu-id="82e9c-135">要還原的可復原實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="82e9c-135">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="82e9c-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82e9c-136">-InputObject</span></span>
<span data-ttu-id="82e9c-137">要還原的實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="82e9c-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="82e9c-138">-InstanceName</span></span>
<span data-ttu-id="82e9c-139">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="82e9c-140">-Name</span></span>
<span data-ttu-id="82e9c-141">要還原的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="82e9c-142">-PointInTime</span></span>
<span data-ttu-id="82e9c-143">要還原資料庫的時間點。</span><span class="sxs-lookup"><span data-stu-id="82e9c-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e9c-144">-ResourceGroupName</span></span>
<span data-ttu-id="82e9c-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82e9c-146">-ResourceId</span></span>
<span data-ttu-id="82e9c-147">要還原之實例資料庫物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="82e9c-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
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

### <span data-ttu-id="82e9c-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="82e9c-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="82e9c-149">要還原到的目標實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="82e9c-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="82e9c-150">-TargetInstanceName</span></span>
<span data-ttu-id="82e9c-151">要還原到的目標實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="82e9c-152">如果未指定，目標實例就會與源實例相同。</span><span class="sxs-lookup"><span data-stu-id="82e9c-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e9c-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="82e9c-154">要還原到的目標資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82e9c-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="82e9c-155">如果未指定，[目標資源] 群組就會與 [來源資源] 群組相同。</span><span class="sxs-lookup"><span data-stu-id="82e9c-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e9c-156">-確認</span><span class="sxs-lookup"><span data-stu-id="82e9c-156">-Confirm</span></span>
<span data-ttu-id="82e9c-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82e9c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e9c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e9c-158">-WhatIf</span></span>
<span data-ttu-id="82e9c-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82e9c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82e9c-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82e9c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e9c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e9c-161">CommonParameters</span></span>
<span data-ttu-id="82e9c-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82e9c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e9c-163">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="82e9c-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e9c-164">輸入</span><span class="sxs-lookup"><span data-stu-id="82e9c-164">INPUTS</span></span>

### <span data-ttu-id="82e9c-165">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="82e9c-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="82e9c-166">AzureSqlRecoverableManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="82e9c-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="82e9c-167">System.object</span><span class="sxs-lookup"><span data-stu-id="82e9c-167">System.String</span></span>

## <span data-ttu-id="82e9c-168">輸出</span><span class="sxs-lookup"><span data-stu-id="82e9c-168">OUTPUTS</span></span>

### <span data-ttu-id="82e9c-169">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="82e9c-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="82e9c-170">筆記</span><span class="sxs-lookup"><span data-stu-id="82e9c-170">NOTES</span></span>

## <span data-ttu-id="82e9c-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="82e9c-171">RELATED LINKS</span></span>
