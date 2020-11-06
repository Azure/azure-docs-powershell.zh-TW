---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453272"
---
# <span data-ttu-id="e96e3-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="e96e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e96e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e96e3-103">建立服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="e96e3-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e96e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e96e3-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e96e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e96e3-105">DESCRIPTION</span></span>
<span data-ttu-id="e96e3-106">**新的-AzureRmSchedulerServiceBusTopicJob** Cmdlet 會在 Azure 排程器中建立服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="e96e3-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="e96e3-107">這個 Cmdlet 支援以 *ErrorActionType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="e96e3-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="e96e3-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="e96e3-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="e96e3-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="e96e3-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e96e3-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="e96e3-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e96e3-111">示例</span><span class="sxs-lookup"><span data-stu-id="e96e3-111">EXAMPLES</span></span>

## <span data-ttu-id="e96e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="e96e3-112">PARAMETERS</span></span>

### <span data-ttu-id="e96e3-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e96e3-113">-EndTime</span></span>
<span data-ttu-id="e96e3-114">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="e96e3-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="e96e3-115">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e96e3-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="e96e3-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="e96e3-116">-ErrorActionType</span></span>
<span data-ttu-id="e96e3-117">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="e96e3-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="e96e3-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96e3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e96e3-119">Http</span><span class="sxs-lookup"><span data-stu-id="e96e3-119">Http</span></span> 
- <span data-ttu-id="e96e3-120">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="e96e3-120">Https</span></span> 
- <span data-ttu-id="e96e3-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="e96e3-121">StorageQueue</span></span> 
- <span data-ttu-id="e96e3-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e96e3-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="e96e3-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e96e3-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="e96e3-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="e96e3-124">-ExecutionCount</span></span>
<span data-ttu-id="e96e3-125">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="e96e3-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="e96e3-126">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="e96e3-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="e96e3-127">頻率</span><span class="sxs-lookup"><span data-stu-id="e96e3-127">-Frequency</span></span>
<span data-ttu-id="e96e3-128">指定工作的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="e96e3-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="e96e3-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96e3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e96e3-130">數</span><span class="sxs-lookup"><span data-stu-id="e96e3-130">Minute</span></span> 
- <span data-ttu-id="e96e3-131">每</span><span class="sxs-lookup"><span data-stu-id="e96e3-131">Hour</span></span> 
- <span data-ttu-id="e96e3-132">之內</span><span class="sxs-lookup"><span data-stu-id="e96e3-132">Day</span></span> 
- <span data-ttu-id="e96e3-133">周</span><span class="sxs-lookup"><span data-stu-id="e96e3-133">Week</span></span> 
- <span data-ttu-id="e96e3-134">月</span><span class="sxs-lookup"><span data-stu-id="e96e3-134">Month</span></span>

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

### <span data-ttu-id="e96e3-135">間隔</span><span class="sxs-lookup"><span data-stu-id="e96e3-135">-Interval</span></span>
<span data-ttu-id="e96e3-136">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="e96e3-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="e96e3-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e96e3-137">-JobCollectionName</span></span>
<span data-ttu-id="e96e3-138">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="e96e3-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="e96e3-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="e96e3-139">-JobName</span></span>
<span data-ttu-id="e96e3-140">指定工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e96e3-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="e96e3-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="e96e3-141">-JobState</span></span>
<span data-ttu-id="e96e3-142">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e96e3-142">Specifies the state of the job.</span></span>
<span data-ttu-id="e96e3-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96e3-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e96e3-144">後</span><span class="sxs-lookup"><span data-stu-id="e96e3-144">Enabled</span></span> 
- <span data-ttu-id="e96e3-145">禁止</span><span class="sxs-lookup"><span data-stu-id="e96e3-145">Disabled</span></span>

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

### <span data-ttu-id="e96e3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96e3-146">-ResourceGroupName</span></span>
<span data-ttu-id="e96e3-147">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e96e3-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="e96e3-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="e96e3-148">-ServiceBusMessage</span></span>
<span data-ttu-id="e96e3-149">指定服務匯流排主題訊息。</span><span class="sxs-lookup"><span data-stu-id="e96e3-149">Specifies a service bus topic message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e96e3-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="e96e3-151">指定服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="e96e3-151">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="e96e3-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="e96e3-153">指定共用的 access 簽名金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="e96e3-153">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="e96e3-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="e96e3-155">指定共用的存取簽名金鑰值。</span><span class="sxs-lookup"><span data-stu-id="e96e3-155">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="e96e3-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="e96e3-157">指定服務匯流排主題路徑。</span><span class="sxs-lookup"><span data-stu-id="e96e3-157">Specifies a service bus topic path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="e96e3-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="e96e3-159">指定服務匯流排傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="e96e3-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="e96e3-160">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96e3-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e96e3-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="e96e3-161">NetMessaging</span></span>
- <span data-ttu-id="e96e3-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="e96e3-162">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96e3-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e96e3-163">-StartTime</span></span>
<span data-ttu-id="e96e3-164">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="e96e3-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="e96e3-165">-確認</span><span class="sxs-lookup"><span data-stu-id="e96e3-165">-Confirm</span></span>
<span data-ttu-id="e96e3-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e96e3-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e96e3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96e3-167">-WhatIf</span></span>
<span data-ttu-id="e96e3-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e96e3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96e3-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e96e3-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e96e3-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96e3-170">-DefaultProfile</span></span>
<span data-ttu-id="e96e3-171">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e96e3-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e96e3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96e3-172">CommonParameters</span></span>
<span data-ttu-id="e96e3-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e96e3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96e3-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e96e3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96e3-175">輸入</span><span class="sxs-lookup"><span data-stu-id="e96e3-175">INPUTS</span></span>

## <span data-ttu-id="e96e3-176">輸出</span><span class="sxs-lookup"><span data-stu-id="e96e3-176">OUTPUTS</span></span>

### <span data-ttu-id="e96e3-177">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e96e3-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="e96e3-178">筆記</span><span class="sxs-lookup"><span data-stu-id="e96e3-178">NOTES</span></span>

## <span data-ttu-id="e96e3-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="e96e3-179">RELATED LINKS</span></span>

[<span data-ttu-id="e96e3-180">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="e96e3-181">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e96e3-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e96e3-182">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="e96e3-183">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="e96e3-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="e96e3-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e96e3-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e96e3-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="e96e3-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="e96e3-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="e96e3-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


