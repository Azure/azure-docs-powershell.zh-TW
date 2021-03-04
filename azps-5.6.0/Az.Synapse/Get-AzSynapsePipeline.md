---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905721"
---
# <span data-ttu-id="6a951-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="6a951-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="6a951-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a951-102">SYNOPSIS</span></span>
<span data-ttu-id="6a951-103">在工作區中獲取管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="6a951-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a951-104">SYNTAX</span></span>

### <span data-ttu-id="6a951-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6a951-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a951-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="6a951-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a951-107">描述</span><span class="sxs-lookup"><span data-stu-id="6a951-107">DESCRIPTION</span></span>
<span data-ttu-id="6a951-108">**Get-AzSynapsePipeline Cmdlet** 會取得工作區中管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="6a951-109">如果您指定管線的名稱，此 Cmdlet 會獲得該管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="6a951-110">如果您未指定名稱，此 Cmdlet 會獲得工作區中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="6a951-111">例子</span><span class="sxs-lookup"><span data-stu-id="6a951-111">EXAMPLES</span></span>

### <span data-ttu-id="6a951-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6a951-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6a951-113">此命令會獲得名為 ContosoWorkspace 工作區中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6a951-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="6a951-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="6a951-115">此命令會從名為 ContosoWorkspace 的工作區中，獲得名為 ContosoPipeline 的管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6a951-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="6a951-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="6a951-117">此命令會透過管道，在名為 ContosoWorkspace 的工作區中，獲得名為 ContosoPipeline 的管線相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6a951-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6a951-118">參數</span><span class="sxs-lookup"><span data-stu-id="6a951-118">PARAMETERS</span></span>

### <span data-ttu-id="6a951-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a951-119">-DefaultProfile</span></span>
<span data-ttu-id="6a951-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a951-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a951-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a951-121">-Name</span></span>
<span data-ttu-id="6a951-122">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="6a951-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a951-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a951-123">-WorkspaceName</span></span>
<span data-ttu-id="6a951-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a951-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a951-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a951-125">-WorkspaceObject</span></span>
<span data-ttu-id="6a951-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="6a951-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a951-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a951-127">CommonParameters</span></span>
<span data-ttu-id="6a951-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a951-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a951-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a951-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a951-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6a951-130">INPUTS</span></span>

### <span data-ttu-id="6a951-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a951-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6a951-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6a951-132">OUTPUTS</span></span>

### <span data-ttu-id="6a951-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="6a951-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="6a951-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6a951-134">NOTES</span></span>

## <span data-ttu-id="6a951-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a951-135">RELATED LINKS</span></span>
