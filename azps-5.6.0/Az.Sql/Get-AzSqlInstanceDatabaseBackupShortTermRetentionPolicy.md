---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0334f022266843290f56fa8ee635634bce7caa56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907498"
---
# <span data-ttu-id="0c74d-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0c74d-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="0c74d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c74d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c74d-103">獲得備份的短期保留政策。</span><span class="sxs-lookup"><span data-stu-id="0c74d-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="0c74d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c74d-104">SYNTAX</span></span>

### <span data-ttu-id="0c74d-105">PolicyByResourceInstanceDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0c74d-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c74d-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c74d-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c74d-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0c74d-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c74d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0c74d-108">DESCRIPTION</span></span>
<span data-ttu-id="0c74d-109">**Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolidlet** 會取得註冊至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c74d-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="0c74d-110">此為時間點還原備份的保留期間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="0c74d-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="0c74d-111">例子</span><span class="sxs-lookup"><span data-stu-id="0c74d-111">EXAMPLES</span></span>

### <span data-ttu-id="0c74d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0c74d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="0c74d-113">此命令會獲得資料庫01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c74d-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="0c74d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="0c74d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="0c74d-115">此命令會透過資料庫物件的管道，獲得資料庫01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c74d-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="0c74d-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="0c74d-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="0c74d-117">此命令會透過刪除的資料庫物件中的管道，針對名為 database01 的所有已刪除資料庫，獲得短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c74d-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="0c74d-118">參數</span><span class="sxs-lookup"><span data-stu-id="0c74d-118">PARAMETERS</span></span>

### <span data-ttu-id="0c74d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c74d-119">-DatabaseName</span></span>
<span data-ttu-id="0c74d-120">要取回備份的 Azure SQL 實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0c74d-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="0c74d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c74d-121">-DefaultProfile</span></span>
<span data-ttu-id="0c74d-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c74d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c74d-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0c74d-123">-DeletionDate</span></span>
<span data-ttu-id="0c74d-124">Azure SQL 實例資料庫的刪除日期，用於以毫秒精確度 (例如 2016-02-23T00：21：22.847Z) </span><span class="sxs-lookup"><span data-stu-id="0c74d-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="0c74d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c74d-125">-InputObject</span></span>
<span data-ttu-id="0c74d-126">要取得/設定其政策之即時或刪除的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="0c74d-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c74d-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0c74d-127">-InstanceName</span></span>
<span data-ttu-id="0c74d-128">資料庫位於 Azure SQL Managed 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c74d-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="0c74d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c74d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c74d-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c74d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c74d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c74d-131">-ResourceId</span></span>
<span data-ttu-id="0c74d-132">短期保留政策資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c74d-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c74d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c74d-133">CommonParameters</span></span>
<span data-ttu-id="0c74d-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c74d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c74d-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c74d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c74d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0c74d-136">INPUTS</span></span>

### <span data-ttu-id="0c74d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="0c74d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="0c74d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0c74d-138">System.String</span></span>

## <span data-ttu-id="0c74d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0c74d-139">OUTPUTS</span></span>

### <span data-ttu-id="0c74d-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0c74d-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="0c74d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0c74d-141">NOTES</span></span>

## <span data-ttu-id="0c74d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c74d-142">RELATED LINKS</span></span>
