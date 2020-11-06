---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: ac5735d66a7b44c7183a9af3a32c01445f2b3486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451272"
---
# <span data-ttu-id="9f255-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="9f255-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="9f255-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f255-102">SYNOPSIS</span></span>
<span data-ttu-id="9f255-103">取得有關管道執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="9f255-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f255-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f255-104">SYNTAX</span></span>

### <span data-ttu-id="9f255-105">ByFactoryNameByRunId (預設) </span><span class="sxs-lookup"><span data-stu-id="9f255-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f255-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="9f255-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f255-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="9f255-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f255-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="9f255-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f255-109">說明</span><span class="sxs-lookup"><span data-stu-id="9f255-109">DESCRIPTION</span></span>
<span data-ttu-id="9f255-110">[ **取得 AzureRmDataFactoryV2PipelineRun** ] 命令會傳回指定管線執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f255-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="9f255-111">如果已指定 PipelineRunId，則會顯示該 ID 執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f255-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="9f255-112">如果未指定 PipelineRunId，則會顯示在 LastUpdatedAfter 和 LastUpdatedBefore 值之間發生之特定管線的所有執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f255-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="9f255-113">示例</span><span class="sxs-lookup"><span data-stu-id="9f255-113">EXAMPLES</span></span>

### <span data-ttu-id="9f255-114">範例1：取得 pipline 執行的資訊</span><span class="sxs-lookup"><span data-stu-id="9f255-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="9f255-115">這個命令會取得 ID 為 "61eb095a-fe23-4591-8a97-fade6c65ca72" 的管線執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f255-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="9f255-116">參數</span><span class="sxs-lookup"><span data-stu-id="9f255-116">PARAMETERS</span></span>

### <span data-ttu-id="9f255-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f255-117">-DataFactory</span></span>
<span data-ttu-id="9f255-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="9f255-118">The data factory object.</span></span>

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

### <span data-ttu-id="9f255-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f255-119">-DataFactoryName</span></span>
<span data-ttu-id="9f255-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="9f255-120">The data factory name.</span></span>

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

### <span data-ttu-id="9f255-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f255-121">-DefaultProfile</span></span>
<span data-ttu-id="9f255-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f255-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f255-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="9f255-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="9f255-124">以 ISO8601 格式更新管線執行時間或之後的時間。</span><span class="sxs-lookup"><span data-stu-id="9f255-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="9f255-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="9f255-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="9f255-126">在管道執行之前或之前的時間，以 ISO8601 格式更新。</span><span class="sxs-lookup"><span data-stu-id="9f255-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="9f255-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="9f255-127">-PipelineName</span></span>
<span data-ttu-id="9f255-128">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="9f255-128">The pipeline name.</span></span>

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

### <span data-ttu-id="9f255-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="9f255-129">-PipelineRunId</span></span>
<span data-ttu-id="9f255-130">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9f255-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="9f255-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f255-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f255-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f255-132">The resource group name.</span></span>

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

### <span data-ttu-id="9f255-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f255-133">CommonParameters</span></span>
<span data-ttu-id="9f255-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f255-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f255-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f255-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f255-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9f255-136">INPUTS</span></span>

### <span data-ttu-id="9f255-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f255-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9f255-138">參數： DataFactory (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9f255-138">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="9f255-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9f255-139">System.String</span></span>

## <span data-ttu-id="9f255-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9f255-140">OUTPUTS</span></span>

### <span data-ttu-id="9f255-141">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="9f255-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="9f255-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9f255-142">NOTES</span></span>

## <span data-ttu-id="9f255-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f255-143">RELATED LINKS</span></span>

[<span data-ttu-id="9f255-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9f255-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9f255-145">AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="9f255-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

