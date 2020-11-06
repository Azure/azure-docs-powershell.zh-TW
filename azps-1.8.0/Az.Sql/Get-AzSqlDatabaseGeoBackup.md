---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 07f6e9b01e3def2dfe7cc88602b9643344ff3c4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620478"
---
# <span data-ttu-id="ea0e9-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ea0e9-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="ea0e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0e9-103">取得資料庫的地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="ea0e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea0e9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea0e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0e9-106">**AzSqlDatabaseGeoBackup** Cmdlet 會在指定的伺服器上取得 SQL 資料庫或所有可用地域冗余備份的特定地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="ea0e9-107">地域冗余備份是從個別地理位置使用資料檔案的可還原資源。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="ea0e9-108">在區域停用期間，您可以使用 Geo-Restore 來還原地域冗余備份，以將您的資料庫復原至新的區域。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="ea0e9-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ea0e9-110">示例</span><span class="sxs-lookup"><span data-stu-id="ea0e9-110">EXAMPLES</span></span>

### <span data-ttu-id="ea0e9-111">範例1：在伺服器上取得所有地域冗余備份</span><span class="sxs-lookup"><span data-stu-id="ea0e9-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="ea0e9-112">這個命令會在指定的伺服器上取得所有可用地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="ea0e9-113">範例2：取得特定地域冗余備份</span><span class="sxs-lookup"><span data-stu-id="ea0e9-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="ea0e9-114">這個命令會取得名為 ContosoDatabase 的資料庫地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="ea0e9-115">範例3：使用篩選在伺服器上取得所有地域冗余備份</span><span class="sxs-lookup"><span data-stu-id="ea0e9-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="ea0e9-116">這個命令會在以 "Contoso" 開頭的指定伺服器上取得所有可用地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="ea0e9-117">參數</span><span class="sxs-lookup"><span data-stu-id="ea0e9-117">PARAMETERS</span></span>

### <span data-ttu-id="ea0e9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea0e9-118">-DatabaseName</span></span>
<span data-ttu-id="ea0e9-119">指定要取得之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ea0e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0e9-120">-DefaultProfile</span></span>
<span data-ttu-id="ea0e9-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ea0e9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea0e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea0e9-123">指定 SQL 資料庫伺服器指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="ea0e9-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea0e9-124">-ServerName</span></span>
<span data-ttu-id="ea0e9-125">指定主持備份要還原的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="ea0e9-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ea0e9-126">-Confirm</span></span>
<span data-ttu-id="ea0e9-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0e9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0e9-128">-WhatIf</span></span>
<span data-ttu-id="ea0e9-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0e9-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0e9-131">CommonParameters</span></span>
<span data-ttu-id="ea0e9-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0e9-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0e9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ea0e9-134">INPUTS</span></span>

### <span data-ttu-id="ea0e9-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ea0e9-135">System.String</span></span>

## <span data-ttu-id="ea0e9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ea0e9-136">OUTPUTS</span></span>

### <span data-ttu-id="ea0e9-137">AzureSqlDatabaseGeoBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="ea0e9-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="ea0e9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ea0e9-138">NOTES</span></span>

## <span data-ttu-id="ea0e9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea0e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea0e9-140">概覽：使用 SQL Database 進行雲端業務連續性與資料庫災害復原</span><span class="sxs-lookup"><span data-stu-id="ea0e9-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="ea0e9-141">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="ea0e9-141">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="ea0e9-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea0e9-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="ea0e9-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ea0e9-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
