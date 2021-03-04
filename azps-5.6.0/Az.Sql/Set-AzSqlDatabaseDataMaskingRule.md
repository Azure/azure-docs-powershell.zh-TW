---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8ed90e6c3a145298029f1ef4d12b6248ed39526e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913029"
---
# <span data-ttu-id="bb4f4-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb4f4-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="bb4f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4f4-103">設定資料庫的資料遮罩規則屬性。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="bb4f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb4f4-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb4f4-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4f4-106">**Set-AzSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="bb4f4-107">若要使用 Cmdlet，請提供 *ResourceGroupName、ServerName、DatabaseName* 和 *RuleId* 參數來識別規則。  </span><span class="sxs-lookup"><span data-stu-id="bb4f4-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="bb4f4-108">您可以提供 *SchemaName、TableName* 和 *ColumnName* 的任何參數，以重新設定規則目標。 </span><span class="sxs-lookup"><span data-stu-id="bb4f4-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="bb4f4-109">指定 *MaskingFunction 參數* 以修改資料的遮罩方法。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="bb4f4-110">如果您為 *MaskingFunction* 指定 Number 或 Text 的值，您可以指定數位遮罩的 *NumberFrom* 和 *NumberTo* 參數，或是文字遮罩的 *首碼Size、ReplacementString* 和 *SuffixSize* 參數。 </span><span class="sxs-lookup"><span data-stu-id="bb4f4-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="bb4f4-111">如果命令成功，而且如果您指定 *PassThru* 參數，Cmdlet 會傳回描述資料遮罩規則屬性和規則識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="bb4f4-112">規則識別碼包含但不限於 ResourceGroupName、ServerName、DatabaseName和 **RuleId。** </span><span class="sxs-lookup"><span data-stu-id="bb4f4-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="bb4f4-113">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bb4f4-114">例子</span><span class="sxs-lookup"><span data-stu-id="bb4f4-114">EXAMPLES</span></span>

### <span data-ttu-id="bb4f4-115">範例 1：變更資料庫中的資料遮罩規則範圍</span><span class="sxs-lookup"><span data-stu-id="bb4f4-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="bb4f4-116">此命令會修改具有識別碼 Rule17 的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="bb4f4-117">規則在伺服器 Server01 名為 Database01 的資料庫中運作。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="bb4f4-118">此命令會變更亂數產生為遮罩值之間隔的邊界。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="bb4f4-119">新的範圍介於 23 到 42 之間。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="bb4f4-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="bb4f4-120">Example 2</span></span>

<span data-ttu-id="bb4f4-121">設定資料庫的資料遮罩規則屬性。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="bb4f4-122"> (自動) </span><span class="sxs-lookup"><span data-stu-id="bb4f4-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="bb4f4-123">參數</span><span class="sxs-lookup"><span data-stu-id="bb4f4-123">PARAMETERS</span></span>

### <span data-ttu-id="bb4f4-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-124">-ColumnName</span></span>
<span data-ttu-id="bb4f4-125">指定遮罩規則所針對之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="bb4f4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-126">-DatabaseName</span></span>
<span data-ttu-id="bb4f4-127">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="bb4f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4f4-128">-DefaultProfile</span></span>
<span data-ttu-id="bb4f4-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bb4f4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb4f4-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="bb4f4-130">-MaskingFunction</span></span>
<span data-ttu-id="bb4f4-131">指定規則使用的遮罩函數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="bb4f4-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bb4f4-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb4f4-133">預設</span><span class="sxs-lookup"><span data-stu-id="bb4f4-133">Default</span></span>
- <span data-ttu-id="bb4f4-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="bb4f4-134">NoMasking</span></span>
- <span data-ttu-id="bb4f4-135">文本</span><span class="sxs-lookup"><span data-stu-id="bb4f4-135">Text</span></span>
- <span data-ttu-id="bb4f4-136">數量</span><span class="sxs-lookup"><span data-stu-id="bb4f4-136">Number</span></span>
- <span data-ttu-id="bb4f4-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="bb4f4-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="bb4f4-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="bb4f4-138">CreditCardNumber</span></span>
- <span data-ttu-id="bb4f4-139">電子郵件 預設值為預設值。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="bb4f4-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="bb4f4-140">-NumberFrom</span></span>
<span data-ttu-id="bb4f4-141">指定選取隨機值之區間的下限。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="bb4f4-142">只有在您為 *MaskingFunction* 參數指定 Number 值時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="bb4f4-143">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-143">The default value is 0.</span></span>

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

