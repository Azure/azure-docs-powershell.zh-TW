---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 84df5d0ed28b2d11b3e03e298242da4938a47eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456340"
---
# <span data-ttu-id="45777-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45777-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="45777-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45777-102">SYNOPSIS</span></span>
<span data-ttu-id="45777-103">建立或更新作業輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45777-104">句法</span><span class="sxs-lookup"><span data-stu-id="45777-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45777-105">說明</span><span class="sxs-lookup"><span data-stu-id="45777-105">DESCRIPTION</span></span>
<span data-ttu-id="45777-106">**AzureRmStreamAnalyticsInput** Cmdlet 會在串流分析作業中建立輸入，或更新現有的輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="45777-107">輸入的名稱可以在 JSON 檔案或命令列上指定。</span><span class="sxs-lookup"><span data-stu-id="45777-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="45777-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="45777-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="45777-109">如果您指定的輸入已經存在，而且沒有指定 *Force* 參數，則 Cmdlet 會詢問是否要取代現有的輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="45777-110">如果您指定 *Force* 參數並指定現有的輸入名稱，則會在未確認的情況下取代輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="45777-111">示例</span><span class="sxs-lookup"><span data-stu-id="45777-111">EXAMPLES</span></span>

### <span data-ttu-id="45777-112">範例1：使用檔案的定義來建立作業輸入</span><span class="sxs-lookup"><span data-stu-id="45777-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="45777-113">這個命令會從 Input.js的檔案建立輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="45777-114">如果已定義輸入定義檔中指定名稱的現有輸入，則 Cmdlet 會詢問是否要取代該輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="45777-115">範例2：建立作業輸入</span><span class="sxs-lookup"><span data-stu-id="45777-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="45777-116">這個命令會在名為 EntryStream 的工作上建立新的輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="45777-117">如果已定義具有此名稱的現有輸入，則此 Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="45777-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="45777-118">範例3：使用檔案的定義來取代作業輸入</span><span class="sxs-lookup"><span data-stu-id="45777-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="45777-119">這個命令會將名為 EntryStream 的現有輸入來源的定義取代為 [來自檔案的定義，無需確認]。</span><span class="sxs-lookup"><span data-stu-id="45777-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="45777-120">參數</span><span class="sxs-lookup"><span data-stu-id="45777-120">PARAMETERS</span></span>

### <span data-ttu-id="45777-121">檔案</span><span class="sxs-lookup"><span data-stu-id="45777-121">-File</span></span>
<span data-ttu-id="45777-122">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 資料流程分析輸入的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="45777-122">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="45777-123">-Force</span><span class="sxs-lookup"><span data-stu-id="45777-123">-Force</span></span>
<span data-ttu-id="45777-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="45777-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45777-125">-JobName</span><span class="sxs-lookup"><span data-stu-id="45777-125">-JobName</span></span>
<span data-ttu-id="45777-126">指定 Azure Stream Analytics 作業的名稱，以在其上建立 Azure 資料流程分析輸入。</span><span class="sxs-lookup"><span data-stu-id="45777-126">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="45777-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="45777-127">-Name</span></span>
<span data-ttu-id="45777-128">指定要建立之 Azure 串流分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="45777-128">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="45777-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45777-129">-ResourceGroupName</span></span>
<span data-ttu-id="45777-130">指定要在哪個資源群組中建立 Azure 資料流程輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="45777-130">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="45777-131">-確認</span><span class="sxs-lookup"><span data-stu-id="45777-131">-Confirm</span></span>
<span data-ttu-id="45777-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45777-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45777-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45777-133">-WhatIf</span></span>
<span data-ttu-id="45777-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45777-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45777-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45777-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45777-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45777-136">-DefaultProfile</span></span>
<span data-ttu-id="45777-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45777-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45777-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45777-138">CommonParameters</span></span>
<span data-ttu-id="45777-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45777-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45777-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45777-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45777-141">輸入</span><span class="sxs-lookup"><span data-stu-id="45777-141">INPUTS</span></span>

## <span data-ttu-id="45777-142">輸出</span><span class="sxs-lookup"><span data-stu-id="45777-142">OUTPUTS</span></span>

### <span data-ttu-id="45777-143">PSInput 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="45777-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="45777-144">筆記</span><span class="sxs-lookup"><span data-stu-id="45777-144">NOTES</span></span>

## <span data-ttu-id="45777-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="45777-145">RELATED LINKS</span></span>

[<span data-ttu-id="45777-146">AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45777-146">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="45777-147">移除-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45777-147">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="45777-148">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45777-148">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


