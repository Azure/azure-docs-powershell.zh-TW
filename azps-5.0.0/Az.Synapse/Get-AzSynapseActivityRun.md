---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137951"
---
# <span data-ttu-id="50ee5-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="50ee5-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="50ee5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="50ee5-103">取得管道執行的活動執行資訊。</span><span class="sxs-lookup"><span data-stu-id="50ee5-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="50ee5-104">句法</span><span class="sxs-lookup"><span data-stu-id="50ee5-104">SYNTAX</span></span>

### <span data-ttu-id="50ee5-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="50ee5-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50ee5-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="50ee5-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50ee5-107">說明</span><span class="sxs-lookup"><span data-stu-id="50ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="50ee5-108">**AzSynapseActivityRun** Cmdlet 會取得在工作區中針對在給定時間範圍內執行的指定管線執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="50ee5-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="50ee5-109">此外，您也可以指定 [活動名稱] 和 [執行] 狀態的篩選。</span><span class="sxs-lookup"><span data-stu-id="50ee5-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="50ee5-110">示例</span><span class="sxs-lookup"><span data-stu-id="50ee5-110">EXAMPLES</span></span>

### <span data-ttu-id="50ee5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="50ee5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="50ee5-112">這個命令會取得在「2018-09-01T21：00」和「2018-09-30T21：00」之間，在名為 "f288712d-fb08-4cb8-96ef-82d3b9b30621" 的管道中執行的所有活動執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="50ee5-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="50ee5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="50ee5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="50ee5-114">這個命令會取得在「2018-09-01T21： 00 "和" 2018-09-30T21： 00 "到管線之間發生的所有活動執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="50ee5-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="50ee5-115">參數</span><span class="sxs-lookup"><span data-stu-id="50ee5-115">PARAMETERS</span></span>

### <span data-ttu-id="50ee5-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="50ee5-116">-ActivityName</span></span>
<span data-ttu-id="50ee5-117">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="50ee5-117">The name of the activity.</span></span>

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

### <span data-ttu-id="50ee5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ee5-118">-DefaultProfile</span></span>
<span data-ttu-id="50ee5-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50ee5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50ee5-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="50ee5-120">-PipelineName</span></span>
<span data-ttu-id="50ee5-121">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="50ee5-121">The pipeline name.</span></span>

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

### <span data-ttu-id="50ee5-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="50ee5-122">-PipelineRunId</span></span>
<span data-ttu-id="50ee5-123">管線執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="50ee5-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="50ee5-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="50ee5-124">-RunStartedAfter</span></span>
<span data-ttu-id="50ee5-125">以 "ISO 8601" 格式更新 run 事件的時間或之後。</span><span class="sxs-lookup"><span data-stu-id="50ee5-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="50ee5-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="50ee5-126">-RunStartedBefore</span></span>
<span data-ttu-id="50ee5-127">以 "ISO 8601" 格式更新 run 事件之前或之前的時間。</span><span class="sxs-lookup"><span data-stu-id="50ee5-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="50ee5-128">-狀態</span><span class="sxs-lookup"><span data-stu-id="50ee5-128">-Status</span></span>
<span data-ttu-id="50ee5-129">管線的狀態為 [執行]。</span><span class="sxs-lookup"><span data-stu-id="50ee5-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="50ee5-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50ee5-130">-WorkspaceName</span></span>
<span data-ttu-id="50ee5-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="50ee5-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="50ee5-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50ee5-132">-WorkspaceObject</span></span>
<span data-ttu-id="50ee5-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="50ee5-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="50ee5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ee5-134">CommonParameters</span></span>
<span data-ttu-id="50ee5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50ee5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ee5-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50ee5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ee5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="50ee5-137">INPUTS</span></span>

### <span data-ttu-id="50ee5-138">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="50ee5-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="50ee5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="50ee5-139">OUTPUTS</span></span>

### <span data-ttu-id="50ee5-140">PSActivityRunsQueryResponse 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="50ee5-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="50ee5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="50ee5-141">NOTES</span></span>

## <span data-ttu-id="50ee5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="50ee5-142">RELATED LINKS</span></span>
