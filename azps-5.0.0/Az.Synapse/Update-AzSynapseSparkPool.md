---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139899"
---
# <span data-ttu-id="67063-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="67063-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="67063-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67063-102">SYNOPSIS</span></span>
<span data-ttu-id="67063-103">更新 Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="67063-104">句法</span><span class="sxs-lookup"><span data-stu-id="67063-104">SYNTAX</span></span>

### <span data-ttu-id="67063-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="67063-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67063-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67063-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67063-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67063-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67063-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67063-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67063-109">說明</span><span class="sxs-lookup"><span data-stu-id="67063-109">DESCRIPTION</span></span>
<span data-ttu-id="67063-110">**AzSynapseSparkPool** Cmdlet 會更新 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="67063-111">示例</span><span class="sxs-lookup"><span data-stu-id="67063-111">EXAMPLES</span></span>

### <span data-ttu-id="67063-112">範例1</span><span class="sxs-lookup"><span data-stu-id="67063-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="67063-113">這個命令會更新 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="67063-114">範例2</span><span class="sxs-lookup"><span data-stu-id="67063-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="67063-115">這個命令會透過管線更新 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="67063-116">範例3</span><span class="sxs-lookup"><span data-stu-id="67063-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="67063-117">這個命令會透過管線更新 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="67063-118">範例4</span><span class="sxs-lookup"><span data-stu-id="67063-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="67063-119">這個命令會更新含有資源識別碼的 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="67063-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="67063-120">範例5</span><span class="sxs-lookup"><span data-stu-id="67063-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="67063-121">這個命令會針對 Azure Synapse Analytics Spark 池啟用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="67063-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="67063-122">範例6</span><span class="sxs-lookup"><span data-stu-id="67063-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="67063-123">這個命令會針對 Azure Synapse 分析 Spark 池停用自動調整。</span><span class="sxs-lookup"><span data-stu-id="67063-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="67063-124">範例7</span><span class="sxs-lookup"><span data-stu-id="67063-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="67063-125">此命令會針對 Azure Synapse Analytics Spark 池啟用自動暫停功能。</span><span class="sxs-lookup"><span data-stu-id="67063-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="67063-126">範例8</span><span class="sxs-lookup"><span data-stu-id="67063-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="67063-127">此命令會針對 Azure Synapse Analytics Spark 池停用自動暫停。</span><span class="sxs-lookup"><span data-stu-id="67063-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="67063-128">參數</span><span class="sxs-lookup"><span data-stu-id="67063-128">PARAMETERS</span></span>

### <span data-ttu-id="67063-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67063-129">-AsJob</span></span>
<span data-ttu-id="67063-130">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67063-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67063-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="67063-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="67063-132">空閒的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="67063-132">Number of minutes idle.</span></span> <span data-ttu-id="67063-133">啟用自動暫停時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="67063-133">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="67063-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="67063-135">要在指定的 Spark 池中指派的節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="67063-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="67063-136">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="67063-136">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="67063-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="67063-138">要在指定 Spark 池中指派之最小節點數。</span><span class="sxs-lookup"><span data-stu-id="67063-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="67063-139">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="67063-139">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67063-140">-DefaultProfile</span></span>
<span data-ttu-id="67063-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67063-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67063-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="67063-142">-EnableAutoPause</span></span>
<span data-ttu-id="67063-143">指出是否應該啟用自動暫停。</span><span class="sxs-lookup"><span data-stu-id="67063-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="67063-144">-EnableAutoScale</span></span>
<span data-ttu-id="67063-145">指示是否應該啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="67063-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67063-146">-InputObject</span></span>
<span data-ttu-id="67063-147">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="67063-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67063-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="67063-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="67063-149">環境設定檔 ( 「PIP 凍結」輸出) 。</span><span class="sxs-lookup"><span data-stu-id="67063-149">Environment configuration file ("PIP freeze" output).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="67063-150">-Name</span></span>
<span data-ttu-id="67063-151">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="67063-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="67063-152">-NodeCount</span></span>
<span data-ttu-id="67063-153">要在指定的 Spark 池中指派的節點數。</span><span class="sxs-lookup"><span data-stu-id="67063-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="67063-154">-NodeSize</span></span>
<span data-ttu-id="67063-155">要用於指定 Spark 池中所指派之節點的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="67063-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="67063-156">停用自動縮放時，必須指定此參數</span><span class="sxs-lookup"><span data-stu-id="67063-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67063-157">-ResourceGroupName</span></span>
<span data-ttu-id="67063-158">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="67063-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67063-159">-ResourceId</span></span>
<span data-ttu-id="67063-160">Synapse Spark 池的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="67063-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="67063-161">-SparkVersion</span></span>
<span data-ttu-id="67063-162">Apache Spark 版本。</span><span class="sxs-lookup"><span data-stu-id="67063-162">Apache Spark version.</span></span>
<span data-ttu-id="67063-163">允許的值：2。4</span><span class="sxs-lookup"><span data-stu-id="67063-163">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="67063-164">-Tag</span></span>
<span data-ttu-id="67063-165">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="67063-165">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67063-166">-WorkspaceName</span></span>
<span data-ttu-id="67063-167">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="67063-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67063-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="67063-168">-WorkspaceObject</span></span>
<span data-ttu-id="67063-169">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="67063-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67063-170">-確認</span><span class="sxs-lookup"><span data-stu-id="67063-170">-Confirm</span></span>
<span data-ttu-id="67063-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67063-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67063-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67063-172">-WhatIf</span></span>
<span data-ttu-id="67063-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67063-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67063-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67063-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67063-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67063-175">CommonParameters</span></span>
<span data-ttu-id="67063-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67063-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67063-177">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67063-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67063-178">輸入</span><span class="sxs-lookup"><span data-stu-id="67063-178">INPUTS</span></span>

### <span data-ttu-id="67063-179">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="67063-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="67063-180">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="67063-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="67063-181">輸出</span><span class="sxs-lookup"><span data-stu-id="67063-181">OUTPUTS</span></span>

### <span data-ttu-id="67063-182">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="67063-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="67063-183">筆記</span><span class="sxs-lookup"><span data-stu-id="67063-183">NOTES</span></span>

## <span data-ttu-id="67063-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="67063-184">RELATED LINKS</span></span>
