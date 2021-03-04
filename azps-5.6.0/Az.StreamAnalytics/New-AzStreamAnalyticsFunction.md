---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ac303b4e458e836238a148f1a33b009e9c0b0e24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907381"
---
# <span data-ttu-id="d79cb-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d79cb-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="d79cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d79cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d79cb-103">在 Stream Analytics 工作中建立或取代函數。</span><span class="sxs-lookup"><span data-stu-id="d79cb-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="d79cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="d79cb-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d79cb-105">描述</span><span class="sxs-lookup"><span data-stu-id="d79cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d79cb-106">**New-AzStreamAnalyticsFunctdion Cmdlet** 在 Azure Stream Analytics 中建立函數，或取代現有的函數。</span><span class="sxs-lookup"><span data-stu-id="d79cb-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="d79cb-107">在 JSON 檔案的 JavaScript 物件表示 (定義) 函數。</span><span class="sxs-lookup"><span data-stu-id="d79cb-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="d79cb-108">您可以使用 Name 參數或在 .json檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="d79cb-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="d79cb-109">如果您以這兩種方式指定名稱，名稱必須相符。</span><span class="sxs-lookup"><span data-stu-id="d79cb-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="d79cb-110">若要取代現有的函數，請指定現有函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="d79cb-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="d79cb-111">例子</span><span class="sxs-lookup"><span data-stu-id="d79cb-111">EXAMPLES</span></span>

### <span data-ttu-id="d79cb-112">範例 1：建立 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="d79cb-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="d79cb-113">此命令會從檔案建立函數，Function07.js上。</span><span class="sxs-lookup"><span data-stu-id="d79cb-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="d79cb-114">函數的名稱會儲存在 .json 檔案中。</span><span class="sxs-lookup"><span data-stu-id="d79cb-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="d79cb-115">範例 2：建立名為 ScoreTweet 的 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="d79cb-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="d79cb-116">此命令在名為 ScoreTweet 的工作上建立函數。</span><span class="sxs-lookup"><span data-stu-id="d79cb-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="d79cb-117">範例 3：取代 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="d79cb-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="d79cb-118">此命令會以現有名為 ScoreTweet 的函式定義取代為Function22.js定義。</span><span class="sxs-lookup"><span data-stu-id="d79cb-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="d79cb-119">參數</span><span class="sxs-lookup"><span data-stu-id="d79cb-119">PARAMETERS</span></span>

### <span data-ttu-id="d79cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79cb-120">-DefaultProfile</span></span>
<span data-ttu-id="d79cb-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d79cb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79cb-122">-檔案</span><span class="sxs-lookup"><span data-stu-id="d79cb-122">-File</span></span>
<span data-ttu-id="d79cb-123">指定包含 Stream Analytics 函數 JSON 標記法的 .json 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="d79cb-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="d79cb-124">-強制</span><span class="sxs-lookup"><span data-stu-id="d79cb-124">-Force</span></span>
<span data-ttu-id="d79cb-125">表示此 Cmdlet 會取代現有的 Stream Analytics 函數，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d79cb-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d79cb-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="d79cb-126">-JobName</span></span>
<span data-ttu-id="d79cb-127">指定 Stream Analytics 工作的名稱，在此名稱下此 Cmdlet 會建立 Stream Analytics 函數。</span><span class="sxs-lookup"><span data-stu-id="d79cb-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="d79cb-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d79cb-128">-Name</span></span>
<span data-ttu-id="d79cb-129">指定此 Cmdlet 所建立 Stream Analytics 函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="d79cb-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d79cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="d79cb-131">指定此 Cmdlet 建立 Stream Analytics 函數的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d79cb-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="d79cb-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d79cb-132">-Confirm</span></span>
<span data-ttu-id="d79cb-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d79cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79cb-134">-WhatIf</span></span>
<span data-ttu-id="d79cb-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d79cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79cb-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d79cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79cb-137">CommonParameters</span></span>
<span data-ttu-id="d79cb-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d79cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79cb-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d79cb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79cb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d79cb-140">INPUTS</span></span>

### <span data-ttu-id="d79cb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d79cb-141">System.String</span></span>

## <span data-ttu-id="d79cb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d79cb-142">OUTPUTS</span></span>

### <span data-ttu-id="d79cb-143">Microsoft.Azure.Commands.StreamAnalytics.models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="d79cb-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="d79cb-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d79cb-144">NOTES</span></span>

## <span data-ttu-id="d79cb-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d79cb-145">RELATED LINKS</span></span>

[<span data-ttu-id="d79cb-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d79cb-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d79cb-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d79cb-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d79cb-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d79cb-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


