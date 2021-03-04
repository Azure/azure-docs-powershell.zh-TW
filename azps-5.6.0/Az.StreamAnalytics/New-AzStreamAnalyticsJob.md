---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: 8a9da4d68456b612cbd1bd4db3997cc67e724975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904222"
---
# <span data-ttu-id="5227c-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="5227c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5227c-102">SYNOPSIS</span></span>
<span data-ttu-id="5227c-103">建立或更新 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="5227c-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="5227c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5227c-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5227c-105">描述</span><span class="sxs-lookup"><span data-stu-id="5227c-105">DESCRIPTION</span></span>
<span data-ttu-id="5227c-106">**New-AzStreamAnalyticsJob** Cmdlet 在 Azure 中建立新的 Stream Analytics 工作，或更新現有指定工作的定義。</span><span class="sxs-lookup"><span data-stu-id="5227c-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="5227c-107">您可以在 中指定工作的名稱。JSON 檔案或命令列。</span><span class="sxs-lookup"><span data-stu-id="5227c-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="5227c-108">如果兩者都指定，命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="5227c-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="5227c-109">如果您指定已存在的工作名稱，而且未指定 *Force* 參數，Cmdlet 會詢問是否要取代現有的工作。</span><span class="sxs-lookup"><span data-stu-id="5227c-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="5227c-110">如果您指定 *Force* 參數並指定現有的職稱，則工作定義將在未確認的情況下取代。</span><span class="sxs-lookup"><span data-stu-id="5227c-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="5227c-111">例子</span><span class="sxs-lookup"><span data-stu-id="5227c-111">EXAMPLES</span></span>

### <span data-ttu-id="5227c-112">範例 1：建立工作</span><span class="sxs-lookup"><span data-stu-id="5227c-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="5227c-113">此命令會從工作上的定義JobDefinition.js工作。</span><span class="sxs-lookup"><span data-stu-id="5227c-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="5227c-114">如果已定義工作定義檔案中具有指定名稱的現有工作，Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="5227c-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="5227c-115">範例 2：取代工作定義</span><span class="sxs-lookup"><span data-stu-id="5227c-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="5227c-116">此命令會取代 StreamingJob 的工作定義，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="5227c-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="5227c-117">參數</span><span class="sxs-lookup"><span data-stu-id="5227c-117">PARAMETERS</span></span>

### <span data-ttu-id="5227c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5227c-118">-DefaultProfile</span></span>
<span data-ttu-id="5227c-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5227c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5227c-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="5227c-120">-File</span></span>
<span data-ttu-id="5227c-121">指定 JSON 檔案的路徑，其中包含要建立之 Azure Stream Analytics 工作之 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="5227c-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-122">-強制</span><span class="sxs-lookup"><span data-stu-id="5227c-122">-Force</span></span>
<span data-ttu-id="5227c-123">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5227c-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5227c-124">-Name</span></span>
<span data-ttu-id="5227c-125">指定要建立之 Azure Stream Analytics 工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="5227c-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5227c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5227c-127">指定 Azure Stream Analytics 工作應所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5227c-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5227c-128">-Confirm</span></span>
<span data-ttu-id="5227c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5227c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5227c-130">-WhatIf</span></span>
<span data-ttu-id="5227c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5227c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5227c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5227c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5227c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5227c-133">CommonParameters</span></span>
<span data-ttu-id="5227c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5227c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5227c-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5227c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5227c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5227c-136">INPUTS</span></span>

### <span data-ttu-id="5227c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5227c-137">System.String</span></span>

## <span data-ttu-id="5227c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5227c-138">OUTPUTS</span></span>

### <span data-ttu-id="5227c-139">Microsoft.Azure.Commands.StreamAnalytics.models.PSJob</span><span class="sxs-lookup"><span data-stu-id="5227c-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="5227c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5227c-140">NOTES</span></span>

## <span data-ttu-id="5227c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5227c-141">RELATED LINKS</span></span>

[<span data-ttu-id="5227c-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5227c-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5227c-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5227c-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5227c-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5227c-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


