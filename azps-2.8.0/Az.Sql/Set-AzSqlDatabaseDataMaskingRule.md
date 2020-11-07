---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 9038fae93cf8f79962a19960da8c103820335961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792658"
---
# <span data-ttu-id="06fb9-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06fb9-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="06fb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="06fb9-103">為資料庫設定資料遮罩規則的屬性。</span><span class="sxs-lookup"><span data-stu-id="06fb9-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="06fb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="06fb9-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06fb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="06fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="06fb9-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="06fb9-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="06fb9-107">若要使用 Cmdlet，請提供 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleId* 參數來識別規則。</span><span class="sxs-lookup"><span data-stu-id="06fb9-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="06fb9-108">您可以提供 *SchemaName* 、 *TableName* 和 *ColumnName* 的任何參數，以將規則重新置放。</span><span class="sxs-lookup"><span data-stu-id="06fb9-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="06fb9-109">指定 *MaskingFunction* 參數來修改資料的遮罩方式。</span><span class="sxs-lookup"><span data-stu-id="06fb9-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="06fb9-110">如果您指定 *MaskingFunction* 的數位或文字值，您可以為數位遮罩指定 *NumberFrom* 和 *NumberTo* 參數，或針對文字遮罩指定 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="06fb9-111">如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述資料遮罩規則屬性與規則識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="06fb9-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="06fb9-112">規則識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 、 **DatabaseName** 及 **RuleId** 。</span><span class="sxs-lookup"><span data-stu-id="06fb9-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="06fb9-113">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fb9-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="06fb9-114">示例</span><span class="sxs-lookup"><span data-stu-id="06fb9-114">EXAMPLES</span></span>

### <span data-ttu-id="06fb9-115">範例1：變更資料庫中資料遮罩規則的範圍</span><span class="sxs-lookup"><span data-stu-id="06fb9-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="06fb9-116">這個命令會修改 ID 為 Rule17 的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="06fb9-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="06fb9-117">該規則會在伺服器 Server01 上名為 Database01 的資料庫中運作。</span><span class="sxs-lookup"><span data-stu-id="06fb9-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="06fb9-118">這個命令會變更作為遮罩值產生亂數字的間隔界限。</span><span class="sxs-lookup"><span data-stu-id="06fb9-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="06fb9-119">新的範圍是23到42。</span><span class="sxs-lookup"><span data-stu-id="06fb9-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="06fb9-120">參數</span><span class="sxs-lookup"><span data-stu-id="06fb9-120">PARAMETERS</span></span>

### <span data-ttu-id="06fb9-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="06fb9-121">-ColumnName</span></span>
<span data-ttu-id="06fb9-122">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="06fb9-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06fb9-123">-DatabaseName</span></span>
<span data-ttu-id="06fb9-124">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="06fb9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fb9-125">-DefaultProfile</span></span>
<span data-ttu-id="06fb9-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="06fb9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06fb9-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="06fb9-127">-MaskingFunction</span></span>
<span data-ttu-id="06fb9-128">指定規則所使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="06fb9-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="06fb9-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06fb9-130">設置</span><span class="sxs-lookup"><span data-stu-id="06fb9-130">Default</span></span>
- <span data-ttu-id="06fb9-131">NoMasking</span><span class="sxs-lookup"><span data-stu-id="06fb9-131">NoMasking</span></span>
- <span data-ttu-id="06fb9-132">字體</span><span class="sxs-lookup"><span data-stu-id="06fb9-132">Text</span></span>
- <span data-ttu-id="06fb9-133">電話</span><span class="sxs-lookup"><span data-stu-id="06fb9-133">Number</span></span>
- <span data-ttu-id="06fb9-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="06fb9-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="06fb9-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="06fb9-135">CreditCardNumber</span></span>
- <span data-ttu-id="06fb9-136">[電子郵件] 預設值為 [預設值]。</span><span class="sxs-lookup"><span data-stu-id="06fb9-136">Email The default value is Default.</span></span>

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

### <span data-ttu-id="06fb9-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="06fb9-137">-NumberFrom</span></span>
<span data-ttu-id="06fb9-138">指定從中選取隨機值的間隔下限數位。</span><span class="sxs-lookup"><span data-stu-id="06fb9-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="06fb9-139">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06fb9-140">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="06fb9-140">The default value is 0.</span></span>

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

### <span data-ttu-id="06fb9-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="06fb9-141">-NumberTo</span></span>
<span data-ttu-id="06fb9-142">指定從哪個間隔開始選取隨機值的上限。</span><span class="sxs-lookup"><span data-stu-id="06fb9-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="06fb9-143">只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06fb9-144">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="06fb9-144">The default value is 0.</span></span>

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

### <span data-ttu-id="06fb9-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06fb9-145">-PassThru</span></span>
<span data-ttu-id="06fb9-146">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="06fb9-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06fb9-147">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="06fb9-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06fb9-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="06fb9-148">-PrefixSize</span></span>
<span data-ttu-id="06fb9-149">指定未遮罩之文字開頭的字元數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="06fb9-150">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06fb9-151">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="06fb9-151">The default value is 0.</span></span>

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

### <span data-ttu-id="06fb9-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="06fb9-152">-ReplacementString</span></span>
<span data-ttu-id="06fb9-153">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="06fb9-154">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06fb9-155">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="06fb9-155">The default value is 0.</span></span>

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

### <span data-ttu-id="06fb9-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fb9-156">-ResourceGroupName</span></span>
<span data-ttu-id="06fb9-157">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="06fb9-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="06fb9-158">-SchemaName</span></span>
<span data-ttu-id="06fb9-159">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="06fb9-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06fb9-160">-ServerName</span></span>
<span data-ttu-id="06fb9-161">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="06fb9-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="06fb9-162">-SuffixSize</span></span>
<span data-ttu-id="06fb9-163">指定未遮罩之文字結尾的字元數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="06fb9-164">只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="06fb9-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06fb9-165">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="06fb9-165">The default value is 0.</span></span>

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

### <span data-ttu-id="06fb9-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="06fb9-166">-TableName</span></span>
<span data-ttu-id="06fb9-167">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="06fb9-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="06fb9-168">-確認</span><span class="sxs-lookup"><span data-stu-id="06fb9-168">-Confirm</span></span>
<span data-ttu-id="06fb9-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06fb9-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06fb9-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06fb9-170">-WhatIf</span></span>
<span data-ttu-id="06fb9-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06fb9-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06fb9-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fb9-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06fb9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fb9-173">CommonParameters</span></span>
<span data-ttu-id="06fb9-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06fb9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fb9-175">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06fb9-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fb9-176">輸入</span><span class="sxs-lookup"><span data-stu-id="06fb9-176">INPUTS</span></span>

### <span data-ttu-id="06fb9-177">System.object</span><span class="sxs-lookup"><span data-stu-id="06fb9-177">System.String</span></span>

### <span data-ttu-id="06fb9-178">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06fb9-178">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="06fb9-179">"CoreLib" 1 ["System.object，System.....，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06fb9-179">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="06fb9-180">輸出</span><span class="sxs-lookup"><span data-stu-id="06fb9-180">OUTPUTS</span></span>

### <span data-ttu-id="06fb9-181">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="06fb9-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="06fb9-182">筆記</span><span class="sxs-lookup"><span data-stu-id="06fb9-182">NOTES</span></span>

## <span data-ttu-id="06fb9-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="06fb9-183">RELATED LINKS</span></span>

[<span data-ttu-id="06fb9-184">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06fb9-184">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06fb9-185">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06fb9-185">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06fb9-186">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06fb9-186">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06fb9-187">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="06fb9-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


