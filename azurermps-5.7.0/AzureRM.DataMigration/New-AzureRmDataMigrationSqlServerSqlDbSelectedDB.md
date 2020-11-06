---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448688"
---
# <span data-ttu-id="fd559-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="fd559-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="fd559-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd559-102">SYNOPSIS</span></span>
<span data-ttu-id="fd559-103">建立一個 MigrateSqlServerSqlDbDatabaseInput 物件，其中包含有關要遷移之來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="fd559-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd559-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd559-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="fd559-105">說明</span><span class="sxs-lookup"><span data-stu-id="fd559-105">DESCRIPTION</span></span>
<span data-ttu-id="fd559-106">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB Cmdlet 會建立一個 MigrateSqlServerSqlDbDatabaseInput 物件，其中包含來源和目標資料庫的相關資訊，以及用於遷移的資料表對應。</span><span class="sxs-lookup"><span data-stu-id="fd559-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="fd559-107">這個 Cmdlet 可以用來做為 New-AzureRmDataMigrationTask Cmdlet 的參數。</span><span class="sxs-lookup"><span data-stu-id="fd559-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="fd559-108">示例</span><span class="sxs-lookup"><span data-stu-id="fd559-108">EXAMPLES</span></span>

### <span data-ttu-id="fd559-109">範例1</span><span class="sxs-lookup"><span data-stu-id="fd559-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="fd559-110">上述範例會建立 MigrateSqlServerSqlDbDatabaseInput 物件，以將 **AdventureWorks2016** 資料庫移轉至具有相同名稱的 SQL Azure 資料庫。</span><span class="sxs-lookup"><span data-stu-id="fd559-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="fd559-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd559-111">PARAMETERS</span></span>

### <span data-ttu-id="fd559-112">-確認</span><span class="sxs-lookup"><span data-stu-id="fd559-112">-Confirm</span></span>
<span data-ttu-id="fd559-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fd559-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd559-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd559-114">-DefaultProfile</span></span>
<span data-ttu-id="fd559-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd559-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd559-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="fd559-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="fd559-117">在遷移前將資料庫設為 readonly</span><span class="sxs-lookup"><span data-stu-id="fd559-117">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="fd559-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd559-118">-Name</span></span>
<span data-ttu-id="fd559-119">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd559-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd559-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="fd559-120">-TableMap</span></span>
<span data-ttu-id="fd559-121">將來源對應至目標資料表</span><span class="sxs-lookup"><span data-stu-id="fd559-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd559-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd559-122">-TargetDatabaseName</span></span>
<span data-ttu-id="fd559-123">目標資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd559-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="fd559-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fd559-124">INPUTS</span></span>

### <span data-ttu-id="fd559-125">所有</span><span class="sxs-lookup"><span data-stu-id="fd559-125">None</span></span>


## <span data-ttu-id="fd559-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fd559-126">OUTPUTS</span></span>

### <span data-ttu-id="fd559-127">MigrateSqlServerSqlDbDatabaseInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="fd559-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="fd559-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fd559-128">NOTES</span></span>

## <span data-ttu-id="fd559-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd559-129">RELATED LINKS</span></span>


