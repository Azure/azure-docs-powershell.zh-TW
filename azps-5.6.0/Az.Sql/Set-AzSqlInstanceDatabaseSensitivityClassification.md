---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fac62ac0e75587e19a9ba0a5e99461693ce31c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903758"
---
# <span data-ttu-id="b73fd-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b73fd-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="b73fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b73fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b73fd-103">在 Azure SQL 受管理的實例資料庫中設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b73fd-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b73fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="b73fd-104">SYNTAX</span></span>

### <span data-ttu-id="b73fd-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b73fd-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73fd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73fd-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73fd-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73fd-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73fd-108">描述</span><span class="sxs-lookup"><span data-stu-id="b73fd-108">DESCRIPTION</span></span>
<span data-ttu-id="b73fd-109">此Set-AzSqlInstanceDatabaseSensitivityClassification Cmdlet 會設定 Azure SQL 受管理實例資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b73fd-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b73fd-110">例子</span><span class="sxs-lookup"><span data-stu-id="b73fd-110">EXAMPLES</span></span>

### <span data-ttu-id="b73fd-111">範例 1：在 Azure SQL 受管理的實例資料庫中設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b73fd-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="b73fd-112">範例 2：在 Azure SQL 受管理的實例資料庫中設定資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b73fd-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="b73fd-113">範例 3：在 Azure SQL 受管理的實例資料庫中，使用管線設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="b73fd-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="b73fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="b73fd-114">PARAMETERS</span></span>

### <span data-ttu-id="b73fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b73fd-115">-AsJob</span></span>
<span data-ttu-id="b73fd-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b73fd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b73fd-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="b73fd-117">-ClassificationObject</span></span>
<span data-ttu-id="b73fd-118">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="b73fd-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="b73fd-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b73fd-119">-ColumnName</span></span>
<span data-ttu-id="b73fd-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-120">Name of column.</span></span>

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

### <span data-ttu-id="b73fd-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b73fd-121">-DatabaseName</span></span>
<span data-ttu-id="b73fd-122">Azure SQL 受管理的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="b73fd-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b73fd-123">-DatabaseObject</span></span>
<span data-ttu-id="b73fd-124">Azure SQL 受管理的實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b73fd-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="b73fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73fd-125">-DefaultProfile</span></span>
<span data-ttu-id="b73fd-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b73fd-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="b73fd-127">-InformationType</span></span>
<span data-ttu-id="b73fd-128">描述資料行中儲存之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="b73fd-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b73fd-129">-InstanceName</span></span>
<span data-ttu-id="b73fd-130">Azure SQL 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="b73fd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b73fd-131">-PassThru</span></span>
<span data-ttu-id="b73fd-132">指定是否要在 Cmdlet 執行結束時輸出敏感度分類模型</span><span class="sxs-lookup"><span data-stu-id="b73fd-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="b73fd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73fd-133">-ResourceGroupName</span></span>
<span data-ttu-id="b73fd-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="b73fd-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b73fd-135">-SchemaName</span></span>
<span data-ttu-id="b73fd-136">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-136">Name of schema.</span></span>

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

### <span data-ttu-id="b73fd-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="b73fd-137">-SensitivityLabel</span></span>
<span data-ttu-id="b73fd-138">描述資料行中儲存之資料的敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="b73fd-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="b73fd-139">-TableName</span></span>
<span data-ttu-id="b73fd-140">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73fd-140">Name of table.</span></span>

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

### <span data-ttu-id="b73fd-141">-確認</span><span class="sxs-lookup"><span data-stu-id="b73fd-141">-Confirm</span></span>
<span data-ttu-id="b73fd-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b73fd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73fd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73fd-143">-WhatIf</span></span>
<span data-ttu-id="b73fd-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b73fd-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b73fd-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b73fd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73fd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73fd-146">CommonParameters</span></span>
<span data-ttu-id="b73fd-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b73fd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73fd-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b73fd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73fd-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b73fd-149">INPUTS</span></span>

### <span data-ttu-id="b73fd-150">Microsoft.Azure.Commands.sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b73fd-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b73fd-151">輸出</span><span class="sxs-lookup"><span data-stu-id="b73fd-151">OUTPUTS</span></span>

### <span data-ttu-id="b73fd-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b73fd-152">System.Boolean</span></span>

## <span data-ttu-id="b73fd-153">筆記</span><span class="sxs-lookup"><span data-stu-id="b73fd-153">NOTES</span></span>

## <span data-ttu-id="b73fd-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b73fd-154">RELATED LINKS</span></span>

[<span data-ttu-id="b73fd-155">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="b73fd-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
