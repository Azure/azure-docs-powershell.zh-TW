---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 10afb514284fb3083110c068b33ffd189afd4039
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798290"
---
# <span data-ttu-id="ecb9a-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ecb9a-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ecb9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb9a-103">為資料庫設定資料遮罩規則的屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="ecb9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecb9a-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecb9a-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecb9a-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb9a-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="ecb9a-107">若要使用 Cmdlet，請提供 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="ecb9a-108">您可以提供 *SchemaName* 、 *TableName* 和 *ColumnName* 的任何參數，以將規則重新置放。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="ecb9a-109">指定 *MaskingFunction* 參數來修改資料的遮罩方式。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="ecb9a-110">如果您指定 *MaskingFunction* 的數位或文字值，您可以為數位遮罩指定 *NumberFrom* 和 *NumberTo* 參數，或針對文字遮罩指定 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="ecb9a-111">如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述資料遮罩規則屬性與規則識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="ecb9a-112">規則識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 、 **DatabaseName** 及 **RuleId** 。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="ecb9a-113">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ecb9a-114">示例</span><span class="sxs-lookup"><span data-stu-id="ecb9a-114">EXAMPLES</span></span>

### <span data-ttu-id="ecb9a-115">範例1：變更資料庫中資料遮罩規則的範圍</span><span class="sxs-lookup"><span data-stu-id="ecb9a-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="ecb9a-116">這個命令會修改 ID 為 Rule17 的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="ecb9a-117">該規則會在伺服器 Server01 上名為 Database01 的資料庫中運作。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="ecb9a-118">這個命令會變更作為遮罩值產生亂數字的間隔界限。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="ecb9a-119">新的範圍是23到42。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="ecb9a-120">參數</span><span class="sxs-lookup"><span data-stu-id="ecb9a-120">PARAMETERS</span></span>

### <span data-ttu-id="ecb9a-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-121">-ColumnName</span></span>
<span data-ttu-id="ecb9a-122">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="ecb9a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-123">-DatabaseName</span></span>
<span data-ttu-id="ecb9a-124">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ecb9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb9a-125">-DefaultProfile</span></span>
<span data-ttu-id="ecb9a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ecb9a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecb9a-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="ecb9a-127">-MaskingFunction</span></span>
<span data-ttu-id="ecb9a-128">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="ecb9a-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ecb9a-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecb9a-130">設置</span><span class="sxs-lookup"><span data-stu-id="ecb9a-130">Default</span></span>
- <span data-ttu-id="ecb9a-131">NoMasking</span><span class="sxs-lookup"><span data-stu-id="ecb9a-131">NoMasking</span></span>
- <span data-ttu-id="ecb9a-132">字體</span><span class="sxs-lookup"><span data-stu-id="ecb9a-132">Text</span></span>
- <span data-ttu-id="ecb9a-133">電話</span><span class="sxs-lookup"><span data-stu-id="ecb9a-133">Number</span></span>
- <span data-ttu-id="ecb9a-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="ecb9a-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="ecb9a-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="ecb9a-135">CreditCardNumber</span></span>
- <span data-ttu-id="ecb9a-136">[電子郵件] 預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-136">Email The default value is Default.</span></span>

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

### <span data-ttu-id="ecb9a-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="ecb9a-137">-NumberFrom</span></span>
<span data-ttu-id="ecb9a-138">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ecb9a-139">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ecb9a-140">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-140">The default value is 0.</span></span>

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

### <span data-ttu-id="ecb9a-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="ecb9a-141">-NumberTo</span></span>
<span data-ttu-id="ecb9a-142">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ecb9a-143">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ecb9a-144">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-144">The default value is 0.</span></span>

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

### <span data-ttu-id="ecb9a-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecb9a-145">-PassThru</span></span>
<span data-ttu-id="ecb9a-146">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecb9a-147">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ecb9a-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="ecb9a-148">-PrefixSize</span></span>
<span data-ttu-id="ecb9a-149">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="ecb9a-150">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ecb9a-151">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-151">The default value is 0.</span></span>

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

### <span data-ttu-id="ecb9a-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="ecb9a-152">-ReplacementString</span></span>
<span data-ttu-id="ecb9a-153">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ecb9a-154">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ecb9a-155">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-155">The default value is 0.</span></span>

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

### <span data-ttu-id="ecb9a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-156">-ResourceGroupName</span></span>
<span data-ttu-id="ecb9a-157">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ecb9a-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-158">-SchemaName</span></span>
<span data-ttu-id="ecb9a-159">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="ecb9a-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-160">-ServerName</span></span>
<span data-ttu-id="ecb9a-161">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ecb9a-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="ecb9a-162">-SuffixSize</span></span>
<span data-ttu-id="ecb9a-163">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ecb9a-164">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ecb9a-165">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-165">The default value is 0.</span></span>

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

### <span data-ttu-id="ecb9a-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="ecb9a-166">-TableName</span></span>
<span data-ttu-id="ecb9a-167">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="ecb9a-168">-確認</span><span class="sxs-lookup"><span data-stu-id="ecb9a-168">-Confirm</span></span>
<span data-ttu-id="ecb9a-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb9a-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb9a-170">-WhatIf</span></span>
<span data-ttu-id="ecb9a-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb9a-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb9a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb9a-173">CommonParameters</span></span>
<span data-ttu-id="ecb9a-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb9a-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ecb9a-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb9a-176">輸入</span><span class="sxs-lookup"><span data-stu-id="ecb9a-176">INPUTS</span></span>

### <span data-ttu-id="ecb9a-177">System.object</span><span class="sxs-lookup"><span data-stu-id="ecb9a-177">System.String</span></span>

### <span data-ttu-id="ecb9a-178">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ecb9a-178">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ecb9a-179">"CoreLib" 1 ["System.object，System.....，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ecb9a-179">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ecb9a-180">輸出</span><span class="sxs-lookup"><span data-stu-id="ecb9a-180">OUTPUTS</span></span>

### <span data-ttu-id="ecb9a-181">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="ecb9a-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ecb9a-182">筆記</span><span class="sxs-lookup"><span data-stu-id="ecb9a-182">NOTES</span></span>

## <span data-ttu-id="ecb9a-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecb9a-183">RELATED LINKS</span></span>

[<span data-ttu-id="ecb9a-184">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ecb9a-184">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ecb9a-185">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ecb9a-185">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ecb9a-186">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ecb9a-186">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ecb9a-187">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ecb9a-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


