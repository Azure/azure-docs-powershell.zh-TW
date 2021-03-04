---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: a9085433bb888fa8e37405881a20a55a4f08b96d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904198"
---
# <span data-ttu-id="9689c-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9689c-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="9689c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9689c-102">SYNOPSIS</span></span>
<span data-ttu-id="9689c-103">停用 (SQL) 欄的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="9689c-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="9689c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9689c-104">SYNTAX</span></span>

### <span data-ttu-id="9689c-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9689c-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9689c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9689c-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9689c-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9689c-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9689c-108">描述</span><span class="sxs-lookup"><span data-stu-id="9689c-108">DESCRIPTION</span></span>
<span data-ttu-id="9689c-109">Cmdlet Disable-AzSynapseSqlPoolSensitivityRecommendation停用 (會) SQL 集區中欄的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="9689c-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="9689c-110">例子</span><span class="sxs-lookup"><span data-stu-id="9689c-110">EXAMPLES</span></span>

### <span data-ttu-id="9689c-111">範例 1：停用 Azure Synapse SQL 資料庫中特定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="9689c-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9689c-112">範例 2：停用在 Azure Synapse SQL 集區使用管道提供敏感度建議的資料行敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="9689c-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="9689c-113">範例 3：使用管道在 Azure Synapse SQL 資料庫中停用特定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="9689c-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9689c-114">參數</span><span class="sxs-lookup"><span data-stu-id="9689c-114">PARAMETERS</span></span>

### <span data-ttu-id="9689c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9689c-115">-AsJob</span></span>
<span data-ttu-id="9689c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9689c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9689c-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9689c-117">-ColumnName</span></span>
<span data-ttu-id="9689c-118">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="9689c-118">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9689c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9689c-119">-DefaultProfile</span></span>
<span data-ttu-id="9689c-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9689c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9689c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9689c-121">-InputObject</span></span>
<span data-ttu-id="9689c-122">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="9689c-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9689c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9689c-123">-PassThru</span></span>
<span data-ttu-id="9689c-124">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="9689c-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9689c-125">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="9689c-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9689c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9689c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9689c-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9689c-127">Resource group name.</span></span>

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

### <span data-ttu-id="9689c-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9689c-128">-SchemaName</span></span>
<span data-ttu-id="9689c-129">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="9689c-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9689c-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9689c-130">-SqlPoolName</span></span>
<span data-ttu-id="9689c-131">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9689c-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9689c-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9689c-132">-SqlPoolObject</span></span>
<span data-ttu-id="9689c-133">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="9689c-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9689c-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="9689c-134">-TableName</span></span>
<span data-ttu-id="9689c-135">資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="9689c-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9689c-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9689c-136">-WorkspaceName</span></span>
<span data-ttu-id="9689c-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9689c-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9689c-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9689c-138">-Confirm</span></span>
<span data-ttu-id="9689c-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9689c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9689c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9689c-140">-WhatIf</span></span>
<span data-ttu-id="9689c-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9689c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9689c-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9689c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9689c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9689c-143">CommonParameters</span></span>
<span data-ttu-id="9689c-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9689c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9689c-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9689c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9689c-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9689c-146">INPUTS</span></span>

### <span data-ttu-id="9689c-147">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9689c-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="9689c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9689c-148">System.String</span></span>

### <span data-ttu-id="9689c-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9689c-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9689c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9689c-150">OUTPUTS</span></span>

### <span data-ttu-id="9689c-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9689c-151">System.Boolean</span></span>

## <span data-ttu-id="9689c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="9689c-152">NOTES</span></span>

## <span data-ttu-id="9689c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="9689c-153">RELATED LINKS</span></span>
