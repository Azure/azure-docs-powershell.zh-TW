---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435795"
---
# <span data-ttu-id="57f1e-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="57f1e-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="57f1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="57f1e-103">取得有關管道執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="57f1e-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="57f1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="57f1e-104">SYNTAX</span></span>

### <span data-ttu-id="57f1e-105">GetByNameAndId (預設) </span><span class="sxs-lookup"><span data-stu-id="57f1e-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57f1e-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="57f1e-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57f1e-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="57f1e-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57f1e-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="57f1e-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57f1e-109">說明</span><span class="sxs-lookup"><span data-stu-id="57f1e-109">DESCRIPTION</span></span>
<span data-ttu-id="57f1e-110">[ **取得 AzSynapsePipelineRun** ] 命令會傳回指定管線執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57f1e-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="57f1e-111">如果已指定 PipelineRunId，則會顯示該 ID 執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57f1e-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="57f1e-112">如果未指定 PipelineRunId，則會顯示在 RunStartedAfter 和 RunStartedBefore 值之間所發生之管線的所有執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57f1e-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="57f1e-113">示例</span><span class="sxs-lookup"><span data-stu-id="57f1e-113">EXAMPLES</span></span>

### <span data-ttu-id="57f1e-114">範例1</span><span class="sxs-lookup"><span data-stu-id="57f1e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="57f1e-115">這個命令會取得 ID 為 "61eb095a-fe23-4591-8a97-fade6c65ca72" 的管線執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57f1e-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="57f1e-116">參數</span><span class="sxs-lookup"><span data-stu-id="57f1e-116">PARAMETERS</span></span>

### <span data-ttu-id="57f1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f1e-117">-DefaultProfile</span></span>
<span data-ttu-id="57f1e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57f1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f1e-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="57f1e-119">-PipelineName</span></span>
<span data-ttu-id="57f1e-120">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="57f1e-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="57f1e-121">-PipelineRunId</span></span>
<span data-ttu-id="57f1e-122">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="57f1e-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="57f1e-123">-RunStartedAfter</span></span>
<span data-ttu-id="57f1e-124">以 "ISO 8601" 格式更新 run 事件的時間或之後。</span><span class="sxs-lookup"><span data-stu-id="57f1e-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="57f1e-125">-RunStartedBefore</span></span>
<span data-ttu-id="57f1e-126">以 "ISO 8601" 格式更新 run 事件之前或之前的時間。</span><span class="sxs-lookup"><span data-stu-id="57f1e-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57f1e-127">-WorkspaceName</span></span>
<span data-ttu-id="57f1e-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="57f1e-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="57f1e-129">-WorkspaceObject</span></span>
<span data-ttu-id="57f1e-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="57f1e-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57f1e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f1e-131">CommonParameters</span></span>
<span data-ttu-id="57f1e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57f1e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f1e-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57f1e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f1e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="57f1e-134">INPUTS</span></span>

### <span data-ttu-id="57f1e-135">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="57f1e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="57f1e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="57f1e-136">OUTPUTS</span></span>

### <span data-ttu-id="57f1e-137">PSPipelineRun 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="57f1e-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="57f1e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="57f1e-138">NOTES</span></span>

## <span data-ttu-id="57f1e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="57f1e-139">RELATED LINKS</span></span>
