---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c41c6afdda39843afa985a53eb572b64f8bcfe19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907938"
---
# <span data-ttu-id="8984e-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8984e-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="8984e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8984e-102">SYNOPSIS</span></span>
<span data-ttu-id="8984e-103">建立 Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8984e-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="8984e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8984e-104">SYNTAX</span></span>

### <span data-ttu-id="8984e-105">CreateByNameAndEnableAutoScaleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8984e-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984e-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984e-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984e-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984e-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984e-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984e-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8984e-109">描述</span><span class="sxs-lookup"><span data-stu-id="8984e-109">DESCRIPTION</span></span>
<span data-ttu-id="8984e-110">**New-AzSynapseSparkPool** Cmdlet 會建立 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8984e-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="8984e-111">例子</span><span class="sxs-lookup"><span data-stu-id="8984e-111">EXAMPLES</span></span>

### <span data-ttu-id="8984e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8984e-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="8984e-113">此命令會建立 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8984e-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="8984e-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="8984e-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="8984e-115">此命令會建立 Azure Synapse Analytics Spark 資料庫，並啟用自動縮放功能。</span><span class="sxs-lookup"><span data-stu-id="8984e-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="8984e-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="8984e-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="8984e-117">此命令會透過管線建立 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8984e-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="8984e-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="8984e-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="8984e-119">此命令會建立 Azure Synapse Analytics Spark 資料庫，透過管道啟用自動縮放功能。</span><span class="sxs-lookup"><span data-stu-id="8984e-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="8984e-120">參數</span><span class="sxs-lookup"><span data-stu-id="8984e-120">PARAMETERS</span></span>

### <span data-ttu-id="8984e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8984e-121">-AsJob</span></span>
<span data-ttu-id="8984e-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8984e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8984e-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="8984e-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="8984e-124">閒置的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="8984e-124">Number of minutes idle.</span></span> <span data-ttu-id="8984e-125">啟用自動暫停時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8984e-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="8984e-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="8984e-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="8984e-127">要于指定的 Spark 計算區中配置節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="8984e-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="8984e-128">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8984e-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="8984e-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="8984e-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="8984e-130">要于指定的 Spark 計算區中配置的最小節點數目。</span><span class="sxs-lookup"><span data-stu-id="8984e-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="8984e-131">啟用自動縮放時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8984e-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="8984e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8984e-132">-DefaultProfile</span></span>
<span data-ttu-id="8984e-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8984e-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8984e-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="8984e-134">-EnableAutoPause</span></span>
<span data-ttu-id="8984e-135">指出是否應該啟用自動暫停。</span><span class="sxs-lookup"><span data-stu-id="8984e-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="8984e-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="8984e-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="8984e-137">環境組 (為「執行長管凍結」輸出) 。</span><span class="sxs-lookup"><span data-stu-id="8984e-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="8984e-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="8984e-138">-Name</span></span>
<span data-ttu-id="8984e-139">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8984e-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8984e-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="8984e-140">-NodeCount</span></span>
<span data-ttu-id="8984e-141">要配置於指定 Spark 計算區中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="8984e-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="8984e-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="8984e-142">-NodeSize</span></span>
<span data-ttu-id="8984e-143">要用於指定 Spark 計算區中配置之節點的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="8984e-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="8984e-144">您必須在停用自動縮放時指定此參數</span><span class="sxs-lookup"><span data-stu-id="8984e-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="8984e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8984e-145">-ResourceGroupName</span></span>
<span data-ttu-id="8984e-146">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8984e-146">Resource group name.</span></span>

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

### <span data-ttu-id="8984e-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="8984e-147">-SparkVersion</span></span>
<span data-ttu-id="8984e-148">Apache Spark 版本。</span><span class="sxs-lookup"><span data-stu-id="8984e-148">Apache Spark version.</span></span>
<span data-ttu-id="8984e-149">允許的值：2.4</span><span class="sxs-lookup"><span data-stu-id="8984e-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="8984e-150">-標記</span><span class="sxs-lookup"><span data-stu-id="8984e-150">-Tag</span></span>
<span data-ttu-id="8984e-151">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="8984e-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="8984e-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8984e-152">-WorkspaceName</span></span>
<span data-ttu-id="8984e-153">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8984e-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8984e-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8984e-154">-WorkspaceObject</span></span>
<span data-ttu-id="8984e-155">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="8984e-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8984e-156">-確認</span><span class="sxs-lookup"><span data-stu-id="8984e-156">-Confirm</span></span>
<span data-ttu-id="8984e-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8984e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8984e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8984e-158">-WhatIf</span></span>
<span data-ttu-id="8984e-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8984e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8984e-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8984e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8984e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8984e-161">CommonParameters</span></span>
<span data-ttu-id="8984e-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8984e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8984e-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8984e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8984e-164">輸入</span><span class="sxs-lookup"><span data-stu-id="8984e-164">INPUTS</span></span>

### <span data-ttu-id="8984e-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8984e-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8984e-166">輸出</span><span class="sxs-lookup"><span data-stu-id="8984e-166">OUTPUTS</span></span>

### <span data-ttu-id="8984e-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8984e-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8984e-168">筆記</span><span class="sxs-lookup"><span data-stu-id="8984e-168">NOTES</span></span>

## <span data-ttu-id="8984e-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="8984e-169">RELATED LINKS</span></span>
