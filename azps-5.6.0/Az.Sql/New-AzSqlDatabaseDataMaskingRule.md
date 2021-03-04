---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b453c11d7a6e63e5365bca5cd186002f66ed13cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913298"
---
# <span data-ttu-id="860ff-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="860ff-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="860ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="860ff-102">SYNOPSIS</span></span>
<span data-ttu-id="860ff-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="860ff-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="860ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="860ff-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="860ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="860ff-105">DESCRIPTION</span></span>
<span data-ttu-id="860ff-106">**New-AzSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="860ff-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="860ff-107">若要使用 Cmdlet，請使用 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="860ff-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="860ff-108">提供 *TableName* 和 *ColumnName* 以指定規則的目標，並提供 *MaskingFunction* 參數來定義資料的遮罩方法。</span><span class="sxs-lookup"><span data-stu-id="860ff-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="860ff-109">如果 *MaskingFunction* 有 Number 或 Text 的值，您可以指定 *NumberFrom* 和 *NumberTo* 參數來設定數位遮罩，或是指定文字遮罩的 *首碼Size、ReplacementString* 和 *SuffixSize。* </span><span class="sxs-lookup"><span data-stu-id="860ff-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="860ff-110">如果命令成功且 *使用 PassThru* 參數，Cmdlet 會傳回描述除了規則識別碼之外的資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="860ff-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="860ff-111">規則識別碼包含但不限於 ResourceGroupName、ServerName、DatabaseName和 *RuleID。* </span><span class="sxs-lookup"><span data-stu-id="860ff-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="860ff-112">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="860ff-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="860ff-113">例子</span><span class="sxs-lookup"><span data-stu-id="860ff-113">EXAMPLES</span></span>

### <span data-ttu-id="860ff-114">範例 1：為資料庫中的數位欄建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="860ff-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="860ff-115">此命令會針對架構名為 Schema01 的 Table01 資料表中名為 Column01 的資料行建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="860ff-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="860ff-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="860ff-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="860ff-117">規則是一種數位遮罩規則，使用介於 5 到 14 之間的亂數字做為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="860ff-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="860ff-118">參數</span><span class="sxs-lookup"><span data-stu-id="860ff-118">PARAMETERS</span></span>

### <span data-ttu-id="860ff-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="860ff-119">-ColumnName</span></span>
<span data-ttu-id="860ff-120">指定遮罩規則所針對之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="860ff-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="860ff-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="860ff-121">-DatabaseName</span></span>
<span data-ttu-id="860ff-122">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="860ff-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="860ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860ff-123">-DefaultProfile</span></span>
<span data-ttu-id="860ff-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="860ff-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="860ff-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="860ff-125">-MaskingFunction</span></span>
<span data-ttu-id="860ff-126">指定規則使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="860ff-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="860ff-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="860ff-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="860ff-128">預設</span><span class="sxs-lookup"><span data-stu-id="860ff-128">Default</span></span>
- <span data-ttu-id="860ff-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="860ff-129">NoMasking</span></span>
- <span data-ttu-id="860ff-130">文本</span><span class="sxs-lookup"><span data-stu-id="860ff-130">Text</span></span>
- <span data-ttu-id="860ff-131">數量</span><span class="sxs-lookup"><span data-stu-id="860ff-131">Number</span></span>
- <span data-ttu-id="860ff-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="860ff-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="860ff-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="860ff-133">CreditCardNumber</span></span>
- <span data-ttu-id="860ff-134">電子郵件 預設值為預設值。</span><span class="sxs-lookup"><span data-stu-id="860ff-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860ff-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="860ff-135">-NumberFrom</span></span>
<span data-ttu-id="860ff-136">指定選取隨機值之區間的下限。</span><span class="sxs-lookup"><span data-stu-id="860ff-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="860ff-137">只有在您為 *MaskingFunction* 參數指定 Number 值時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860ff-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="860ff-138">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="860ff-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860ff-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="860ff-139">-NumberTo</span></span>
<span data-ttu-id="860ff-140">指定選取隨機值之區間的上限。</span><span class="sxs-lookup"><span data-stu-id="860ff-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="860ff-141">只有在您為 *MaskingFunction* 參數指定 Number 值時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860ff-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="860ff-142">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="860ff-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860ff-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="860ff-143">-PassThru</span></span>
<span data-ttu-id="860ff-144">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="860ff-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="860ff-145">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="860ff-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="860ff-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="860ff-146">-PrefixSize</span></span>
<span data-ttu-id="860ff-147">指定文字開始時未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="860ff-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="860ff-148">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860ff-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="860ff-149">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="860ff-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860ff-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="860ff-150">-ReplacementString</span></span>
<span data-ttu-id="860ff-151">指定文字結尾中未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="860ff-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="860ff-152">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860ff-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="860ff-153">預設值為空白字串。</span><span class="sxs-lookup"><span data-stu-id="860ff-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="860ff-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860ff-154">-ResourceGroupName</span></span>
<span data-ttu-id="860ff-155">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="860ff-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="860ff-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="860ff-156">-SchemaName</span></span>
<span data-ttu-id="860ff-157">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="860ff-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="860ff-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="860ff-158">-ServerName</span></span>
<span data-ttu-id="860ff-159">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="860ff-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="860ff-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="860ff-160">-SuffixSize</span></span>
<span data-ttu-id="860ff-161">指定文字結尾未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="860ff-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="860ff-162">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860ff-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="860ff-163">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="860ff-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860ff-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="860ff-164">-TableName</span></span>
<span data-ttu-id="860ff-165">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="860ff-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="860ff-166">-確認</span><span class="sxs-lookup"><span data-stu-id="860ff-166">-Confirm</span></span>
<span data-ttu-id="860ff-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="860ff-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="860ff-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860ff-168">-WhatIf</span></span>
<span data-ttu-id="860ff-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="860ff-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="860ff-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="860ff-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="860ff-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860ff-171">CommonParameters</span></span>
<span data-ttu-id="860ff-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="860ff-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860ff-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="860ff-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860ff-174">輸入</span><span class="sxs-lookup"><span data-stu-id="860ff-174">INPUTS</span></span>

### <span data-ttu-id="860ff-175">System.String</span><span class="sxs-lookup"><span data-stu-id="860ff-175">System.String</span></span>

### <span data-ttu-id="860ff-176">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="860ff-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="860ff-177">System.Nullable'1[[System.Double， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="860ff-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="860ff-178">輸出</span><span class="sxs-lookup"><span data-stu-id="860ff-178">OUTPUTS</span></span>

### <span data-ttu-id="860ff-179">Microsoft.Azure.Commands.sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="860ff-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="860ff-180">筆記</span><span class="sxs-lookup"><span data-stu-id="860ff-180">NOTES</span></span>

## <span data-ttu-id="860ff-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="860ff-181">RELATED LINKS</span></span>

[<span data-ttu-id="860ff-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="860ff-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="860ff-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="860ff-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="860ff-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="860ff-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="860ff-185">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="860ff-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


