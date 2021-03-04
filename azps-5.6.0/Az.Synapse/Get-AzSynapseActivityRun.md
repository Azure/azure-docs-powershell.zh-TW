---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: c32b0714a64e0fa97b5376861360bc3645995418
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909386"
---
# <span data-ttu-id="bb94d-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="bb94d-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="bb94d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb94d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb94d-103">在管線執行中，獲得執行活動的資訊。</span><span class="sxs-lookup"><span data-stu-id="bb94d-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="bb94d-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb94d-104">SYNTAX</span></span>

### <span data-ttu-id="bb94d-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="bb94d-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb94d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="bb94d-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb94d-107">描述</span><span class="sxs-lookup"><span data-stu-id="bb94d-107">DESCRIPTION</span></span>
<span data-ttu-id="bb94d-108">**Get-AzSynapseActivityRun** Cmdlet 會取得指定時間範圍內發生之指定管線執行之工作區中執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="bb94d-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="bb94d-109">此外，您可以為活動名稱及執行狀態指定篩選。</span><span class="sxs-lookup"><span data-stu-id="bb94d-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="bb94d-110">例子</span><span class="sxs-lookup"><span data-stu-id="bb94d-110">EXAMPLES</span></span>

### <span data-ttu-id="bb94d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bb94d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="bb94d-112">此命令會獲得在管道中執行的所有活動詳細資料，該管道名為 ContosoPipeline，其 ID 為 "f288712d-fb08-4cb8-96ef-82d3b9b3 發生于「2018-09-01T21：00」和「2018-09-30T21：00」之間的0621」。</span><span class="sxs-lookup"><span data-stu-id="bb94d-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="bb94d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bb94d-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="bb94d-114">此命令會獲得在管道中執行的所有活動詳細資料，該管道名為 ContosoPipeline，其 ID 為 "f288712d-fb08-4cb8-96ef-82d3b9b30 「2018-09-01T21：00」與「2018-09-30T21：00」之間透過管線發生的621」。</span><span class="sxs-lookup"><span data-stu-id="bb94d-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="bb94d-115">參數</span><span class="sxs-lookup"><span data-stu-id="bb94d-115">PARAMETERS</span></span>

### <span data-ttu-id="bb94d-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="bb94d-116">-ActivityName</span></span>
<span data-ttu-id="bb94d-117">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb94d-117">The name of the activity.</span></span>

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

### <span data-ttu-id="bb94d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb94d-118">-DefaultProfile</span></span>
<span data-ttu-id="bb94d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb94d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb94d-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="bb94d-120">-PipelineName</span></span>
<span data-ttu-id="bb94d-121">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="bb94d-121">The pipeline name.</span></span>

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

### <span data-ttu-id="bb94d-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="bb94d-122">-PipelineRunId</span></span>
<span data-ttu-id="bb94d-123">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb94d-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="bb94d-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="bb94d-124">-RunStartedAfter</span></span>
<span data-ttu-id="bb94d-125">執行事件更新為 'ISO 8601' 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="bb94d-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb94d-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="bb94d-126">-RunStartedBefore</span></span>
<span data-ttu-id="bb94d-127">以 'ISO 8601' 格式更新執行事件的時間。</span><span class="sxs-lookup"><span data-stu-id="bb94d-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb94d-128">-狀態</span><span class="sxs-lookup"><span data-stu-id="bb94d-128">-Status</span></span>
<span data-ttu-id="bb94d-129">管線執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="bb94d-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="bb94d-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bb94d-130">-WorkspaceName</span></span>
<span data-ttu-id="bb94d-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb94d-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bb94d-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bb94d-132">-WorkspaceObject</span></span>
<span data-ttu-id="bb94d-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="bb94d-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bb94d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb94d-134">CommonParameters</span></span>
<span data-ttu-id="bb94d-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb94d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb94d-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb94d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb94d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bb94d-137">INPUTS</span></span>

### <span data-ttu-id="bb94d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb94d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bb94d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="bb94d-139">OUTPUTS</span></span>

### <span data-ttu-id="bb94d-140">Microsoft.Azure.Commands.Synapse.models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="bb94d-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="bb94d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="bb94d-141">NOTES</span></span>

## <span data-ttu-id="bb94d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb94d-142">RELATED LINKS</span></span>
