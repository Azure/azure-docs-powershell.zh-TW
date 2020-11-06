---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446612"
---
# <span data-ttu-id="074aa-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="074aa-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="074aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="074aa-102">SYNOPSIS</span></span>
<span data-ttu-id="074aa-103">為資料庫設定資料遮罩規則的屬性。</span><span class="sxs-lookup"><span data-stu-id="074aa-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="074aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="074aa-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="074aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="074aa-105">DESCRIPTION</span></span>
<span data-ttu-id="074aa-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="074aa-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="074aa-107">若要使用 Cmdlet，請提供 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="074aa-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="074aa-108">您可以提供 *SchemaName* 、 *TableName* 和 *ColumnName* 的任何參數，以將規則重新置放。</span><span class="sxs-lookup"><span data-stu-id="074aa-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="074aa-109">指定 *MaskingFunction* 參數來修改資料的遮罩方式。</span><span class="sxs-lookup"><span data-stu-id="074aa-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="074aa-110">如果您指定 *MaskingFunction* 的數位或文字值，您可以為數位遮罩指定 *NumberFrom* 和 *NumberTo* 參數，或針對文字遮罩指定 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="074aa-111">如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述資料遮罩規則屬性與規則識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="074aa-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="074aa-112">規則識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 、 **DatabaseName** 及 **RuleId** 。</span><span class="sxs-lookup"><span data-stu-id="074aa-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="074aa-113">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="074aa-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="074aa-114">示例</span><span class="sxs-lookup"><span data-stu-id="074aa-114">EXAMPLES</span></span>

### <span data-ttu-id="074aa-115">範例1：變更資料庫中資料遮罩規則的範圍</span><span class="sxs-lookup"><span data-stu-id="074aa-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="074aa-116">這個命令會修改 ID 為 Rule17 的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="074aa-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="074aa-117">該規則會在伺服器 Server01 上名為 Database01 的資料庫中運作。</span><span class="sxs-lookup"><span data-stu-id="074aa-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="074aa-118">這個命令會變更作為遮罩值產生亂數字的間隔界限。</span><span class="sxs-lookup"><span data-stu-id="074aa-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="074aa-119">新的範圍是23到42。</span><span class="sxs-lookup"><span data-stu-id="074aa-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="074aa-120">參數</span><span class="sxs-lookup"><span data-stu-id="074aa-120">PARAMETERS</span></span>

### <span data-ttu-id="074aa-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="074aa-121">-ColumnName</span></span>
<span data-ttu-id="074aa-122">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="074aa-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="074aa-123">-DatabaseName</span></span>
<span data-ttu-id="074aa-124">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="074aa-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="074aa-125">-MaskingFunction</span></span>
<span data-ttu-id="074aa-126">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="074aa-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="074aa-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="074aa-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="074aa-128">設置</span><span class="sxs-lookup"><span data-stu-id="074aa-128">Default</span></span>
- <span data-ttu-id="074aa-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="074aa-129">NoMasking</span></span>
- <span data-ttu-id="074aa-130">字體</span><span class="sxs-lookup"><span data-stu-id="074aa-130">Text</span></span>
- <span data-ttu-id="074aa-131">電話</span><span class="sxs-lookup"><span data-stu-id="074aa-131">Number</span></span>
- <span data-ttu-id="074aa-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="074aa-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="074aa-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="074aa-133">CreditCardNumber</span></span>
- <span data-ttu-id="074aa-134">電子郵件</span><span class="sxs-lookup"><span data-stu-id="074aa-134">Email</span></span>

<span data-ttu-id="074aa-135">預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="074aa-135">The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074aa-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="074aa-136">-NumberFrom</span></span>
<span data-ttu-id="074aa-137">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="074aa-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="074aa-138">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="074aa-139">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="074aa-139">The default value is 0.</span></span>

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

### <span data-ttu-id="074aa-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="074aa-140">-NumberTo</span></span>
<span data-ttu-id="074aa-141">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="074aa-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="074aa-142">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="074aa-143">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="074aa-143">The default value is 0.</span></span>

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

### <span data-ttu-id="074aa-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="074aa-144">-PassThru</span></span>
<span data-ttu-id="074aa-145">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="074aa-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="074aa-146">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="074aa-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="074aa-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="074aa-147">-PrefixSize</span></span>
<span data-ttu-id="074aa-148">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="074aa-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="074aa-149">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="074aa-150">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="074aa-150">The default value is 0.</span></span>

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

### <span data-ttu-id="074aa-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="074aa-151">-ReplacementString</span></span>
<span data-ttu-id="074aa-152">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="074aa-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="074aa-153">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="074aa-154">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="074aa-154">The default value is 0.</span></span>

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

### <span data-ttu-id="074aa-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="074aa-155">-ResourceGroupName</span></span>
<span data-ttu-id="074aa-156">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="074aa-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="074aa-157">-SchemaName</span></span>
<span data-ttu-id="074aa-158">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="074aa-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="074aa-159">-ServerName</span></span>
<span data-ttu-id="074aa-160">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="074aa-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="074aa-161">-SuffixSize</span></span>
<span data-ttu-id="074aa-162">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="074aa-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="074aa-163">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="074aa-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="074aa-164">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="074aa-164">The default value is 0.</span></span>

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

### <span data-ttu-id="074aa-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="074aa-165">-TableName</span></span>
<span data-ttu-id="074aa-166">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="074aa-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="074aa-167">-確認</span><span class="sxs-lookup"><span data-stu-id="074aa-167">-Confirm</span></span>
<span data-ttu-id="074aa-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="074aa-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="074aa-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="074aa-169">-WhatIf</span></span>
<span data-ttu-id="074aa-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="074aa-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="074aa-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="074aa-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="074aa-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074aa-172">-DefaultProfile</span></span>
<span data-ttu-id="074aa-173">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="074aa-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="074aa-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074aa-174">CommonParameters</span></span>
<span data-ttu-id="074aa-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="074aa-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074aa-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="074aa-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074aa-177">輸入</span><span class="sxs-lookup"><span data-stu-id="074aa-177">INPUTS</span></span>

###  
<span data-ttu-id="074aa-178">所有</span><span class="sxs-lookup"><span data-stu-id="074aa-178">None</span></span>

## <span data-ttu-id="074aa-179">輸出</span><span class="sxs-lookup"><span data-stu-id="074aa-179">OUTPUTS</span></span>

### <span data-ttu-id="074aa-180">DatabaseDataMaskingRuleModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="074aa-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="074aa-181">筆記</span><span class="sxs-lookup"><span data-stu-id="074aa-181">NOTES</span></span>

## <span data-ttu-id="074aa-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="074aa-182">RELATED LINKS</span></span>

[<span data-ttu-id="074aa-183">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="074aa-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="074aa-184">新-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="074aa-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="074aa-185">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="074aa-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="074aa-186">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="074aa-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

