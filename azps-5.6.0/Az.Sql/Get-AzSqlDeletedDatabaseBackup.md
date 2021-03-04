---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: f64f7f7e16f18c9213c77df2903c17d8e7ea4ae1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914377"
---
# <span data-ttu-id="ef42e-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ef42e-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="ef42e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef42e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef42e-103">獲得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="ef42e-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="ef42e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef42e-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef42e-105">描述</span><span class="sxs-lookup"><span data-stu-id="ef42e-105">DESCRIPTION</span></span>
<span data-ttu-id="ef42e-106">**Get-AzSqlDeletedDatabaseBackup** Cmdlet 會取得指定的已刪除 SQL 資料庫備份，您可以還原或還原所有已刪除的備份。</span><span class="sxs-lookup"><span data-stu-id="ef42e-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="ef42e-107">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef42e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ef42e-108">例子</span><span class="sxs-lookup"><span data-stu-id="ef42e-108">EXAMPLES</span></span>

### <span data-ttu-id="ef42e-109">範例 1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="ef42e-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="ef42e-110">此命令會在伺服器上獲得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="ef42e-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="ef42e-111">範例 2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="ef42e-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="ef42e-112">此命令會針對 ContosoDatabase 獲得已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="ef42e-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="ef42e-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef42e-113">PARAMETERS</span></span>

### <span data-ttu-id="ef42e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef42e-114">-DatabaseName</span></span>
<span data-ttu-id="ef42e-115">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef42e-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef42e-116">-DefaultProfile</span></span>
<span data-ttu-id="ef42e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ef42e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef42e-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ef42e-118">-DeletionDate</span></span>
<span data-ttu-id="ef42e-119">指定刪除資料庫的日期 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="ef42e-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="ef42e-120">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef42e-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef42e-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef42e-122">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ef42e-122">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef42e-123">-ServerName</span></span>
<span data-ttu-id="ef42e-124">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef42e-124">Specifies the name of the database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ef42e-125">-Confirm</span></span>
<span data-ttu-id="ef42e-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef42e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef42e-127">-WhatIf</span></span>
<span data-ttu-id="ef42e-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef42e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef42e-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef42e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef42e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef42e-130">CommonParameters</span></span>
<span data-ttu-id="ef42e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef42e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef42e-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef42e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef42e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ef42e-133">INPUTS</span></span>

### <span data-ttu-id="ef42e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ef42e-134">System.String</span></span>

### <span data-ttu-id="ef42e-135">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef42e-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef42e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ef42e-136">OUTPUTS</span></span>

### <span data-ttu-id="ef42e-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="ef42e-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="ef42e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ef42e-138">NOTES</span></span>

## <span data-ttu-id="ef42e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef42e-139">RELATED LINKS</span></span>

[<span data-ttu-id="ef42e-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ef42e-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ef42e-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ef42e-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
