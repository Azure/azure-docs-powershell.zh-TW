---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 2529057f7a2963c28175e18bacbc1aa3894a3eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904273"
---
# <span data-ttu-id="69cb9-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="69cb9-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="69cb9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="69cb9-103">從資料庫移除資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="69cb9-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="69cb9-104">語法</span><span class="sxs-lookup"><span data-stu-id="69cb9-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69cb9-105">描述</span><span class="sxs-lookup"><span data-stu-id="69cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="69cb9-106">**Remove-AzSqlDatabaseDataMaskingRule** Cmdlet 會從 Azure SQL 資料庫移除特定的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="69cb9-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="69cb9-107">您可以使用 ResourceGroupName、ServerName、DatabaseName和 *RuleId* 參數來移除資料遮罩規則，以識別此 Cmdlet 移除的規則。 </span><span class="sxs-lookup"><span data-stu-id="69cb9-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="69cb9-108">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69cb9-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="69cb9-109">例子</span><span class="sxs-lookup"><span data-stu-id="69cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="69cb9-110">範例 1：移除資料庫資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="69cb9-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="69cb9-111">此命令會移除為資料庫 Database01 定義的規則名稱 Rule01。</span><span class="sxs-lookup"><span data-stu-id="69cb9-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="69cb9-112">資料庫位於 Server01，並指派給資源群組 ResourceGroup01。</span><span class="sxs-lookup"><span data-stu-id="69cb9-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="69cb9-113">參數</span><span class="sxs-lookup"><span data-stu-id="69cb9-113">PARAMETERS</span></span>

### <span data-ttu-id="69cb9-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="69cb9-114">-ColumnName</span></span>
<span data-ttu-id="69cb9-115">指定遮罩規則所針對之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cb9-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="69cb9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69cb9-116">-DatabaseName</span></span>
<span data-ttu-id="69cb9-117">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cb9-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="69cb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69cb9-118">-DefaultProfile</span></span>
<span data-ttu-id="69cb9-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="69cb9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69cb9-120">-強制</span><span class="sxs-lookup"><span data-stu-id="69cb9-120">-Force</span></span>
<span data-ttu-id="69cb9-121">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="69cb9-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69cb9-122">-PassThru</span></span>
<span data-ttu-id="69cb9-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="69cb9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69cb9-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="69cb9-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69cb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="69cb9-126">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="69cb9-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="69cb9-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="69cb9-127">-SchemaName</span></span>
<span data-ttu-id="69cb9-128">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cb9-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="69cb9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69cb9-129">-ServerName</span></span>
<span data-ttu-id="69cb9-130">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="69cb9-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="69cb9-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="69cb9-131">-TableName</span></span>
<span data-ttu-id="69cb9-132">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cb9-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="69cb9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="69cb9-133">-Confirm</span></span>
<span data-ttu-id="69cb9-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69cb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69cb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69cb9-135">-WhatIf</span></span>
<span data-ttu-id="69cb9-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69cb9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69cb9-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69cb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69cb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69cb9-138">CommonParameters</span></span>
<span data-ttu-id="69cb9-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69cb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69cb9-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69cb9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69cb9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="69cb9-141">INPUTS</span></span>

### <span data-ttu-id="69cb9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69cb9-142">System.String</span></span>

## <span data-ttu-id="69cb9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="69cb9-143">OUTPUTS</span></span>

### <span data-ttu-id="69cb9-144">Microsoft.Azure.Commands.sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="69cb9-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="69cb9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="69cb9-145">NOTES</span></span>

## <span data-ttu-id="69cb9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="69cb9-146">RELATED LINKS</span></span>

[<span data-ttu-id="69cb9-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="69cb9-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="69cb9-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="69cb9-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="69cb9-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="69cb9-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="69cb9-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="69cb9-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


