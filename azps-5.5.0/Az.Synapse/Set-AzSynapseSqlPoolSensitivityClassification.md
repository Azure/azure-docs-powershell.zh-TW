---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130351"
---
# <span data-ttu-id="5baea-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="5baea-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="5baea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5baea-102">SYNOPSIS</span></span>
<span data-ttu-id="5baea-103">設定 SQL 池中欄的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5baea-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="5baea-104">句法</span><span class="sxs-lookup"><span data-stu-id="5baea-104">SYNTAX</span></span>

### <span data-ttu-id="5baea-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5baea-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5baea-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5baea-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5baea-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5baea-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5baea-108">說明</span><span class="sxs-lookup"><span data-stu-id="5baea-108">DESCRIPTION</span></span>
<span data-ttu-id="5baea-109">Set-AzSynapseSqlPoolSensitivityClassification Cmdlet 會設定 SQL 池中欄的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5baea-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="5baea-110">示例</span><span class="sxs-lookup"><span data-stu-id="5baea-110">EXAMPLES</span></span>

### <span data-ttu-id="5baea-111">範例1：在 Azure Synapse SQL pool 中設定欄的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5baea-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="5baea-112">範例2：針對 Azure Synapse SQL pool 中的欄設定建議的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5baea-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="5baea-113">範例3：使用管道在 Azure Synapse SQL pool 中設定資料行的資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="5baea-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="5baea-114">參數</span><span class="sxs-lookup"><span data-stu-id="5baea-114">PARAMETERS</span></span>

### <span data-ttu-id="5baea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5baea-115">-AsJob</span></span>
<span data-ttu-id="5baea-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5baea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5baea-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="5baea-117">-ClassificationObject</span></span>
<span data-ttu-id="5baea-118">代表 SQL Pool 敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="5baea-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5baea-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5baea-119">-ColumnName</span></span>
<span data-ttu-id="5baea-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-120">Name of column.</span></span>

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

### <span data-ttu-id="5baea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5baea-121">-DefaultProfile</span></span>
<span data-ttu-id="5baea-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5baea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5baea-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="5baea-123">-InformationType</span></span>
<span data-ttu-id="5baea-124">描述儲存在欄中之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5baea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5baea-125">-PassThru</span></span>
<span data-ttu-id="5baea-126">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="5baea-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5baea-127">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5baea-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5baea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5baea-128">-ResourceGroupName</span></span>
<span data-ttu-id="5baea-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-129">Resource group name.</span></span>

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

### <span data-ttu-id="5baea-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5baea-130">-SchemaName</span></span>
<span data-ttu-id="5baea-131">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-131">Name of schema.</span></span>

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

### <span data-ttu-id="5baea-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="5baea-132">-SensitivityLabel</span></span>
<span data-ttu-id="5baea-133">描述儲存在欄中之資料敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5baea-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="5baea-134">-SqlPoolName</span></span>
<span data-ttu-id="5baea-135">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5baea-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5baea-136">-SqlPoolObject</span></span>
<span data-ttu-id="5baea-137">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5baea-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5baea-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="5baea-138">-TableName</span></span>
<span data-ttu-id="5baea-139">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-139">Name of table.</span></span>

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

### <span data-ttu-id="5baea-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5baea-140">-WorkspaceName</span></span>
<span data-ttu-id="5baea-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5baea-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5baea-142">-確認</span><span class="sxs-lookup"><span data-stu-id="5baea-142">-Confirm</span></span>
<span data-ttu-id="5baea-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5baea-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5baea-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5baea-144">-WhatIf</span></span>
<span data-ttu-id="5baea-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5baea-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5baea-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5baea-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5baea-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5baea-147">CommonParameters</span></span>
<span data-ttu-id="5baea-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5baea-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5baea-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5baea-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5baea-150">輸入</span><span class="sxs-lookup"><span data-stu-id="5baea-150">INPUTS</span></span>

### <span data-ttu-id="5baea-151">System.object</span><span class="sxs-lookup"><span data-stu-id="5baea-151">System.String</span></span>

### <span data-ttu-id="5baea-152">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="5baea-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="5baea-153">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5baea-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5baea-154">輸出</span><span class="sxs-lookup"><span data-stu-id="5baea-154">OUTPUTS</span></span>

### <span data-ttu-id="5baea-155">System.object</span><span class="sxs-lookup"><span data-stu-id="5baea-155">System.Boolean</span></span>

## <span data-ttu-id="5baea-156">筆記</span><span class="sxs-lookup"><span data-stu-id="5baea-156">NOTES</span></span>

## <span data-ttu-id="5baea-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="5baea-157">RELATED LINKS</span></span>
