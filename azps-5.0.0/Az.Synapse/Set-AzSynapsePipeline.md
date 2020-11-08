---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139351"
---
# <span data-ttu-id="98e96-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="98e96-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="98e96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98e96-102">SYNOPSIS</span></span>
<span data-ttu-id="98e96-103">在工作區中建立管線。</span><span class="sxs-lookup"><span data-stu-id="98e96-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="98e96-104">句法</span><span class="sxs-lookup"><span data-stu-id="98e96-104">SYNTAX</span></span>

### <span data-ttu-id="98e96-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="98e96-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e96-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="98e96-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e96-107">說明</span><span class="sxs-lookup"><span data-stu-id="98e96-107">DESCRIPTION</span></span>
<span data-ttu-id="98e96-108">**AzSynapsePipeline** Cmdlet 會在工作區中建立管線。</span><span class="sxs-lookup"><span data-stu-id="98e96-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="98e96-109">示例</span><span class="sxs-lookup"><span data-stu-id="98e96-109">EXAMPLES</span></span>

### <span data-ttu-id="98e96-110">範例1</span><span class="sxs-lookup"><span data-stu-id="98e96-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="98e96-111">這個命令會在名為 ContosoWorkspace 的工作區中，建立一個名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="98e96-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="98e96-112">該命令根據檔案中 pipeline.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="98e96-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="98e96-113">此檔案包含活動的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98e96-113">This file includes information about activities.</span></span>

### <span data-ttu-id="98e96-114">範例2</span><span class="sxs-lookup"><span data-stu-id="98e96-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="98e96-115">這個命令會在名為 ContosoWorkspace 至管線的工作區中，建立一個名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="98e96-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="98e96-116">該命令根據檔案中 pipeline.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="98e96-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="98e96-117">此檔案包含活動的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98e96-117">This file includes information about activities.</span></span>

## <span data-ttu-id="98e96-118">參數</span><span class="sxs-lookup"><span data-stu-id="98e96-118">PARAMETERS</span></span>

### <span data-ttu-id="98e96-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98e96-119">-AsJob</span></span>
<span data-ttu-id="98e96-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="98e96-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98e96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e96-121">-DefaultProfile</span></span>
<span data-ttu-id="98e96-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98e96-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e96-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="98e96-123">-DefinitionFile</span></span>
<span data-ttu-id="98e96-124">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="98e96-124">The JSON file path.</span></span>

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

### <span data-ttu-id="98e96-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="98e96-125">-Name</span></span>
<span data-ttu-id="98e96-126">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="98e96-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e96-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98e96-127">-WorkspaceName</span></span>
<span data-ttu-id="98e96-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="98e96-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e96-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98e96-129">-WorkspaceObject</span></span>
<span data-ttu-id="98e96-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="98e96-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98e96-131">-確認</span><span class="sxs-lookup"><span data-stu-id="98e96-131">-Confirm</span></span>
<span data-ttu-id="98e96-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98e96-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e96-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e96-133">-WhatIf</span></span>
<span data-ttu-id="98e96-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98e96-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e96-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98e96-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e96-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e96-136">CommonParameters</span></span>
<span data-ttu-id="98e96-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98e96-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e96-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98e96-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e96-139">輸入</span><span class="sxs-lookup"><span data-stu-id="98e96-139">INPUTS</span></span>

### <span data-ttu-id="98e96-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="98e96-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98e96-141">輸出</span><span class="sxs-lookup"><span data-stu-id="98e96-141">OUTPUTS</span></span>

### <span data-ttu-id="98e96-142">PSPipelineResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="98e96-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="98e96-143">筆記</span><span class="sxs-lookup"><span data-stu-id="98e96-143">NOTES</span></span>

## <span data-ttu-id="98e96-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="98e96-144">RELATED LINKS</span></span>