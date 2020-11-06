---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: b9ad7c729395115845349c1e39f8d90666a4fcb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620628"
---
# <span data-ttu-id="277bf-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="277bf-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="277bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="277bf-102">SYNOPSIS</span></span>
<span data-ttu-id="277bf-103">在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="277bf-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="277bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="277bf-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="277bf-105">DESCRIPTION</span></span>
<span data-ttu-id="277bf-106">**新的-AzServiceBusQueue** Cmdlet 會在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="277bf-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="277bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="277bf-107">EXAMPLES</span></span>

### <span data-ttu-id="277bf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="277bf-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="277bf-109">`SB-Queue_example1`在指定的服務匯流排命名空間中建立新的服務匯流排佇列 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="277bf-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="277bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="277bf-110">PARAMETERS</span></span>

### <span data-ttu-id="277bf-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="277bf-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="277bf-112">指定將自動刪除佇列之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="277bf-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="277bf-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="277bf-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="277bf-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="277bf-115">郵件到期時的死字母</span><span class="sxs-lookup"><span data-stu-id="277bf-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="277bf-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="277bf-117">Timespan 到 [即時] 值。</span><span class="sxs-lookup"><span data-stu-id="277bf-117">Timespan to live value.</span></span>
<span data-ttu-id="277bf-118">這是郵件到期後的持續時間，從郵件傳送到服務匯流排的那一段開始。</span><span class="sxs-lookup"><span data-stu-id="277bf-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="277bf-119">這是未在郵件本身設定 TimeToLive 時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="277bf-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="277bf-120">標準 = Timespan.zero. Max 和 Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="277bf-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277bf-121">-DefaultProfile</span></span>
<span data-ttu-id="277bf-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="277bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="277bf-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="277bf-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="277bf-124">指定重複檢測歷程記錄時間視窗， [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat 會定義重複偵測歷程記錄的持續時間。</span><span class="sxs-lookup"><span data-stu-id="277bf-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="277bf-125">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="277bf-125">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="277bf-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="277bf-127">啟用成批次工作-值，指出是否已啟用伺服器端批次作業</span><span class="sxs-lookup"><span data-stu-id="277bf-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="277bf-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="277bf-128">-EnableExpress</span></span>
<span data-ttu-id="277bf-129">EnableExpress-一個指示是否已啟用快速實體的值。</span><span class="sxs-lookup"><span data-stu-id="277bf-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="277bf-130">快速佇列會將郵件暫時儲存在記憶體中，然後再將它寫入持久性儲存。</span><span class="sxs-lookup"><span data-stu-id="277bf-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="277bf-131">-EnablePartitioning</span></span>
<span data-ttu-id="277bf-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="277bf-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="277bf-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="277bf-134">[佇列]/[主題名稱]，轉寄死信訊息</span><span class="sxs-lookup"><span data-stu-id="277bf-134">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="277bf-135">-ForwardTo</span></span>
<span data-ttu-id="277bf-136">[佇列]/[主題名稱] 來轉寄郵件</span><span class="sxs-lookup"><span data-stu-id="277bf-136">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="277bf-137">-LockDuration</span></span>
<span data-ttu-id="277bf-138">鎖定持續時間</span><span class="sxs-lookup"><span data-stu-id="277bf-138">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="277bf-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="277bf-140">MaxDeliveryCount-最大傳送計數。</span><span class="sxs-lookup"><span data-stu-id="277bf-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="277bf-141">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="277bf-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="277bf-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="277bf-143">MaxSizeInMegabytes-佇列的最大大小（mb），這是指派給佇列的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="277bf-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="277bf-144">-MessageCount</span></span>
<span data-ttu-id="277bf-145">MessageCount-佇列中的郵件數目</span><span class="sxs-lookup"><span data-stu-id="277bf-145">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="277bf-146">-Name</span></span>
<span data-ttu-id="277bf-147">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="277bf-147">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-148">-命名空間</span><span class="sxs-lookup"><span data-stu-id="277bf-148">-Namespace</span></span>
<span data-ttu-id="277bf-149">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="277bf-149">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="277bf-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="277bf-151">RequiresDuplicateDetection-一個值，指出佇列是否支援會話概念</span><span class="sxs-lookup"><span data-stu-id="277bf-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="277bf-152">-RequiresSession</span></span>
<span data-ttu-id="277bf-153">RequiresSession-此值指出此佇列是否需要重複偵測</span><span class="sxs-lookup"><span data-stu-id="277bf-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277bf-154">-ResourceGroupName</span></span>
<span data-ttu-id="277bf-155">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="277bf-155">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="277bf-156">-SizeInBytes</span></span>
<span data-ttu-id="277bf-157">SizeInBytes-佇列大小（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="277bf-157">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-158">-確認</span><span class="sxs-lookup"><span data-stu-id="277bf-158">-Confirm</span></span>
<span data-ttu-id="277bf-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="277bf-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277bf-160">-WhatIf</span></span>
<span data-ttu-id="277bf-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="277bf-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277bf-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="277bf-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277bf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277bf-163">CommonParameters</span></span>
<span data-ttu-id="277bf-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="277bf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277bf-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="277bf-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277bf-166">輸入</span><span class="sxs-lookup"><span data-stu-id="277bf-166">INPUTS</span></span>

### <span data-ttu-id="277bf-167">System.object</span><span class="sxs-lookup"><span data-stu-id="277bf-167">System.String</span></span>

### <span data-ttu-id="277bf-168">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="277bf-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="277bf-169">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="277bf-169">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="277bf-170">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="277bf-170">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="277bf-171">輸出</span><span class="sxs-lookup"><span data-stu-id="277bf-171">OUTPUTS</span></span>

### <span data-ttu-id="277bf-172">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="277bf-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="277bf-173">筆記</span><span class="sxs-lookup"><span data-stu-id="277bf-173">NOTES</span></span>

## <span data-ttu-id="277bf-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="277bf-174">RELATED LINKS</span></span>
