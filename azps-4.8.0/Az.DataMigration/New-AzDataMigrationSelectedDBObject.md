---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969285"
---
# <span data-ttu-id="2a5be-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2a5be-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="2a5be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a5be-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5be-103">建立一個資料庫輸入物件，其中包含有關要遷移之來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="2a5be-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="2a5be-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a5be-104">SYNTAX</span></span>

### <span data-ttu-id="2a5be-105">MigrateSqlServerSqlDb (預設) </span><span class="sxs-lookup"><span data-stu-id="2a5be-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a5be-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="2a5be-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a5be-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a5be-107">DESCRIPTION</span></span>
<span data-ttu-id="2a5be-108">New-AzDataMigrationSelectedDB Cmdlet 會建立一個資料庫資訊物件，其中包含有關來源和目標資料庫的資訊，以及用於遷移的資料表對應資訊。</span><span class="sxs-lookup"><span data-stu-id="2a5be-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="2a5be-109">這個 Cmdlet 可以用來做為 New-AzDataMigrationTask Cmdlet 的參數。</span><span class="sxs-lookup"><span data-stu-id="2a5be-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="2a5be-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a5be-110">EXAMPLES</span></span>

### <span data-ttu-id="2a5be-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2a5be-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="2a5be-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2a5be-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="2a5be-113">參數</span><span class="sxs-lookup"><span data-stu-id="2a5be-113">PARAMETERS</span></span>

### <span data-ttu-id="2a5be-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="2a5be-114">-BackupFileShare</span></span>
<span data-ttu-id="2a5be-115">檔案共用：此資料庫的源伺服器資料庫檔案應該備份。</span><span class="sxs-lookup"><span data-stu-id="2a5be-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="2a5be-116">使用此設定來覆寫每個資料庫的檔案共用資訊。</span><span class="sxs-lookup"><span data-stu-id="2a5be-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="2a5be-117">針對伺服器使用完整的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="2a5be-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="2a5be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5be-118">-DefaultProfile</span></span>
<span data-ttu-id="2a5be-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a5be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5be-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="2a5be-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="2a5be-121">在遷移前將資料庫設為 readonly</span><span class="sxs-lookup"><span data-stu-id="2a5be-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="2a5be-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="2a5be-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="2a5be-123">將遷移類型設定為 SQL Server 以進行 SQL 資料庫遷移。</span><span class="sxs-lookup"><span data-stu-id="2a5be-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="2a5be-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="2a5be-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="2a5be-125">將遷移類型設定為 SQL Server 以進行 SQL 資料庫 MI 遷移。</span><span class="sxs-lookup"><span data-stu-id="2a5be-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="2a5be-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a5be-126">-SourceDatabaseName</span></span>
<span data-ttu-id="2a5be-127">來源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a5be-127">The name of the source database.</span></span>

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

### <span data-ttu-id="2a5be-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="2a5be-128">-TableMap</span></span>
<span data-ttu-id="2a5be-129">將來源對應至目標資料表</span><span class="sxs-lookup"><span data-stu-id="2a5be-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="2a5be-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a5be-130">-TargetDatabaseName</span></span>
<span data-ttu-id="2a5be-131">目標資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a5be-131">The name of the target database.</span></span>

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

### <span data-ttu-id="2a5be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5be-132">CommonParameters</span></span>
<span data-ttu-id="2a5be-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a5be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5be-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a5be-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5be-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2a5be-135">INPUTS</span></span>

### <span data-ttu-id="2a5be-136">DataMigration.................。</span><span class="sxs-lookup"><span data-stu-id="2a5be-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="2a5be-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2a5be-137">OUTPUTS</span></span>

### <span data-ttu-id="2a5be-138">MigrateSqlServerSqlDbDatabaseInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="2a5be-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="2a5be-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2a5be-139">NOTES</span></span>

## <span data-ttu-id="2a5be-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a5be-140">RELATED LINKS</span></span>
