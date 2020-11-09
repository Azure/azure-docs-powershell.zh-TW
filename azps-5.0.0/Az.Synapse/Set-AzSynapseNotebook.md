---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287619"
---
# <span data-ttu-id="8c041-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="8c041-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="8c041-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c041-102">SYNOPSIS</span></span>
<span data-ttu-id="8c041-103">在工作區中建立或更新筆記本。</span><span class="sxs-lookup"><span data-stu-id="8c041-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="8c041-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c041-104">SYNTAX</span></span>

### <span data-ttu-id="8c041-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8c041-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c041-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="8c041-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c041-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="8c041-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c041-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="8c041-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c041-109">說明</span><span class="sxs-lookup"><span data-stu-id="8c041-109">DESCRIPTION</span></span>
<span data-ttu-id="8c041-110">**AzSynapseNotebook** Cmdlet 會建立或更新工作區中的筆記本。</span><span class="sxs-lookup"><span data-stu-id="8c041-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="8c041-111">示例</span><span class="sxs-lookup"><span data-stu-id="8c041-111">EXAMPLES</span></span>

### <span data-ttu-id="8c041-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8c041-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="8c041-113">這個命令會在名為 ContosoWorkspace 的工作區中，從筆記本檔案筆記本 ipynb 建立或更新筆記本。</span><span class="sxs-lookup"><span data-stu-id="8c041-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8c041-114">範例2</span><span class="sxs-lookup"><span data-stu-id="8c041-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="8c041-115">這個命令會建立或更新筆記本檔案筆記本中的筆記本，ipynb 在名為 ContosoWorkspace 至管線的工作區中。</span><span class="sxs-lookup"><span data-stu-id="8c041-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="8c041-116">範例3</span><span class="sxs-lookup"><span data-stu-id="8c041-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="8c041-117">這個命令會從筆記本檔案筆記本中建立或更新筆記本。 ipynb 會附加到 ContosoSparkPool，並在名為 ContosoWorkspace 的工作區中使用2個執行程式。</span><span class="sxs-lookup"><span data-stu-id="8c041-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8c041-118">參數</span><span class="sxs-lookup"><span data-stu-id="8c041-118">PARAMETERS</span></span>

### <span data-ttu-id="8c041-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c041-119">-AsJob</span></span>
<span data-ttu-id="8c041-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c041-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c041-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c041-121">-DefaultProfile</span></span>
<span data-ttu-id="8c041-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c041-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c041-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8c041-123">-DefinitionFile</span></span>
<span data-ttu-id="8c041-124">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="8c041-124">The JSON file path.</span></span>

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

### <span data-ttu-id="8c041-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="8c041-125">-ExecutorCount</span></span>
<span data-ttu-id="8c041-126">要在指定的 Spark 池中為作業指派的執行次數。</span><span class="sxs-lookup"><span data-stu-id="8c041-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="8c041-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="8c041-127">-ExecutorSize</span></span>
<span data-ttu-id="8c041-128">在作業的指定 Spark 池中，要用於執行程式的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="8c041-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="8c041-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c041-129">-Name</span></span>
<span data-ttu-id="8c041-130">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="8c041-130">The notebook name.</span></span>

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

### <span data-ttu-id="8c041-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8c041-131">-SparkPoolName</span></span>
<span data-ttu-id="8c041-132">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c041-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8c041-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8c041-133">-WorkspaceName</span></span>
<span data-ttu-id="8c041-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c041-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8c041-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8c041-135">-WorkspaceObject</span></span>
<span data-ttu-id="8c041-136">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="8c041-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8c041-137">-確認</span><span class="sxs-lookup"><span data-stu-id="8c041-137">-Confirm</span></span>
<span data-ttu-id="8c041-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c041-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c041-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c041-139">-WhatIf</span></span>
<span data-ttu-id="8c041-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c041-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c041-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c041-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c041-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c041-142">CommonParameters</span></span>
<span data-ttu-id="8c041-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c041-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c041-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c041-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c041-145">輸入</span><span class="sxs-lookup"><span data-stu-id="8c041-145">INPUTS</span></span>

### <span data-ttu-id="8c041-146">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8c041-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8c041-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8c041-147">OUTPUTS</span></span>

### <span data-ttu-id="8c041-148">PSNotebookResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8c041-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="8c041-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8c041-149">NOTES</span></span>

## <span data-ttu-id="8c041-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c041-150">RELATED LINKS</span></span>
