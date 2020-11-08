---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129192"
---
# <span data-ttu-id="be220-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be220-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="be220-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be220-102">SYNOPSIS</span></span>
<span data-ttu-id="be220-103">取得備份短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="be220-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="be220-104">句法</span><span class="sxs-lookup"><span data-stu-id="be220-104">SYNTAX</span></span>

### <span data-ttu-id="be220-105">PolicyByResourceInstanceDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be220-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be220-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="be220-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be220-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="be220-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be220-108">說明</span><span class="sxs-lookup"><span data-stu-id="be220-108">DESCRIPTION</span></span>
<span data-ttu-id="be220-109">**AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="be220-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="be220-110">原則是在時間點還原備份的保留期間（以天數為單位）。</span><span class="sxs-lookup"><span data-stu-id="be220-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="be220-111">示例</span><span class="sxs-lookup"><span data-stu-id="be220-111">EXAMPLES</span></span>

### <span data-ttu-id="be220-112">範例1</span><span class="sxs-lookup"><span data-stu-id="be220-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="be220-113">這個命令會取得 database01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="be220-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="be220-114">範例2</span><span class="sxs-lookup"><span data-stu-id="be220-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="be220-115">這個命令會取得 database01 透過管道在資料庫物件中進行的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="be220-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="be220-116">範例3</span><span class="sxs-lookup"><span data-stu-id="be220-116">Example 3</span></span>
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

<span data-ttu-id="be220-117">這個命令會透過已刪除資料庫物件中以 [管道] 為 database01 的所有已刪除資料庫，取得該短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="be220-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="be220-118">參數</span><span class="sxs-lookup"><span data-stu-id="be220-118">PARAMETERS</span></span>

### <span data-ttu-id="be220-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be220-119">-DatabaseName</span></span>
<span data-ttu-id="be220-120">要為其檢索備份之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="be220-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="be220-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be220-121">-DefaultProfile</span></span>
<span data-ttu-id="be220-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be220-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be220-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="be220-123">-DeletionDate</span></span>
<span data-ttu-id="be220-124">要為其檢索備份的 Azure SQL 實例資料庫的刪除日期，以毫秒為單位 (（例如 2016-02-23T00：21： 22.847 Z) </span><span class="sxs-lookup"><span data-stu-id="be220-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="be220-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be220-125">-InputObject</span></span>
<span data-ttu-id="be220-126">要取得/設定原則的即時或刪除資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="be220-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="be220-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="be220-127">-InstanceName</span></span>
<span data-ttu-id="be220-128">資料庫所在之 Azure SQL 託管實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="be220-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="be220-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be220-129">-ResourceGroupName</span></span>
<span data-ttu-id="be220-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be220-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="be220-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be220-131">-ResourceId</span></span>
<span data-ttu-id="be220-132">短期保留原則資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="be220-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="be220-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be220-133">CommonParameters</span></span>
<span data-ttu-id="be220-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be220-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be220-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be220-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be220-136">輸入</span><span class="sxs-lookup"><span data-stu-id="be220-136">INPUTS</span></span>

### <span data-ttu-id="be220-137">AzureSqlManagedDatabaseBaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="be220-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="be220-138">System.object</span><span class="sxs-lookup"><span data-stu-id="be220-138">System.String</span></span>

## <span data-ttu-id="be220-139">輸出</span><span class="sxs-lookup"><span data-stu-id="be220-139">OUTPUTS</span></span>

### <span data-ttu-id="be220-140">AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="be220-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="be220-141">筆記</span><span class="sxs-lookup"><span data-stu-id="be220-141">NOTES</span></span>

## <span data-ttu-id="be220-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="be220-142">RELATED LINKS</span></span>
