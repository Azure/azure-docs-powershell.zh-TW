---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 95c5829c3d715b1510c1a58e8baf5e7809f9cd8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917641"
---
# <span data-ttu-id="5a0e0-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5a0e0-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="5a0e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0e0-103">停用 (Azure SQL) 實例資料庫中的欄之敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="5a0e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a0e0-104">SYNTAX</span></span>

### <span data-ttu-id="5a0e0-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a0e0-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0e0-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a0e0-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0e0-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a0e0-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a0e0-108">描述</span><span class="sxs-lookup"><span data-stu-id="5a0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="5a0e0-109">Cmdlet 會Disable-AzSqlInstanceDatabaseSensitivityRecommendation Azure SQL 受管理實例 (中) 欄的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="5a0e0-110">例子</span><span class="sxs-lookup"><span data-stu-id="5a0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="5a0e0-111">範例 1：停用 Azure SQL 受管理實例資料庫中的特定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="5a0e0-112">範例 2：停用在 Azure SQL 受管理的實例資料庫中具有使用管道的敏感度建議欄的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="5a0e0-113">範例 3：在 Azure SQL 受管理的實例資料庫中，使用管道停用特定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="5a0e0-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a0e0-114">PARAMETERS</span></span>

### <span data-ttu-id="5a0e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a0e0-115">-AsJob</span></span>
<span data-ttu-id="5a0e0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a0e0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a0e0-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-117">-ColumnName</span></span>
<span data-ttu-id="5a0e0-118">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-118">Name of column.</span></span>

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

### <span data-ttu-id="5a0e0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-119">-DatabaseName</span></span>
<span data-ttu-id="5a0e0-120">Azure SQL 受管理的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="5a0e0-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5a0e0-121">-DatabaseObject</span></span>
<span data-ttu-id="5a0e0-122">Azure SQL 受管理的實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="5a0e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0e0-123">-DefaultProfile</span></span>
<span data-ttu-id="5a0e0-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a0e0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a0e0-125">-InputObject</span></span>
<span data-ttu-id="5a0e0-126">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5a0e0-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-127">-InstanceName</span></span>
<span data-ttu-id="5a0e0-128">Azure SQL 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="5a0e0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a0e0-129">-PassThru</span></span>
<span data-ttu-id="5a0e0-130">指定是否要在 Cmdlet 執行結束時輸出敏感度分類模型</span><span class="sxs-lookup"><span data-stu-id="5a0e0-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="5a0e0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a0e0-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a0e0-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-133">-SchemaName</span></span>
<span data-ttu-id="5a0e0-134">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-134">Name of schema.</span></span>

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

### <span data-ttu-id="5a0e0-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="5a0e0-135">-TableName</span></span>
<span data-ttu-id="5a0e0-136">資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-136">Name of table.</span></span>

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

### <span data-ttu-id="5a0e0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="5a0e0-137">-Confirm</span></span>
<span data-ttu-id="5a0e0-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a0e0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0e0-139">-WhatIf</span></span>
<span data-ttu-id="5a0e0-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a0e0-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a0e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0e0-142">CommonParameters</span></span>
<span data-ttu-id="5a0e0-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a0e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0e0-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a0e0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0e0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="5a0e0-145">INPUTS</span></span>

### <span data-ttu-id="5a0e0-146">Microsoft.Azure.Commands.sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5a0e0-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="5a0e0-147">輸出</span><span class="sxs-lookup"><span data-stu-id="5a0e0-147">OUTPUTS</span></span>

### <span data-ttu-id="5a0e0-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a0e0-148">System.Boolean</span></span>

## <span data-ttu-id="5a0e0-149">筆記</span><span class="sxs-lookup"><span data-stu-id="5a0e0-149">NOTES</span></span>

## <span data-ttu-id="5a0e0-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a0e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="5a0e0-151">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="5a0e0-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)