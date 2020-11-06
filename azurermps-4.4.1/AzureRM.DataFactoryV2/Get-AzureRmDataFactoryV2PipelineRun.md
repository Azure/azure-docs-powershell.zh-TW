---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456744"
---
# <span data-ttu-id="773a0-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="773a0-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="773a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="773a0-102">SYNOPSIS</span></span>
<span data-ttu-id="773a0-103">取得有關管道執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="773a0-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="773a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="773a0-104">SYNTAX</span></span>

### <span data-ttu-id="773a0-105">ByFactoryNameByRunId (預設) </span><span class="sxs-lookup"><span data-stu-id="773a0-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### <span data-ttu-id="773a0-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="773a0-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### <span data-ttu-id="773a0-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="773a0-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### <span data-ttu-id="773a0-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="773a0-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## <span data-ttu-id="773a0-109">說明</span><span class="sxs-lookup"><span data-stu-id="773a0-109">DESCRIPTION</span></span>
<span data-ttu-id="773a0-110">[ **取得 AzureRmDataFactoryV2PipelineRun** ] 命令會傳回指定管線執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="773a0-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="773a0-111">如果已指定 PipelineRunId，則會顯示該 ID 執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="773a0-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="773a0-112">如果未指定 PipelineRunId，則會顯示在 LastUpdatedAfter 和 LastUpdatedBefore 值之間發生之特定管線的所有執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="773a0-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="773a0-113">示例</span><span class="sxs-lookup"><span data-stu-id="773a0-113">EXAMPLES</span></span>

### <span data-ttu-id="773a0-114">範例1：取得 pipline 執行的資訊</span><span class="sxs-lookup"><span data-stu-id="773a0-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :

```

<span data-ttu-id="773a0-115">這個命令會取得 ID 為 "61eb095a-fe23-4591-8a97-fade6c65ca72" 的管線執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="773a0-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>


## <span data-ttu-id="773a0-116">參數</span><span class="sxs-lookup"><span data-stu-id="773a0-116">PARAMETERS</span></span>

### <span data-ttu-id="773a0-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="773a0-117">-DataFactory</span></span>
<span data-ttu-id="773a0-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="773a0-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="773a0-119">-DataFactoryName</span></span>
<span data-ttu-id="773a0-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="773a0-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="773a0-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="773a0-122">以 ISO8601 格式更新管線執行時間或之後的時間。</span><span class="sxs-lookup"><span data-stu-id="773a0-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="773a0-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="773a0-124">在管道執行之前或之前的時間，以 ISO8601 格式更新。</span><span class="sxs-lookup"><span data-stu-id="773a0-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="773a0-125">-PipelineName</span></span>
<span data-ttu-id="773a0-126">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="773a0-126">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="773a0-127">-PipelineRunId</span></span>
<span data-ttu-id="773a0-128">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="773a0-128">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773a0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="773a0-129">-ResourceGroupName</span></span>
<span data-ttu-id="773a0-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="773a0-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="773a0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="773a0-131">INPUTS</span></span>

### <span data-ttu-id="773a0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="773a0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="773a0-133">System.object</span><span class="sxs-lookup"><span data-stu-id="773a0-133">System.String</span></span>


## <span data-ttu-id="773a0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="773a0-134">OUTPUTS</span></span>

### <span data-ttu-id="773a0-135">[System.object]。清單 ' 1 [DataFactoryV2. PSPipelineRun，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="773a0-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="773a0-136">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="773a0-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>


## <span data-ttu-id="773a0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="773a0-137">NOTES</span></span>

## <span data-ttu-id="773a0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="773a0-138">RELATED LINKS</span></span>
[<span data-ttu-id="773a0-139">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="773a0-139">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="773a0-140">AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="773a0-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

