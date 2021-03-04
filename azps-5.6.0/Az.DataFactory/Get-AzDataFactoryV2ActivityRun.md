---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5262e5b9d1229905c80a7a2f83c71d9a77840ece
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907746"
---
# <span data-ttu-id="d769a-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d769a-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="d769a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d769a-102">SYNOPSIS</span></span>
<span data-ttu-id="d769a-103">在管線執行中，獲得執行活動的資訊。</span><span class="sxs-lookup"><span data-stu-id="d769a-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="d769a-104">語法</span><span class="sxs-lookup"><span data-stu-id="d769a-104">SYNTAX</span></span>

### <span data-ttu-id="d769a-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d769a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d769a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d769a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d769a-107">描述</span><span class="sxs-lookup"><span data-stu-id="d769a-107">DESCRIPTION</span></span>
<span data-ttu-id="d769a-108">**Get-AzDataFactoryV2ActivityRun** Cmdlet 會取得在 Azure Data Factory 中針對指定時間範圍內發生之指定管線執行執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="d769a-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="d769a-109">此外，您可以指定活動名稱、執行執行之連結服務名稱，以及執行狀態的篩選。</span><span class="sxs-lookup"><span data-stu-id="d769a-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="d769a-110">例子</span><span class="sxs-lookup"><span data-stu-id="d769a-110">EXAMPLES</span></span>

### <span data-ttu-id="d769a-111">範例 1：取得管線執行的所有活動執行</span><span class="sxs-lookup"><span data-stu-id="d769a-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="d769a-112">此命令會詳細瞭解在管線執行期間執行的所有活動，其 ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" 發生于 "2017-09-01" 和 "2017-09-30" 之間。</span><span class="sxs-lookup"><span data-stu-id="d769a-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="d769a-113">參數</span><span class="sxs-lookup"><span data-stu-id="d769a-113">PARAMETERS</span></span>

### <span data-ttu-id="d769a-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d769a-114">-ActivityName</span></span>
<span data-ttu-id="d769a-115">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="d769a-115">The name of the activity.</span></span>

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

### <span data-ttu-id="d769a-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d769a-116">-DataFactory</span></span>
<span data-ttu-id="d769a-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="d769a-117">The data factory object.</span></span>

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

### <span data-ttu-id="d769a-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d769a-118">-DataFactoryName</span></span>
<span data-ttu-id="d769a-119">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d769a-119">The data factory name.</span></span>

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

### <span data-ttu-id="d769a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d769a-120">-DefaultProfile</span></span>
<span data-ttu-id="d769a-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d769a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d769a-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d769a-122">-PipelineRunId</span></span>
<span data-ttu-id="d769a-123">管線的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d769a-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="d769a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d769a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d769a-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d769a-125">The resource group name.</span></span>

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

### <span data-ttu-id="d769a-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d769a-126">-RunStartedAfter</span></span>
<span data-ttu-id="d769a-127">管線執行開始執行的時間或時間。</span><span class="sxs-lookup"><span data-stu-id="d769a-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="d769a-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d769a-128">-RunStartedBefore</span></span>
<span data-ttu-id="d769a-129">管線執行開始執行的時間或之前。</span><span class="sxs-lookup"><span data-stu-id="d769a-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="d769a-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="d769a-130">-Status</span></span>
<span data-ttu-id="d769a-131">管線執行的狀態。</span><span class="sxs-lookup"><span data-stu-id="d769a-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="d769a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d769a-132">CommonParameters</span></span>
<span data-ttu-id="d769a-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d769a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d769a-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d769a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d769a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d769a-135">INPUTS</span></span>

### <span data-ttu-id="d769a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d769a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d769a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d769a-137">System.String</span></span>

## <span data-ttu-id="d769a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d769a-138">OUTPUTS</span></span>

### <span data-ttu-id="d769a-139">Microsoft.Azure.Commands.DataFactoryV2.models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="d769a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="d769a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d769a-140">NOTES</span></span>

## <span data-ttu-id="d769a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d769a-141">RELATED LINKS</span></span>

[<span data-ttu-id="d769a-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d769a-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d769a-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d769a-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

