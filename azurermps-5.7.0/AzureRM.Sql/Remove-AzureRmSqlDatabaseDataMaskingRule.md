---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: d20e6f838370e73dc4d6ff849e6088df9b9f28cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453012"
---
# <span data-ttu-id="ccde9-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ccde9-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ccde9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccde9-102">SYNOPSIS</span></span>
<span data-ttu-id="ccde9-103">從資料庫移除資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ccde9-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccde9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccde9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccde9-105">說明</span><span class="sxs-lookup"><span data-stu-id="ccde9-105">DESCRIPTION</span></span>
<span data-ttu-id="ccde9-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會將特定的資料遮罩規則從 Azure SQL 資料庫中移除。</span><span class="sxs-lookup"><span data-stu-id="ccde9-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="ccde9-107">您可以使用 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 和 *RuleId* 參數來移除資料遮罩規則，以識別此 Cmdlet 移除的規則。</span><span class="sxs-lookup"><span data-stu-id="ccde9-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="ccde9-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccde9-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ccde9-109">示例</span><span class="sxs-lookup"><span data-stu-id="ccde9-109">EXAMPLES</span></span>

### <span data-ttu-id="ccde9-110">範例1：移除資料庫資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="ccde9-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="ccde9-111">這個命令會移除為資料庫 Database01 定義的規則名稱 Rule01。</span><span class="sxs-lookup"><span data-stu-id="ccde9-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="ccde9-112">資料庫位於 Server01 上，且已指派給資源群組 ResourceGroup01。</span><span class="sxs-lookup"><span data-stu-id="ccde9-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ccde9-113">參數</span><span class="sxs-lookup"><span data-stu-id="ccde9-113">PARAMETERS</span></span>

### <span data-ttu-id="ccde9-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ccde9-114">-ColumnName</span></span>
<span data-ttu-id="ccde9-115">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccde9-116">-DatabaseName</span></span>
<span data-ttu-id="ccde9-117">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-117">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccde9-118">-DefaultProfile</span></span>
<span data-ttu-id="ccde9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ccde9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccde9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ccde9-120">-Force</span></span>
<span data-ttu-id="ccde9-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ccde9-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccde9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccde9-122">-PassThru</span></span>
<span data-ttu-id="ccde9-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ccde9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ccde9-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ccde9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccde9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccde9-125">-ResourceGroupName</span></span>
<span data-ttu-id="ccde9-126">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-126">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ccde9-127">-SchemaName</span></span>
<span data-ttu-id="ccde9-128">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-128">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccde9-129">-ServerName</span></span>
<span data-ttu-id="ccde9-130">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-130">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="ccde9-131">-TableName</span></span>
<span data-ttu-id="ccde9-132">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccde9-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ccde9-133">-Confirm</span></span>
<span data-ttu-id="ccde9-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ccde9-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccde9-135">-WhatIf</span></span>
<span data-ttu-id="ccde9-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccde9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccde9-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccde9-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccde9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccde9-138">CommonParameters</span></span>
<span data-ttu-id="ccde9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccde9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccde9-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ccde9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccde9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ccde9-141">INPUTS</span></span>

### <span data-ttu-id="ccde9-142">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="ccde9-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ccde9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ccde9-143">OUTPUTS</span></span>

### <span data-ttu-id="ccde9-144">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="ccde9-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ccde9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ccde9-145">NOTES</span></span>

## <span data-ttu-id="ccde9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccde9-146">RELATED LINKS</span></span>

[<span data-ttu-id="ccde9-147">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ccde9-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ccde9-148">新-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ccde9-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ccde9-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ccde9-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ccde9-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ccde9-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

