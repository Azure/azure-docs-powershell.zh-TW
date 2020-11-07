---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 337371f4ba42c80d8ebf3feed166a3804dd3f25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793116"
---
# <span data-ttu-id="0de30-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="0de30-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="0de30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0de30-102">SYNOPSIS</span></span>
<span data-ttu-id="0de30-103">在作業內建立或更新轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="0de30-104">句法</span><span class="sxs-lookup"><span data-stu-id="0de30-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0de30-105">說明</span><span class="sxs-lookup"><span data-stu-id="0de30-105">DESCRIPTION</span></span>
<span data-ttu-id="0de30-106">**AzStreamAnalyticsTransformation** Cmdlet 會在串流分析作業中建立轉換，或更新現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="0de30-107">您可以在中指定轉換的名稱。JSON 檔案或命令列上。</span><span class="sxs-lookup"><span data-stu-id="0de30-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="0de30-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="0de30-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="0de30-109">如果您指定的轉換已存在，但未指定 Force 參數，則 Cmdlet 會詢問是否要取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="0de30-110">如果您指定 *Force* 參數並指定現有的轉換名稱，則會在未確認的情況下取代轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="0de30-111">示例</span><span class="sxs-lookup"><span data-stu-id="0de30-111">EXAMPLES</span></span>

### <span data-ttu-id="0de30-112">範例1：建立或取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="0de30-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="0de30-113">這個命令會在稱為 StreamingJob 的作業中建立稱為 StreamingJobTransform 的轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="0de30-114">如果現有的轉換已定義為該名稱，則 Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="0de30-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="0de30-115">範例2：取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="0de30-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="0de30-116">這個命令會取代作業 StreamingJob 中的 StreamingJobTransform 定義，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="0de30-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="0de30-117">參數</span><span class="sxs-lookup"><span data-stu-id="0de30-117">PARAMETERS</span></span>

### <span data-ttu-id="0de30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de30-118">-DefaultProfile</span></span>
<span data-ttu-id="0de30-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0de30-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de30-120">檔案</span><span class="sxs-lookup"><span data-stu-id="0de30-120">-File</span></span>
<span data-ttu-id="0de30-121">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 資料流程分析轉換的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="0de30-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de30-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0de30-122">-Force</span></span>
<span data-ttu-id="0de30-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0de30-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0de30-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="0de30-124">-JobName</span></span>
<span data-ttu-id="0de30-125">指定 Azure Stream Analytics 作業的名稱，以在其上建立 Azure 資料流程分析轉換。</span><span class="sxs-lookup"><span data-stu-id="0de30-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de30-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0de30-126">-Name</span></span>
<span data-ttu-id="0de30-127">指定要建立之 Azure 串流分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="0de30-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de30-128">-ResourceGroupName</span></span>
<span data-ttu-id="0de30-129">指定要在哪個資源群組中建立 Azure 資料流程分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="0de30-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="0de30-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0de30-130">-Confirm</span></span>
<span data-ttu-id="0de30-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0de30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de30-132">-WhatIf</span></span>
<span data-ttu-id="0de30-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0de30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de30-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0de30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de30-135">CommonParameters</span></span>
<span data-ttu-id="0de30-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0de30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de30-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0de30-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de30-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0de30-138">INPUTS</span></span>

### <span data-ttu-id="0de30-139">System.object</span><span class="sxs-lookup"><span data-stu-id="0de30-139">System.String</span></span>

## <span data-ttu-id="0de30-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0de30-140">OUTPUTS</span></span>

### <span data-ttu-id="0de30-141">PSTransformation 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="0de30-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="0de30-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0de30-142">NOTES</span></span>

## <span data-ttu-id="0de30-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0de30-143">RELATED LINKS</span></span>

[<span data-ttu-id="0de30-144">AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="0de30-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)

