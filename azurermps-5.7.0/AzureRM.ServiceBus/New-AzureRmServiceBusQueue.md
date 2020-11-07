---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624664"
---
# <span data-ttu-id="a547b-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a547b-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="a547b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a547b-102">SYNOPSIS</span></span>
<span data-ttu-id="a547b-103">在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="a547b-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a547b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a547b-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a547b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a547b-105">DESCRIPTION</span></span>
<span data-ttu-id="a547b-106">**新的-AzureRmServiceBusQueue** Cmdlet 會在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="a547b-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a547b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a547b-107">EXAMPLES</span></span>

### <span data-ttu-id="a547b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a547b-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="a547b-109">`SB-Queue_exampl1`在指定的服務匯流排命名空間中建立新的服務匯流排佇列 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="a547b-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a547b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a547b-110">PARAMETERS</span></span>

### <span data-ttu-id="a547b-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="a547b-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="a547b-112">指定將自動刪除佇列之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="a547b-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="a547b-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="a547b-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="a547b-114">-確認</span><span class="sxs-lookup"><span data-stu-id="a547b-114">-Confirm</span></span>
<span data-ttu-id="a547b-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a547b-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="a547b-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="a547b-117">郵件到期時的死字母</span><span class="sxs-lookup"><span data-stu-id="a547b-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="a547b-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="a547b-119">Timespan 到 [即時] 值。</span><span class="sxs-lookup"><span data-stu-id="a547b-119">Timespan to live value.</span></span>
<span data-ttu-id="a547b-120">這是郵件到期後的持續時間，從郵件傳送到服務匯流排的那一段開始。</span><span class="sxs-lookup"><span data-stu-id="a547b-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="a547b-121">這是未在郵件本身設定 TimeToLive 時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="a547b-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="a547b-122">標準 = Timespan.zero. Max 和 Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="a547b-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="a547b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a547b-123">-DefaultProfile</span></span>
<span data-ttu-id="a547b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a547b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a547b-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="a547b-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="a547b-126">指定重複檢測歷程記錄時間視窗， [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat 會定義重複偵測歷程記錄的持續時間。</span><span class="sxs-lookup"><span data-stu-id="a547b-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="a547b-127">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="a547b-127">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="a547b-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="a547b-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="a547b-129">啟用成批次工作-值，指出是否已啟用伺服器端批次作業</span><span class="sxs-lookup"><span data-stu-id="a547b-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="a547b-130">-EnableExpress</span></span>
<span data-ttu-id="a547b-131">EnableExpress-一個指示是否已啟用快速實體的值。</span><span class="sxs-lookup"><span data-stu-id="a547b-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="a547b-132">快速佇列會將郵件暫時儲存在記憶體中，然後再將它寫入持久性儲存。</span><span class="sxs-lookup"><span data-stu-id="a547b-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a547b-133">-EnablePartitioning</span></span>
<span data-ttu-id="a547b-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a547b-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="a547b-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="a547b-136">[佇列]/[主題名稱]，轉寄死信訊息</span><span class="sxs-lookup"><span data-stu-id="a547b-136">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="a547b-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="a547b-137">-ForwardTo</span></span>
<span data-ttu-id="a547b-138">[佇列]/[主題名稱] 來轉寄郵件</span><span class="sxs-lookup"><span data-stu-id="a547b-138">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="a547b-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="a547b-139">-LockDuration</span></span>
<span data-ttu-id="a547b-140">鎖定持續時間</span><span class="sxs-lookup"><span data-stu-id="a547b-140">Lock Duration</span></span>

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

### <span data-ttu-id="a547b-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="a547b-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="a547b-142">MaxDeliveryCount-最大傳送計數。</span><span class="sxs-lookup"><span data-stu-id="a547b-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="a547b-143">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="a547b-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a547b-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="a547b-145">MaxSizeInMegabytes-佇列的最大大小（mb），這是指派給佇列的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="a547b-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="a547b-146">-MessageCount</span></span>
<span data-ttu-id="a547b-147">MessageCount-佇列中的郵件數目</span><span class="sxs-lookup"><span data-stu-id="a547b-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="a547b-148">-Name</span></span>
<span data-ttu-id="a547b-149">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="a547b-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-150">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a547b-150">-Namespace</span></span>
<span data-ttu-id="a547b-151">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a547b-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="a547b-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="a547b-153">RequiresDuplicateDetection-一個值，指出佇列是否支援會話概念</span><span class="sxs-lookup"><span data-stu-id="a547b-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="a547b-154">-RequiresSession</span></span>
<span data-ttu-id="a547b-155">RequiresSession-此值指出此佇列是否需要重複偵測</span><span class="sxs-lookup"><span data-stu-id="a547b-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a547b-156">-ResourceGroupName</span></span>
<span data-ttu-id="a547b-157">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a547b-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a547b-158">-SizeInBytes</span></span>
<span data-ttu-id="a547b-159">SizeInBytes-佇列大小（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="a547b-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a547b-160">-WhatIf</span></span>
<span data-ttu-id="a547b-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a547b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a547b-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a547b-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a547b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a547b-163">CommonParameters</span></span>
<span data-ttu-id="a547b-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a547b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a547b-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a547b-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a547b-166">輸入</span><span class="sxs-lookup"><span data-stu-id="a547b-166">INPUTS</span></span>

### <span data-ttu-id="a547b-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a547b-167">-ResourceGroup</span></span>
 <span data-ttu-id="a547b-168">System.object</span><span class="sxs-lookup"><span data-stu-id="a547b-168">System.String</span></span>

### <span data-ttu-id="a547b-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a547b-169">-NamespaceName</span></span>
 <span data-ttu-id="a547b-170">System.object</span><span class="sxs-lookup"><span data-stu-id="a547b-170">System.String</span></span>

### <span data-ttu-id="a547b-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="a547b-171">-QueueName</span></span>
 <span data-ttu-id="a547b-172">System.object</span><span class="sxs-lookup"><span data-stu-id="a547b-172">System.String</span></span>

### <span data-ttu-id="a547b-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="a547b-173">-EnablePartitioning</span></span>
 <span data-ttu-id="a547b-174">System.object？</span><span class="sxs-lookup"><span data-stu-id="a547b-174">System.Boolean?</span></span>


## <span data-ttu-id="a547b-175">輸出</span><span class="sxs-lookup"><span data-stu-id="a547b-175">OUTPUTS</span></span>

### <span data-ttu-id="a547b-176">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a547b-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="a547b-177">筆記</span><span class="sxs-lookup"><span data-stu-id="a547b-177">NOTES</span></span>

## <span data-ttu-id="a547b-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="a547b-178">RELATED LINKS</span></span>
