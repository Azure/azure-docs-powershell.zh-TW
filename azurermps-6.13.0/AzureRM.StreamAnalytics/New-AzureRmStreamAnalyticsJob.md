---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 540ea984d165a841288d1928192ad0ce035f7eb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449689"
---
# <span data-ttu-id="2dba4-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="2dba4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dba4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dba4-103">建立或更新資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="2dba4-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dba4-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dba4-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dba4-105">說明</span><span class="sxs-lookup"><span data-stu-id="2dba4-105">DESCRIPTION</span></span>
<span data-ttu-id="2dba4-106">**新的 AzureRmStreamAnalyticsJob** Cmdlet 會在 Azure 中建立新的資料流程分析作業，或更新現有指定作業的定義。</span><span class="sxs-lookup"><span data-stu-id="2dba4-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="2dba4-107">您可以在中指定作業名稱。JSON 檔案或命令列上。</span><span class="sxs-lookup"><span data-stu-id="2dba4-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2dba4-108">如果兩者都指定，則命令列上的名稱必須與檔案中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="2dba4-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2dba4-109">如果您指定的作業名稱已經存在，但沒有指定 *Force* 參數，則 Cmdlet 會詢問是否要取代現有的作業。</span><span class="sxs-lookup"><span data-stu-id="2dba4-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="2dba4-110">如果您指定 *Force* 參數並指定現有的作業名稱，作業定義將會不經確認就加以取代。</span><span class="sxs-lookup"><span data-stu-id="2dba4-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="2dba4-111">示例</span><span class="sxs-lookup"><span data-stu-id="2dba4-111">EXAMPLES</span></span>

### <span data-ttu-id="2dba4-112">範例1：建立工作</span><span class="sxs-lookup"><span data-stu-id="2dba4-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="2dba4-113">這個命令會從 JobDefinition.js的定義建立作業。</span><span class="sxs-lookup"><span data-stu-id="2dba4-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="2dba4-114">如果已定義作業定義檔中具有指定名稱的現有作業，則 Cmdlet 會詢問是否要取代該作業。</span><span class="sxs-lookup"><span data-stu-id="2dba4-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2dba4-115">範例2：取代作業定義</span><span class="sxs-lookup"><span data-stu-id="2dba4-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="2dba4-116">這個命令會取代 StreamingJob 的作業定義而不需確認。</span><span class="sxs-lookup"><span data-stu-id="2dba4-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2dba4-117">參數</span><span class="sxs-lookup"><span data-stu-id="2dba4-117">PARAMETERS</span></span>

### <span data-ttu-id="2dba4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dba4-118">-DefaultProfile</span></span>
<span data-ttu-id="2dba4-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dba4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dba4-120">檔案</span><span class="sxs-lookup"><span data-stu-id="2dba4-120">-File</span></span>
<span data-ttu-id="2dba4-121">指定 JSON 檔案的路徑，該檔案包含要建立之 Azure 串流分析作業的 JSON 標記法。</span><span class="sxs-lookup"><span data-stu-id="2dba4-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dba4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2dba4-122">-Force</span></span>
<span data-ttu-id="2dba4-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2dba4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2dba4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2dba4-124">-Name</span></span>
<span data-ttu-id="2dba4-125">指定要建立之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dba4-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dba4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dba4-126">-ResourceGroupName</span></span>
<span data-ttu-id="2dba4-127">指定 Azure 資料流程分析作業應該屬於的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dba4-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="2dba4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2dba4-128">-Confirm</span></span>
<span data-ttu-id="2dba4-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2dba4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dba4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dba4-130">-WhatIf</span></span>
<span data-ttu-id="2dba4-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dba4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dba4-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dba4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dba4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dba4-133">CommonParameters</span></span>
<span data-ttu-id="2dba4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dba4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dba4-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2dba4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dba4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2dba4-136">INPUTS</span></span>

### <span data-ttu-id="2dba4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="2dba4-137">System.String</span></span>

## <span data-ttu-id="2dba4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2dba4-138">OUTPUTS</span></span>

### <span data-ttu-id="2dba4-139">PSJob 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="2dba4-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="2dba4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2dba4-140">NOTES</span></span>

## <span data-ttu-id="2dba4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dba4-141">RELATED LINKS</span></span>

[<span data-ttu-id="2dba4-142">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-142">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2dba4-143">移除-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-143">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2dba4-144">開始-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-144">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2dba4-145">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2dba4-146">停止 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2dba4-146">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

