---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: 6fa95473091afe991eac90ad87d7321b8401a8be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913566"
---
# <span data-ttu-id="dc5e1-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="dc5e1-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="dc5e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5e1-103">建立同步處理案例的特定資料庫資訊物件，以用於移移工作。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="dc5e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc5e1-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc5e1-105">描述</span><span class="sxs-lookup"><span data-stu-id="dc5e1-105">DESCRIPTION</span></span>

<span data-ttu-id="dc5e1-106">Cmdlet New-AzDataMigrationSyncSelectedDB會建立同步分析案例特定的資料庫資訊物件，其中包含來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="dc5e1-107">例子</span><span class="sxs-lookup"><span data-stu-id="dc5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5e1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="dc5e1-108">Example 1</span></span>
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

<span data-ttu-id="dc5e1-109">此範例會建立資料庫中繼資料物件，描述要移$DatabaseName資料庫的$DatabaseName。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="dc5e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc5e1-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5e1-111">-DefaultProfile</span></span>
<span data-ttu-id="dc5e1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc5e1-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="dc5e1-113">-MigrationSetting</span></span>
<span data-ttu-id="dc5e1-114">調整移移行為的移移設定</span><span class="sxs-lookup"><span data-stu-id="dc5e1-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="dc5e1-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dc5e1-115">-SchemaName</span></span>
<span data-ttu-id="dc5e1-116">要移移的架構名稱</span><span class="sxs-lookup"><span data-stu-id="dc5e1-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="dc5e1-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc5e1-117">-SourceDatabaseName</span></span>
<span data-ttu-id="dc5e1-118">源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-118">The name of the source database.</span></span>

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

### <span data-ttu-id="dc5e1-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="dc5e1-119">-SourceSetting</span></span>
<span data-ttu-id="dc5e1-120">調整來源端點移移行為的來源設定</span><span class="sxs-lookup"><span data-stu-id="dc5e1-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="dc5e1-121">-表格地圖</span><span class="sxs-lookup"><span data-stu-id="dc5e1-121">-TableMap</span></span>
<span data-ttu-id="dc5e1-122">來源與目標資料表的關聯</span><span class="sxs-lookup"><span data-stu-id="dc5e1-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="dc5e1-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc5e1-123">-TargetDatabaseName</span></span>
<span data-ttu-id="dc5e1-124">目標資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="dc5e1-124">The name of the target database</span></span>

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

### <span data-ttu-id="dc5e1-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="dc5e1-125">-TargetSetting</span></span>
<span data-ttu-id="dc5e1-126">調整目標端點移移行為的目標設定</span><span class="sxs-lookup"><span data-stu-id="dc5e1-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="dc5e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5e1-127">CommonParameters</span></span>
<span data-ttu-id="dc5e1-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5e1-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dc5e1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5e1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dc5e1-130">INPUTS</span></span>

### <span data-ttu-id="dc5e1-131">沒有</span><span class="sxs-lookup"><span data-stu-id="dc5e1-131">None</span></span>

## <span data-ttu-id="dc5e1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dc5e1-132">OUTPUTS</span></span>

### <span data-ttu-id="dc5e1-133">Microsoft.Azure.management.DataMigration.models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="dc5e1-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="dc5e1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="dc5e1-134">NOTES</span></span>

## <span data-ttu-id="dc5e1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc5e1-135">RELATED LINKS</span></span>
