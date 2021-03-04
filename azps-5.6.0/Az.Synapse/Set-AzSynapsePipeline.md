---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: cd79d9315c6352b604a40269286073792596a41e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912234"
---
# <span data-ttu-id="f1a33-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="f1a33-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="f1a33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1a33-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a33-103">在工作區中建立管線。</span><span class="sxs-lookup"><span data-stu-id="f1a33-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="f1a33-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1a33-104">SYNTAX</span></span>

### <span data-ttu-id="f1a33-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1a33-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a33-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="f1a33-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a33-107">描述</span><span class="sxs-lookup"><span data-stu-id="f1a33-107">DESCRIPTION</span></span>
<span data-ttu-id="f1a33-108">**Set-AzSynapsePipeline** Cmdlet 會建立工作區中的管線。</span><span class="sxs-lookup"><span data-stu-id="f1a33-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="f1a33-109">例子</span><span class="sxs-lookup"><span data-stu-id="f1a33-109">EXAMPLES</span></span>

### <span data-ttu-id="f1a33-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f1a33-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="f1a33-111">此命令在名為 ContosoWorkspace 的工作區中建立名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="f1a33-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="f1a33-112">命令會依據檔案中pipeline.js的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1a33-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="f1a33-113">此檔案包含活動相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1a33-113">This file includes information about activities.</span></span>

### <span data-ttu-id="f1a33-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="f1a33-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="f1a33-115">此命令在名為 ContosoWorkspace 的工作區中，透過管線建立名為 ContosoPipeline 的管線。</span><span class="sxs-lookup"><span data-stu-id="f1a33-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="f1a33-116">命令會依據檔案中pipeline.js的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1a33-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="f1a33-117">此檔案包含活動相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1a33-117">This file includes information about activities.</span></span>

## <span data-ttu-id="f1a33-118">參數</span><span class="sxs-lookup"><span data-stu-id="f1a33-118">PARAMETERS</span></span>

### <span data-ttu-id="f1a33-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a33-119">-AsJob</span></span>
<span data-ttu-id="f1a33-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1a33-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1a33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a33-121">-DefaultProfile</span></span>
<span data-ttu-id="f1a33-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1a33-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a33-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f1a33-123">-DefinitionFile</span></span>
<span data-ttu-id="f1a33-124">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f1a33-124">The JSON file path.</span></span>

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

### <span data-ttu-id="f1a33-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1a33-125">-Name</span></span>
<span data-ttu-id="f1a33-126">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a33-126">The pipeline name.</span></span>

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

### <span data-ttu-id="f1a33-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1a33-127">-WorkspaceName</span></span>
<span data-ttu-id="f1a33-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a33-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1a33-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1a33-129">-WorkspaceObject</span></span>
<span data-ttu-id="f1a33-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="f1a33-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1a33-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f1a33-131">-Confirm</span></span>
<span data-ttu-id="f1a33-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1a33-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a33-133">-WhatIf</span></span>
<span data-ttu-id="f1a33-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1a33-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a33-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1a33-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a33-136">CommonParameters</span></span>
<span data-ttu-id="f1a33-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1a33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a33-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a33-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a33-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f1a33-139">INPUTS</span></span>

### <span data-ttu-id="f1a33-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1a33-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f1a33-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f1a33-141">OUTPUTS</span></span>

### <span data-ttu-id="f1a33-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="f1a33-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="f1a33-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f1a33-143">NOTES</span></span>

## <span data-ttu-id="f1a33-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1a33-144">RELATED LINKS</span></span>
