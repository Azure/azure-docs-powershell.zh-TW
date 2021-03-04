---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913922"
---
# <span data-ttu-id="662a6-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="662a6-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="662a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="662a6-102">SYNOPSIS</span></span>
<span data-ttu-id="662a6-103">建立資料庫輸入物件，其中包含移移來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="662a6-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="662a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="662a6-104">SYNTAX</span></span>

### <span data-ttu-id="662a6-105">MigrateSqlServerSqlDb (預設) </span><span class="sxs-lookup"><span data-stu-id="662a6-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="662a6-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="662a6-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="662a6-107">描述</span><span class="sxs-lookup"><span data-stu-id="662a6-107">DESCRIPTION</span></span>
<span data-ttu-id="662a6-108">此New-AzDataMigrationSelectedDB Cmdlet 會建立一個資料庫資訊物件，其中包含來源和目標資料庫，以及資料表的移轉資訊。</span><span class="sxs-lookup"><span data-stu-id="662a6-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="662a6-109">此 Cmdlet 可做為與 Cmdlet New-AzDataMigrationTask參數。</span><span class="sxs-lookup"><span data-stu-id="662a6-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="662a6-110">例子</span><span class="sxs-lookup"><span data-stu-id="662a6-110">EXAMPLES</span></span>

### <span data-ttu-id="662a6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="662a6-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="662a6-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="662a6-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="662a6-113">參數</span><span class="sxs-lookup"><span data-stu-id="662a6-113">PARAMETERS</span></span>

### <span data-ttu-id="662a6-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="662a6-114">-BackupFileShare</span></span>
<span data-ttu-id="662a6-115">應備份此資料庫之源伺服器資料庫檔案的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="662a6-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="662a6-116">使用此設定可覆蓋每個資料庫的檔案共用資訊。</span><span class="sxs-lookup"><span data-stu-id="662a6-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="662a6-117">針對伺服器使用完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="662a6-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662a6-118">-DefaultProfile</span></span>
<span data-ttu-id="662a6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="662a6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="662a6-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="662a6-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="662a6-121">在移移之前將資料庫設為唯讀</span><span class="sxs-lookup"><span data-stu-id="662a6-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662a6-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="662a6-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="662a6-123">將移移類型設定為 SQL Server 至 SQL DB 移移。</span><span class="sxs-lookup"><span data-stu-id="662a6-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662a6-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="662a6-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="662a6-125">將移移類型設定為 SQL Server 至 SQL DB MI 移移。</span><span class="sxs-lookup"><span data-stu-id="662a6-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662a6-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="662a6-126">-SourceDatabaseName</span></span>
<span data-ttu-id="662a6-127">源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="662a6-127">The name of the source database.</span></span>

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

### <span data-ttu-id="662a6-128">-表格地圖</span><span class="sxs-lookup"><span data-stu-id="662a6-128">-TableMap</span></span>
<span data-ttu-id="662a6-129">將來源與目標資料表的關聯</span><span class="sxs-lookup"><span data-stu-id="662a6-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662a6-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="662a6-130">-TargetDatabaseName</span></span>
<span data-ttu-id="662a6-131">目標資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="662a6-131">The name of the target database.</span></span>

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

### <span data-ttu-id="662a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662a6-132">CommonParameters</span></span>
<span data-ttu-id="662a6-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="662a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662a6-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="662a6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662a6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="662a6-135">INPUTS</span></span>

### <span data-ttu-id="662a6-136">Microsoft.Azure.management.DataMigration.models.FileShare</span><span class="sxs-lookup"><span data-stu-id="662a6-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="662a6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="662a6-137">OUTPUTS</span></span>

### <span data-ttu-id="662a6-138">Microsoft.Azure.management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="662a6-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="662a6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="662a6-139">NOTES</span></span>

## <span data-ttu-id="662a6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="662a6-140">RELATED LINKS</span></span>
