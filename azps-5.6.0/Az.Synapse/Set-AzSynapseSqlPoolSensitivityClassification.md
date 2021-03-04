---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 2eec7ea6f89bea726cdbee483162ec455e5722aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912225"
---
# <span data-ttu-id="89f87-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="89f87-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="89f87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89f87-102">SYNOPSIS</span></span>
<span data-ttu-id="89f87-103">在 SQL 資料庫中設定欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="89f87-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="89f87-104">語法</span><span class="sxs-lookup"><span data-stu-id="89f87-104">SYNTAX</span></span>

### <span data-ttu-id="89f87-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89f87-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f87-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f87-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f87-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="89f87-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f87-108">描述</span><span class="sxs-lookup"><span data-stu-id="89f87-108">DESCRIPTION</span></span>
<span data-ttu-id="89f87-109">Cmdlet Set-AzSynapseSqlPoolSensitivityClassification設定 SQL 資料庫中欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="89f87-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="89f87-110">例子</span><span class="sxs-lookup"><span data-stu-id="89f87-110">EXAMPLES</span></span>

### <span data-ttu-id="89f87-111">範例 1：在 Azure Synapse SQL 集區中設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="89f87-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="89f87-112">範例 2：在 Azure Synapse SQL 資料庫中設定欄的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="89f87-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="89f87-113">範例 3：在 Azure Synapse SQL 集區中，使用管線設定資料行的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="89f87-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="89f87-114">參數</span><span class="sxs-lookup"><span data-stu-id="89f87-114">PARAMETERS</span></span>

### <span data-ttu-id="89f87-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89f87-115">-AsJob</span></span>
<span data-ttu-id="89f87-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="89f87-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89f87-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="89f87-117">-ClassificationObject</span></span>
<span data-ttu-id="89f87-118">代表 SQL 資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="89f87-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="89f87-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="89f87-119">-ColumnName</span></span>
<span data-ttu-id="89f87-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-120">Name of column.</span></span>

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

### <span data-ttu-id="89f87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f87-121">-DefaultProfile</span></span>
<span data-ttu-id="89f87-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89f87-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f87-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="89f87-123">-InformationType</span></span>
<span data-ttu-id="89f87-124">描述資料行中儲存之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-124">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="89f87-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89f87-125">-PassThru</span></span>
<span data-ttu-id="89f87-126">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="89f87-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="89f87-127">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="89f87-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="89f87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f87-128">-ResourceGroupName</span></span>
<span data-ttu-id="89f87-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="89f87-129">Resource group name.</span></span>

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

### <span data-ttu-id="89f87-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="89f87-130">-SchemaName</span></span>
<span data-ttu-id="89f87-131">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-131">Name of schema.</span></span>

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

### <span data-ttu-id="89f87-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="89f87-132">-SensitivityLabel</span></span>
<span data-ttu-id="89f87-133">描述資料行中儲存之資料的敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-133">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="89f87-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="89f87-134">-SqlPoolName</span></span>
<span data-ttu-id="89f87-135">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="89f87-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="89f87-136">-SqlPoolObject</span></span>
<span data-ttu-id="89f87-137">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="89f87-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89f87-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="89f87-138">-TableName</span></span>
<span data-ttu-id="89f87-139">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-139">Name of table.</span></span>

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

### <span data-ttu-id="89f87-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89f87-140">-WorkspaceName</span></span>
<span data-ttu-id="89f87-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f87-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89f87-142">-確認</span><span class="sxs-lookup"><span data-stu-id="89f87-142">-Confirm</span></span>
<span data-ttu-id="89f87-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="89f87-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f87-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f87-144">-WhatIf</span></span>
<span data-ttu-id="89f87-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89f87-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f87-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89f87-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f87-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f87-147">CommonParameters</span></span>
<span data-ttu-id="89f87-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89f87-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f87-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89f87-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f87-150">輸入</span><span class="sxs-lookup"><span data-stu-id="89f87-150">INPUTS</span></span>

### <span data-ttu-id="89f87-151">System.String</span><span class="sxs-lookup"><span data-stu-id="89f87-151">System.String</span></span>

### <span data-ttu-id="89f87-152">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="89f87-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="89f87-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="89f87-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="89f87-154">輸出</span><span class="sxs-lookup"><span data-stu-id="89f87-154">OUTPUTS</span></span>

### <span data-ttu-id="89f87-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89f87-155">System.Boolean</span></span>

## <span data-ttu-id="89f87-156">筆記</span><span class="sxs-lookup"><span data-stu-id="89f87-156">NOTES</span></span>

## <span data-ttu-id="89f87-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="89f87-157">RELATED LINKS</span></span>
