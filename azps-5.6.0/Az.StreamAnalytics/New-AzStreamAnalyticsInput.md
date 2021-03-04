---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6dfb659987178b4bfe65855552e1018d085de360
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907378"
---
# <span data-ttu-id="14b94-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14b94-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="14b94-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14b94-102">SYNOPSIS</span></span>
<span data-ttu-id="14b94-103">建立或更新工作輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="14b94-104">語法</span><span class="sxs-lookup"><span data-stu-id="14b94-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14b94-105">描述</span><span class="sxs-lookup"><span data-stu-id="14b94-105">DESCRIPTION</span></span>
<span data-ttu-id="14b94-106">**New-AzStreamAnalyticsInput** Cmdlet 在 Stream Analytics 工作內建立輸入，或更新現有的輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="14b94-107">您可以在 JSON 檔案或命令列中指定輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="14b94-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="14b94-108">如果兩者都指定，命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="14b94-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="14b94-109">如果您指定已存在的輸入，而且未指定 *Force* 參數，Cmdlet 會詢問是否要取代現有的輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="14b94-110">如果您指定 *Force* 參數並指定現有的輸入名稱，將會取代輸入而不確認。</span><span class="sxs-lookup"><span data-stu-id="14b94-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="14b94-111">例子</span><span class="sxs-lookup"><span data-stu-id="14b94-111">EXAMPLES</span></span>

### <span data-ttu-id="14b94-112">範例 1：從檔案建立具有定義的工作輸入</span><span class="sxs-lookup"><span data-stu-id="14b94-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="14b94-113">此命令會從您輸入的檔案Input.js輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="14b94-114">如果已定義輸入定義檔案中指定之名稱的現有輸入，Cmdlet 會詢問是否要取代。</span><span class="sxs-lookup"><span data-stu-id="14b94-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="14b94-115">範例 2：建立工作輸入</span><span class="sxs-lookup"><span data-stu-id="14b94-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="14b94-116">此命令會為名為 EntryStream 的工作建立新輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="14b94-117">如果已定義具有此名稱的現有輸入，Cmdlet 會詢問是否要取代。</span><span class="sxs-lookup"><span data-stu-id="14b94-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="14b94-118">範例 3：以檔案的定義取代工作輸入</span><span class="sxs-lookup"><span data-stu-id="14b94-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="14b94-119">此命令會以檔案定義取代名為 EntryStream 的現有輸入來源定義，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="14b94-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="14b94-120">參數</span><span class="sxs-lookup"><span data-stu-id="14b94-120">PARAMETERS</span></span>

### <span data-ttu-id="14b94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b94-121">-DefaultProfile</span></span>
<span data-ttu-id="14b94-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14b94-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b94-123">-檔案</span><span class="sxs-lookup"><span data-stu-id="14b94-123">-File</span></span>
<span data-ttu-id="14b94-124">指定 JSON 檔案的路徑，其中包含要建立之 Azure Stream Analytics 輸入的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="14b94-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="14b94-125">-強制</span><span class="sxs-lookup"><span data-stu-id="14b94-125">-Force</span></span>
<span data-ttu-id="14b94-126">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="14b94-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14b94-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="14b94-127">-JobName</span></span>
<span data-ttu-id="14b94-128">指定 Azure Stream Analytics 工作的名稱，以根據該工作建立 Azure Stream Analytics 輸入。</span><span class="sxs-lookup"><span data-stu-id="14b94-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="14b94-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="14b94-129">-Name</span></span>
<span data-ttu-id="14b94-130">指定要建立之 Azure Stream Analytics 輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="14b94-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="14b94-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b94-131">-ResourceGroupName</span></span>
<span data-ttu-id="14b94-132">指定要建立 Azure 串流輸入的資源組名。</span><span class="sxs-lookup"><span data-stu-id="14b94-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="14b94-133">-確認</span><span class="sxs-lookup"><span data-stu-id="14b94-133">-Confirm</span></span>
<span data-ttu-id="14b94-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="14b94-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b94-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b94-135">-WhatIf</span></span>
<span data-ttu-id="14b94-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14b94-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b94-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14b94-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b94-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b94-138">CommonParameters</span></span>
<span data-ttu-id="14b94-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14b94-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b94-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14b94-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b94-141">輸入</span><span class="sxs-lookup"><span data-stu-id="14b94-141">INPUTS</span></span>

### <span data-ttu-id="14b94-142">System.String</span><span class="sxs-lookup"><span data-stu-id="14b94-142">System.String</span></span>

## <span data-ttu-id="14b94-143">輸出</span><span class="sxs-lookup"><span data-stu-id="14b94-143">OUTPUTS</span></span>

### <span data-ttu-id="14b94-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="14b94-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="14b94-145">筆記</span><span class="sxs-lookup"><span data-stu-id="14b94-145">NOTES</span></span>

## <span data-ttu-id="14b94-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="14b94-146">RELATED LINKS</span></span>

[<span data-ttu-id="14b94-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14b94-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="14b94-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14b94-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="14b94-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14b94-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


