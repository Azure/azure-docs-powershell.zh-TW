---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137046"
---
# <span data-ttu-id="66fd3-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fd3-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="66fd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="66fd3-103">從資料庫移除資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="66fd3-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="66fd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="66fd3-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fd3-105">說明</span><span class="sxs-lookup"><span data-stu-id="66fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="66fd3-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會將特定的資料遮罩規則從 Azure SQL 資料庫中移除。</span><span class="sxs-lookup"><span data-stu-id="66fd3-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="66fd3-107">您可以使用 *ResourceGroupName*、 *ServerName*、 *DatabaseName* 和 *RuleId* 參數來移除資料遮罩規則，以識別此 Cmdlet 移除的規則。</span><span class="sxs-lookup"><span data-stu-id="66fd3-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="66fd3-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66fd3-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="66fd3-109">示例</span><span class="sxs-lookup"><span data-stu-id="66fd3-109">EXAMPLES</span></span>

### <span data-ttu-id="66fd3-110">範例1：移除資料庫資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="66fd3-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="66fd3-111">這個命令會移除為資料庫 Database01 定義的規則名稱 Rule01。</span><span class="sxs-lookup"><span data-stu-id="66fd3-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="66fd3-112">資料庫位於 Server01 上，且已指派給資源群組 ResourceGroup01。</span><span class="sxs-lookup"><span data-stu-id="66fd3-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="66fd3-113">參數</span><span class="sxs-lookup"><span data-stu-id="66fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="66fd3-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="66fd3-114">-ColumnName</span></span>
<span data-ttu-id="66fd3-115">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="66fd3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66fd3-116">-DatabaseName</span></span>
<span data-ttu-id="66fd3-117">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="66fd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fd3-118">-DefaultProfile</span></span>
<span data-ttu-id="66fd3-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="66fd3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66fd3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="66fd3-120">-Force</span></span>
<span data-ttu-id="66fd3-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="66fd3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66fd3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66fd3-122">-PassThru</span></span>
<span data-ttu-id="66fd3-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="66fd3-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66fd3-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="66fd3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66fd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="66fd3-126">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="66fd3-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="66fd3-127">-SchemaName</span></span>
<span data-ttu-id="66fd3-128">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="66fd3-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66fd3-129">-ServerName</span></span>
<span data-ttu-id="66fd3-130">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="66fd3-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="66fd3-131">-TableName</span></span>
<span data-ttu-id="66fd3-132">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="66fd3-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="66fd3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="66fd3-133">-Confirm</span></span>
<span data-ttu-id="66fd3-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66fd3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fd3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fd3-135">-WhatIf</span></span>
<span data-ttu-id="66fd3-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66fd3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fd3-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66fd3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fd3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fd3-138">CommonParameters</span></span>
<span data-ttu-id="66fd3-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66fd3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fd3-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66fd3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fd3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="66fd3-141">INPUTS</span></span>

### <span data-ttu-id="66fd3-142">System.object</span><span class="sxs-lookup"><span data-stu-id="66fd3-142">System.String</span></span>

## <span data-ttu-id="66fd3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="66fd3-143">OUTPUTS</span></span>

### <span data-ttu-id="66fd3-144">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="66fd3-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="66fd3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="66fd3-145">NOTES</span></span>

## <span data-ttu-id="66fd3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="66fd3-146">RELATED LINKS</span></span>

[<span data-ttu-id="66fd3-147">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fd3-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fd3-148">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fd3-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fd3-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fd3-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fd3-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="66fd3-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


