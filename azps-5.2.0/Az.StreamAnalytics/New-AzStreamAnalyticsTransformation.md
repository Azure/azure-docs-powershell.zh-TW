---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283248"
---
# <span data-ttu-id="41cfd-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="41cfd-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="41cfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="41cfd-103">在作業內建立或更新轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="41cfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="41cfd-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41cfd-105">說明</span><span class="sxs-lookup"><span data-stu-id="41cfd-105">DESCRIPTION</span></span>
<span data-ttu-id="41cfd-106">**AzStreamAnalyticsTransformation** Cmdlet 會在串流分析作業中建立轉換，或更新現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="41cfd-107">您可以在中指定轉換的名稱。JSON 檔案或命令列上。</span><span class="sxs-lookup"><span data-stu-id="41cfd-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="41cfd-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="41cfd-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="41cfd-109">如果您指定的轉換已存在，但未指定 Force 參數，則 Cmdlet 會詢問是否要取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="41cfd-110">如果您指定 *Force* 參數並指定現有的轉換名稱，則會在未確認的情況下取代轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="41cfd-111">示例</span><span class="sxs-lookup"><span data-stu-id="41cfd-111">EXAMPLES</span></span>

### <span data-ttu-id="41cfd-112">範例1：建立或取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="41cfd-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="41cfd-113">這個命令會在稱為 StreamingJob 的作業中建立稱為 StreamingJobTransform 的轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="41cfd-114">如果現有的轉換已定義為該名稱，則 Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="41cfd-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="41cfd-115">範例2：取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="41cfd-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="41cfd-116">這個命令會取代作業 StreamingJob 中的 StreamingJobTransform 定義，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="41cfd-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="41cfd-117">參數</span><span class="sxs-lookup"><span data-stu-id="41cfd-117">PARAMETERS</span></span>

### <span data-ttu-id="41cfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cfd-118">-DefaultProfile</span></span>
<span data-ttu-id="41cfd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41cfd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cfd-120">檔案</span><span class="sxs-lookup"><span data-stu-id="41cfd-120">-File</span></span>
<span data-ttu-id="41cfd-121">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 資料流程分析轉換的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="41cfd-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="41cfd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="41cfd-122">-Force</span></span>
<span data-ttu-id="41cfd-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="41cfd-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41cfd-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="41cfd-124">-JobName</span></span>
<span data-ttu-id="41cfd-125">指定 Azure Stream Analytics 作業的名稱，以在其上建立 Azure 資料流程分析轉換。</span><span class="sxs-lookup"><span data-stu-id="41cfd-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="41cfd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="41cfd-126">-Name</span></span>
<span data-ttu-id="41cfd-127">指定要建立之 Azure 串流分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cfd-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="41cfd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cfd-128">-ResourceGroupName</span></span>
<span data-ttu-id="41cfd-129">指定要在哪個資源群組中建立 Azure 資料流程分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="41cfd-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="41cfd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="41cfd-130">-Confirm</span></span>
<span data-ttu-id="41cfd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41cfd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cfd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cfd-132">-WhatIf</span></span>
<span data-ttu-id="41cfd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41cfd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cfd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41cfd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cfd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cfd-135">CommonParameters</span></span>
<span data-ttu-id="41cfd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41cfd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cfd-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41cfd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cfd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="41cfd-138">INPUTS</span></span>

### <span data-ttu-id="41cfd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="41cfd-139">System.String</span></span>

## <span data-ttu-id="41cfd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="41cfd-140">OUTPUTS</span></span>

### <span data-ttu-id="41cfd-141">PSTransformation 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="41cfd-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="41cfd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="41cfd-142">NOTES</span></span>

## <span data-ttu-id="41cfd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="41cfd-143">RELATED LINKS</span></span>

[<span data-ttu-id="41cfd-144">AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="41cfd-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


