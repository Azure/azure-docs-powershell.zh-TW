---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283872"
---
# <span data-ttu-id="38ddb-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="38ddb-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="38ddb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="38ddb-103">建立 Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="38ddb-104">句法</span><span class="sxs-lookup"><span data-stu-id="38ddb-104">SYNTAX</span></span>

### <span data-ttu-id="38ddb-105">CreateByNameAndEnableAutoScaleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="38ddb-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ddb-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="38ddb-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ddb-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="38ddb-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ddb-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="38ddb-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ddb-109">說明</span><span class="sxs-lookup"><span data-stu-id="38ddb-109">DESCRIPTION</span></span>
<span data-ttu-id="38ddb-110">**新的-AzSynapseSparkPool** Cmdlet 會建立 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="38ddb-111">示例</span><span class="sxs-lookup"><span data-stu-id="38ddb-111">EXAMPLES</span></span>

### <span data-ttu-id="38ddb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="38ddb-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="38ddb-113">這個命令會建立 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="38ddb-114">範例2</span><span class="sxs-lookup"><span data-stu-id="38ddb-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="38ddb-115">這個命令會建立已啟用自動調整的 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="38ddb-116">範例3</span><span class="sxs-lookup"><span data-stu-id="38ddb-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="38ddb-117">這個命令會透過管線建立 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="38ddb-118">範例4</span><span class="sxs-lookup"><span data-stu-id="38ddb-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="38ddb-119">這個命令會建立可透過流水線啟用自動縮放的 Azure Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="38ddb-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="38ddb-120">參數</span><span class="sxs-lookup"><span data-stu-id="38ddb-120">PARAMETERS</span></span>

### <span data-ttu-id="38ddb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38ddb-121">-AsJob</span></span>
<span data-ttu-id="38ddb-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38ddb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38ddb-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="38ddb-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="38ddb-124">空閒的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-124">Number of minutes idle.</span></span> <span data-ttu-id="38ddb-125">啟用自動暫停時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="38ddb-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="38ddb-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="38ddb-127">要在指定的 Spark 池中指派的節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="38ddb-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="38ddb-128">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="38ddb-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="38ddb-130">要在指定 Spark 池中指派之最小節點數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="38ddb-131">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ddb-132">-DefaultProfile</span></span>
<span data-ttu-id="38ddb-133">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38ddb-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ddb-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="38ddb-134">-EnableAutoPause</span></span>
<span data-ttu-id="38ddb-135">指出是否應該啟用自動暫停。</span><span class="sxs-lookup"><span data-stu-id="38ddb-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="38ddb-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="38ddb-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="38ddb-137">環境設定檔 ( 「PIP 凍結」輸出) 。</span><span class="sxs-lookup"><span data-stu-id="38ddb-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="38ddb-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="38ddb-138">-Name</span></span>
<span data-ttu-id="38ddb-139">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="38ddb-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="38ddb-140">-NodeCount</span></span>
<span data-ttu-id="38ddb-141">要在指定的 Spark 池中指派的節點數。</span><span class="sxs-lookup"><span data-stu-id="38ddb-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="38ddb-142">-NodeSize</span></span>
<span data-ttu-id="38ddb-143">要用於指定 Spark 池中所指派之節點的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="38ddb-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="38ddb-144">停用自動縮放時，必須指定此參數</span><span class="sxs-lookup"><span data-stu-id="38ddb-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ddb-145">-ResourceGroupName</span></span>
<span data-ttu-id="38ddb-146">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="38ddb-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="38ddb-147">-SparkVersion</span></span>
<span data-ttu-id="38ddb-148">Apache Spark 版本。</span><span class="sxs-lookup"><span data-stu-id="38ddb-148">Apache Spark version.</span></span>
<span data-ttu-id="38ddb-149">允許的值：2。4</span><span class="sxs-lookup"><span data-stu-id="38ddb-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="38ddb-150">-Tag</span></span>
<span data-ttu-id="38ddb-151">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="38ddb-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="38ddb-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38ddb-152">-WorkspaceName</span></span>
<span data-ttu-id="38ddb-153">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="38ddb-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38ddb-154">-WorkspaceObject</span></span>
<span data-ttu-id="38ddb-155">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="38ddb-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ddb-156">-確認</span><span class="sxs-lookup"><span data-stu-id="38ddb-156">-Confirm</span></span>
<span data-ttu-id="38ddb-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38ddb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ddb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ddb-158">-WhatIf</span></span>
<span data-ttu-id="38ddb-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38ddb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ddb-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38ddb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ddb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ddb-161">CommonParameters</span></span>
<span data-ttu-id="38ddb-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38ddb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ddb-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38ddb-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ddb-164">輸入</span><span class="sxs-lookup"><span data-stu-id="38ddb-164">INPUTS</span></span>

### <span data-ttu-id="38ddb-165">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="38ddb-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="38ddb-166">輸出</span><span class="sxs-lookup"><span data-stu-id="38ddb-166">OUTPUTS</span></span>

### <span data-ttu-id="38ddb-167">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="38ddb-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="38ddb-168">筆記</span><span class="sxs-lookup"><span data-stu-id="38ddb-168">NOTES</span></span>

## <span data-ttu-id="38ddb-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="38ddb-169">RELATED LINKS</span></span>
