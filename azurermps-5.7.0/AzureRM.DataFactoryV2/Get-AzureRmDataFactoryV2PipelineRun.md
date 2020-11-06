---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455452"
---
# <span data-ttu-id="a60be-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a60be-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="a60be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a60be-102">SYNOPSIS</span></span>
<span data-ttu-id="a60be-103">取得有關管道執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="a60be-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a60be-104">句法</span><span class="sxs-lookup"><span data-stu-id="a60be-104">SYNTAX</span></span>

### <span data-ttu-id="a60be-105">ByFactoryNameByRunId (預設) </span><span class="sxs-lookup"><span data-stu-id="a60be-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a60be-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="a60be-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a60be-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="a60be-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a60be-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="a60be-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60be-109">說明</span><span class="sxs-lookup"><span data-stu-id="a60be-109">DESCRIPTION</span></span>
<span data-ttu-id="a60be-110">[ **取得 AzureRmDataFactoryV2PipelineRun** ] 命令會傳回指定管線執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a60be-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="a60be-111">如果已指定 PipelineRunId，則會顯示該 ID 執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a60be-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="a60be-112">如果未指定 PipelineRunId，則會顯示在 LastUpdatedAfter 和 LastUpdatedBefore 值之間發生之特定管線的所有執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a60be-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="a60be-113">示例</span><span class="sxs-lookup"><span data-stu-id="a60be-113">EXAMPLES</span></span>

### <span data-ttu-id="a60be-114">範例1：取得 pipline 執行的資訊</span><span class="sxs-lookup"><span data-stu-id="a60be-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="a60be-115">這個命令會取得 ID 為 "61eb095a-fe23-4591-8a97-fade6c65ca72" 的管線執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a60be-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="a60be-116">參數</span><span class="sxs-lookup"><span data-stu-id="a60be-116">PARAMETERS</span></span>

### <span data-ttu-id="a60be-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a60be-117">-DataFactory</span></span>
<span data-ttu-id="a60be-118">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="a60be-118">The data factory object.</span></span>

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

### <span data-ttu-id="a60be-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a60be-119">-DataFactoryName</span></span>
<span data-ttu-id="a60be-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a60be-120">The data factory name.</span></span>

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

### <span data-ttu-id="a60be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60be-121">-DefaultProfile</span></span>
<span data-ttu-id="a60be-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a60be-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60be-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="a60be-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="a60be-124">以 ISO8601 格式更新管線執行時間或之後的時間。</span><span class="sxs-lookup"><span data-stu-id="a60be-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="a60be-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="a60be-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="a60be-126">在管道執行之前或之前的時間，以 ISO8601 格式更新。</span><span class="sxs-lookup"><span data-stu-id="a60be-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="a60be-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a60be-127">-PipelineName</span></span>
<span data-ttu-id="a60be-128">管線名稱。</span><span class="sxs-lookup"><span data-stu-id="a60be-128">The pipeline name.</span></span>

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

### <span data-ttu-id="a60be-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a60be-129">-PipelineRunId</span></span>
<span data-ttu-id="a60be-130">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a60be-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60be-131">-ResourceGroupName</span></span>
<span data-ttu-id="a60be-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a60be-132">The resource group name.</span></span>

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

### <span data-ttu-id="a60be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60be-133">CommonParameters</span></span>
<span data-ttu-id="a60be-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a60be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60be-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a60be-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60be-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a60be-136">INPUTS</span></span>

### <span data-ttu-id="a60be-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a60be-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="a60be-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a60be-138">System.String</span></span>

## <span data-ttu-id="a60be-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a60be-139">OUTPUTS</span></span>

### <span data-ttu-id="a60be-140">[System.object]。清單 ' 1 [DataFactoryV2. PSPipelineRun，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="a60be-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a60be-141">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="a60be-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="a60be-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a60be-142">NOTES</span></span>

## <span data-ttu-id="a60be-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a60be-143">RELATED LINKS</span></span>

[<span data-ttu-id="a60be-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a60be-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a60be-145">AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a60be-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