### <span data-ttu-id="bb4f4-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="bb4f4-144">-NumberTo</span></span>
<span data-ttu-id="bb4f4-145">指定選取隨機值之區間的上限。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="bb4f4-146">只有在您為 *MaskingFunction* 參數指定 Number 值時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="bb4f4-147">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-147">The default value is 0.</span></span>

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

### <span data-ttu-id="bb4f4-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb4f4-148">-PassThru</span></span>
<span data-ttu-id="bb4f4-149">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb4f4-150">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb4f4-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="bb4f4-151">-PrefixSize</span></span>
<span data-ttu-id="bb4f4-152">指定文字開始時未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="bb4f4-153">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="bb4f4-154">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-154">The default value is 0.</span></span>

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

### <span data-ttu-id="bb4f4-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="bb4f4-155">-ReplacementString</span></span>
<span data-ttu-id="bb4f4-156">指定文字結尾未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="bb4f4-157">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="bb4f4-158">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-158">The default value is 0.</span></span>

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

### <span data-ttu-id="bb4f4-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-159">-ResourceGroupName</span></span>
<span data-ttu-id="bb4f4-160">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bb4f4-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-161">-SchemaName</span></span>
<span data-ttu-id="bb4f4-162">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="bb4f4-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-163">-ServerName</span></span>
<span data-ttu-id="bb4f4-164">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bb4f4-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="bb4f4-165">-SuffixSize</span></span>
<span data-ttu-id="bb4f4-166">指定文字結尾未遮罩的字元數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="bb4f4-167">只有在您為 *MaskingFunction* 參數指定 Text 值時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="bb4f4-168">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-168">The default value is 0.</span></span>

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

### <span data-ttu-id="bb4f4-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="bb4f4-169">-TableName</span></span>
<span data-ttu-id="bb4f4-170">指定包含遮罩資料行的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="bb4f4-171">-確認</span><span class="sxs-lookup"><span data-stu-id="bb4f4-171">-Confirm</span></span>
<span data-ttu-id="bb4f4-172">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb4f4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4f4-173">-WhatIf</span></span>
<span data-ttu-id="bb4f4-174">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4f4-175">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb4f4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4f4-176">CommonParameters</span></span>
<span data-ttu-id="bb4f4-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb4f4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4f4-178">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb4f4-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4f4-179">輸入</span><span class="sxs-lookup"><span data-stu-id="bb4f4-179">INPUTS</span></span>

### <span data-ttu-id="bb4f4-180">System.String</span><span class="sxs-lookup"><span data-stu-id="bb4f4-180">System.String</span></span>

### <span data-ttu-id="bb4f4-181">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb4f4-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bb4f4-182">System.Nullable'1[[System.Double， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb4f4-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bb4f4-183">輸出</span><span class="sxs-lookup"><span data-stu-id="bb4f4-183">OUTPUTS</span></span>

### <span data-ttu-id="bb4f4-184">Microsoft.Azure.Commands.sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="bb4f4-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="bb4f4-185">筆記</span><span class="sxs-lookup"><span data-stu-id="bb4f4-185">NOTES</span></span>

## <span data-ttu-id="bb4f4-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb4f4-186">RELATED LINKS</span></span>

[<span data-ttu-id="bb4f4-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb4f4-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bb4f4-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb4f4-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bb4f4-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb4f4-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bb4f4-190">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="bb4f4-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


