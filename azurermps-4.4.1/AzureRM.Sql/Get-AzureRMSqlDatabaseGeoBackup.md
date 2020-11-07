---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626210"
---
# <span data-ttu-id="1a08e-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="1a08e-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="1a08e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a08e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a08e-103">取得資料庫的地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="1a08e-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a08e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a08e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a08e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1a08e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a08e-106">**AzureRMSqlDatabaseGeoBackup** Cmdlet 會在指定的伺服器上取得 SQL 資料庫或所有可用地域冗余備份的特定地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="1a08e-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="1a08e-107">地域冗余備份是從個別地理位置使用資料檔案的可還原資源。</span><span class="sxs-lookup"><span data-stu-id="1a08e-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="1a08e-108">在區域停用期間，您可以使用 Geo-Restore 來還原地域冗余備份，以將您的資料庫復原至新的區域。</span><span class="sxs-lookup"><span data-stu-id="1a08e-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="1a08e-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a08e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1a08e-110">示例</span><span class="sxs-lookup"><span data-stu-id="1a08e-110">EXAMPLES</span></span>

### <span data-ttu-id="1a08e-111">範例1：在伺服器上取得所有地域冗余備份</span><span class="sxs-lookup"><span data-stu-id="1a08e-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="1a08e-112">這個命令會在指定的伺服器上取得所有可用地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="1a08e-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="1a08e-113">範例2：取得特定地域冗余備份</span><span class="sxs-lookup"><span data-stu-id="1a08e-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="1a08e-114">這個命令會取得名為 ContosoDatabase 的資料庫地域冗余備份。</span><span class="sxs-lookup"><span data-stu-id="1a08e-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="1a08e-115">參數</span><span class="sxs-lookup"><span data-stu-id="1a08e-115">PARAMETERS</span></span>

### <span data-ttu-id="1a08e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a08e-116">-DatabaseName</span></span>
<span data-ttu-id="1a08e-117">指定要取得之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a08e-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="1a08e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a08e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a08e-119">指定 SQL 資料庫伺服器指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a08e-119">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="1a08e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a08e-120">-ServerName</span></span>
<span data-ttu-id="1a08e-121">指定主持備份要還原的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1a08e-121">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="1a08e-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1a08e-122">-Confirm</span></span>
<span data-ttu-id="1a08e-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a08e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a08e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a08e-124">-WhatIf</span></span>
<span data-ttu-id="1a08e-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a08e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a08e-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a08e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a08e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a08e-127">-DefaultProfile</span></span>
<span data-ttu-id="1a08e-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a08e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a08e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a08e-129">CommonParameters</span></span>
<span data-ttu-id="1a08e-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a08e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a08e-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a08e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a08e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1a08e-132">INPUTS</span></span>

## <span data-ttu-id="1a08e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1a08e-133">OUTPUTS</span></span>

### <span data-ttu-id="1a08e-134">AzureSqlDatabaseGeoBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="1a08e-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="1a08e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1a08e-135">NOTES</span></span>

## <span data-ttu-id="1a08e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a08e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a08e-137">概覽：使用 SQL Database 進行雲端業務連續性與資料庫災害復原</span><span class="sxs-lookup"><span data-stu-id="1a08e-137">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="1a08e-138">從中斷中復原 Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="1a08e-138">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="1a08e-139">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1a08e-139">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="1a08e-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1a08e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
