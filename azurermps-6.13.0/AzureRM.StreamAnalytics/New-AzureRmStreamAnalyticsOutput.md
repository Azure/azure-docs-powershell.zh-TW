---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 175dca4da4c392ecf0ee16a4ad48a93fea9d6398
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449688"
---
# <span data-ttu-id="cc7c4-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cc7c4-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="cc7c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7c4-103">建立或更新資料流程分析作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc7c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc7c4-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc7c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc7c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7c4-106">**AzureRmStreamAnalyticsOutput** Cmdlet 會在串流分析作業中建立輸出，或更新現有的輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="cc7c4-107">您可以在中指定輸出的名稱。JSON 檔案或命令列上。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="cc7c4-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="cc7c4-109">如果您指定的輸出已存在，但未指定 *Force* 參數，則 Cmdlet 會詢問是否要取代現有的輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="cc7c4-110">如果您指定 *Force* 參數並指定現有的輸出名稱，則會在未確認的情況下取代輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="cc7c4-111">示例</span><span class="sxs-lookup"><span data-stu-id="cc7c4-111">EXAMPLES</span></span>

### <span data-ttu-id="cc7c4-112">範例1：將輸出新增至作業</span><span class="sxs-lookup"><span data-stu-id="cc7c4-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="cc7c4-113">這個命令會在名為 StreamingJob 的作業中建立稱為輸出的新輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="cc7c4-114">如果已定義具有此名稱的現有輸出，該 Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="cc7c4-115">範例2：取代作業輸出定義</span><span class="sxs-lookup"><span data-stu-id="cc7c4-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="cc7c4-116">這個命令會取代作業中名為 StreamingJob 的輸出定義，無需確認。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="cc7c4-117">參數</span><span class="sxs-lookup"><span data-stu-id="cc7c4-117">PARAMETERS</span></span>

### <span data-ttu-id="cc7c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7c4-118">-DefaultProfile</span></span>
<span data-ttu-id="cc7c4-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc7c4-120">檔案</span><span class="sxs-lookup"><span data-stu-id="cc7c4-120">-File</span></span>
<span data-ttu-id="cc7c4-121">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 資料流程分析輸出的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="cc7c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cc7c4-122">-Force</span></span>
<span data-ttu-id="cc7c4-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc7c4-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="cc7c4-124">-JobName</span></span>
<span data-ttu-id="cc7c4-125">指定 Azure Stream Analytics 作業的名稱，以在其上建立 Azure 資料流程分析輸出。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="cc7c4-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc7c4-126">-Name</span></span>
<span data-ttu-id="cc7c4-127">指定要建立之 Azure 串流分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="cc7c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc7c4-129">指定要在其中建立 Azure 資料流程分析輸出的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="cc7c4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cc7c4-130">-Confirm</span></span>
<span data-ttu-id="cc7c4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7c4-132">-WhatIf</span></span>
<span data-ttu-id="cc7c4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7c4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7c4-135">CommonParameters</span></span>
<span data-ttu-id="cc7c4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7c4-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7c4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cc7c4-138">INPUTS</span></span>

### <span data-ttu-id="cc7c4-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cc7c4-139">System.String</span></span>

## <span data-ttu-id="cc7c4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cc7c4-140">OUTPUTS</span></span>

### <span data-ttu-id="cc7c4-141">PSOutput 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="cc7c4-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="cc7c4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cc7c4-142">NOTES</span></span>

## <span data-ttu-id="cc7c4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc7c4-143">RELATED LINKS</span></span>

[<span data-ttu-id="cc7c4-144">AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cc7c4-144">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="cc7c4-145">移除-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cc7c4-145">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="cc7c4-146">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cc7c4-146">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


