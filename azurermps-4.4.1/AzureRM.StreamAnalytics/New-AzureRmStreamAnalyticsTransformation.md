---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447898"
---
# <span data-ttu-id="5d650-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="5d650-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="5d650-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d650-102">SYNOPSIS</span></span>
<span data-ttu-id="5d650-103">在作業內建立或更新轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d650-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d650-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d650-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d650-105">DESCRIPTION</span></span>
<span data-ttu-id="5d650-106">**AzureRmStreamAnalyticsTransformation** Cmdlet 會在串流分析作業中建立轉換，或更新現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="5d650-107">您可以在中指定轉換的名稱。JSON 檔案或命令列上。</span><span class="sxs-lookup"><span data-stu-id="5d650-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="5d650-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="5d650-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="5d650-109">如果您指定的轉換已存在，但未指定 Force 參數，則 Cmdlet 會詢問是否要取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="5d650-110">如果您指定 *Force* 參數並指定現有的轉換名稱，則會在未確認的情況下取代轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="5d650-111">示例</span><span class="sxs-lookup"><span data-stu-id="5d650-111">EXAMPLES</span></span>

### <span data-ttu-id="5d650-112">範例1：建立或取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="5d650-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="5d650-113">這個命令會在稱為 StreamingJob 的作業中建立稱為 StreamingJobTransform 的轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="5d650-114">如果現有的轉換已定義為該名稱，則 Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="5d650-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="5d650-115">範例2：取代作業中的轉換</span><span class="sxs-lookup"><span data-stu-id="5d650-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="5d650-116">這個命令會取代作業 StreamingJob 中的 StreamingJobTransform 定義，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="5d650-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="5d650-117">參數</span><span class="sxs-lookup"><span data-stu-id="5d650-117">PARAMETERS</span></span>

### <span data-ttu-id="5d650-118">檔案</span><span class="sxs-lookup"><span data-stu-id="5d650-118">-File</span></span>
<span data-ttu-id="5d650-119">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 資料流程分析轉換的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="5d650-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="5d650-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5d650-120">-Force</span></span>
<span data-ttu-id="5d650-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5d650-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d650-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="5d650-122">-JobName</span></span>
<span data-ttu-id="5d650-123">指定 Azure Stream Analytics 作業的名稱，以在其上建立 Azure 資料流程分析轉換。</span><span class="sxs-lookup"><span data-stu-id="5d650-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="5d650-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d650-124">-Name</span></span>
<span data-ttu-id="5d650-125">指定要建立之 Azure 串流分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d650-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="5d650-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d650-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d650-127">指定要在哪個資源群組中建立 Azure 資料流程分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d650-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="5d650-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5d650-128">-Confirm</span></span>
<span data-ttu-id="5d650-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d650-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d650-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d650-130">-WhatIf</span></span>
<span data-ttu-id="5d650-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d650-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d650-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d650-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d650-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d650-133">-DefaultProfile</span></span>
<span data-ttu-id="5d650-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d650-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d650-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d650-135">CommonParameters</span></span>
<span data-ttu-id="5d650-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d650-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d650-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d650-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d650-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5d650-138">INPUTS</span></span>

## <span data-ttu-id="5d650-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5d650-139">OUTPUTS</span></span>

### <span data-ttu-id="5d650-140">PSTransformation 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="5d650-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="5d650-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5d650-141">NOTES</span></span>

## <span data-ttu-id="5d650-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d650-142">RELATED LINKS</span></span>

[<span data-ttu-id="5d650-143">AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="5d650-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)

