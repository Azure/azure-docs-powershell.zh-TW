---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: aefcbe869dd8564e2225d478e95980558ba67bb3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917610"
---
# <span data-ttu-id="c8260-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c8260-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="c8260-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8260-102">SYNOPSIS</span></span>
<span data-ttu-id="c8260-103">會取回可還原 SQL 資料倉儲的明顯還原點。</span><span class="sxs-lookup"><span data-stu-id="c8260-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="c8260-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8260-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8260-105">描述</span><span class="sxs-lookup"><span data-stu-id="c8260-105">DESCRIPTION</span></span>
<span data-ttu-id="c8260-106">**Get-AzSqlDatabaseRestorePoint** Cmdlet 會從 Azure SQL Data Warehouse 中取得可還原的還原點。</span><span class="sxs-lookup"><span data-stu-id="c8260-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="c8260-107">對於 Azure SQL Database，還原視窗是連續的。</span><span class="sxs-lookup"><span data-stu-id="c8260-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="c8260-108">這表示資料庫備份保留期間的任何時間點都可以做為還原點。</span><span class="sxs-lookup"><span data-stu-id="c8260-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="c8260-109">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8260-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c8260-110">例子</span><span class="sxs-lookup"><span data-stu-id="c8260-110">EXAMPLES</span></span>

### <span data-ttu-id="c8260-111">範例 1：取得所有還原點</span><span class="sxs-lookup"><span data-stu-id="c8260-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="c8260-112">此命令會針對名為 Database01 的 Azure SQL Database，會返回所有可用的還原點。</span><span class="sxs-lookup"><span data-stu-id="c8260-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="c8260-113">參數</span><span class="sxs-lookup"><span data-stu-id="c8260-113">PARAMETERS</span></span>

### <span data-ttu-id="c8260-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8260-114">-DatabaseName</span></span>
<span data-ttu-id="c8260-115">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8260-115">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8260-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8260-116">-DefaultProfile</span></span>
<span data-ttu-id="c8260-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c8260-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8260-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8260-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8260-119">指定指派給 SQL Database 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c8260-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="c8260-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8260-120">-ServerName</span></span>
<span data-ttu-id="c8260-121">指定主託管資料庫的 AzureSQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c8260-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="c8260-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c8260-122">-Confirm</span></span>
<span data-ttu-id="c8260-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8260-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8260-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8260-124">-WhatIf</span></span>
<span data-ttu-id="c8260-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8260-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8260-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8260-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8260-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8260-127">CommonParameters</span></span>
<span data-ttu-id="c8260-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8260-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8260-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8260-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8260-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c8260-130">INPUTS</span></span>

### <span data-ttu-id="c8260-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c8260-131">System.String</span></span>

## <span data-ttu-id="c8260-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c8260-132">OUTPUTS</span></span>

### <span data-ttu-id="c8260-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="c8260-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="c8260-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c8260-134">NOTES</span></span>

## <span data-ttu-id="c8260-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8260-135">RELATED LINKS</span></span>
