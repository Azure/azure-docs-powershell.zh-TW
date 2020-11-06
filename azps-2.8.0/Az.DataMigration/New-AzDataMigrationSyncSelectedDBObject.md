---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d25a97e7c7a783910d63262075209402bb299c0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612704"
---
# <span data-ttu-id="1d47a-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="1d47a-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="1d47a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d47a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d47a-103">建立要用於遷移工作之同步處理案例的特定資料庫資訊物件。</span><span class="sxs-lookup"><span data-stu-id="1d47a-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="1d47a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d47a-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d47a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d47a-105">DESCRIPTION</span></span>

<span data-ttu-id="1d47a-106">New-AzDataMigrationSyncSelectedDB Cmdlet 會建立一個特定于同步處理案例的資料庫資訊物件，其中包含來源和目標資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1d47a-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="1d47a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1d47a-107">EXAMPLES</span></span>

### <span data-ttu-id="1d47a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1d47a-108">Example 1</span></span>
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

<span data-ttu-id="1d47a-109">這個範例會建立資料庫中繼資料物件來描述 $DatabaseName 到資料庫 $DatabaseName 的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="1d47a-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="1d47a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d47a-110">PARAMETERS</span></span>

### <span data-ttu-id="1d47a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d47a-111">-DefaultProfile</span></span>
<span data-ttu-id="1d47a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d47a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d47a-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="1d47a-113">-MigrationSetting</span></span>
<span data-ttu-id="1d47a-114">調整遷移行為的遷移設定</span><span class="sxs-lookup"><span data-stu-id="1d47a-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="1d47a-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1d47a-115">-SchemaName</span></span>
<span data-ttu-id="1d47a-116">要遷移的架構名稱</span><span class="sxs-lookup"><span data-stu-id="1d47a-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="1d47a-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d47a-117">-SourceDatabaseName</span></span>
<span data-ttu-id="1d47a-118">來源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d47a-118">The name of the source database.</span></span>

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

### <span data-ttu-id="1d47a-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="1d47a-119">-SourceSetting</span></span>
<span data-ttu-id="1d47a-120">微調來源端點遷移行為的來源設定</span><span class="sxs-lookup"><span data-stu-id="1d47a-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="1d47a-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="1d47a-121">-TableMap</span></span>
<span data-ttu-id="1d47a-122">將來源對應至目標資料表</span><span class="sxs-lookup"><span data-stu-id="1d47a-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="1d47a-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d47a-123">-TargetDatabaseName</span></span>
<span data-ttu-id="1d47a-124">目標資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="1d47a-124">The name of the target database</span></span>

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

### <span data-ttu-id="1d47a-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="1d47a-125">-TargetSetting</span></span>
<span data-ttu-id="1d47a-126">要調整目標端點遷移行為的目標設定</span><span class="sxs-lookup"><span data-stu-id="1d47a-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="1d47a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d47a-127">CommonParameters</span></span>
<span data-ttu-id="1d47a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d47a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d47a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d47a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d47a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1d47a-130">INPUTS</span></span>

### <span data-ttu-id="1d47a-131">所有</span><span class="sxs-lookup"><span data-stu-id="1d47a-131">None</span></span>

## <span data-ttu-id="1d47a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1d47a-132">OUTPUTS</span></span>

### <span data-ttu-id="1d47a-133">MigrateSqlServerSqlDbSyncTaskInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="1d47a-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="1d47a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1d47a-134">NOTES</span></span>

## <span data-ttu-id="1d47a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d47a-135">RELATED LINKS</span></span>
