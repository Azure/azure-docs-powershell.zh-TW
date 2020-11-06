---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: eb5e809b3f48403a6095f84643af0a169b2cecf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614845"
---
# <span data-ttu-id="32881-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32881-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="32881-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32881-102">SYNOPSIS</span></span>
<span data-ttu-id="32881-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="32881-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="32881-104">句法</span><span class="sxs-lookup"><span data-stu-id="32881-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32881-105">說明</span><span class="sxs-lookup"><span data-stu-id="32881-105">DESCRIPTION</span></span>
<span data-ttu-id="32881-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會建立 Azure SQL 資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="32881-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="32881-107">若要使用 Cmdlet，請使用 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 和 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="32881-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="32881-108">提供 *TableName* 和 *ColumnName* 來指定規則的目標，以及 *MaskingFunction* 參數，以定義如何遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="32881-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="32881-109">如果 *MaskingFunction* 的值為 Number 或 Text，您可以指定 *NumberFrom* 和 *NumberTo* 參數（適用于數位遮罩），或是 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* （用於文字遮罩）。</span><span class="sxs-lookup"><span data-stu-id="32881-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="32881-110">如果命令成功且使用 *PassThru* 參數，則除了規則識別碼之外，此 Cmdlet 還會傳回描述資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="32881-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="32881-111">規則識別碼包括但不限於、 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleID* 。</span><span class="sxs-lookup"><span data-stu-id="32881-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="32881-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32881-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="32881-113">示例</span><span class="sxs-lookup"><span data-stu-id="32881-113">EXAMPLES</span></span>

### <span data-ttu-id="32881-114">範例1：針對資料庫中的數位資料行建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="32881-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="32881-115">這個命令會在名為 [Schema01] 架構中名為 Table01 的資料表中，為名為 Column01 的欄建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="32881-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="32881-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="32881-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="32881-117">規則是一個數位遮罩規則，該規則使用介於5到14的亂數作為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="32881-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="32881-118">規則稱為 [Rule01]。</span><span class="sxs-lookup"><span data-stu-id="32881-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="32881-119">參數</span><span class="sxs-lookup"><span data-stu-id="32881-119">PARAMETERS</span></span>

### <span data-ttu-id="32881-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="32881-120">-ColumnName</span></span>
<span data-ttu-id="32881-121">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="32881-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32881-122">-DatabaseName</span></span>
<span data-ttu-id="32881-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="32881-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32881-124">-DefaultProfile</span></span>
<span data-ttu-id="32881-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="32881-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32881-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="32881-126">-MaskingFunction</span></span>
<span data-ttu-id="32881-127">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="32881-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="32881-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="32881-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32881-129">設置</span><span class="sxs-lookup"><span data-stu-id="32881-129">Default</span></span>
- <span data-ttu-id="32881-130">NoMasking</span><span class="sxs-lookup"><span data-stu-id="32881-130">NoMasking</span></span>
- <span data-ttu-id="32881-131">字體</span><span class="sxs-lookup"><span data-stu-id="32881-131">Text</span></span>
- <span data-ttu-id="32881-132">電話</span><span class="sxs-lookup"><span data-stu-id="32881-132">Number</span></span>
- <span data-ttu-id="32881-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="32881-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="32881-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="32881-134">CreditCardNumber</span></span>
- <span data-ttu-id="32881-135">[電子郵件] 預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="32881-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="32881-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="32881-136">-NumberFrom</span></span>
<span data-ttu-id="32881-137">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="32881-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="32881-138">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="32881-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="32881-139">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="32881-139">The default value is 0.</span></span>

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

### <span data-ttu-id="32881-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="32881-140">-NumberTo</span></span>
<span data-ttu-id="32881-141">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="32881-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="32881-142">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="32881-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="32881-143">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="32881-143">The default value is 0.</span></span>

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

### <span data-ttu-id="32881-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32881-144">-PassThru</span></span>
<span data-ttu-id="32881-145">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="32881-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32881-146">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="32881-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32881-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="32881-147">-PrefixSize</span></span>
<span data-ttu-id="32881-148">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="32881-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="32881-149">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="32881-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="32881-150">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="32881-150">The default value is 0.</span></span>

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

### <span data-ttu-id="32881-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="32881-151">-ReplacementString</span></span>
<span data-ttu-id="32881-152">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="32881-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="32881-153">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="32881-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="32881-154">預設值是空字串。</span><span class="sxs-lookup"><span data-stu-id="32881-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="32881-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32881-155">-ResourceGroupName</span></span>
<span data-ttu-id="32881-156">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="32881-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="32881-157">-SchemaName</span></span>
<span data-ttu-id="32881-158">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="32881-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32881-159">-ServerName</span></span>
<span data-ttu-id="32881-160">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="32881-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="32881-161">-SuffixSize</span></span>
<span data-ttu-id="32881-162">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="32881-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="32881-163">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="32881-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="32881-164">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="32881-164">The default value is 0.</span></span>

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

### <span data-ttu-id="32881-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="32881-165">-TableName</span></span>
<span data-ttu-id="32881-166">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="32881-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="32881-167">-確認</span><span class="sxs-lookup"><span data-stu-id="32881-167">-Confirm</span></span>
<span data-ttu-id="32881-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32881-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32881-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32881-169">-WhatIf</span></span>
<span data-ttu-id="32881-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32881-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32881-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32881-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32881-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32881-172">CommonParameters</span></span>
<span data-ttu-id="32881-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32881-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32881-174">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32881-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32881-175">輸入</span><span class="sxs-lookup"><span data-stu-id="32881-175">INPUTS</span></span>

### <span data-ttu-id="32881-176">System.object</span><span class="sxs-lookup"><span data-stu-id="32881-176">System.String</span></span>

### <span data-ttu-id="32881-177">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32881-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32881-178">"CoreLib" 1 ["System.object，System.....，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32881-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="32881-179">輸出</span><span class="sxs-lookup"><span data-stu-id="32881-179">OUTPUTS</span></span>

### <span data-ttu-id="32881-180">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="32881-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="32881-181">筆記</span><span class="sxs-lookup"><span data-stu-id="32881-181">NOTES</span></span>

## <span data-ttu-id="32881-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="32881-182">RELATED LINKS</span></span>

[<span data-ttu-id="32881-183">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32881-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32881-184">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32881-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32881-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32881-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32881-186">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="32881-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


