---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 68c524f2c8712b0da0600abda2fa8035dd5a979c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907706"
---
# <span data-ttu-id="08eab-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="08eab-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="08eab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="08eab-102">SYNOPSIS</span></span>
<span data-ttu-id="08eab-103">瞭解管線執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="08eab-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="08eab-104">語法</span><span class="sxs-lookup"><span data-stu-id="08eab-104">SYNTAX</span></span>

### <span data-ttu-id="08eab-105">ByFactoryNameByRunId (預設) </span><span class="sxs-lookup"><span data-stu-id="08eab-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08eab-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="08eab-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08eab-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="08eab-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08eab-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="08eab-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08eab-109">描述</span><span class="sxs-lookup"><span data-stu-id="08eab-109">DESCRIPTION</span></span>
<span data-ttu-id="08eab-110">**Get-AzDataFactoryV2PipelineRun** 命令會針對指定的管線，會傳送執行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08eab-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="08eab-111">如果指定 PipelineRunId，它會以該識別碼顯示執行詳細資料。</span><span class="sxs-lookup"><span data-stu-id="08eab-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="08eab-112">如果未指定 PipelineRunId，則會顯示 LastUpdatedAfter 和 LastUpdatedBefore 值之間發生之管線的所有執行資訊。</span><span class="sxs-lookup"><span data-stu-id="08eab-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="08eab-113">例子</span><span class="sxs-lookup"><span data-stu-id="08eab-113">EXAMPLES</span></span>

### <span data-ttu-id="08eab-114">範例 1：取得管線執行的資訊</span><span class="sxs-lookup"><span data-stu-id="08eab-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="08eab-115">此命令會獲得使用 ID "61eb095a-fe23-4591-8a97-fade6c65ca72" 執行管線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="08eab-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="08eab-116">參數</span><span class="sxs-lookup"><span data-stu-id="08eab-116">PARAMETERS</span></span>

### <span data-ttu-id="08eab-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="08eab-117">-DataFactory</span></span>
<span data-ttu-id="08eab-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="08eab-118">The data factory object.</span></span>

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

### <span data-ttu-id="08eab-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="08eab-119">-DataFactoryName</span></span>
<span data-ttu-id="08eab-120">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="08eab-120">The data factory name.</span></span>

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

### <span data-ttu-id="08eab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08eab-121">-DefaultProfile</span></span>
<span data-ttu-id="08eab-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="08eab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08eab-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="08eab-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="08eab-124">以 ISO8601 格式更新管線執行的時間。</span><span class="sxs-lookup"><span data-stu-id="08eab-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="08eab-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="08eab-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="08eab-126">以 ISO8601 格式更新管線執行的時間。</span><span class="sxs-lookup"><span data-stu-id="08eab-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="08eab-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="08eab-127">-PipelineName</span></span>
<span data-ttu-id="08eab-128">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="08eab-128">The pipeline name.</span></span>

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

### <span data-ttu-id="08eab-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="08eab-129">-PipelineRunId</span></span>
<span data-ttu-id="08eab-130">管線的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="08eab-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="08eab-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08eab-131">-ResourceGroupName</span></span>
<span data-ttu-id="08eab-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="08eab-132">The resource group name.</span></span>

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

### <span data-ttu-id="08eab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08eab-133">CommonParameters</span></span>
<span data-ttu-id="08eab-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="08eab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08eab-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="08eab-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08eab-136">輸入</span><span class="sxs-lookup"><span data-stu-id="08eab-136">INPUTS</span></span>

### <span data-ttu-id="08eab-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="08eab-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="08eab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="08eab-138">System.String</span></span>

## <span data-ttu-id="08eab-139">輸出</span><span class="sxs-lookup"><span data-stu-id="08eab-139">OUTPUTS</span></span>

### <span data-ttu-id="08eab-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="08eab-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="08eab-141">筆記</span><span class="sxs-lookup"><span data-stu-id="08eab-141">NOTES</span></span>

## <span data-ttu-id="08eab-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="08eab-142">RELATED LINKS</span></span>

[<span data-ttu-id="08eab-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="08eab-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="08eab-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="08eab-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

