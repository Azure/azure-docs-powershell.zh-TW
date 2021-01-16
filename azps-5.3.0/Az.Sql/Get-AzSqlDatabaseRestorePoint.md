---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285708"
---
# <span data-ttu-id="f6813-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f6813-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="f6813-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6813-102">SYNOPSIS</span></span>
<span data-ttu-id="f6813-103">檢索可還原 SQL 資料倉儲的不同還原點。</span><span class="sxs-lookup"><span data-stu-id="f6813-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="f6813-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6813-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6813-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6813-105">DESCRIPTION</span></span>
<span data-ttu-id="f6813-106">**AzSqlDatabaseRestorePoint** Cmdlet 會檢索 Azure SQL 資料倉儲可以還原的不同還原點。</span><span class="sxs-lookup"><span data-stu-id="f6813-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="f6813-107">針對 Azure SQL 資料庫，[還原] 視窗是連續的。</span><span class="sxs-lookup"><span data-stu-id="f6813-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="f6813-108">這表示資料庫備份保留期間中的任何時間點都可以用來做為還原點。</span><span class="sxs-lookup"><span data-stu-id="f6813-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="f6813-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6813-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f6813-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6813-110">EXAMPLES</span></span>

### <span data-ttu-id="f6813-111">範例1：取得所有還原點</span><span class="sxs-lookup"><span data-stu-id="f6813-111">Example 1: Get all restore points</span></span>
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

<span data-ttu-id="f6813-112">這個命令會傳回 Azure SQL Database （名為 Database01）所有可用的還原點。</span><span class="sxs-lookup"><span data-stu-id="f6813-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="f6813-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6813-113">PARAMETERS</span></span>

### <span data-ttu-id="f6813-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6813-114">-DatabaseName</span></span>
<span data-ttu-id="f6813-115">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6813-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="f6813-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6813-116">-DefaultProfile</span></span>
<span data-ttu-id="f6813-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6813-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6813-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6813-118">-ResourceGroupName</span></span>
<span data-ttu-id="f6813-119">指定指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6813-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="f6813-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6813-120">-ServerName</span></span>
<span data-ttu-id="f6813-121">指定裝載資料庫之 AzureSQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6813-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="f6813-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f6813-122">-Confirm</span></span>
<span data-ttu-id="f6813-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6813-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6813-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6813-124">-WhatIf</span></span>
<span data-ttu-id="f6813-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6813-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6813-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6813-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6813-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6813-127">CommonParameters</span></span>
<span data-ttu-id="f6813-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6813-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6813-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6813-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6813-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f6813-130">INPUTS</span></span>

### <span data-ttu-id="f6813-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f6813-131">System.String</span></span>

## <span data-ttu-id="f6813-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f6813-132">OUTPUTS</span></span>

### <span data-ttu-id="f6813-133">AzureSqlDatabaseRestorePointModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="f6813-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="f6813-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f6813-134">NOTES</span></span>

## <span data-ttu-id="f6813-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6813-135">RELATED LINKS</span></span>
