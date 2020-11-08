---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140850"
---
# <span data-ttu-id="22d7f-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="22d7f-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="22d7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="22d7f-103">針對 Azure SQL managed 實例資料庫中的欄停用 (關閉) 敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="22d7f-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="22d7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="22d7f-104">SYNTAX</span></span>

### <span data-ttu-id="22d7f-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22d7f-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d7f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d7f-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d7f-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d7f-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="22d7f-108">DESCRIPTION</span></span>
<span data-ttu-id="22d7f-109">Disable-AzSqlInstanceDatabaseSensitivityRecommendation Cmdlet 會針對 Azure SQL managed 實例資料庫中的欄停用 (關閉) 敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="22d7f-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="22d7f-110">示例</span><span class="sxs-lookup"><span data-stu-id="22d7f-110">EXAMPLES</span></span>

### <span data-ttu-id="22d7f-111">範例1：針對 Azure SQL managed 實例資料庫中的特定欄停用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="22d7f-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="22d7f-112">範例2：針對有管道的 Azure SQL managed 實例資料庫中具有敏感度建議的欄停用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="22d7f-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="22d7f-113">範例3：針對具有管道的 Azure SQL managed 實例資料庫中的特定欄停用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="22d7f-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="22d7f-114">參數</span><span class="sxs-lookup"><span data-stu-id="22d7f-114">PARAMETERS</span></span>

### <span data-ttu-id="22d7f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22d7f-115">-AsJob</span></span>
<span data-ttu-id="22d7f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="22d7f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22d7f-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="22d7f-117">-ColumnName</span></span>
<span data-ttu-id="22d7f-118">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-118">Name of column.</span></span>

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

### <span data-ttu-id="22d7f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22d7f-119">-DatabaseName</span></span>
<span data-ttu-id="22d7f-120">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="22d7f-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="22d7f-121">-DatabaseObject</span></span>
<span data-ttu-id="22d7f-122">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="22d7f-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="22d7f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d7f-123">-DefaultProfile</span></span>
<span data-ttu-id="22d7f-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d7f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22d7f-125">-InputObject</span></span>
<span data-ttu-id="22d7f-126">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="22d7f-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="22d7f-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22d7f-127">-InstanceName</span></span>
<span data-ttu-id="22d7f-128">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="22d7f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22d7f-129">-PassThru</span></span>
<span data-ttu-id="22d7f-130">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="22d7f-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="22d7f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d7f-131">-ResourceGroupName</span></span>
<span data-ttu-id="22d7f-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="22d7f-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="22d7f-133">-SchemaName</span></span>
<span data-ttu-id="22d7f-134">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-134">Name of schema.</span></span>

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

### <span data-ttu-id="22d7f-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="22d7f-135">-TableName</span></span>
<span data-ttu-id="22d7f-136">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="22d7f-136">Name of table.</span></span>

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

### <span data-ttu-id="22d7f-137">-確認</span><span class="sxs-lookup"><span data-stu-id="22d7f-137">-Confirm</span></span>
<span data-ttu-id="22d7f-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22d7f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d7f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d7f-139">-WhatIf</span></span>
<span data-ttu-id="22d7f-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22d7f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22d7f-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22d7f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d7f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d7f-142">CommonParameters</span></span>
<span data-ttu-id="22d7f-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22d7f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d7f-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22d7f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d7f-145">輸入</span><span class="sxs-lookup"><span data-stu-id="22d7f-145">INPUTS</span></span>

### <span data-ttu-id="22d7f-146">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="22d7f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="22d7f-147">輸出</span><span class="sxs-lookup"><span data-stu-id="22d7f-147">OUTPUTS</span></span>

### <span data-ttu-id="22d7f-148">System.object</span><span class="sxs-lookup"><span data-stu-id="22d7f-148">System.Boolean</span></span>

## <span data-ttu-id="22d7f-149">筆記</span><span class="sxs-lookup"><span data-stu-id="22d7f-149">NOTES</span></span>

## <span data-ttu-id="22d7f-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="22d7f-150">RELATED LINKS</span></span>

[<span data-ttu-id="22d7f-151">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="22d7f-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)