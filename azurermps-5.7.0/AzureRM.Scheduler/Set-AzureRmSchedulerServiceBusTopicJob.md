---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 7da7382359202f3856309c24a3ea484bd9b3e9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446023"
---
# <span data-ttu-id="24dc9-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="24dc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="24dc9-103">修改服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="24dc9-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24dc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="24dc9-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24dc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="24dc9-105">DESCRIPTION</span></span>
<span data-ttu-id="24dc9-106">**AzureRmSchedulerServiceBusTopicJob** Cmdlet 會修改 Azure 排程器中的服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="24dc9-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="24dc9-107">這個 Cmdlet 支援以 *ErrorActionType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="24dc9-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="24dc9-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="24dc9-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="24dc9-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="24dc9-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="24dc9-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="24dc9-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="24dc9-111">示例</span><span class="sxs-lookup"><span data-stu-id="24dc9-111">EXAMPLES</span></span>

## <span data-ttu-id="24dc9-112">參數</span><span class="sxs-lookup"><span data-stu-id="24dc9-112">PARAMETERS</span></span>

### <span data-ttu-id="24dc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24dc9-113">-DefaultProfile</span></span>
<span data-ttu-id="24dc9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24dc9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="24dc9-115">-EndTime</span></span>
<span data-ttu-id="24dc9-116">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="24dc9-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="24dc9-117">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24dc9-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="24dc9-118">-ErrorActionType</span></span>
<span data-ttu-id="24dc9-119">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="24dc9-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="24dc9-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="24dc9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24dc9-121">Http</span><span class="sxs-lookup"><span data-stu-id="24dc9-121">Http</span></span> 
- <span data-ttu-id="24dc9-122">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="24dc9-122">Https</span></span> 
- <span data-ttu-id="24dc9-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="24dc9-123">StorageQueue</span></span> 
- <span data-ttu-id="24dc9-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="24dc9-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="24dc9-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="24dc9-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="24dc9-126">-ExecutionCount</span></span>
<span data-ttu-id="24dc9-127">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="24dc9-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="24dc9-128">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="24dc9-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-129">頻率</span><span class="sxs-lookup"><span data-stu-id="24dc9-129">-Frequency</span></span>
<span data-ttu-id="24dc9-130">指定工作的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="24dc9-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="24dc9-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="24dc9-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24dc9-132">數</span><span class="sxs-lookup"><span data-stu-id="24dc9-132">Minute</span></span> 
- <span data-ttu-id="24dc9-133">每</span><span class="sxs-lookup"><span data-stu-id="24dc9-133">Hour</span></span> 
- <span data-ttu-id="24dc9-134">之內</span><span class="sxs-lookup"><span data-stu-id="24dc9-134">Day</span></span> 
- <span data-ttu-id="24dc9-135">周</span><span class="sxs-lookup"><span data-stu-id="24dc9-135">Week</span></span> 
- <span data-ttu-id="24dc9-136">月</span><span class="sxs-lookup"><span data-stu-id="24dc9-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-137">間隔</span><span class="sxs-lookup"><span data-stu-id="24dc9-137">-Interval</span></span>
<span data-ttu-id="24dc9-138">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="24dc9-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="24dc9-139">-JobCollectionName</span></span>
<span data-ttu-id="24dc9-140">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="24dc9-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="24dc9-141">-JobName</span></span>
<span data-ttu-id="24dc9-142">指定此 Cmdlet 修改的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="24dc9-142">Specifies the name of the job that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="24dc9-143">-JobState</span></span>
<span data-ttu-id="24dc9-144">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="24dc9-144">Specifies the state of the job.</span></span>
<span data-ttu-id="24dc9-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="24dc9-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24dc9-146">後</span><span class="sxs-lookup"><span data-stu-id="24dc9-146">Enabled</span></span> 
- <span data-ttu-id="24dc9-147">禁止</span><span class="sxs-lookup"><span data-stu-id="24dc9-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24dc9-148">-ResourceGroupName</span></span>
<span data-ttu-id="24dc9-149">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="24dc9-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="24dc9-150">-ServiceBusMessage</span></span>
<span data-ttu-id="24dc9-151">指定服務匯流排主題訊息。</span><span class="sxs-lookup"><span data-stu-id="24dc9-151">Specifies a service bus topic message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="24dc9-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="24dc9-153">指定服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="24dc9-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="24dc9-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="24dc9-155">指定共用的 access 簽名金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="24dc9-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="24dc9-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="24dc9-157">指定共用的存取簽名金鑰值。</span><span class="sxs-lookup"><span data-stu-id="24dc9-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="24dc9-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="24dc9-159">指定服務匯流排主題路徑。</span><span class="sxs-lookup"><span data-stu-id="24dc9-159">Specifies a service bus topic path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="24dc9-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="24dc9-161">指定服務匯流排傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="24dc9-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="24dc9-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="24dc9-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24dc9-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="24dc9-163">NetMessaging</span></span>
- <span data-ttu-id="24dc9-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="24dc9-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="24dc9-165">-StartTime</span></span>
<span data-ttu-id="24dc9-166">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="24dc9-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-167">-確認</span><span class="sxs-lookup"><span data-stu-id="24dc9-167">-Confirm</span></span>
<span data-ttu-id="24dc9-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24dc9-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24dc9-169">-WhatIf</span></span>
<span data-ttu-id="24dc9-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24dc9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24dc9-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24dc9-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24dc9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24dc9-172">CommonParameters</span></span>
<span data-ttu-id="24dc9-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24dc9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24dc9-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24dc9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24dc9-175">輸入</span><span class="sxs-lookup"><span data-stu-id="24dc9-175">INPUTS</span></span>

### <span data-ttu-id="24dc9-176">所有</span><span class="sxs-lookup"><span data-stu-id="24dc9-176">None</span></span>
<span data-ttu-id="24dc9-177">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="24dc9-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24dc9-178">輸出</span><span class="sxs-lookup"><span data-stu-id="24dc9-178">OUTPUTS</span></span>

### <span data-ttu-id="24dc9-179">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24dc9-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="24dc9-180">筆記</span><span class="sxs-lookup"><span data-stu-id="24dc9-180">NOTES</span></span>

## <span data-ttu-id="24dc9-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="24dc9-181">RELATED LINKS</span></span>

[<span data-ttu-id="24dc9-182">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="24dc9-183">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="24dc9-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="24dc9-184">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="24dc9-185">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="24dc9-186">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="24dc9-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="24dc9-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="24dc9-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="24dc9-189">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-189">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="24dc9-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="24dc9-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


