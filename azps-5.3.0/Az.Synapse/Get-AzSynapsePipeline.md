---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288311"
---
# <span data-ttu-id="d1b88-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d1b88-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="d1b88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1b88-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b88-103">取得有關工作區中管道的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="d1b88-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1b88-104">SYNTAX</span></span>

### <span data-ttu-id="d1b88-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d1b88-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1b88-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d1b88-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1b88-107">說明</span><span class="sxs-lookup"><span data-stu-id="d1b88-107">DESCRIPTION</span></span>
<span data-ttu-id="d1b88-108">**AzSynapsePipeline** Cmdlet 會取得工作區中管道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="d1b88-109">如果您指定管線的名稱，此 Cmdlet 會取得該管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="d1b88-110">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有管線的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="d1b88-111">示例</span><span class="sxs-lookup"><span data-stu-id="d1b88-111">EXAMPLES</span></span>

### <span data-ttu-id="d1b88-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d1b88-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d1b88-113">這個命令會取得名為 ContosoWorkspace 的工作區中所有管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d1b88-114">範例2</span><span class="sxs-lookup"><span data-stu-id="d1b88-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="d1b88-115">這個命令會在名為 ContosoWorkspace 的工作區中，取得名為 ContosoPipeline 的管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d1b88-116">範例3</span><span class="sxs-lookup"><span data-stu-id="d1b88-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="d1b88-117">這個命令會在名為 ContosoWorkspace 至管線的工作區中，取得名為 ContosoPipeline 的管線的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b88-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d1b88-118">參數</span><span class="sxs-lookup"><span data-stu-id="d1b88-118">PARAMETERS</span></span>

### <span data-ttu-id="d1b88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b88-119">-DefaultProfile</span></span>
<span data-ttu-id="d1b88-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1b88-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1b88-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1b88-121">-Name</span></span>
<span data-ttu-id="d1b88-122">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b88-122">The pipeline name.</span></span>

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

### <span data-ttu-id="d1b88-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1b88-123">-WorkspaceName</span></span>
<span data-ttu-id="d1b88-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b88-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d1b88-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d1b88-125">-WorkspaceObject</span></span>
<span data-ttu-id="d1b88-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d1b88-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d1b88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b88-127">CommonParameters</span></span>
<span data-ttu-id="d1b88-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1b88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b88-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d1b88-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b88-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d1b88-130">INPUTS</span></span>

### <span data-ttu-id="d1b88-131">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d1b88-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d1b88-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d1b88-132">OUTPUTS</span></span>

### <span data-ttu-id="d1b88-133">PSPipelineResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d1b88-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="d1b88-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d1b88-134">NOTES</span></span>

## <span data-ttu-id="d1b88-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1b88-135">RELATED LINKS</span></span>
