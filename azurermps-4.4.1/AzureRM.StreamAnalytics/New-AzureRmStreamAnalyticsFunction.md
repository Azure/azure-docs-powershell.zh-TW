---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448814"
---
# <span data-ttu-id="8e9b5-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8e9b5-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="8e9b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9b5-103">建立或取代串流分析作業中的函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e9b5-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e9b5-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9b5-106">**AzureRmStreamAnalyticsFunction** Cmdlet 會在 Azure 串流分析作業中建立函數，或取代現有的函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="8e9b5-107">在 JavaScript 物件符號 (JSON) 檔案中定義函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="8e9b5-108">您可以使用 *name* 參數或在 json 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="8e9b5-109">如果您以兩種方式指定名稱，則名稱必須相符。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="8e9b5-110">若要取代現有的函數，請指定現有函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="8e9b5-111">示例</span><span class="sxs-lookup"><span data-stu-id="8e9b5-111">EXAMPLES</span></span>

### <span data-ttu-id="8e9b5-112">範例1：建立串流分析函數</span><span class="sxs-lookup"><span data-stu-id="8e9b5-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="8e9b5-113">這個命令會從檔案 Function07.js建立函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="8e9b5-114">函數的名稱會儲存在 json 檔案中。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="8e9b5-115">範例2：建立名為 ScoreTweet 的串流分析函數</span><span class="sxs-lookup"><span data-stu-id="8e9b5-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="8e9b5-116">這個命令會在名為 ScoreTweet 的作業上建立一個函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="8e9b5-117">範例3：取代串流分析函數</span><span class="sxs-lookup"><span data-stu-id="8e9b5-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="8e9b5-118">這個命令會將名為 ScoreTweet 的現有函式定義替換為 Function22.js的定義。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="8e9b5-119">參數</span><span class="sxs-lookup"><span data-stu-id="8e9b5-119">PARAMETERS</span></span>

### <span data-ttu-id="8e9b5-120">檔案</span><span class="sxs-lookup"><span data-stu-id="8e9b5-120">-File</span></span>
<span data-ttu-id="8e9b5-121">指定包含 Stream Analytics 函數 JSON 標記法的 json 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="8e9b5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9b5-122">-Force</span></span>
<span data-ttu-id="8e9b5-123">表示此 Cmdlet 會取代現有的資料流程分析函數，且不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8e9b5-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="8e9b5-124">-JobName</span></span>
<span data-ttu-id="8e9b5-125">指定 Stream Analytics 作業的名稱，此 Cmdlet 會在此建立串流分析函數。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="8e9b5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e9b5-126">-Name</span></span>
<span data-ttu-id="8e9b5-127">指定此 Cmdlet 所建立的串流分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8e9b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e9b5-129">指定此 Cmdlet 建立串流分析函式所依據的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="8e9b5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8e9b5-130">-Confirm</span></span>
<span data-ttu-id="8e9b5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9b5-132">-WhatIf</span></span>
<span data-ttu-id="8e9b5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9b5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9b5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9b5-135">-DefaultProfile</span></span>
<span data-ttu-id="8e9b5-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e9b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9b5-137">CommonParameters</span></span>
<span data-ttu-id="8e9b5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9b5-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9b5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="8e9b5-140">INPUTS</span></span>

## <span data-ttu-id="8e9b5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8e9b5-141">OUTPUTS</span></span>

### <span data-ttu-id="8e9b5-142">PSFunction 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="8e9b5-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="8e9b5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8e9b5-143">NOTES</span></span>

## <span data-ttu-id="8e9b5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e9b5-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e9b5-145">AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8e9b5-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8e9b5-146">移除-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8e9b5-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8e9b5-147">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8e9b5-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


