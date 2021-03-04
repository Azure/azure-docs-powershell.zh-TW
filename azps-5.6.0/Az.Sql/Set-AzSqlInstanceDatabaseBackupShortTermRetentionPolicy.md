---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0a08176dab2d4bb40d25f11574850d584981063c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909309"
---
# <span data-ttu-id="636d2-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="636d2-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="636d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="636d2-102">SYNOPSIS</span></span>
<span data-ttu-id="636d2-103">設定備份短期保留政策。</span><span class="sxs-lookup"><span data-stu-id="636d2-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="636d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="636d2-104">SYNTAX</span></span>

### <span data-ttu-id="636d2-105">PolicyByResourceInstanceDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="636d2-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="636d2-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="636d2-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="636d2-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="636d2-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="636d2-108">描述</span><span class="sxs-lookup"><span data-stu-id="636d2-108">DESCRIPTION</span></span>
<span data-ttu-id="636d2-109">**Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolidlet** 會登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="636d2-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="636d2-110">此為時間點還原備份的保留期間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="636d2-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="636d2-111">例子</span><span class="sxs-lookup"><span data-stu-id="636d2-111">EXAMPLES</span></span>

### <span data-ttu-id="636d2-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="636d2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="636d2-113">此命令將資料庫01 的短期保留政策設定為 35 天。</span><span class="sxs-lookup"><span data-stu-id="636d2-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="636d2-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="636d2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="636d2-115">此命令會透過資料庫物件的管道將資料庫01 的短期保留政策設定為 35 天。</span><span class="sxs-lookup"><span data-stu-id="636d2-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="636d2-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="636d2-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="636d2-117">此命令會透過刪除的資料庫物件中的管道，針對名為 DB1 的所有已刪除資料庫設定短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="636d2-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="636d2-118">請注意，您僅能減少已刪除資料庫的保留期間。</span><span class="sxs-lookup"><span data-stu-id="636d2-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="636d2-119">參數</span><span class="sxs-lookup"><span data-stu-id="636d2-119">PARAMETERS</span></span>

### <span data-ttu-id="636d2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="636d2-120">-DatabaseName</span></span>
<span data-ttu-id="636d2-121">要取回備份的 Azure SQL 實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="636d2-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636d2-122">-DefaultProfile</span></span>
<span data-ttu-id="636d2-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="636d2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="636d2-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="636d2-124">-DeletionDate</span></span>
<span data-ttu-id="636d2-125">Azure SQL 實例資料庫的刪除日期，用於以毫秒精確度 (例如 2016-02-23T00：21：22.847Z) </span><span class="sxs-lookup"><span data-stu-id="636d2-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="636d2-126">-InputObject</span></span>
<span data-ttu-id="636d2-127">要取得/設定其政策之即時或刪除的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="636d2-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="636d2-128">-InstanceName</span></span>
<span data-ttu-id="636d2-129">資料庫位於 Azure SQL Managed 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="636d2-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="636d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="636d2-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="636d2-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="636d2-132">-ResourceId</span></span>
<span data-ttu-id="636d2-133">短期保留政策資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="636d2-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="636d2-134">-RetentionDays</span></span>
<span data-ttu-id="636d2-135">備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="636d2-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636d2-136">-確認</span><span class="sxs-lookup"><span data-stu-id="636d2-136">-Confirm</span></span>
<span data-ttu-id="636d2-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="636d2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="636d2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="636d2-138">-WhatIf</span></span>
<span data-ttu-id="636d2-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="636d2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="636d2-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="636d2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="636d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636d2-141">CommonParameters</span></span>
<span data-ttu-id="636d2-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="636d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636d2-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="636d2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636d2-144">輸入</span><span class="sxs-lookup"><span data-stu-id="636d2-144">INPUTS</span></span>

### <span data-ttu-id="636d2-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="636d2-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="636d2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="636d2-146">System.String</span></span>

## <span data-ttu-id="636d2-147">輸出</span><span class="sxs-lookup"><span data-stu-id="636d2-147">OUTPUTS</span></span>

### <span data-ttu-id="636d2-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="636d2-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="636d2-149">筆記</span><span class="sxs-lookup"><span data-stu-id="636d2-149">NOTES</span></span>

## <span data-ttu-id="636d2-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="636d2-150">RELATED LINKS</span></span>
