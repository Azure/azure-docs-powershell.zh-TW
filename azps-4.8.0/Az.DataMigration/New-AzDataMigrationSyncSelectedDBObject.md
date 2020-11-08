---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136019"
---
# <span data-ttu-id="18f6f-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="18f6f-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="18f6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="18f6f-103">建立要用於遷移工作之同步處理案例的特定資料庫資訊物件。</span><span class="sxs-lookup"><span data-stu-id="18f6f-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="18f6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="18f6f-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f6f-105">說明</span><span class="sxs-lookup"><span data-stu-id="18f6f-105">DESCRIPTION</span></span>

<span data-ttu-id="18f6f-106">New-AzDataMigrationSyncSelectedDB Cmdlet 會建立一個特定于同步處理案例的資料庫資訊物件，其中包含來源和目標資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="18f6f-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="18f6f-107">示例</span><span class="sxs-lookup"><span data-stu-id="18f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="18f6f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="18f6f-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="18f6f-109">這個範例會建立資料庫中繼資料物件來描述 $DatabaseName 到資料庫 $DatabaseName 的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="18f6f-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="18f6f-110">參數</span><span class="sxs-lookup"><span data-stu-id="18f6f-110">PARAMETERS</span></span>

### <span data-ttu-id="18f6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f6f-111">-DefaultProfile</span></span>
<span data-ttu-id="18f6f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18f6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f6f-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="18f6f-113">-MigrationSetting</span></span>
<span data-ttu-id="18f6f-114">調整遷移行為的遷移設定</span><span class="sxs-lookup"><span data-stu-id="18f6f-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6f-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="18f6f-115">-SchemaName</span></span>
<span data-ttu-id="18f6f-116">要遷移的架構名稱</span><span class="sxs-lookup"><span data-stu-id="18f6f-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="18f6f-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="18f6f-117">-SourceDatabaseName</span></span>
<span data-ttu-id="18f6f-118">來源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="18f6f-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6f-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="18f6f-119">-SourceSetting</span></span>
<span data-ttu-id="18f6f-120">微調來源端點遷移行為的來源設定</span><span class="sxs-lookup"><span data-stu-id="18f6f-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6f-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="18f6f-121">-TableMap</span></span>
<span data-ttu-id="18f6f-122">將來源對應至目標資料表</span><span class="sxs-lookup"><span data-stu-id="18f6f-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6f-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="18f6f-123">-TargetDatabaseName</span></span>
<span data-ttu-id="18f6f-124">目標資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="18f6f-124">The name of the target database</span></span>

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

### <span data-ttu-id="18f6f-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="18f6f-125">-TargetSetting</span></span>
<span data-ttu-id="18f6f-126">要調整目標端點遷移行為的目標設定</span><span class="sxs-lookup"><span data-stu-id="18f6f-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f6f-127">CommonParameters</span></span>
<span data-ttu-id="18f6f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18f6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f6f-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18f6f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f6f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="18f6f-130">INPUTS</span></span>

### <span data-ttu-id="18f6f-131">所有</span><span class="sxs-lookup"><span data-stu-id="18f6f-131">None</span></span>

## <span data-ttu-id="18f6f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="18f6f-132">OUTPUTS</span></span>

### <span data-ttu-id="18f6f-133">MigrateSqlServerSqlDbSyncTaskInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="18f6f-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="18f6f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="18f6f-134">NOTES</span></span>

## <span data-ttu-id="18f6f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="18f6f-135">RELATED LINKS</span></span>