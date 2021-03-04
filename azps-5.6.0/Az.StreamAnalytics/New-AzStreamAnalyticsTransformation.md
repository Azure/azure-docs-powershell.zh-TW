---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: d9529d31ab53c16b3d8be10c2d92761a2c8a5fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916334"
---
# <span data-ttu-id="68191-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="68191-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="68191-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68191-102">SYNOPSIS</span></span>
<span data-ttu-id="68191-103">建立或更新工作內部的轉換。</span><span class="sxs-lookup"><span data-stu-id="68191-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="68191-104">語法</span><span class="sxs-lookup"><span data-stu-id="68191-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68191-105">描述</span><span class="sxs-lookup"><span data-stu-id="68191-105">DESCRIPTION</span></span>
<span data-ttu-id="68191-106">**New-AzStreamAnalyticsTransformation** Cmdlet 在 Stream Analytics 工作內建立轉換，或更新現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="68191-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="68191-107">您可以在 中指定轉換的名稱。JSON 檔案或命令列。</span><span class="sxs-lookup"><span data-stu-id="68191-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="68191-108">如果兩者都指定，命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="68191-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="68191-109">如果您指定已存在的轉換，而且未指定 Force 參數，Cmdlet 會詢問是否要取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="68191-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="68191-110">如果您指定 *Force* 參數並指定現有的轉換名稱，轉換將會取代而不確認。</span><span class="sxs-lookup"><span data-stu-id="68191-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="68191-111">例子</span><span class="sxs-lookup"><span data-stu-id="68191-111">EXAMPLES</span></span>

### <span data-ttu-id="68191-112">範例 1：在工作中建立或取代轉換</span><span class="sxs-lookup"><span data-stu-id="68191-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="68191-113">此命令在名為 StreamingJob 的工作中建立名為 StreamingJobTransform 的轉換。</span><span class="sxs-lookup"><span data-stu-id="68191-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="68191-114">如果已經用該名稱定義現有的轉換，Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="68191-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="68191-115">範例 2：取代工作中的轉換</span><span class="sxs-lookup"><span data-stu-id="68191-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="68191-116">此命令會取代 Job StreamingJob 中 StreamingJobTransform 的定義，而不會確認。</span><span class="sxs-lookup"><span data-stu-id="68191-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="68191-117">參數</span><span class="sxs-lookup"><span data-stu-id="68191-117">PARAMETERS</span></span>

### <span data-ttu-id="68191-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68191-118">-DefaultProfile</span></span>
<span data-ttu-id="68191-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68191-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68191-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="68191-120">-File</span></span>
<span data-ttu-id="68191-121">指定 JSON 檔案的路徑，其中包含要建立之 Azure Stream Analytics 轉換的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="68191-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="68191-122">-強制</span><span class="sxs-lookup"><span data-stu-id="68191-122">-Force</span></span>
<span data-ttu-id="68191-123">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="68191-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68191-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="68191-124">-JobName</span></span>
<span data-ttu-id="68191-125">指定建立 Azure Stream Analytics 轉換的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="68191-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="68191-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="68191-126">-Name</span></span>
<span data-ttu-id="68191-127">指定要建立之 Azure Stream Analytics 轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="68191-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="68191-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68191-128">-ResourceGroupName</span></span>
<span data-ttu-id="68191-129">指定要建立 Azure Stream Analytics 轉換的資源組名。</span><span class="sxs-lookup"><span data-stu-id="68191-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="68191-130">-確認</span><span class="sxs-lookup"><span data-stu-id="68191-130">-Confirm</span></span>
<span data-ttu-id="68191-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="68191-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68191-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68191-132">-WhatIf</span></span>
<span data-ttu-id="68191-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68191-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68191-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68191-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68191-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68191-135">CommonParameters</span></span>
<span data-ttu-id="68191-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68191-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68191-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="68191-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68191-138">輸入</span><span class="sxs-lookup"><span data-stu-id="68191-138">INPUTS</span></span>

### <span data-ttu-id="68191-139">System.String</span><span class="sxs-lookup"><span data-stu-id="68191-139">System.String</span></span>

## <span data-ttu-id="68191-140">輸出</span><span class="sxs-lookup"><span data-stu-id="68191-140">OUTPUTS</span></span>

### <span data-ttu-id="68191-141">Microsoft.Azure.Commands.StreamAnalytics.models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="68191-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="68191-142">筆記</span><span class="sxs-lookup"><span data-stu-id="68191-142">NOTES</span></span>

## <span data-ttu-id="68191-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="68191-143">RELATED LINKS</span></span>

[<span data-ttu-id="68191-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="68191-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


