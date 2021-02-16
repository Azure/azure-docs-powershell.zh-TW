---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133026"
---
# <span data-ttu-id="c4e12-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="c4e12-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="c4e12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4e12-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e12-103">移除 Azure SQL managed 實例資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c4e12-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c4e12-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4e12-104">SYNTAX</span></span>

### <span data-ttu-id="c4e12-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c4e12-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e12-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e12-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e12-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e12-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e12-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4e12-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e12-109">Remove-AzSqlInstanceDatabaseSensitivityClassification Cmdlet 會移除 Azure SQL managed 實例資料庫中資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c4e12-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c4e12-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4e12-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e12-111">範例1：移除 Azure SQL managed 實例資料庫中資料行的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c4e12-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="c4e12-112">範例2：使用管道在 Azure SQL managed 實例資料庫中移除欄的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c4e12-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="c4e12-113">範例3：使用管道從 Azure SQL managed 實例資料庫中的欄移除資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="c4e12-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="c4e12-114">參數</span><span class="sxs-lookup"><span data-stu-id="c4e12-114">PARAMETERS</span></span>

### <span data-ttu-id="c4e12-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4e12-115">-AsJob</span></span>
<span data-ttu-id="c4e12-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4e12-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4e12-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="c4e12-117">-ClassificationObject</span></span>
<span data-ttu-id="c4e12-118">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="c4e12-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e12-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c4e12-119">-ColumnName</span></span>
<span data-ttu-id="c4e12-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-120">Name of column.</span></span>

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

### <span data-ttu-id="c4e12-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4e12-121">-DatabaseName</span></span>
<span data-ttu-id="c4e12-122">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="c4e12-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c4e12-123">-DatabaseObject</span></span>
<span data-ttu-id="c4e12-124">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="c4e12-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e12-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e12-125">-DefaultProfile</span></span>
<span data-ttu-id="c4e12-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e12-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c4e12-127">-InstanceName</span></span>
<span data-ttu-id="c4e12-128">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="c4e12-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4e12-129">-PassThru</span></span>
<span data-ttu-id="c4e12-130">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="c4e12-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c4e12-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e12-131">-ResourceGroupName</span></span>
<span data-ttu-id="c4e12-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4e12-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c4e12-133">-SchemaName</span></span>
<span data-ttu-id="c4e12-134">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-134">Name of schema.</span></span>

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

### <span data-ttu-id="c4e12-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="c4e12-135">-TableName</span></span>
<span data-ttu-id="c4e12-136">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4e12-136">Name of table.</span></span>

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

### <span data-ttu-id="c4e12-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c4e12-137">-Confirm</span></span>
<span data-ttu-id="c4e12-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4e12-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e12-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e12-139">-WhatIf</span></span>
<span data-ttu-id="c4e12-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4e12-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4e12-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4e12-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e12-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e12-142">CommonParameters</span></span>
<span data-ttu-id="c4e12-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4e12-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e12-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4e12-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e12-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c4e12-145">INPUTS</span></span>

### <span data-ttu-id="c4e12-146">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="c4e12-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c4e12-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c4e12-147">OUTPUTS</span></span>

### <span data-ttu-id="c4e12-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c4e12-148">System.Boolean</span></span>

## <span data-ttu-id="c4e12-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c4e12-149">NOTES</span></span>

## <span data-ttu-id="c4e12-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4e12-150">RELATED LINKS</span></span>

[<span data-ttu-id="c4e12-151">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="c4e12-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
