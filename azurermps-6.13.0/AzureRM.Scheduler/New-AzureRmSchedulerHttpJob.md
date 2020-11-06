---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455015"
---
# <span data-ttu-id="020af-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="020af-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="020af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="020af-102">SYNOPSIS</span></span>
<span data-ttu-id="020af-103">建立 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="020af-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="020af-104">句法</span><span class="sxs-lookup"><span data-stu-id="020af-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="020af-105">說明</span><span class="sxs-lookup"><span data-stu-id="020af-105">DESCRIPTION</span></span>
<span data-ttu-id="020af-106">**新的-AzureRmSchedulerHttpJob** Cmdlet 會在 Azure 排程器中建立一個 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="020af-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="020af-107">這個 Cmdlet 支援以 *ErrorActionType* 和 *HttpAuthenticationType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="020af-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="020af-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="020af-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="020af-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="020af-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="020af-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="020af-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="020af-111">示例</span><span class="sxs-lookup"><span data-stu-id="020af-111">EXAMPLES</span></span>

## <span data-ttu-id="020af-112">參數</span><span class="sxs-lookup"><span data-stu-id="020af-112">PARAMETERS</span></span>

### <span data-ttu-id="020af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020af-113">-DefaultProfile</span></span>
<span data-ttu-id="020af-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="020af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="020af-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="020af-115">-EndTime</span></span>
<span data-ttu-id="020af-116">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="020af-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="020af-117">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="020af-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="020af-118">-ErrorActionType</span></span>
<span data-ttu-id="020af-119">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="020af-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="020af-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="020af-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020af-121">Http</span><span class="sxs-lookup"><span data-stu-id="020af-121">Http</span></span> 
- <span data-ttu-id="020af-122">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="020af-122">Https</span></span> 
- <span data-ttu-id="020af-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="020af-123">StorageQueue</span></span> 
- <span data-ttu-id="020af-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="020af-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="020af-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="020af-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="020af-126">-ExecutionCount</span></span>
<span data-ttu-id="020af-127">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="020af-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="020af-128">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="020af-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-129">頻率</span><span class="sxs-lookup"><span data-stu-id="020af-129">-Frequency</span></span>
<span data-ttu-id="020af-130">指定工作的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="020af-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="020af-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="020af-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020af-132">數</span><span class="sxs-lookup"><span data-stu-id="020af-132">Minute</span></span> 
- <span data-ttu-id="020af-133">每</span><span class="sxs-lookup"><span data-stu-id="020af-133">Hour</span></span> 
- <span data-ttu-id="020af-134">之內</span><span class="sxs-lookup"><span data-stu-id="020af-134">Day</span></span> 
- <span data-ttu-id="020af-135">周</span><span class="sxs-lookup"><span data-stu-id="020af-135">Week</span></span> 
- <span data-ttu-id="020af-136">月</span><span class="sxs-lookup"><span data-stu-id="020af-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-137">-標題</span><span class="sxs-lookup"><span data-stu-id="020af-137">-Headers</span></span>
<span data-ttu-id="020af-138">指定包含標頭的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="020af-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="020af-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="020af-140">指定 HTTP 驗證類型。</span><span class="sxs-lookup"><span data-stu-id="020af-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="020af-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="020af-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020af-142">所有</span><span class="sxs-lookup"><span data-stu-id="020af-142">None</span></span> 
- <span data-ttu-id="020af-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="020af-143">ClientCertificate</span></span> 
- <span data-ttu-id="020af-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="020af-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="020af-145">空白</span><span class="sxs-lookup"><span data-stu-id="020af-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-146">間隔</span><span class="sxs-lookup"><span data-stu-id="020af-146">-Interval</span></span>
<span data-ttu-id="020af-147">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="020af-147">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="020af-148">-JobCollectionName</span></span>
<span data-ttu-id="020af-149">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="020af-149">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="020af-150">-JobName</span></span>
<span data-ttu-id="020af-151">指定工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="020af-151">Specifies a name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="020af-152">-JobState</span></span>
<span data-ttu-id="020af-153">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="020af-153">Specifies the state of the job.</span></span>
<span data-ttu-id="020af-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="020af-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020af-155">後</span><span class="sxs-lookup"><span data-stu-id="020af-155">Enabled</span></span> 
- <span data-ttu-id="020af-156">禁止</span><span class="sxs-lookup"><span data-stu-id="020af-156">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-157">-方法</span><span class="sxs-lookup"><span data-stu-id="020af-157">-Method</span></span>
<span data-ttu-id="020af-158">指定作業之動作類型的方法。</span><span class="sxs-lookup"><span data-stu-id="020af-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="020af-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="020af-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020af-160">獲取</span><span class="sxs-lookup"><span data-stu-id="020af-160">GET</span></span> 
- <span data-ttu-id="020af-161">將</span><span class="sxs-lookup"><span data-stu-id="020af-161">PUT</span></span> 
- <span data-ttu-id="020af-162">發佈</span><span class="sxs-lookup"><span data-stu-id="020af-162">POST</span></span> 
- <span data-ttu-id="020af-163">DELETE</span><span class="sxs-lookup"><span data-stu-id="020af-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="020af-164">-RequestBody</span></span>
<span data-ttu-id="020af-165">指定放入和張貼作業動作之本文的值。</span><span class="sxs-lookup"><span data-stu-id="020af-165">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020af-166">-ResourceGroupName</span></span>
<span data-ttu-id="020af-167">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="020af-167">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020af-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="020af-168">-StartTime</span></span>
<span data-ttu-id="020af-169">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="020af-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-170">-Uri</span><span class="sxs-lookup"><span data-stu-id="020af-170">-Uri</span></span>
<span data-ttu-id="020af-171">指定作業動作的 URI。</span><span class="sxs-lookup"><span data-stu-id="020af-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-172">-確認</span><span class="sxs-lookup"><span data-stu-id="020af-172">-Confirm</span></span>
<span data-ttu-id="020af-173">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="020af-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020af-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020af-174">-WhatIf</span></span>
<span data-ttu-id="020af-175">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="020af-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020af-176">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="020af-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020af-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020af-177">CommonParameters</span></span>
<span data-ttu-id="020af-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="020af-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020af-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="020af-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020af-180">輸入</span><span class="sxs-lookup"><span data-stu-id="020af-180">INPUTS</span></span>

### <span data-ttu-id="020af-181">System.object</span><span class="sxs-lookup"><span data-stu-id="020af-181">System.String</span></span>

### <span data-ttu-id="020af-182">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="020af-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="020af-183">輸出</span><span class="sxs-lookup"><span data-stu-id="020af-183">OUTPUTS</span></span>

### <span data-ttu-id="020af-184">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="020af-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="020af-185">筆記</span><span class="sxs-lookup"><span data-stu-id="020af-185">NOTES</span></span>

## <span data-ttu-id="020af-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="020af-186">RELATED LINKS</span></span>

[<span data-ttu-id="020af-187">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="020af-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="020af-188">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="020af-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="020af-189">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="020af-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="020af-190">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="020af-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="020af-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="020af-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="020af-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="020af-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="020af-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="020af-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="020af-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="020af-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="020af-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="020af-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


