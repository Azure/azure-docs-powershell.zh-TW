---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: bbc2661f585dacc5537583d8282c76e6fdcd7562
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624991"
---
# <span data-ttu-id="73ddb-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="73ddb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="73ddb-103">修改服務匯流排佇列作業。</span><span class="sxs-lookup"><span data-stu-id="73ddb-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73ddb-104">句法</span><span class="sxs-lookup"><span data-stu-id="73ddb-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ddb-105">說明</span><span class="sxs-lookup"><span data-stu-id="73ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="73ddb-106">**AzureRmSchedulerServiceBusQueueJob** Cmdlet 會修改 Azure 排程器中的服務匯流排佇列作業。</span><span class="sxs-lookup"><span data-stu-id="73ddb-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="73ddb-107">這個 Cmdlet 支援以 *ErrorActionType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="73ddb-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="73ddb-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="73ddb-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="73ddb-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="73ddb-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73ddb-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="73ddb-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73ddb-111">示例</span><span class="sxs-lookup"><span data-stu-id="73ddb-111">EXAMPLES</span></span>

## <span data-ttu-id="73ddb-112">參數</span><span class="sxs-lookup"><span data-stu-id="73ddb-112">PARAMETERS</span></span>

### <span data-ttu-id="73ddb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ddb-113">-DefaultProfile</span></span>
<span data-ttu-id="73ddb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73ddb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73ddb-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="73ddb-115">-EndTime</span></span>
<span data-ttu-id="73ddb-116">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="73ddb-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="73ddb-117">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ddb-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="73ddb-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="73ddb-118">-ErrorActionType</span></span>
<span data-ttu-id="73ddb-119">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="73ddb-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="73ddb-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="73ddb-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73ddb-121">Http</span><span class="sxs-lookup"><span data-stu-id="73ddb-121">Http</span></span> 
- <span data-ttu-id="73ddb-122">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="73ddb-122">Https</span></span> 
- <span data-ttu-id="73ddb-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="73ddb-123">StorageQueue</span></span> 
- <span data-ttu-id="73ddb-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="73ddb-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="73ddb-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="73ddb-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="73ddb-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="73ddb-126">-ExecutionCount</span></span>
<span data-ttu-id="73ddb-127">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="73ddb-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="73ddb-128">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="73ddb-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="73ddb-129">頻率</span><span class="sxs-lookup"><span data-stu-id="73ddb-129">-Frequency</span></span>
<span data-ttu-id="73ddb-130">指定作業的頻率。</span><span class="sxs-lookup"><span data-stu-id="73ddb-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="73ddb-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="73ddb-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73ddb-132">數</span><span class="sxs-lookup"><span data-stu-id="73ddb-132">Minute</span></span> 
- <span data-ttu-id="73ddb-133">每</span><span class="sxs-lookup"><span data-stu-id="73ddb-133">Hour</span></span> 
- <span data-ttu-id="73ddb-134">之內</span><span class="sxs-lookup"><span data-stu-id="73ddb-134">Day</span></span> 
- <span data-ttu-id="73ddb-135">周</span><span class="sxs-lookup"><span data-stu-id="73ddb-135">Week</span></span> 
- <span data-ttu-id="73ddb-136">月</span><span class="sxs-lookup"><span data-stu-id="73ddb-136">Month</span></span>

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

### <span data-ttu-id="73ddb-137">間隔</span><span class="sxs-lookup"><span data-stu-id="73ddb-137">-Interval</span></span>
<span data-ttu-id="73ddb-138">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="73ddb-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="73ddb-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="73ddb-139">-JobCollectionName</span></span>
<span data-ttu-id="73ddb-140">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="73ddb-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="73ddb-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="73ddb-141">-JobName</span></span>
<span data-ttu-id="73ddb-142">指定此 Cmdlet 修改的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="73ddb-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="73ddb-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="73ddb-143">-JobState</span></span>
<span data-ttu-id="73ddb-144">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="73ddb-144">Specifies the state of the job.</span></span>
<span data-ttu-id="73ddb-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="73ddb-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73ddb-146">後</span><span class="sxs-lookup"><span data-stu-id="73ddb-146">Enabled</span></span> 
- <span data-ttu-id="73ddb-147">禁止</span><span class="sxs-lookup"><span data-stu-id="73ddb-147">Disabled</span></span>

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

### <span data-ttu-id="73ddb-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ddb-148">-ResourceGroupName</span></span>
<span data-ttu-id="73ddb-149">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="73ddb-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="73ddb-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="73ddb-150">-ServiceBusMessage</span></span>
<span data-ttu-id="73ddb-151">指定服務匯流排佇列訊息。</span><span class="sxs-lookup"><span data-stu-id="73ddb-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="73ddb-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="73ddb-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="73ddb-153">指定服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="73ddb-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="73ddb-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="73ddb-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="73ddb-155">指定服務匯流排佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="73ddb-155">Specifies a service bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ddb-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="73ddb-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="73ddb-157">指定共用的 access 簽名金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="73ddb-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="73ddb-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="73ddb-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="73ddb-159">指定共用的存取簽名金鑰值。</span><span class="sxs-lookup"><span data-stu-id="73ddb-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="73ddb-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="73ddb-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="73ddb-161">指定服務匯流排傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="73ddb-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="73ddb-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="73ddb-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73ddb-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="73ddb-163">NetMessaging</span></span> 
- <span data-ttu-id="73ddb-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="73ddb-164">AMQP</span></span>

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

### <span data-ttu-id="73ddb-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="73ddb-165">-StartTime</span></span>
<span data-ttu-id="73ddb-166">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="73ddb-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="73ddb-167">-確認</span><span class="sxs-lookup"><span data-stu-id="73ddb-167">-Confirm</span></span>
<span data-ttu-id="73ddb-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ddb-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ddb-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ddb-169">-WhatIf</span></span>
<span data-ttu-id="73ddb-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73ddb-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ddb-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ddb-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ddb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ddb-172">CommonParameters</span></span>
<span data-ttu-id="73ddb-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73ddb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ddb-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73ddb-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ddb-175">輸入</span><span class="sxs-lookup"><span data-stu-id="73ddb-175">INPUTS</span></span>

### <span data-ttu-id="73ddb-176">所有</span><span class="sxs-lookup"><span data-stu-id="73ddb-176">None</span></span>
<span data-ttu-id="73ddb-177">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="73ddb-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73ddb-178">輸出</span><span class="sxs-lookup"><span data-stu-id="73ddb-178">OUTPUTS</span></span>

### <span data-ttu-id="73ddb-179">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="73ddb-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="73ddb-180">筆記</span><span class="sxs-lookup"><span data-stu-id="73ddb-180">NOTES</span></span>

## <span data-ttu-id="73ddb-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="73ddb-181">RELATED LINKS</span></span>

[<span data-ttu-id="73ddb-182">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="73ddb-183">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="73ddb-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="73ddb-184">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="73ddb-185">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="73ddb-186">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="73ddb-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="73ddb-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="73ddb-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="73ddb-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="73ddb-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="73ddb-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


