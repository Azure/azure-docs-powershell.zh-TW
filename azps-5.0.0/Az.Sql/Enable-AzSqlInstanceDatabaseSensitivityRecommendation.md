---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138156"
---
# <span data-ttu-id="67c12-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="67c12-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="67c12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67c12-102">SYNOPSIS</span></span>
<span data-ttu-id="67c12-103">針對資料行啟用敏感度建議， (預設會針對 Azure SQL managed 實例資料庫中的所有資料行) 建議。</span><span class="sxs-lookup"><span data-stu-id="67c12-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="67c12-104">句法</span><span class="sxs-lookup"><span data-stu-id="67c12-104">SYNTAX</span></span>

### <span data-ttu-id="67c12-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="67c12-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c12-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c12-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c12-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c12-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c12-108">說明</span><span class="sxs-lookup"><span data-stu-id="67c12-108">DESCRIPTION</span></span>
<span data-ttu-id="67c12-109">Enable-AzSqlInstanceDatabaseSensitivityRecommendation Cmdlet 會針對 Azure SQL managed 實例資料庫中的欄啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="67c12-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="67c12-110">示例</span><span class="sxs-lookup"><span data-stu-id="67c12-110">EXAMPLES</span></span>

### <span data-ttu-id="67c12-111">範例1：針對 Azure SQL managed 實例資料庫中的特定欄啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="67c12-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="67c12-112">範例2：使用管道針對 Azure SQL managed 實例資料庫中的特定欄啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="67c12-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="67c12-113">參數</span><span class="sxs-lookup"><span data-stu-id="67c12-113">PARAMETERS</span></span>

### <span data-ttu-id="67c12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67c12-114">-AsJob</span></span>
<span data-ttu-id="67c12-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67c12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67c12-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="67c12-116">-ColumnName</span></span>
<span data-ttu-id="67c12-117">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-117">Name of column.</span></span>

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

### <span data-ttu-id="67c12-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67c12-118">-DatabaseName</span></span>
<span data-ttu-id="67c12-119">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="67c12-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="67c12-120">-DatabaseObject</span></span>
<span data-ttu-id="67c12-121">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="67c12-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="67c12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c12-122">-DefaultProfile</span></span>
<span data-ttu-id="67c12-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67c12-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c12-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c12-124">-InputObject</span></span>
<span data-ttu-id="67c12-125">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="67c12-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67c12-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="67c12-126">-InstanceName</span></span>
<span data-ttu-id="67c12-127">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="67c12-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67c12-128">-PassThru</span></span>
<span data-ttu-id="67c12-129">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="67c12-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="67c12-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c12-130">-ResourceGroupName</span></span>
<span data-ttu-id="67c12-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="67c12-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="67c12-132">-SchemaName</span></span>
<span data-ttu-id="67c12-133">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-133">Name of schema.</span></span>

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

### <span data-ttu-id="67c12-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="67c12-134">-TableName</span></span>
<span data-ttu-id="67c12-135">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="67c12-135">Name of table.</span></span>

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

### <span data-ttu-id="67c12-136">-確認</span><span class="sxs-lookup"><span data-stu-id="67c12-136">-Confirm</span></span>
<span data-ttu-id="67c12-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67c12-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c12-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c12-138">-WhatIf</span></span>
<span data-ttu-id="67c12-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67c12-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67c12-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67c12-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c12-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c12-141">CommonParameters</span></span>
<span data-ttu-id="67c12-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67c12-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c12-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67c12-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c12-144">輸入</span><span class="sxs-lookup"><span data-stu-id="67c12-144">INPUTS</span></span>

### <span data-ttu-id="67c12-145">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="67c12-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="67c12-146">輸出</span><span class="sxs-lookup"><span data-stu-id="67c12-146">OUTPUTS</span></span>

### <span data-ttu-id="67c12-147">System.object</span><span class="sxs-lookup"><span data-stu-id="67c12-147">System.Boolean</span></span>

## <span data-ttu-id="67c12-148">筆記</span><span class="sxs-lookup"><span data-stu-id="67c12-148">NOTES</span></span>

## <span data-ttu-id="67c12-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="67c12-149">RELATED LINKS</span></span>

[<span data-ttu-id="67c12-150">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="67c12-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)