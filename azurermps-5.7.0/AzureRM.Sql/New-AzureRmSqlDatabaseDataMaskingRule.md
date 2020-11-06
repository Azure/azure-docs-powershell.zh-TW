---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444240"
---
# <span data-ttu-id="3dd3f-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3dd3f-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="3dd3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd3f-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dd3f-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3dd3f-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd3f-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會建立 Azure SQL 資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="3dd3f-107">若要使用 Cmdlet，請使用 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 和 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="3dd3f-108">提供 *TableName* 和 *ColumnName* 來指定規則的目標，以及 *MaskingFunction* 參數，以定義如何遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="3dd3f-109">如果 *MaskingFunction* 的值為 Number 或 Text，您可以指定 *NumberFrom* 和 *NumberTo* 參數（適用于數位遮罩），或是 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* （用於文字遮罩）。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="3dd3f-110">如果命令成功且使用 *PassThru* 參數，則除了規則識別碼之外，此 Cmdlet 還會傳回描述資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="3dd3f-111">規則識別碼包括但不限於、 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleID* 。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="3dd3f-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3dd3f-113">示例</span><span class="sxs-lookup"><span data-stu-id="3dd3f-113">EXAMPLES</span></span>

### <span data-ttu-id="3dd3f-114">範例1：針對資料庫中的數位資料行建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="3dd3f-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="3dd3f-115">這個命令會在名為 [Schema01] 架構中名為 Table01 的資料表中，為名為 Column01 的欄建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="3dd3f-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="3dd3f-117">規則是一個數位遮罩規則，該規則使用介於5到14的亂數作為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="3dd3f-118">規則稱為 [Rule01]。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="3dd3f-119">參數</span><span class="sxs-lookup"><span data-stu-id="3dd3f-119">PARAMETERS</span></span>

### <span data-ttu-id="3dd3f-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-120">-ColumnName</span></span>
<span data-ttu-id="3dd3f-121">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="3dd3f-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-122">-DatabaseName</span></span>
<span data-ttu-id="3dd3f-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3dd3f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd3f-124">-DefaultProfile</span></span>
<span data-ttu-id="3dd3f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3dd3f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dd3f-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="3dd3f-126">-MaskingFunction</span></span>
<span data-ttu-id="3dd3f-127">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="3dd3f-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3dd3f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dd3f-129">設置</span><span class="sxs-lookup"><span data-stu-id="3dd3f-129">Default</span></span>
- <span data-ttu-id="3dd3f-130">NoMasking</span><span class="sxs-lookup"><span data-stu-id="3dd3f-130">NoMasking</span></span>
- <span data-ttu-id="3dd3f-131">字體</span><span class="sxs-lookup"><span data-stu-id="3dd3f-131">Text</span></span>
- <span data-ttu-id="3dd3f-132">電話</span><span class="sxs-lookup"><span data-stu-id="3dd3f-132">Number</span></span>
- <span data-ttu-id="3dd3f-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="3dd3f-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="3dd3f-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="3dd3f-134">CreditCardNumber</span></span>
- <span data-ttu-id="3dd3f-135">電子郵件</span><span class="sxs-lookup"><span data-stu-id="3dd3f-135">Email</span></span>

<span data-ttu-id="3dd3f-136">預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="3dd3f-137">-NumberFrom</span></span>
<span data-ttu-id="3dd3f-138">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="3dd3f-139">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3dd3f-140">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="3dd3f-141">-NumberTo</span></span>
<span data-ttu-id="3dd3f-142">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="3dd3f-143">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3dd3f-144">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dd3f-145">-PassThru</span></span>
<span data-ttu-id="3dd3f-146">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3dd3f-147">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3dd3f-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="3dd3f-148">-PrefixSize</span></span>
<span data-ttu-id="3dd3f-149">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="3dd3f-150">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3dd3f-151">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="3dd3f-152">-ReplacementString</span></span>
<span data-ttu-id="3dd3f-153">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="3dd3f-154">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3dd3f-155">預設值是空字串。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-156">-ResourceGroupName</span></span>
<span data-ttu-id="3dd3f-157">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3dd3f-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-158">-SchemaName</span></span>
<span data-ttu-id="3dd3f-159">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="3dd3f-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-160">-ServerName</span></span>
<span data-ttu-id="3dd3f-161">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3dd3f-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="3dd3f-162">-SuffixSize</span></span>
<span data-ttu-id="3dd3f-163">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="3dd3f-164">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3dd3f-165">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd3f-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="3dd3f-166">-TableName</span></span>
<span data-ttu-id="3dd3f-167">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="3dd3f-168">-確認</span><span class="sxs-lookup"><span data-stu-id="3dd3f-168">-Confirm</span></span>
<span data-ttu-id="3dd3f-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd3f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd3f-170">-WhatIf</span></span>
<span data-ttu-id="3dd3f-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd3f-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd3f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd3f-173">CommonParameters</span></span>
<span data-ttu-id="3dd3f-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd3f-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dd3f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd3f-176">輸入</span><span class="sxs-lookup"><span data-stu-id="3dd3f-176">INPUTS</span></span>

###  
<span data-ttu-id="3dd3f-177">所有.</span><span class="sxs-lookup"><span data-stu-id="3dd3f-177">None.</span></span>

## <span data-ttu-id="3dd3f-178">輸出</span><span class="sxs-lookup"><span data-stu-id="3dd3f-178">OUTPUTS</span></span>

### <span data-ttu-id="3dd3f-179">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="3dd3f-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="3dd3f-180">筆記</span><span class="sxs-lookup"><span data-stu-id="3dd3f-180">NOTES</span></span>

## <span data-ttu-id="3dd3f-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dd3f-181">RELATED LINKS</span></span>

[<span data-ttu-id="3dd3f-182">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3dd3f-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3dd3f-183">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3dd3f-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3dd3f-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3dd3f-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3dd3f-185">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3dd3f-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


