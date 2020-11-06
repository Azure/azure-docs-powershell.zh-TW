---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: eba11e68d23c852426a7d4541359874bd813fc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622596"
---
# <span data-ttu-id="d1a11-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d1a11-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="d1a11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a11-103">取得有關管道執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1a11-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="d1a11-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1a11-104">SYNTAX</span></span>

### <span data-ttu-id="d1a11-105">ByFactoryNameByRunId (預設) </span><span class="sxs-lookup"><span data-stu-id="d1a11-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a11-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="d1a11-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a11-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="d1a11-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1a11-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="d1a11-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1a11-109">說明</span><span class="sxs-lookup"><span data-stu-id="d1a11-109">DESCRIPTION</span></span>
<span data-ttu-id="d1a11-110">[ **取得 AzDataFactoryV2PipelineRun** ] 命令會傳回指定管線執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1a11-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="d1a11-111">如果已指定 PipelineRunId，則會顯示該 ID 執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1a11-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="d1a11-112">如果未指定 PipelineRunId，則會顯示在 LastUpdatedAfter 和 LastUpdatedBefore 值之間發生之特定管線的所有執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1a11-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="d1a11-113">示例</span><span class="sxs-lookup"><span data-stu-id="d1a11-113">EXAMPLES</span></span>

### <span data-ttu-id="d1a11-114">範例1：取得 pipline 執行的資訊</span><span class="sxs-lookup"><span data-stu-id="d1a11-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="d1a11-115">這個命令會取得 ID 為 "61eb095a-fe23-4591-8a97-fade6c65ca72" 的管線執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1a11-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="d1a11-116">參數</span><span class="sxs-lookup"><span data-stu-id="d1a11-116">PARAMETERS</span></span>

### <span data-ttu-id="d1a11-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1a11-117">-DataFactory</span></span>
<span data-ttu-id="d1a11-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="d1a11-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d1a11-119">-DataFactoryName</span></span>
<span data-ttu-id="d1a11-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a11-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a11-121">-DefaultProfile</span></span>
<span data-ttu-id="d1a11-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1a11-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a11-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="d1a11-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="d1a11-124">以 ISO8601 格式更新管線執行時間或之後的時間。</span><span class="sxs-lookup"><span data-stu-id="d1a11-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="d1a11-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="d1a11-126">在管道執行之前或之前的時間，以 ISO8601 格式更新。</span><span class="sxs-lookup"><span data-stu-id="d1a11-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d1a11-127">-PipelineName</span></span>
<span data-ttu-id="d1a11-128">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a11-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d1a11-129">-PipelineRunId</span></span>
<span data-ttu-id="d1a11-130">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d1a11-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a11-131">-ResourceGroupName</span></span>
<span data-ttu-id="d1a11-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a11-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a11-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a11-133">CommonParameters</span></span>
<span data-ttu-id="d1a11-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1a11-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a11-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1a11-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a11-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d1a11-136">INPUTS</span></span>

### <span data-ttu-id="d1a11-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1a11-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d1a11-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d1a11-138">System.String</span></span>

## <span data-ttu-id="d1a11-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d1a11-139">OUTPUTS</span></span>

### <span data-ttu-id="d1a11-140">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d1a11-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="d1a11-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d1a11-141">NOTES</span></span>

## <span data-ttu-id="d1a11-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1a11-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1a11-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d1a11-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d1a11-144">AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d1a11-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

