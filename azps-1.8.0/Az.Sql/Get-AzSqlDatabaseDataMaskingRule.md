---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620483"
---
# <span data-ttu-id="08b30-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08b30-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="08b30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08b30-102">SYNOPSIS</span></span>
<span data-ttu-id="08b30-103">從資料庫取得資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="08b30-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="08b30-104">句法</span><span class="sxs-lookup"><span data-stu-id="08b30-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b30-105">說明</span><span class="sxs-lookup"><span data-stu-id="08b30-105">DESCRIPTION</span></span>
<span data-ttu-id="08b30-106">**AzSqlDatabaseDataMaskingRule** Cmdlet 會取得特定資料遮罩規則或 Azure SQL 資料庫的所有資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="08b30-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="08b30-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫，並使用 *RuleId* 參數指定這個 Cmdlet 傳回的規則。</span><span class="sxs-lookup"><span data-stu-id="08b30-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="08b30-108">如果您不提供 *RuleId* ，則會傳回該 Azure SQL 資料庫的所有資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="08b30-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="08b30-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08b30-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="08b30-110">示例</span><span class="sxs-lookup"><span data-stu-id="08b30-110">EXAMPLES</span></span>

### <span data-ttu-id="08b30-111">範例1：從資料庫取得所有資料遮罩規則</span><span class="sxs-lookup"><span data-stu-id="08b30-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="08b30-112">範例2：取得架構 "dbo"、table "table1" 和欄 "欄 1" 中定義的資料遮罩規則。</span><span class="sxs-lookup"><span data-stu-id="08b30-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="08b30-113">參數</span><span class="sxs-lookup"><span data-stu-id="08b30-113">PARAMETERS</span></span>

### <span data-ttu-id="08b30-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="08b30-114">-ColumnName</span></span>
<span data-ttu-id="08b30-115">指定遮罩規則所針對的欄名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="08b30-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08b30-116">-DatabaseName</span></span>
<span data-ttu-id="08b30-117">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="08b30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b30-118">-DefaultProfile</span></span>
<span data-ttu-id="08b30-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="08b30-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08b30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b30-120">-ResourceGroupName</span></span>
<span data-ttu-id="08b30-121">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="08b30-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="08b30-122">-SchemaName</span></span>
<span data-ttu-id="08b30-123">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="08b30-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08b30-124">-ServerName</span></span>
<span data-ttu-id="08b30-125">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="08b30-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="08b30-126">-TableName</span></span>
<span data-ttu-id="08b30-127">指定 Azure SQL 資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="08b30-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="08b30-128">-確認</span><span class="sxs-lookup"><span data-stu-id="08b30-128">-Confirm</span></span>
<span data-ttu-id="08b30-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08b30-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b30-130">-WhatIf</span></span>
<span data-ttu-id="08b30-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08b30-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b30-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08b30-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b30-133">CommonParameters</span></span>
<span data-ttu-id="08b30-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08b30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b30-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08b30-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b30-136">輸入</span><span class="sxs-lookup"><span data-stu-id="08b30-136">INPUTS</span></span>

### <span data-ttu-id="08b30-137">System.object</span><span class="sxs-lookup"><span data-stu-id="08b30-137">System.String</span></span>

## <span data-ttu-id="08b30-138">輸出</span><span class="sxs-lookup"><span data-stu-id="08b30-138">OUTPUTS</span></span>

### <span data-ttu-id="08b30-139">DatabaseDataMaskingRuleModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="08b30-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="08b30-140">筆記</span><span class="sxs-lookup"><span data-stu-id="08b30-140">NOTES</span></span>

## <span data-ttu-id="08b30-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="08b30-141">RELATED LINKS</span></span>

[<span data-ttu-id="08b30-142">AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="08b30-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="08b30-143">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08b30-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="08b30-144">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08b30-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="08b30-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="08b30-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="08b30-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="08b30-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


