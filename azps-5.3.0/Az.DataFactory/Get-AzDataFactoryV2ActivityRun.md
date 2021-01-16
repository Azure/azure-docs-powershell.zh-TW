---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439528"
---
# <span data-ttu-id="cf019-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="cf019-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="cf019-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf019-102">SYNOPSIS</span></span>
<span data-ttu-id="cf019-103">取得管道執行的活動執行資訊。</span><span class="sxs-lookup"><span data-stu-id="cf019-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="cf019-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf019-104">SYNTAX</span></span>

### <span data-ttu-id="cf019-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf019-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf019-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cf019-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf019-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf019-107">DESCRIPTION</span></span>
<span data-ttu-id="cf019-108">**AzDataFactoryV2ActivityRun** Cmdlet 會取得有關 Azure 資料工廠中針對在指定的管道執行中所發生的特定管線執行情況的資訊。</span><span class="sxs-lookup"><span data-stu-id="cf019-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="cf019-109">此外，您也可以指定 [活動名稱]、[已執行此執行的連結服務名稱] 和 [執行] 狀態的篩選。</span><span class="sxs-lookup"><span data-stu-id="cf019-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="cf019-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf019-110">EXAMPLES</span></span>

### <span data-ttu-id="cf019-111">範例1：取得管線執行的所有活動執行</span><span class="sxs-lookup"><span data-stu-id="cf019-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="cf019-112">這個命令會取得在「2017-09-01」和 "2017-09-30" 之間的 [使用 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" 執行管線時所執行的所有活動的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf019-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="cf019-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf019-113">PARAMETERS</span></span>

### <span data-ttu-id="cf019-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="cf019-114">-ActivityName</span></span>
<span data-ttu-id="cf019-115">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf019-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cf019-116">-DataFactory</span></span>
<span data-ttu-id="cf019-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="cf019-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf019-118">-DataFactoryName</span></span>
<span data-ttu-id="cf019-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cf019-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf019-120">-DefaultProfile</span></span>
<span data-ttu-id="cf019-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf019-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf019-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="cf019-122">-PipelineRunId</span></span>
<span data-ttu-id="cf019-123">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cf019-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf019-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf019-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf019-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="cf019-126">-RunStartedAfter</span></span>
<span data-ttu-id="cf019-127">在管道開始執行之前或之後的時間。</span><span class="sxs-lookup"><span data-stu-id="cf019-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="cf019-128">-RunStartedBefore</span></span>
<span data-ttu-id="cf019-129">在管道開始執行之前或之前的時間。</span><span class="sxs-lookup"><span data-stu-id="cf019-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="cf019-130">-Status</span></span>
<span data-ttu-id="cf019-131">管線的狀態為 [執行]。</span><span class="sxs-lookup"><span data-stu-id="cf019-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf019-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf019-132">CommonParameters</span></span>
<span data-ttu-id="cf019-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf019-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf019-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf019-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf019-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cf019-135">INPUTS</span></span>

### <span data-ttu-id="cf019-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cf019-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="cf019-137">System.object</span><span class="sxs-lookup"><span data-stu-id="cf019-137">System.String</span></span>

## <span data-ttu-id="cf019-138">輸出</span><span class="sxs-lookup"><span data-stu-id="cf019-138">OUTPUTS</span></span>

### <span data-ttu-id="cf019-139">PSActivityRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cf019-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="cf019-140">筆記</span><span class="sxs-lookup"><span data-stu-id="cf019-140">NOTES</span></span>

## <span data-ttu-id="cf019-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf019-141">RELATED LINKS</span></span>

[<span data-ttu-id="cf019-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cf019-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="cf019-143">AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="cf019-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

