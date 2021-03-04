---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912549"
---
# <span data-ttu-id="5c734-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="5c734-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="5c734-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c734-102">SYNOPSIS</span></span>
<span data-ttu-id="5c734-103">獲得資料庫作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5c734-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="5c734-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c734-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c734-105">描述</span><span class="sxs-lookup"><span data-stu-id="5c734-105">DESCRIPTION</span></span>
<span data-ttu-id="5c734-106">**Get-AzSqlDatabaseActivity** Cmdlet 會取得 Azure SQL Database 中的資料庫作業狀態。</span><span class="sxs-lookup"><span data-stu-id="5c734-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="5c734-107">例子</span><span class="sxs-lookup"><span data-stu-id="5c734-107">EXAMPLES</span></span>

### <span data-ttu-id="5c734-108">範例 1：取得所有 SQL Database 實例的狀態</span><span class="sxs-lookup"><span data-stu-id="5c734-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5c734-109">此命令會以一個名為Pool01 的彈性資料庫，會返回所有 SQL Database 實例的作業狀態。</span><span class="sxs-lookup"><span data-stu-id="5c734-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="5c734-110">範例 2：取得所有 SQL Database 作業的狀態</span><span class="sxs-lookup"><span data-stu-id="5c734-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5c734-111">此命令會返回資料庫中所有 SQL Database 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5c734-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="5c734-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c734-112">PARAMETERS</span></span>

### <span data-ttu-id="5c734-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c734-113">-DatabaseName</span></span>
<span data-ttu-id="5c734-114">指定此 Cmdlet 會進入狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5c734-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c734-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c734-115">-DefaultProfile</span></span>
<span data-ttu-id="5c734-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c734-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c734-117">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="5c734-117">-ElasticPoolName</span></span>
<span data-ttu-id="5c734-118">指定此 Cmdlet 會獲得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c734-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c734-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5c734-119">-OperationId</span></span>
<span data-ttu-id="5c734-120">指定此 Cmdlet 所進行作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c734-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c734-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c734-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c734-122">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c734-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5c734-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c734-123">-ServerName</span></span>
<span data-ttu-id="5c734-124">指定主託管資料庫的 Microsoft SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c734-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="5c734-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5c734-125">-Confirm</span></span>
<span data-ttu-id="5c734-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c734-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c734-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c734-127">-WhatIf</span></span>
<span data-ttu-id="5c734-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c734-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c734-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c734-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c734-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c734-130">CommonParameters</span></span>
<span data-ttu-id="5c734-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c734-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c734-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c734-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c734-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5c734-133">INPUTS</span></span>

### <span data-ttu-id="5c734-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5c734-134">System.String</span></span>

### <span data-ttu-id="5c734-135">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5c734-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5c734-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5c734-136">OUTPUTS</span></span>

### <span data-ttu-id="5c734-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="5c734-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="5c734-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5c734-138">NOTES</span></span>

## <span data-ttu-id="5c734-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c734-139">RELATED LINKS</span></span>
