---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455608"
---
# <span data-ttu-id="459d2-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="459d2-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="459d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="459d2-102">SYNOPSIS</span></span>
<span data-ttu-id="459d2-103">修改服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="459d2-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="459d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="459d2-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="459d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="459d2-105">DESCRIPTION</span></span>
<span data-ttu-id="459d2-106">**AzureRmSchedulerServiceBusTopicJob** Cmdlet 會修改 Azure 排程器中的服務匯流排主題作業。</span><span class="sxs-lookup"><span data-stu-id="459d2-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="459d2-107">這個 Cmdlet 支援以 *ErrorActionType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="459d2-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="459d2-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="459d2-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="459d2-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="459d2-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="459d2-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="459d2-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="459d2-111">示例</span><span class="sxs-lookup"><span data-stu-id="459d2-111">EXAMPLES</span></span>

## <span data-ttu-id="459d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="459d2-112">PARAMETERS</span></span>

### <span data-ttu-id="459d2-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="459d2-113">-EndTime</span></span>
<span data-ttu-id="459d2-114">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="459d2-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="459d2-115">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="459d2-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="459d2-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="459d2-116">-ErrorActionType</span></span>
<span data-ttu-id="459d2-117">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="459d2-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="459d2-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="459d2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="459d2-119">Http</span><span class="sxs-lookup"><span data-stu-id="459d2-119">Http</span></span> 
- <span data-ttu-id="459d2-120">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="459d2-120">Https</span></span> 
- <span data-ttu-id="459d2-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="459d2-121">StorageQueue</span></span> 
- <span data-ttu-id="459d2-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="459d2-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="459d2-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="459d2-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="459d2-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="459d2-124">-ExecutionCount</span></span>
<span data-ttu-id="459d2-125">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="459d2-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="459d2-126">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="459d2-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="459d2-127">頻率</span><span class="sxs-lookup"><span data-stu-id="459d2-127">-Frequency</span></span>
<span data-ttu-id="459d2-128">指定工作的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="459d2-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="459d2-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="459d2-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="459d2-130">數</span><span class="sxs-lookup"><span data-stu-id="459d2-130">Minute</span></span> 
- <span data-ttu-id="459d2-131">每</span><span class="sxs-lookup"><span data-stu-id="459d2-131">Hour</span></span> 
- <span data-ttu-id="459d2-132">之內</span><span class="sxs-lookup"><span data-stu-id="459d2-132">Day</span></span> 
- <span data-ttu-id="459d2-133">周</span><span class="sxs-lookup"><span data-stu-id="459d2-133">Week</span></span> 
- <span data-ttu-id="459d2-134">月</span><span class="sxs-lookup"><span data-stu-id="459d2-134">Month</span></span>

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

### <span data-ttu-id="459d2-135">間隔</span><span class="sxs-lookup"><span data-stu-id="459d2-135">-Interval</span></span>
<span data-ttu-id="459d2-136">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="459d2-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="459d2-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="459d2-137">-JobCollectionName</span></span>
<span data-ttu-id="459d2-138">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="459d2-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="459d2-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="459d2-139">-JobName</span></span>
<span data-ttu-id="459d2-140">指定此 Cmdlet 修改的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="459d2-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="459d2-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="459d2-141">-JobState</span></span>
<span data-ttu-id="459d2-142">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="459d2-142">Specifies the state of the job.</span></span>
<span data-ttu-id="459d2-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="459d2-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="459d2-144">後</span><span class="sxs-lookup"><span data-stu-id="459d2-144">Enabled</span></span> 
- <span data-ttu-id="459d2-145">禁止</span><span class="sxs-lookup"><span data-stu-id="459d2-145">Disabled</span></span>

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

### <span data-ttu-id="459d2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459d2-146">-ResourceGroupName</span></span>
<span data-ttu-id="459d2-147">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="459d2-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="459d2-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="459d2-148">-ServiceBusMessage</span></span>
<span data-ttu-id="459d2-149">指定服務匯流排主題訊息。</span><span class="sxs-lookup"><span data-stu-id="459d2-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="459d2-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="459d2-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="459d2-151">指定服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="459d2-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="459d2-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="459d2-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="459d2-153">指定共用的 access 簽名金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="459d2-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="459d2-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="459d2-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="459d2-155">指定共用的存取簽名金鑰值。</span><span class="sxs-lookup"><span data-stu-id="459d2-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="459d2-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="459d2-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="459d2-157">指定服務匯流排主題路徑。</span><span class="sxs-lookup"><span data-stu-id="459d2-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="459d2-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="459d2-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="459d2-159">指定服務匯流排傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="459d2-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="459d2-160">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="459d2-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="459d2-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="459d2-161">NetMessaging</span></span>
- <span data-ttu-id="459d2-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="459d2-162">AMQP</span></span>

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

### <span data-ttu-id="459d2-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="459d2-163">-StartTime</span></span>
<span data-ttu-id="459d2-164">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="459d2-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="459d2-165">-確認</span><span class="sxs-lookup"><span data-stu-id="459d2-165">-Confirm</span></span>
<span data-ttu-id="459d2-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="459d2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="459d2-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459d2-167">-WhatIf</span></span>
<span data-ttu-id="459d2-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="459d2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459d2-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="459d2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="459d2-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459d2-170">-DefaultProfile</span></span>
<span data-ttu-id="459d2-171">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="459d2-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="459d2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459d2-172">CommonParameters</span></span>
<span data-ttu-id="459d2-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="459d2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459d2-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="459d2-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459d2-175">輸入</span><span class="sxs-lookup"><span data-stu-id="459d2-175">INPUTS</span></span>

## <span data-ttu-id="459d2-176">輸出</span><span class="sxs-lookup"><span data-stu-id="459d2-176">OUTPUTS</span></span>

### <span data-ttu-id="459d2-177">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="459d2-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="459d2-178">筆記</span><span class="sxs-lookup"><span data-stu-id="459d2-178">NOTES</span></span>

## <span data-ttu-id="459d2-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="459d2-179">RELATED LINKS</span></span>

[<span data-ttu-id="459d2-180">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="459d2-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="459d2-181">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="459d2-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="459d2-182">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="459d2-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="459d2-183">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="459d2-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="459d2-184">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="459d2-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="459d2-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="459d2-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="459d2-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="459d2-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="459d2-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="459d2-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="459d2-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="459d2-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


