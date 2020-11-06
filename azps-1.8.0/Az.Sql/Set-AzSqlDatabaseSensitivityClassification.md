---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 3b3bc7b98bd4325eda075e24220f88c6e5874aaf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614729"
---
# <span data-ttu-id="75a33-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="75a33-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="75a33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a33-102">SYNOPSIS</span></span>
<span data-ttu-id="75a33-103">設定資料庫中資料行的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="75a33-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="75a33-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a33-104">SYNTAX</span></span>

### <span data-ttu-id="75a33-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75a33-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a33-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a33-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a33-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a33-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a33-108">說明</span><span class="sxs-lookup"><span data-stu-id="75a33-108">DESCRIPTION</span></span>
<span data-ttu-id="75a33-109">Set-AzSqlDatabaseSensitivityClassification Cmdlet 會設定資料庫中資料行的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="75a33-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="75a33-110">示例</span><span class="sxs-lookup"><span data-stu-id="75a33-110">EXAMPLES</span></span>

### <span data-ttu-id="75a33-111">範例1：在 Azure SQL 資料庫中設定欄的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="75a33-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="75a33-112">範例2：針對 Azure SQL 資料庫中的欄設定建議的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="75a33-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="75a33-113">範例3：使用管道在 Azure SQL 資料庫中設定資料行的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="75a33-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="75a33-114">參數</span><span class="sxs-lookup"><span data-stu-id="75a33-114">PARAMETERS</span></span>

### <span data-ttu-id="75a33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75a33-115">-AsJob</span></span>
<span data-ttu-id="75a33-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75a33-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75a33-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="75a33-117">-ClassificationObject</span></span>
<span data-ttu-id="75a33-118">代表 SQL 資料庫靈敏度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="75a33-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="75a33-119">-ColumnName</span></span>
<span data-ttu-id="75a33-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75a33-121">-DatabaseName</span></span>
<span data-ttu-id="75a33-122">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="75a33-123">-DatabaseObject</span></span>
<span data-ttu-id="75a33-124">SQL 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="75a33-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a33-125">-DefaultProfile</span></span>
<span data-ttu-id="75a33-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75a33-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a33-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="75a33-127">-InformationType</span></span>
<span data-ttu-id="75a33-128">描述儲存在欄中之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75a33-129">-PassThru</span></span>
<span data-ttu-id="75a33-130">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="75a33-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="75a33-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a33-131">-ResourceGroupName</span></span>
<span data-ttu-id="75a33-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="75a33-133">-SchemaName</span></span>
<span data-ttu-id="75a33-134">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-134">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="75a33-135">-SensitivityLabel</span></span>
<span data-ttu-id="75a33-136">描述儲存在欄中之資料敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75a33-137">-ServerName</span></span>
<span data-ttu-id="75a33-138">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="75a33-139">-TableName</span></span>
<span data-ttu-id="75a33-140">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a33-140">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-141">-確認</span><span class="sxs-lookup"><span data-stu-id="75a33-141">-Confirm</span></span>
<span data-ttu-id="75a33-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75a33-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a33-143">-WhatIf</span></span>
<span data-ttu-id="75a33-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75a33-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75a33-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75a33-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a33-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a33-146">CommonParameters</span></span>
<span data-ttu-id="75a33-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a33-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a33-148">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75a33-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a33-149">輸入</span><span class="sxs-lookup"><span data-stu-id="75a33-149">INPUTS</span></span>

### <span data-ttu-id="75a33-150">SqlDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="75a33-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="75a33-151">輸出</span><span class="sxs-lookup"><span data-stu-id="75a33-151">OUTPUTS</span></span>

### <span data-ttu-id="75a33-152">System.object</span><span class="sxs-lookup"><span data-stu-id="75a33-152">System.Boolean</span></span>

## <span data-ttu-id="75a33-153">筆記</span><span class="sxs-lookup"><span data-stu-id="75a33-153">NOTES</span></span>

## <span data-ttu-id="75a33-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a33-154">RELATED LINKS</span></span>

[<span data-ttu-id="75a33-155">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="75a33-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
