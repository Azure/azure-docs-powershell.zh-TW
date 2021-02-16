---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137722"
---
# <span data-ttu-id="f197e-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f197e-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="f197e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f197e-102">SYNOPSIS</span></span>
<span data-ttu-id="f197e-103">針對 SQL 池中的欄停用 (關閉) 敏感性建議。</span><span class="sxs-lookup"><span data-stu-id="f197e-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f197e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f197e-104">SYNTAX</span></span>

### <span data-ttu-id="f197e-105">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f197e-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f197e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f197e-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f197e-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f197e-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f197e-108">說明</span><span class="sxs-lookup"><span data-stu-id="f197e-108">DESCRIPTION</span></span>
<span data-ttu-id="f197e-109">Disable-AzSynapseSqlPoolSensitivityRecommendation Cmdlet 會針對 SQL 池中的欄停用 (關閉) 敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="f197e-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f197e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f197e-110">EXAMPLES</span></span>

### <span data-ttu-id="f197e-111">範例1：停用 Azure Synapse SQL pool 中指定資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="f197e-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f197e-112">範例2：在使用管道的 Azure Synapse SQL pool 中，針對具有靈敏度建議的欄停用靈敏度建議。</span><span class="sxs-lookup"><span data-stu-id="f197e-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="f197e-113">範例3：在 Azure Synapse SQL pool 中使用管道停用特定欄上的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="f197e-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f197e-114">參數</span><span class="sxs-lookup"><span data-stu-id="f197e-114">PARAMETERS</span></span>

### <span data-ttu-id="f197e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f197e-115">-AsJob</span></span>
<span data-ttu-id="f197e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f197e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f197e-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f197e-117">-ColumnName</span></span>
<span data-ttu-id="f197e-118">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-118">Name of column.</span></span>

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

### <span data-ttu-id="f197e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f197e-119">-DefaultProfile</span></span>
<span data-ttu-id="f197e-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f197e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f197e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f197e-121">-InputObject</span></span>
<span data-ttu-id="f197e-122">代表 SQL Pool 敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="f197e-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f197e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f197e-123">-PassThru</span></span>
<span data-ttu-id="f197e-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="f197e-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f197e-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="f197e-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f197e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f197e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f197e-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-127">Resource group name.</span></span>

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

### <span data-ttu-id="f197e-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f197e-128">-SchemaName</span></span>
<span data-ttu-id="f197e-129">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-129">Name of schema.</span></span>

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

### <span data-ttu-id="f197e-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="f197e-130">-SqlPoolName</span></span>
<span data-ttu-id="f197e-131">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f197e-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="f197e-132">-SqlPoolObject</span></span>
<span data-ttu-id="f197e-133">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f197e-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f197e-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="f197e-134">-TableName</span></span>
<span data-ttu-id="f197e-135">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-135">Name of table.</span></span>

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

### <span data-ttu-id="f197e-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f197e-136">-WorkspaceName</span></span>
<span data-ttu-id="f197e-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f197e-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f197e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f197e-138">-Confirm</span></span>
<span data-ttu-id="f197e-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f197e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f197e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f197e-140">-WhatIf</span></span>
<span data-ttu-id="f197e-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f197e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f197e-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f197e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f197e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f197e-143">CommonParameters</span></span>
<span data-ttu-id="f197e-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f197e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f197e-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f197e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f197e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f197e-146">INPUTS</span></span>

### <span data-ttu-id="f197e-147">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="f197e-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="f197e-148">System.object</span><span class="sxs-lookup"><span data-stu-id="f197e-148">System.String</span></span>

### <span data-ttu-id="f197e-149">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f197e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f197e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f197e-150">OUTPUTS</span></span>

### <span data-ttu-id="f197e-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f197e-151">System.Boolean</span></span>

## <span data-ttu-id="f197e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f197e-152">NOTES</span></span>

## <span data-ttu-id="f197e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f197e-153">RELATED LINKS</span></span>
