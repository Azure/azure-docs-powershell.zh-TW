---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: dd29dd7e58a233d62e3af5260971d56300a43230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623785"
---
# <span data-ttu-id="36e47-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36e47-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="36e47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36e47-102">SYNOPSIS</span></span>
<span data-ttu-id="36e47-103">為資料庫設定資料遮罩規則的屬性。</span><span class="sxs-lookup"><span data-stu-id="36e47-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e47-104">句法</span><span class="sxs-lookup"><span data-stu-id="36e47-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36e47-105">說明</span><span class="sxs-lookup"><span data-stu-id="36e47-105">DESCRIPTION</span></span>
<span data-ttu-id="36e47-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="36e47-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="36e47-107">若要使用 Cmdlet，請提供 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="36e47-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="36e47-108">您可以提供 *SchemaName* 、 *TableName* 和 *ColumnName* 的任何參數，以將規則重新置放。</span><span class="sxs-lookup"><span data-stu-id="36e47-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="36e47-109">指定 *MaskingFunction* 參數來修改資料的遮罩方式。</span><span class="sxs-lookup"><span data-stu-id="36e47-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="36e47-110">如果您指定 *MaskingFunction* 的數位或文字值，您可以為數位遮罩指定 *NumberFrom* 和 *NumberTo* 參數，或針對文字遮罩指定 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="36e47-111">如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述資料遮罩規則屬性與規則識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="36e47-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="36e47-112">規則識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 、 **DatabaseName** 及 **RuleId** 。</span><span class="sxs-lookup"><span data-stu-id="36e47-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="36e47-113">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36e47-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="36e47-114">示例</span><span class="sxs-lookup"><span data-stu-id="36e47-114">EXAMPLES</span></span>

### <span data-ttu-id="36e47-115">範例1：變更資料庫中資料遮罩規則的範圍</span><span class="sxs-lookup"><span data-stu-id="36e47-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="36e47-116">這個命令會修改 ID 為 Rule17 的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="36e47-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="36e47-117">該規則會在伺服器 Server01 上名為 Database01 的資料庫中運作。</span><span class="sxs-lookup"><span data-stu-id="36e47-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="36e47-118">這個命令會變更作為遮罩值產生亂數字的間隔界限。</span><span class="sxs-lookup"><span data-stu-id="36e47-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="36e47-119">新的範圍是23到42。</span><span class="sxs-lookup"><span data-stu-id="36e47-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="36e47-120">參數</span><span class="sxs-lookup"><span data-stu-id="36e47-120">PARAMETERS</span></span>

### <span data-ttu-id="36e47-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="36e47-121">-ColumnName</span></span>
<span data-ttu-id="36e47-122">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="36e47-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36e47-123">-DatabaseName</span></span>
<span data-ttu-id="36e47-124">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="36e47-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e47-125">-DefaultProfile</span></span>
<span data-ttu-id="36e47-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36e47-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e47-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="36e47-127">-MaskingFunction</span></span>
<span data-ttu-id="36e47-128">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="36e47-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="36e47-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="36e47-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36e47-130">設置</span><span class="sxs-lookup"><span data-stu-id="36e47-130">Default</span></span>
- <span data-ttu-id="36e47-131">NoMasking</span><span class="sxs-lookup"><span data-stu-id="36e47-131">NoMasking</span></span>
- <span data-ttu-id="36e47-132">字體</span><span class="sxs-lookup"><span data-stu-id="36e47-132">Text</span></span>
- <span data-ttu-id="36e47-133">電話</span><span class="sxs-lookup"><span data-stu-id="36e47-133">Number</span></span>
- <span data-ttu-id="36e47-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="36e47-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="36e47-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="36e47-135">CreditCardNumber</span></span>
- <span data-ttu-id="36e47-136">電子郵件</span><span class="sxs-lookup"><span data-stu-id="36e47-136">Email</span></span>

<span data-ttu-id="36e47-137">預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="36e47-137">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e47-138">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="36e47-138">-NumberFrom</span></span>
<span data-ttu-id="36e47-139">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="36e47-139">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="36e47-140">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-140">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36e47-141">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="36e47-141">The default value is 0.</span></span>

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

### <span data-ttu-id="36e47-142">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="36e47-142">-NumberTo</span></span>
<span data-ttu-id="36e47-143">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="36e47-143">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="36e47-144">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-144">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36e47-145">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="36e47-145">The default value is 0.</span></span>

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

### <span data-ttu-id="36e47-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36e47-146">-PassThru</span></span>
<span data-ttu-id="36e47-147">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="36e47-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36e47-148">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="36e47-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36e47-149">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="36e47-149">-PrefixSize</span></span>
<span data-ttu-id="36e47-150">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="36e47-150">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="36e47-151">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-151">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36e47-152">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="36e47-152">The default value is 0.</span></span>

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

### <span data-ttu-id="36e47-153">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="36e47-153">-ReplacementString</span></span>
<span data-ttu-id="36e47-154">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="36e47-154">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="36e47-155">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-155">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36e47-156">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="36e47-156">The default value is 0.</span></span>

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

### <span data-ttu-id="36e47-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e47-157">-ResourceGroupName</span></span>
<span data-ttu-id="36e47-158">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-158">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="36e47-159">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="36e47-159">-SchemaName</span></span>
<span data-ttu-id="36e47-160">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-160">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="36e47-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36e47-161">-ServerName</span></span>
<span data-ttu-id="36e47-162">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="36e47-163">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="36e47-163">-SuffixSize</span></span>
<span data-ttu-id="36e47-164">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="36e47-164">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="36e47-165">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="36e47-165">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36e47-166">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="36e47-166">The default value is 0.</span></span>

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

### <span data-ttu-id="36e47-167">-TableName</span><span class="sxs-lookup"><span data-stu-id="36e47-167">-TableName</span></span>
<span data-ttu-id="36e47-168">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="36e47-168">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="36e47-169">-確認</span><span class="sxs-lookup"><span data-stu-id="36e47-169">-Confirm</span></span>
<span data-ttu-id="36e47-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36e47-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e47-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e47-171">-WhatIf</span></span>
<span data-ttu-id="36e47-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36e47-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e47-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36e47-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e47-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e47-174">CommonParameters</span></span>
<span data-ttu-id="36e47-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36e47-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e47-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36e47-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e47-177">輸入</span><span class="sxs-lookup"><span data-stu-id="36e47-177">INPUTS</span></span>

###  
<span data-ttu-id="36e47-178">所有</span><span class="sxs-lookup"><span data-stu-id="36e47-178">None</span></span>

## <span data-ttu-id="36e47-179">輸出</span><span class="sxs-lookup"><span data-stu-id="36e47-179">OUTPUTS</span></span>

### <span data-ttu-id="36e47-180">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="36e47-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="36e47-181">筆記</span><span class="sxs-lookup"><span data-stu-id="36e47-181">NOTES</span></span>

## <span data-ttu-id="36e47-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="36e47-182">RELATED LINKS</span></span>

[<span data-ttu-id="36e47-183">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36e47-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36e47-184">新-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36e47-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36e47-185">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36e47-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36e47-186">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="36e47-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


