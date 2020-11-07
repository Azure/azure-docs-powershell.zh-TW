---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: b93f9a4ffe0e77d464b1913207d0fd3bf7691699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792494"
---
# <span data-ttu-id="993b6-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="993b6-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="993b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="993b6-102">SYNOPSIS</span></span>
<span data-ttu-id="993b6-103">取得備份短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="993b6-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="993b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="993b6-104">SYNTAX</span></span>

### <span data-ttu-id="993b6-105">PolicyByResourceInstanceDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="993b6-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="993b6-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="993b6-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="993b6-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="993b6-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="993b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="993b6-108">DESCRIPTION</span></span>
<span data-ttu-id="993b6-109">**AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="993b6-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="993b6-110">原則是在時間點還原備份的保留期間（以天數為單位）。</span><span class="sxs-lookup"><span data-stu-id="993b6-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="993b6-111">示例</span><span class="sxs-lookup"><span data-stu-id="993b6-111">EXAMPLES</span></span>

### <span data-ttu-id="993b6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="993b6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="993b6-113">這個命令會取得 database01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="993b6-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="993b6-114">範例2</span><span class="sxs-lookup"><span data-stu-id="993b6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="993b6-115">這個命令會取得 database01 透過管道在資料庫物件中進行的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="993b6-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="993b6-116">範例3</span><span class="sxs-lookup"><span data-stu-id="993b6-116">Example 3</span></span>
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

<span data-ttu-id="993b6-117">這個命令會透過已刪除資料庫物件中以 [管道] 為 database01 的所有已刪除資料庫，取得該短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="993b6-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="993b6-118">參數</span><span class="sxs-lookup"><span data-stu-id="993b6-118">PARAMETERS</span></span>

### <span data-ttu-id="993b6-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="993b6-119">-DatabaseName</span></span>
<span data-ttu-id="993b6-120">要為其檢索備份之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="993b6-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="993b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993b6-121">-DefaultProfile</span></span>
<span data-ttu-id="993b6-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="993b6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="993b6-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="993b6-123">-DeletionDate</span></span>
<span data-ttu-id="993b6-124">要為其檢索備份的 Azure SQL 實例資料庫的刪除日期，以毫秒為單位 (（例如 2016-02-23T00：21： 22.847 Z) </span><span class="sxs-lookup"><span data-stu-id="993b6-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="993b6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="993b6-125">-InputObject</span></span>
<span data-ttu-id="993b6-126">要取得/設定原則的即時或刪除資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="993b6-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="993b6-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="993b6-127">-InstanceName</span></span>
<span data-ttu-id="993b6-128">資料庫所在之 Azure SQL 託管實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="993b6-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="993b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="993b6-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="993b6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="993b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="993b6-131">-ResourceId</span></span>
<span data-ttu-id="993b6-132">短期保留原則資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="993b6-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="993b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993b6-133">CommonParameters</span></span>
<span data-ttu-id="993b6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="993b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993b6-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="993b6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993b6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="993b6-136">INPUTS</span></span>

### <span data-ttu-id="993b6-137">AzureSqlManagedDatabaseBaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="993b6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="993b6-138">System.object</span><span class="sxs-lookup"><span data-stu-id="993b6-138">System.String</span></span>

## <span data-ttu-id="993b6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="993b6-139">OUTPUTS</span></span>

### <span data-ttu-id="993b6-140">AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="993b6-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="993b6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="993b6-141">NOTES</span></span>

## <span data-ttu-id="993b6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="993b6-142">RELATED LINKS</span></span>
