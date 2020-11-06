---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455916"
---
# <span data-ttu-id="ef899-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ef899-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="ef899-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef899-102">SYNOPSIS</span></span>
<span data-ttu-id="ef899-103">還原 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef899-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef899-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef899-104">SYNTAX</span></span>

### <span data-ttu-id="ef899-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="ef899-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef899-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ef899-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef899-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ef899-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef899-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="ef899-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef899-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ef899-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef899-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ef899-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef899-111">說明</span><span class="sxs-lookup"><span data-stu-id="ef899-111">DESCRIPTION</span></span>
<span data-ttu-id="ef899-112">**Restore-AzureRmSqlInstanceDatabase** Cmdlet 會從即時資料庫的某個時間點還原實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef899-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="ef899-113">已還原的資料庫會建立為新的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef899-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="ef899-114">示例</span><span class="sxs-lookup"><span data-stu-id="ef899-114">EXAMPLES</span></span>

### <span data-ttu-id="ef899-115">範例1：從某個時間點還原實例資料庫</span><span class="sxs-lookup"><span data-stu-id="ef899-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="ef899-116">該命令會將實例資料庫 Database01 從指定的時間點備份還原到名為 Database01_restored 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef899-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="ef899-117">範例2：從某個時間點將實例資料庫還原到不同資源群組上的另一個實例</span><span class="sxs-lookup"><span data-stu-id="ef899-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="ef899-118">該命令會將 [資源群組] ResourceGroup01 上的實例 managedInstance1 的實例資料庫 Database01 還原至資源群組 ResourceGroup02 上實例 managedInstance2 上名為 [Database01_restored] 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef899-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="ef899-119">參數</span><span class="sxs-lookup"><span data-stu-id="ef899-119">PARAMETERS</span></span>

### <span data-ttu-id="ef899-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef899-120">-AsJob</span></span>
<span data-ttu-id="ef899-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef899-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef899-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef899-122">-DefaultProfile</span></span>
<span data-ttu-id="ef899-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef899-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef899-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ef899-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="ef899-125">從時間點備份中還原。</span><span class="sxs-lookup"><span data-stu-id="ef899-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef899-126">-InputObject</span></span>
<span data-ttu-id="ef899-127">要還原的實例資料庫物件</span><span class="sxs-lookup"><span data-stu-id="ef899-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ef899-128">-InstanceName</span></span>
<span data-ttu-id="ef899-129">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef899-130">-Name</span></span>
<span data-ttu-id="ef899-131">要還原的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="ef899-132">-PointInTime</span></span>
<span data-ttu-id="ef899-133">要還原資料庫的時間點。</span><span class="sxs-lookup"><span data-stu-id="ef899-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef899-134">-ResourceGroupName</span></span>
<span data-ttu-id="ef899-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef899-136">-ResourceId</span></span>
<span data-ttu-id="ef899-137">要還原之實例資料庫物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ef899-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef899-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="ef899-139">要還原到的目標實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="ef899-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="ef899-140">-TargetInstanceName</span></span>
<span data-ttu-id="ef899-141">要還原到的目標實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="ef899-142">如果未指定，目標實例就會與源實例相同。</span><span class="sxs-lookup"><span data-stu-id="ef899-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef899-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="ef899-144">要還原到的目標資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef899-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="ef899-145">如果未指定，[目標資源] 群組就會與 [來源資源] 群組相同。</span><span class="sxs-lookup"><span data-stu-id="ef899-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-146">-確認</span><span class="sxs-lookup"><span data-stu-id="ef899-146">-Confirm</span></span>
<span data-ttu-id="ef899-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef899-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef899-148">-WhatIf</span></span>
<span data-ttu-id="ef899-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef899-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef899-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef899-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef899-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef899-151">CommonParameters</span></span>
<span data-ttu-id="ef899-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef899-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef899-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef899-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef899-154">輸入</span><span class="sxs-lookup"><span data-stu-id="ef899-154">INPUTS</span></span>

### <span data-ttu-id="ef899-155">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ef899-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="ef899-156">System.object</span><span class="sxs-lookup"><span data-stu-id="ef899-156">System.String</span></span>

## <span data-ttu-id="ef899-157">輸出</span><span class="sxs-lookup"><span data-stu-id="ef899-157">OUTPUTS</span></span>

### <span data-ttu-id="ef899-158">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="ef899-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ef899-159">筆記</span><span class="sxs-lookup"><span data-stu-id="ef899-159">NOTES</span></span>

## <span data-ttu-id="ef899-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef899-160">RELATED LINKS</span></span>
