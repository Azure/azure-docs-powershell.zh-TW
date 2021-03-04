---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903945"
---
# <span data-ttu-id="09047-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="09047-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="09047-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09047-102">SYNOPSIS</span></span>
<span data-ttu-id="09047-103">為資料庫進行異地備份。</span><span class="sxs-lookup"><span data-stu-id="09047-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="09047-104">語法</span><span class="sxs-lookup"><span data-stu-id="09047-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09047-105">描述</span><span class="sxs-lookup"><span data-stu-id="09047-105">DESCRIPTION</span></span>
<span data-ttu-id="09047-106">**Get-AzSqlDatabaseGeoBackup** Cmdlet 會取得 SQL 資料庫的指定異地重複備份，或指定伺服器上所有可用的異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="09047-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="09047-107">異地重複備份是使用個別地理位置的資料檔案可還原的資源。</span><span class="sxs-lookup"><span data-stu-id="09047-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="09047-108">您可以在Geo-Restore中斷時還原異地重複備份，以將資料庫復原至新區域。</span><span class="sxs-lookup"><span data-stu-id="09047-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="09047-109">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09047-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="09047-110">例子</span><span class="sxs-lookup"><span data-stu-id="09047-110">EXAMPLES</span></span>

### <span data-ttu-id="09047-111">範例 1：在伺服器上取得所有異地重複備份</span><span class="sxs-lookup"><span data-stu-id="09047-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="09047-112">此命令會獲得指定伺服器上所有可用的異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="09047-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="09047-113">範例 2：取得指定的異地重複備份</span><span class="sxs-lookup"><span data-stu-id="09047-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="09047-114">此命令會獲得名為 ContosoDatabase 的資料庫異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="09047-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="09047-115">範例 3：使用篩選在伺服器上取得所有異地重複備份</span><span class="sxs-lookup"><span data-stu-id="09047-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="09047-116">此命令可在以 「Contoso」為開始的指定伺服器上，獲得所有可用的異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="09047-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="09047-117">參數</span><span class="sxs-lookup"><span data-stu-id="09047-117">PARAMETERS</span></span>

### <span data-ttu-id="09047-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09047-118">-DatabaseName</span></span>
<span data-ttu-id="09047-119">指定要取得的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="09047-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="09047-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09047-120">-DefaultProfile</span></span>
<span data-ttu-id="09047-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09047-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09047-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09047-122">-ResourceGroupName</span></span>
<span data-ttu-id="09047-123">指定指派給 SQL 資料庫伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09047-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="09047-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09047-124">-ServerName</span></span>
<span data-ttu-id="09047-125">指定主做要還原之備份的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="09047-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="09047-126">-確認</span><span class="sxs-lookup"><span data-stu-id="09047-126">-Confirm</span></span>
<span data-ttu-id="09047-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09047-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09047-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09047-128">-WhatIf</span></span>
<span data-ttu-id="09047-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09047-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09047-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09047-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09047-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09047-131">CommonParameters</span></span>
<span data-ttu-id="09047-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09047-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09047-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09047-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09047-134">輸入</span><span class="sxs-lookup"><span data-stu-id="09047-134">INPUTS</span></span>

### <span data-ttu-id="09047-135">System.String</span><span class="sxs-lookup"><span data-stu-id="09047-135">System.String</span></span>

## <span data-ttu-id="09047-136">輸出</span><span class="sxs-lookup"><span data-stu-id="09047-136">OUTPUTS</span></span>

### <span data-ttu-id="09047-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="09047-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="09047-138">筆記</span><span class="sxs-lookup"><span data-stu-id="09047-138">NOTES</span></span>

## <span data-ttu-id="09047-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="09047-139">RELATED LINKS</span></span>

[<span data-ttu-id="09047-140">概觀：使用 SQL Database 進行雲端業務連續性與資料庫災害復原</span><span class="sxs-lookup"><span data-stu-id="09047-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="09047-141">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="09047-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="09047-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09047-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="09047-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="09047-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
