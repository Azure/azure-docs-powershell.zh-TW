---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137715"
---
# <span data-ttu-id="f1fda-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f1fda-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="f1fda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1fda-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fda-103">啟用欄上的敏感度建議 (建議預設會在 SQL 池中) 的所有資料行上啟用。</span><span class="sxs-lookup"><span data-stu-id="f1fda-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="f1fda-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1fda-104">SYNTAX</span></span>

### <span data-ttu-id="f1fda-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f1fda-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1fda-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fda-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1fda-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fda-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1fda-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1fda-108">DESCRIPTION</span></span>
<span data-ttu-id="f1fda-109">Enable-AzSynapseSqlPoolSensitivityRecommendation Cmdlet 會針對 SQL 池中的欄啟用敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="f1fda-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f1fda-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1fda-110">EXAMPLES</span></span>

### <span data-ttu-id="f1fda-111">範例1：針對 Azure Synapse SQL pool 中的特定資料行啟用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="f1fda-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f1fda-112">範例2：使用管道在特定欄的 Azure Synapse SQL pool 上啟用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="f1fda-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f1fda-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1fda-113">PARAMETERS</span></span>

### <span data-ttu-id="f1fda-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1fda-114">-AsJob</span></span>
<span data-ttu-id="f1fda-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1fda-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1fda-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f1fda-116">-ColumnName</span></span>
<span data-ttu-id="f1fda-117">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-117">Name of column.</span></span>

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

### <span data-ttu-id="f1fda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fda-118">-DefaultProfile</span></span>
<span data-ttu-id="f1fda-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1fda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1fda-120">-InputObject</span></span>
<span data-ttu-id="f1fda-121">代表 SQL Pool 敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="f1fda-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f1fda-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1fda-122">-PassThru</span></span>
<span data-ttu-id="f1fda-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="f1fda-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f1fda-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="f1fda-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f1fda-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fda-125">-ResourceGroupName</span></span>
<span data-ttu-id="f1fda-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-126">Resource group name.</span></span>

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

### <span data-ttu-id="f1fda-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f1fda-127">-SchemaName</span></span>
<span data-ttu-id="f1fda-128">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-128">Name of schema.</span></span>

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

### <span data-ttu-id="f1fda-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="f1fda-129">-SqlPoolName</span></span>
<span data-ttu-id="f1fda-130">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f1fda-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="f1fda-131">-SqlPoolObject</span></span>
<span data-ttu-id="f1fda-132">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f1fda-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1fda-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="f1fda-133">-TableName</span></span>
<span data-ttu-id="f1fda-134">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-134">Name of table.</span></span>

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

### <span data-ttu-id="f1fda-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1fda-135">-WorkspaceName</span></span>
<span data-ttu-id="f1fda-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fda-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1fda-137">-確認</span><span class="sxs-lookup"><span data-stu-id="f1fda-137">-Confirm</span></span>
<span data-ttu-id="f1fda-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1fda-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fda-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fda-139">-WhatIf</span></span>
<span data-ttu-id="f1fda-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1fda-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fda-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1fda-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fda-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fda-142">CommonParameters</span></span>
<span data-ttu-id="f1fda-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1fda-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fda-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1fda-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fda-145">輸入</span><span class="sxs-lookup"><span data-stu-id="f1fda-145">INPUTS</span></span>

### <span data-ttu-id="f1fda-146">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="f1fda-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="f1fda-147">System.object</span><span class="sxs-lookup"><span data-stu-id="f1fda-147">System.String</span></span>

### <span data-ttu-id="f1fda-148">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f1fda-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f1fda-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f1fda-149">OUTPUTS</span></span>

### <span data-ttu-id="f1fda-150">System.object</span><span class="sxs-lookup"><span data-stu-id="f1fda-150">System.Boolean</span></span>

## <span data-ttu-id="f1fda-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f1fda-151">NOTES</span></span>

## <span data-ttu-id="f1fda-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1fda-152">RELATED LINKS</span></span>
