---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 6facaef4255d37ccaa0e2c192c40c8888d485357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456344"
---
# <span data-ttu-id="ddb39-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddb39-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ddb39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddb39-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb39-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ddb39-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb39-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddb39-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddb39-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddb39-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb39-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會建立 Azure SQL 資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ddb39-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="ddb39-107">若要使用 Cmdlet，請使用 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 和 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="ddb39-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="ddb39-108">提供 *TableName* 和 *ColumnName* 來指定規則的目標，以及 *MaskingFunction* 參數，以定義如何遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="ddb39-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="ddb39-109">如果 *MaskingFunction* 的值為 Number 或 Text，您可以指定 *NumberFrom* 和 *NumberTo* 參數（適用于數位遮罩），或是 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* （用於文字遮罩）。</span><span class="sxs-lookup"><span data-stu-id="ddb39-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="ddb39-110">如果命令成功且使用 *PassThru* 參數，則除了規則識別碼之外，此 Cmdlet 還會傳回描述資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="ddb39-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="ddb39-111">規則識別碼包括但不限於、 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleID* 。</span><span class="sxs-lookup"><span data-stu-id="ddb39-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="ddb39-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddb39-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ddb39-113">示例</span><span class="sxs-lookup"><span data-stu-id="ddb39-113">EXAMPLES</span></span>

### <span data-ttu-id="ddb39-114">範例1：針對資料庫中的數位資料行建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="ddb39-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="ddb39-115">這個命令會在名為 [Schema01] 架構中名為 Table01 的資料表中，為名為 Column01 的欄建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ddb39-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="ddb39-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="ddb39-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="ddb39-117">規則是一個數位遮罩規則，該規則使用介於5到14的亂數作為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="ddb39-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="ddb39-118">規則稱為 [Rule01]。</span><span class="sxs-lookup"><span data-stu-id="ddb39-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="ddb39-119">參數</span><span class="sxs-lookup"><span data-stu-id="ddb39-119">PARAMETERS</span></span>

### <span data-ttu-id="ddb39-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ddb39-120">-ColumnName</span></span>
<span data-ttu-id="ddb39-121">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="ddb39-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddb39-122">-DatabaseName</span></span>
<span data-ttu-id="ddb39-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ddb39-124">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="ddb39-124">-MaskingFunction</span></span>
<span data-ttu-id="ddb39-125">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-125">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="ddb39-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ddb39-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddb39-127">設置</span><span class="sxs-lookup"><span data-stu-id="ddb39-127">Default</span></span>
- <span data-ttu-id="ddb39-128">NoMasking</span><span class="sxs-lookup"><span data-stu-id="ddb39-128">NoMasking</span></span>
- <span data-ttu-id="ddb39-129">字體</span><span class="sxs-lookup"><span data-stu-id="ddb39-129">Text</span></span>
- <span data-ttu-id="ddb39-130">電話</span><span class="sxs-lookup"><span data-stu-id="ddb39-130">Number</span></span>
- <span data-ttu-id="ddb39-131">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="ddb39-131">SocialSecurityNumber</span></span>
- <span data-ttu-id="ddb39-132">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="ddb39-132">CreditCardNumber</span></span>
- <span data-ttu-id="ddb39-133">電子郵件</span><span class="sxs-lookup"><span data-stu-id="ddb39-133">Email</span></span>

<span data-ttu-id="ddb39-134">預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="ddb39-134">The default value is Default.</span></span>

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

### <span data-ttu-id="ddb39-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="ddb39-135">-NumberFrom</span></span>
<span data-ttu-id="ddb39-136">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="ddb39-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ddb39-137">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ddb39-138">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ddb39-138">The default value is 0.</span></span>

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

### <span data-ttu-id="ddb39-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="ddb39-139">-NumberTo</span></span>
<span data-ttu-id="ddb39-140">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="ddb39-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ddb39-141">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ddb39-142">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ddb39-142">The default value is 0.</span></span>

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

### <span data-ttu-id="ddb39-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddb39-143">-PassThru</span></span>
<span data-ttu-id="ddb39-144">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ddb39-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddb39-145">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ddb39-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddb39-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="ddb39-146">-PrefixSize</span></span>
<span data-ttu-id="ddb39-147">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="ddb39-148">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ddb39-149">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ddb39-149">The default value is 0.</span></span>

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

### <span data-ttu-id="ddb39-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="ddb39-150">-ReplacementString</span></span>
<span data-ttu-id="ddb39-151">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="ddb39-152">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ddb39-153">預設值是空字串。</span><span class="sxs-lookup"><span data-stu-id="ddb39-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="ddb39-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb39-154">-ResourceGroupName</span></span>
<span data-ttu-id="ddb39-155">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ddb39-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ddb39-156">-SchemaName</span></span>
<span data-ttu-id="ddb39-157">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="ddb39-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ddb39-158">-ServerName</span></span>
<span data-ttu-id="ddb39-159">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ddb39-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="ddb39-160">-SuffixSize</span></span>
<span data-ttu-id="ddb39-161">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ddb39-162">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ddb39-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ddb39-163">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ddb39-163">The default value is 0.</span></span>

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

### <span data-ttu-id="ddb39-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="ddb39-164">-TableName</span></span>
<span data-ttu-id="ddb39-165">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="ddb39-166">-確認</span><span class="sxs-lookup"><span data-stu-id="ddb39-166">-Confirm</span></span>
<span data-ttu-id="ddb39-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddb39-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb39-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb39-168">-WhatIf</span></span>
<span data-ttu-id="ddb39-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddb39-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb39-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddb39-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb39-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb39-171">-DefaultProfile</span></span>
<span data-ttu-id="ddb39-172">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddb39-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb39-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb39-173">CommonParameters</span></span>
<span data-ttu-id="ddb39-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddb39-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb39-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddb39-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb39-176">輸入</span><span class="sxs-lookup"><span data-stu-id="ddb39-176">INPUTS</span></span>

###  
<span data-ttu-id="ddb39-177">所有.</span><span class="sxs-lookup"><span data-stu-id="ddb39-177">None.</span></span>

## <span data-ttu-id="ddb39-178">輸出</span><span class="sxs-lookup"><span data-stu-id="ddb39-178">OUTPUTS</span></span>

### <span data-ttu-id="ddb39-179">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="ddb39-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ddb39-180">筆記</span><span class="sxs-lookup"><span data-stu-id="ddb39-180">NOTES</span></span>

## <span data-ttu-id="ddb39-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddb39-181">RELATED LINKS</span></span>

[<span data-ttu-id="ddb39-182">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddb39-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddb39-183">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddb39-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddb39-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ddb39-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ddb39-185">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ddb39-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


