---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623587"
---
# <span data-ttu-id="c8842-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c8842-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="c8842-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8842-102">SYNOPSIS</span></span>
<span data-ttu-id="c8842-103">修改儲存佇列作業。</span><span class="sxs-lookup"><span data-stu-id="c8842-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8842-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8842-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8842-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8842-105">DESCRIPTION</span></span>
<span data-ttu-id="c8842-106">**AzureRmSchedulerStorageQueueJob** Cmdlet 會修改 Azure 排程器中的儲存佇列作業。</span><span class="sxs-lookup"><span data-stu-id="c8842-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="c8842-107">這個 Cmdlet 支援以 *ErrorActionType* 參數為基礎的動態參數。</span><span class="sxs-lookup"><span data-stu-id="c8842-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="c8842-108">動態參數會根據其他參數值提供。</span><span class="sxs-lookup"><span data-stu-id="c8842-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="c8842-109">若要在指定其他參數之後發現動態參數的名稱，請輸入連字號 ( ) ，然後重複按 Tab 鍵，以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="c8842-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c8842-110">如果您省略必要的參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="c8842-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c8842-111">示例</span><span class="sxs-lookup"><span data-stu-id="c8842-111">EXAMPLES</span></span>

## <span data-ttu-id="c8842-112">參數</span><span class="sxs-lookup"><span data-stu-id="c8842-112">PARAMETERS</span></span>

### <span data-ttu-id="c8842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8842-113">-DefaultProfile</span></span>
<span data-ttu-id="c8842-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8842-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8842-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c8842-115">-EndTime</span></span>
<span data-ttu-id="c8842-116">指定作業的結束時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="c8842-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="c8842-117">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8842-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c8842-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="c8842-118">-ErrorActionType</span></span>
<span data-ttu-id="c8842-119">指定作業的錯誤動作設定。</span><span class="sxs-lookup"><span data-stu-id="c8842-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="c8842-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8842-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8842-121">Http</span><span class="sxs-lookup"><span data-stu-id="c8842-121">Http</span></span> 
- <span data-ttu-id="c8842-122">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="c8842-122">Https</span></span> 
- <span data-ttu-id="c8842-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="c8842-123">StorageQueue</span></span> 
- <span data-ttu-id="c8842-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c8842-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="c8842-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c8842-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="c8842-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c8842-126">-ExecutionCount</span></span>
<span data-ttu-id="c8842-127">指定作業執行的次數。</span><span class="sxs-lookup"><span data-stu-id="c8842-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="c8842-128">根據預設，作業會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="c8842-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="c8842-129">頻率</span><span class="sxs-lookup"><span data-stu-id="c8842-129">-Frequency</span></span>
<span data-ttu-id="c8842-130">指定作業的頻率。</span><span class="sxs-lookup"><span data-stu-id="c8842-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="c8842-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8842-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8842-132">數</span><span class="sxs-lookup"><span data-stu-id="c8842-132">Minute</span></span> 
- <span data-ttu-id="c8842-133">每</span><span class="sxs-lookup"><span data-stu-id="c8842-133">Hour</span></span> 
- <span data-ttu-id="c8842-134">之內</span><span class="sxs-lookup"><span data-stu-id="c8842-134">Day</span></span> 
- <span data-ttu-id="c8842-135">周</span><span class="sxs-lookup"><span data-stu-id="c8842-135">Week</span></span> 
- <span data-ttu-id="c8842-136">月</span><span class="sxs-lookup"><span data-stu-id="c8842-136">Month</span></span>

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

### <span data-ttu-id="c8842-137">間隔</span><span class="sxs-lookup"><span data-stu-id="c8842-137">-Interval</span></span>
<span data-ttu-id="c8842-138">指定作業的定期間隔。</span><span class="sxs-lookup"><span data-stu-id="c8842-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="c8842-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c8842-139">-JobCollectionName</span></span>
<span data-ttu-id="c8842-140">指定作業所屬作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8842-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="c8842-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="c8842-141">-JobName</span></span>
<span data-ttu-id="c8842-142">指定此 Cmdlet 修改的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="c8842-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c8842-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="c8842-143">-JobState</span></span>
<span data-ttu-id="c8842-144">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8842-144">Specifies the state of the job.</span></span>
<span data-ttu-id="c8842-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8842-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8842-146">後</span><span class="sxs-lookup"><span data-stu-id="c8842-146">Enabled</span></span> 
- <span data-ttu-id="c8842-147">禁止</span><span class="sxs-lookup"><span data-stu-id="c8842-147">Disabled</span></span>

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

### <span data-ttu-id="c8842-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8842-148">-ResourceGroupName</span></span>
<span data-ttu-id="c8842-149">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c8842-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c8842-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c8842-150">-StartTime</span></span>
<span data-ttu-id="c8842-151">指定作業的開始時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="c8842-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="c8842-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="c8842-152">-StorageQueueAccount</span></span>
<span data-ttu-id="c8842-153">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c8842-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8842-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="c8842-154">-StorageQueueMessage</span></span>
<span data-ttu-id="c8842-155">指定 [儲存作業] 的佇列訊息。</span><span class="sxs-lookup"><span data-stu-id="c8842-155">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="c8842-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="c8842-156">-StorageQueueName</span></span>
<span data-ttu-id="c8842-157">指定儲存佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="c8842-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8842-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="c8842-158">-StorageSASToken</span></span>
<span data-ttu-id="c8842-159">指定儲存佇列的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c8842-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8842-160">-確認</span><span class="sxs-lookup"><span data-stu-id="c8842-160">-Confirm</span></span>
<span data-ttu-id="c8842-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8842-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8842-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8842-162">-WhatIf</span></span>
<span data-ttu-id="c8842-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8842-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8842-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8842-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8842-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8842-165">CommonParameters</span></span>
<span data-ttu-id="c8842-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8842-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8842-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8842-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8842-168">輸入</span><span class="sxs-lookup"><span data-stu-id="c8842-168">INPUTS</span></span>

### <span data-ttu-id="c8842-169">所有</span><span class="sxs-lookup"><span data-stu-id="c8842-169">None</span></span>
<span data-ttu-id="c8842-170">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c8842-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8842-171">輸出</span><span class="sxs-lookup"><span data-stu-id="c8842-171">OUTPUTS</span></span>

### <span data-ttu-id="c8842-172">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8842-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c8842-173">筆記</span><span class="sxs-lookup"><span data-stu-id="c8842-173">NOTES</span></span>

## <span data-ttu-id="c8842-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8842-174">RELATED LINKS</span></span>

[<span data-ttu-id="c8842-175">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c8842-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c8842-176">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8842-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8842-177">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c8842-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c8842-178">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c8842-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c8842-179">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c8842-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c8842-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c8842-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c8842-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8842-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8842-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c8842-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c8842-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c8842-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

