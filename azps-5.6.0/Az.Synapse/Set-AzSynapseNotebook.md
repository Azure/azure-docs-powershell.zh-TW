---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: 9b960c3b671ecada8f4f24e1b5a8897de7004440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916314"
---
# <span data-ttu-id="b44a2-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="b44a2-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="b44a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b44a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b44a2-103">在工作區中建立或更新筆記本。</span><span class="sxs-lookup"><span data-stu-id="b44a2-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="b44a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b44a2-104">SYNTAX</span></span>

### <span data-ttu-id="b44a2-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b44a2-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44a2-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="b44a2-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44a2-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="b44a2-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44a2-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="b44a2-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b44a2-109">描述</span><span class="sxs-lookup"><span data-stu-id="b44a2-109">DESCRIPTION</span></span>
<span data-ttu-id="b44a2-110">**Set-AzSynapseNotebook** Cmdlet 會建立或更新工作區中的筆記本。</span><span class="sxs-lookup"><span data-stu-id="b44a2-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="b44a2-111">例子</span><span class="sxs-lookup"><span data-stu-id="b44a2-111">EXAMPLES</span></span>

### <span data-ttu-id="b44a2-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b44a2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="b44a2-113">此命令會從名為 ContosoWorkspace 的工作區中的筆記本檔案筆記本.ipynb 建立或更新筆記本。</span><span class="sxs-lookup"><span data-stu-id="b44a2-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b44a2-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="b44a2-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="b44a2-115">此命令會透過管道從名為 ContosoWorkspace 的工作區中的筆記本檔案 notebook.ipynb 建立或更新筆記本。</span><span class="sxs-lookup"><span data-stu-id="b44a2-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b44a2-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="b44a2-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="b44a2-117">此命令會從筆記本檔案筆記本.ipynb 建立或更新筆記本，該筆記本會附加到 ContosoSparkPool，並使用名為 ContosoWorkspace 的工作區中的 2 個執行器。</span><span class="sxs-lookup"><span data-stu-id="b44a2-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b44a2-118">參數</span><span class="sxs-lookup"><span data-stu-id="b44a2-118">PARAMETERS</span></span>

### <span data-ttu-id="b44a2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b44a2-119">-AsJob</span></span>
<span data-ttu-id="b44a2-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b44a2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b44a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44a2-121">-DefaultProfile</span></span>
<span data-ttu-id="b44a2-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b44a2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b44a2-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b44a2-123">-DefinitionFile</span></span>
<span data-ttu-id="b44a2-124">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b44a2-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-125">-執行器計數</span><span class="sxs-lookup"><span data-stu-id="b44a2-125">-ExecutorCount</span></span>
<span data-ttu-id="b44a2-126">要配置於指定工作之 Spark 區中的執行者數目。</span><span class="sxs-lookup"><span data-stu-id="b44a2-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-127">-執行器Size</span><span class="sxs-lookup"><span data-stu-id="b44a2-127">-ExecutorSize</span></span>
<span data-ttu-id="b44a2-128">要用於指定工作之 Spark 資料集中之執行者的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="b44a2-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b44a2-129">-Name</span></span>
<span data-ttu-id="b44a2-130">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="b44a2-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b44a2-131">-SparkPoolName</span></span>
<span data-ttu-id="b44a2-132">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b44a2-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b44a2-133">-WorkspaceName</span></span>
<span data-ttu-id="b44a2-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b44a2-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b44a2-135">-WorkspaceObject</span></span>
<span data-ttu-id="b44a2-136">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b44a2-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b44a2-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b44a2-137">-Confirm</span></span>
<span data-ttu-id="b44a2-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b44a2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b44a2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b44a2-139">-WhatIf</span></span>
<span data-ttu-id="b44a2-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b44a2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b44a2-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b44a2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b44a2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44a2-142">CommonParameters</span></span>
<span data-ttu-id="b44a2-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b44a2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44a2-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b44a2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44a2-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b44a2-145">INPUTS</span></span>

### <span data-ttu-id="b44a2-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b44a2-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b44a2-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b44a2-147">OUTPUTS</span></span>

### <span data-ttu-id="b44a2-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="b44a2-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="b44a2-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b44a2-149">NOTES</span></span>

## <span data-ttu-id="b44a2-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b44a2-150">RELATED LINKS</span></span>
