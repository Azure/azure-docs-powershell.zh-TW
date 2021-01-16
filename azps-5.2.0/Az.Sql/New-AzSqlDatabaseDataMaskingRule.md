---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281862"
---
# <span data-ttu-id="59435-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="59435-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="59435-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59435-102">SYNOPSIS</span></span>
<span data-ttu-id="59435-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="59435-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="59435-104">句法</span><span class="sxs-lookup"><span data-stu-id="59435-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59435-105">說明</span><span class="sxs-lookup"><span data-stu-id="59435-105">DESCRIPTION</span></span>
<span data-ttu-id="59435-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會建立 Azure SQL 資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="59435-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="59435-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName*]、[ *ServerName*] 和 [ *DatabaseName* ] 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="59435-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="59435-108">提供 *TableName* 和 *ColumnName* 來指定規則的目標，以及 *MaskingFunction* 參數，以定義如何遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="59435-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="59435-109">如果 *MaskingFunction* 的值為 Number 或 Text，您可以指定 *NumberFrom* 和 *NumberTo* 參數（適用于數位遮罩），或是 *PrefixSize*、 *ReplacementString* 和 *SuffixSize* （用於文字遮罩）。</span><span class="sxs-lookup"><span data-stu-id="59435-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="59435-110">如果命令成功且使用 *PassThru* 參數，則除了規則識別碼之外，此 Cmdlet 還會傳回描述資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="59435-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="59435-111">規則識別碼包括但不限於、 *ResourceGroupName*、 *ServerName*、 *DatabaseName* 及 *RuleID*。</span><span class="sxs-lookup"><span data-stu-id="59435-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="59435-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59435-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="59435-113">示例</span><span class="sxs-lookup"><span data-stu-id="59435-113">EXAMPLES</span></span>

### <span data-ttu-id="59435-114">範例1：針對資料庫中的數位資料行建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="59435-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="59435-115">這個命令會在名為 [Schema01] 架構中名為 Table01 的資料表中，為名為 Column01 的欄建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="59435-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="59435-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="59435-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="59435-117">規則是一個數位遮罩規則，該規則使用介於5到14的亂數作為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="59435-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="59435-118">參數</span><span class="sxs-lookup"><span data-stu-id="59435-118">PARAMETERS</span></span>

### <span data-ttu-id="59435-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="59435-119">-ColumnName</span></span>
<span data-ttu-id="59435-120">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="59435-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59435-121">-DatabaseName</span></span>
<span data-ttu-id="59435-122">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="59435-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59435-123">-DefaultProfile</span></span>
<span data-ttu-id="59435-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59435-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59435-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="59435-125">-MaskingFunction</span></span>
<span data-ttu-id="59435-126">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="59435-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="59435-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="59435-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59435-128">設置</span><span class="sxs-lookup"><span data-stu-id="59435-128">Default</span></span>
- <span data-ttu-id="59435-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="59435-129">NoMasking</span></span>
- <span data-ttu-id="59435-130">字體</span><span class="sxs-lookup"><span data-stu-id="59435-130">Text</span></span>
- <span data-ttu-id="59435-131">電話</span><span class="sxs-lookup"><span data-stu-id="59435-131">Number</span></span>
- <span data-ttu-id="59435-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="59435-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="59435-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="59435-133">CreditCardNumber</span></span>
- <span data-ttu-id="59435-134">[電子郵件] 預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="59435-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="59435-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="59435-135">-NumberFrom</span></span>
<span data-ttu-id="59435-136">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="59435-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="59435-137">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="59435-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="59435-138">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="59435-138">The default value is 0.</span></span>

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

### <span data-ttu-id="59435-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="59435-139">-NumberTo</span></span>
<span data-ttu-id="59435-140">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="59435-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="59435-141">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="59435-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="59435-142">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="59435-142">The default value is 0.</span></span>

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

### <span data-ttu-id="59435-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59435-143">-PassThru</span></span>
<span data-ttu-id="59435-144">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="59435-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59435-145">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="59435-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59435-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="59435-146">-PrefixSize</span></span>
<span data-ttu-id="59435-147">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="59435-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="59435-148">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="59435-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="59435-149">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="59435-149">The default value is 0.</span></span>

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

### <span data-ttu-id="59435-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="59435-150">-ReplacementString</span></span>
<span data-ttu-id="59435-151">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="59435-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="59435-152">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="59435-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="59435-153">預設值是空字串。</span><span class="sxs-lookup"><span data-stu-id="59435-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="59435-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59435-154">-ResourceGroupName</span></span>
<span data-ttu-id="59435-155">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="59435-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="59435-156">-SchemaName</span></span>
<span data-ttu-id="59435-157">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="59435-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59435-158">-ServerName</span></span>
<span data-ttu-id="59435-159">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="59435-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="59435-160">-SuffixSize</span></span>
<span data-ttu-id="59435-161">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="59435-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="59435-162">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="59435-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="59435-163">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="59435-163">The default value is 0.</span></span>

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

### <span data-ttu-id="59435-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="59435-164">-TableName</span></span>
<span data-ttu-id="59435-165">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="59435-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="59435-166">-確認</span><span class="sxs-lookup"><span data-stu-id="59435-166">-Confirm</span></span>
<span data-ttu-id="59435-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59435-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59435-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59435-168">-WhatIf</span></span>
<span data-ttu-id="59435-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59435-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59435-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59435-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59435-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59435-171">CommonParameters</span></span>
<span data-ttu-id="59435-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59435-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59435-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59435-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59435-174">輸入</span><span class="sxs-lookup"><span data-stu-id="59435-174">INPUTS</span></span>

### <span data-ttu-id="59435-175">System.object</span><span class="sxs-lookup"><span data-stu-id="59435-175">System.String</span></span>

### <span data-ttu-id="59435-176">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59435-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59435-177">"CoreLib" 1 ["System.object，System.....，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59435-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="59435-178">輸出</span><span class="sxs-lookup"><span data-stu-id="59435-178">OUTPUTS</span></span>

### <span data-ttu-id="59435-179">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="59435-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="59435-180">筆記</span><span class="sxs-lookup"><span data-stu-id="59435-180">NOTES</span></span>

## <span data-ttu-id="59435-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="59435-181">RELATED LINKS</span></span>

[<span data-ttu-id="59435-182">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="59435-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="59435-183">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="59435-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="59435-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="59435-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="59435-185">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="59435-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


