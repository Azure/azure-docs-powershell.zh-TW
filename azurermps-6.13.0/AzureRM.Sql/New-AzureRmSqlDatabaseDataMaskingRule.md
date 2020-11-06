---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 69e59580d5ada03400420788169bba18d2f30444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454515"
---
# <span data-ttu-id="25adf-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25adf-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="25adf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25adf-102">SYNOPSIS</span></span>
<span data-ttu-id="25adf-103">建立資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="25adf-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25adf-104">句法</span><span class="sxs-lookup"><span data-stu-id="25adf-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25adf-105">說明</span><span class="sxs-lookup"><span data-stu-id="25adf-105">DESCRIPTION</span></span>
<span data-ttu-id="25adf-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會建立 Azure SQL 資料庫的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="25adf-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="25adf-107">若要使用 Cmdlet，請使用 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 和 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="25adf-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="25adf-108">提供 *TableName* 和 *ColumnName* 來指定規則的目標，以及 *MaskingFunction* 參數，以定義如何遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="25adf-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="25adf-109">如果 *MaskingFunction* 的值為 Number 或 Text，您可以指定 *NumberFrom* 和 *NumberTo* 參數（適用于數位遮罩），或是 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* （用於文字遮罩）。</span><span class="sxs-lookup"><span data-stu-id="25adf-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="25adf-110">如果命令成功且使用 *PassThru* 參數，則除了規則識別碼之外，此 Cmdlet 還會傳回描述資料遮罩規則屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="25adf-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="25adf-111">規則識別碼包括但不限於、 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleID* 。</span><span class="sxs-lookup"><span data-stu-id="25adf-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="25adf-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25adf-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="25adf-113">示例</span><span class="sxs-lookup"><span data-stu-id="25adf-113">EXAMPLES</span></span>

### <span data-ttu-id="25adf-114">範例1：針對資料庫中的數位資料行建立資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="25adf-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="25adf-115">這個命令會在名為 [Schema01] 架構中名為 Table01 的資料表中，為名為 Column01 的欄建立資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="25adf-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="25adf-116">名為 Database01 的資料庫包含所有這些專案。</span><span class="sxs-lookup"><span data-stu-id="25adf-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="25adf-117">規則是一個數位遮罩規則，該規則使用介於5到14的亂數作為遮罩值。</span><span class="sxs-lookup"><span data-stu-id="25adf-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="25adf-118">規則稱為 [Rule01]。</span><span class="sxs-lookup"><span data-stu-id="25adf-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="25adf-119">參數</span><span class="sxs-lookup"><span data-stu-id="25adf-119">PARAMETERS</span></span>

### <span data-ttu-id="25adf-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="25adf-120">-ColumnName</span></span>
<span data-ttu-id="25adf-121">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="25adf-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25adf-122">-DatabaseName</span></span>
<span data-ttu-id="25adf-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="25adf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25adf-124">-DefaultProfile</span></span>
<span data-ttu-id="25adf-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="25adf-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25adf-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="25adf-126">-MaskingFunction</span></span>
<span data-ttu-id="25adf-127">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="25adf-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="25adf-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="25adf-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25adf-129">設置</span><span class="sxs-lookup"><span data-stu-id="25adf-129">Default</span></span>
- <span data-ttu-id="25adf-130">NoMasking</span><span class="sxs-lookup"><span data-stu-id="25adf-130">NoMasking</span></span>
- <span data-ttu-id="25adf-131">字體</span><span class="sxs-lookup"><span data-stu-id="25adf-131">Text</span></span>
- <span data-ttu-id="25adf-132">電話</span><span class="sxs-lookup"><span data-stu-id="25adf-132">Number</span></span>
- <span data-ttu-id="25adf-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="25adf-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="25adf-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="25adf-134">CreditCardNumber</span></span>
- <span data-ttu-id="25adf-135">[電子郵件] 預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="25adf-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="25adf-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="25adf-136">-NumberFrom</span></span>
<span data-ttu-id="25adf-137">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="25adf-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="25adf-138">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25adf-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="25adf-139">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="25adf-139">The default value is 0.</span></span>

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

### <span data-ttu-id="25adf-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="25adf-140">-NumberTo</span></span>
<span data-ttu-id="25adf-141">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="25adf-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="25adf-142">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25adf-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="25adf-143">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="25adf-143">The default value is 0.</span></span>

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

### <span data-ttu-id="25adf-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25adf-144">-PassThru</span></span>
<span data-ttu-id="25adf-145">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="25adf-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25adf-146">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="25adf-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25adf-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="25adf-147">-PrefixSize</span></span>
<span data-ttu-id="25adf-148">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="25adf-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="25adf-149">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25adf-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="25adf-150">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="25adf-150">The default value is 0.</span></span>

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

### <span data-ttu-id="25adf-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="25adf-151">-ReplacementString</span></span>
<span data-ttu-id="25adf-152">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="25adf-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="25adf-153">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25adf-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="25adf-154">預設值是空字串。</span><span class="sxs-lookup"><span data-stu-id="25adf-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="25adf-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25adf-155">-ResourceGroupName</span></span>
<span data-ttu-id="25adf-156">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="25adf-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="25adf-157">-SchemaName</span></span>
<span data-ttu-id="25adf-158">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="25adf-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25adf-159">-ServerName</span></span>
<span data-ttu-id="25adf-160">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="25adf-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="25adf-161">-SuffixSize</span></span>
<span data-ttu-id="25adf-162">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="25adf-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="25adf-163">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25adf-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="25adf-164">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="25adf-164">The default value is 0.</span></span>

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

### <span data-ttu-id="25adf-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="25adf-165">-TableName</span></span>
<span data-ttu-id="25adf-166">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="25adf-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="25adf-167">-確認</span><span class="sxs-lookup"><span data-stu-id="25adf-167">-Confirm</span></span>
<span data-ttu-id="25adf-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25adf-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25adf-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25adf-169">-WhatIf</span></span>
<span data-ttu-id="25adf-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25adf-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25adf-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25adf-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25adf-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25adf-172">CommonParameters</span></span>
<span data-ttu-id="25adf-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25adf-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25adf-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25adf-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25adf-175">輸入</span><span class="sxs-lookup"><span data-stu-id="25adf-175">INPUTS</span></span>

### <span data-ttu-id="25adf-176">System.object</span><span class="sxs-lookup"><span data-stu-id="25adf-176">System.String</span></span>

### <span data-ttu-id="25adf-177">System.object "1 [[System. UInt32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25adf-177">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="25adf-178">System.object "1 [[System. Double，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25adf-178">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="25adf-179">輸出</span><span class="sxs-lookup"><span data-stu-id="25adf-179">OUTPUTS</span></span>

### <span data-ttu-id="25adf-180">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="25adf-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="25adf-181">筆記</span><span class="sxs-lookup"><span data-stu-id="25adf-181">NOTES</span></span>

## <span data-ttu-id="25adf-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="25adf-182">RELATED LINKS</span></span>

[<span data-ttu-id="25adf-183">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25adf-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25adf-184">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25adf-184">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25adf-185">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25adf-185">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25adf-186">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="25adf-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


