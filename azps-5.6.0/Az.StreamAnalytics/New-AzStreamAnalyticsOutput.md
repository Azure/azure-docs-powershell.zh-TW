---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b4484d06802a8b17fc08b359b5dafb7e0a406ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916337"
---
# <span data-ttu-id="50268-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="50268-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="50268-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50268-102">SYNOPSIS</span></span>
<span data-ttu-id="50268-103">為 Stream Analytics 工作建立或更新輸出。</span><span class="sxs-lookup"><span data-stu-id="50268-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="50268-104">語法</span><span class="sxs-lookup"><span data-stu-id="50268-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50268-105">描述</span><span class="sxs-lookup"><span data-stu-id="50268-105">DESCRIPTION</span></span>
<span data-ttu-id="50268-106">**New-AzStreamAnalyticsOutput** Cmdlet 在 Stream Analytics 工作內建立輸出，或更新現有的輸出。</span><span class="sxs-lookup"><span data-stu-id="50268-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="50268-107">您可以在 中指定輸出的名稱。JSON 檔案或命令列。</span><span class="sxs-lookup"><span data-stu-id="50268-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="50268-108">如果兩者都指定，命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="50268-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="50268-109">如果您指定已存在的輸出，而且未指定 *Force* 參數，Cmdlet 會詢問是否要取代現有的輸出。</span><span class="sxs-lookup"><span data-stu-id="50268-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="50268-110">如果您指定 *Force* 參數並指定現有的輸出名稱，輸出將會取代而不確認。</span><span class="sxs-lookup"><span data-stu-id="50268-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="50268-111">例子</span><span class="sxs-lookup"><span data-stu-id="50268-111">EXAMPLES</span></span>

### <span data-ttu-id="50268-112">範例 1：新增輸出至工作</span><span class="sxs-lookup"><span data-stu-id="50268-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="50268-113">此命令在名為 StreamingJob 的工作中建立名為 Output 的新輸出。</span><span class="sxs-lookup"><span data-stu-id="50268-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="50268-114">如果已定義具有此名稱的現有輸出，Cmdlet 會詢問是否要取代它。</span><span class="sxs-lookup"><span data-stu-id="50268-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="50268-115">範例 2：取代工作輸出定義</span><span class="sxs-lookup"><span data-stu-id="50268-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="50268-116">此命令會取代名為 StreamingJob 的工作中的 Output 定義，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="50268-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="50268-117">參數</span><span class="sxs-lookup"><span data-stu-id="50268-117">PARAMETERS</span></span>

### <span data-ttu-id="50268-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50268-118">-DefaultProfile</span></span>
<span data-ttu-id="50268-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50268-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50268-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="50268-120">-File</span></span>
<span data-ttu-id="50268-121">指定 JSON 檔案的路徑，其中包含要建立之 Azure Stream Analytics 輸出的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="50268-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="50268-122">-強制</span><span class="sxs-lookup"><span data-stu-id="50268-122">-Force</span></span>
<span data-ttu-id="50268-123">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="50268-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50268-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="50268-124">-JobName</span></span>
<span data-ttu-id="50268-125">指定 Azure Stream Analytics 工作的名稱，以根據該工作建立 Azure Stream Analytics 輸出。</span><span class="sxs-lookup"><span data-stu-id="50268-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="50268-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="50268-126">-Name</span></span>
<span data-ttu-id="50268-127">指定要建立之 Azure Stream Analytics 輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="50268-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="50268-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50268-128">-ResourceGroupName</span></span>
<span data-ttu-id="50268-129">指定要建立 Azure Stream Analytics 輸出之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50268-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="50268-130">-確認</span><span class="sxs-lookup"><span data-stu-id="50268-130">-Confirm</span></span>
<span data-ttu-id="50268-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50268-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50268-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50268-132">-WhatIf</span></span>
<span data-ttu-id="50268-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50268-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50268-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50268-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50268-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50268-135">CommonParameters</span></span>
<span data-ttu-id="50268-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50268-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50268-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="50268-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50268-138">輸入</span><span class="sxs-lookup"><span data-stu-id="50268-138">INPUTS</span></span>

### <span data-ttu-id="50268-139">System.String</span><span class="sxs-lookup"><span data-stu-id="50268-139">System.String</span></span>

## <span data-ttu-id="50268-140">輸出</span><span class="sxs-lookup"><span data-stu-id="50268-140">OUTPUTS</span></span>

### <span data-ttu-id="50268-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="50268-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="50268-142">筆記</span><span class="sxs-lookup"><span data-stu-id="50268-142">NOTES</span></span>

## <span data-ttu-id="50268-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="50268-143">RELATED LINKS</span></span>

[<span data-ttu-id="50268-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="50268-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="50268-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="50268-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="50268-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="50268-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


