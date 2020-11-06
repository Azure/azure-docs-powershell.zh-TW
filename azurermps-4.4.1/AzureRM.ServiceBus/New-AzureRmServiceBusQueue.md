---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446664"
---
# <span data-ttu-id="f556f-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f556f-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="f556f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f556f-102">SYNOPSIS</span></span>
<span data-ttu-id="f556f-103">在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="f556f-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f556f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f556f-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f556f-105">說明</span><span class="sxs-lookup"><span data-stu-id="f556f-105">DESCRIPTION</span></span>
<span data-ttu-id="f556f-106">**新的-AzureRmServiceBusQueue** Cmdlet 會在指定的服務匯流排命名空間中建立服務匯流排佇列。</span><span class="sxs-lookup"><span data-stu-id="f556f-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f556f-107">示例</span><span class="sxs-lookup"><span data-stu-id="f556f-107">EXAMPLES</span></span>

### <span data-ttu-id="f556f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f556f-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="f556f-109">`SB-Queue_exampl1`在指定的服務匯流排命名空間中建立新的服務匯流排佇列 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="f556f-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f556f-110">參數</span><span class="sxs-lookup"><span data-stu-id="f556f-110">PARAMETERS</span></span>

### <span data-ttu-id="f556f-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="f556f-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="f556f-112">指定將自動刪除佇列之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="f556f-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="f556f-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="f556f-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="f556f-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="f556f-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="f556f-115">指定郵件在到期時是否 deadlettered。</span><span class="sxs-lookup"><span data-stu-id="f556f-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="f556f-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="f556f-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="f556f-117">指定預設的訊息存留時間 (TTL) 。</span><span class="sxs-lookup"><span data-stu-id="f556f-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="f556f-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f556f-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="f556f-119">指定重複檢測歷程記錄時間視窗， [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat 會定義重複偵測歷程記錄的持續時間。</span><span class="sxs-lookup"><span data-stu-id="f556f-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="f556f-120">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="f556f-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="f556f-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="f556f-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="f556f-122">指定是否已啟用伺服器端批次作業。</span><span class="sxs-lookup"><span data-stu-id="f556f-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="f556f-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="f556f-123">-EnableExpress</span></span>
<span data-ttu-id="f556f-124">指定是否已啟用快速實體。</span><span class="sxs-lookup"><span data-stu-id="f556f-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="f556f-125">快速佇列會將郵件暫時儲存在記憶體中，然後再將它寫入持久性儲存。</span><span class="sxs-lookup"><span data-stu-id="f556f-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="f556f-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="f556f-126">-EnablePartitioning</span></span>
<span data-ttu-id="f556f-127">指定是否已啟用 EnablePartitioning。</span><span class="sxs-lookup"><span data-stu-id="f556f-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556f-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="f556f-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="f556f-129">指定是否可匿名存取該訊息。</span><span class="sxs-lookup"><span data-stu-id="f556f-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="f556f-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="f556f-130">-LockDuration</span></span>
<span data-ttu-id="f556f-131">指定鎖定持續時間。</span><span class="sxs-lookup"><span data-stu-id="f556f-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="f556f-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="f556f-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="f556f-133">指定最大傳送計數。</span><span class="sxs-lookup"><span data-stu-id="f556f-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="f556f-134">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="f556f-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="f556f-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f556f-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="f556f-136">指定佇列的最大大小（mb），這是指派給佇列的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="f556f-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="f556f-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="f556f-137">-MessageCount</span></span>
<span data-ttu-id="f556f-138">指定佇列中的郵件數目。</span><span class="sxs-lookup"><span data-stu-id="f556f-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="f556f-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="f556f-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="f556f-140">指定佇列是否需要重複偵測。</span><span class="sxs-lookup"><span data-stu-id="f556f-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="f556f-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="f556f-141">-RequiresSession</span></span>
<span data-ttu-id="f556f-142">指定此佇列是否支援會話。</span><span class="sxs-lookup"><span data-stu-id="f556f-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="f556f-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="f556f-143">-SizeInBytes</span></span>
<span data-ttu-id="f556f-144">佇列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f556f-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="f556f-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f556f-145">-Confirm</span></span>
<span data-ttu-id="f556f-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f556f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f556f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f556f-147">-WhatIf</span></span>
<span data-ttu-id="f556f-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f556f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f556f-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f556f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f556f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f556f-150">-DefaultProfile</span></span>
<span data-ttu-id="f556f-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f556f-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f556f-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="f556f-152">-Name</span></span>
<span data-ttu-id="f556f-153">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="f556f-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556f-154">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f556f-154">-Namespace</span></span>
<span data-ttu-id="f556f-155">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f556f-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f556f-156">-ResourceGroupName</span></span>
<span data-ttu-id="f556f-157">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f556f-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f556f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f556f-158">CommonParameters</span></span>
<span data-ttu-id="f556f-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f556f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f556f-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f556f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f556f-161">輸入</span><span class="sxs-lookup"><span data-stu-id="f556f-161">INPUTS</span></span>

### <span data-ttu-id="f556f-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f556f-162">-ResourceGroup</span></span>
 <span data-ttu-id="f556f-163">System.object</span><span class="sxs-lookup"><span data-stu-id="f556f-163">System.String</span></span>

### <span data-ttu-id="f556f-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f556f-164">-NamespaceName</span></span>
 <span data-ttu-id="f556f-165">System.object</span><span class="sxs-lookup"><span data-stu-id="f556f-165">System.String</span></span>

### <span data-ttu-id="f556f-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="f556f-166">-QueueName</span></span>
 <span data-ttu-id="f556f-167">System.object</span><span class="sxs-lookup"><span data-stu-id="f556f-167">System.String</span></span>

### <span data-ttu-id="f556f-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="f556f-168">-EnablePartitioning</span></span>
 <span data-ttu-id="f556f-169">System.object？</span><span class="sxs-lookup"><span data-stu-id="f556f-169">System.Boolean?</span></span>

## <span data-ttu-id="f556f-170">輸出</span><span class="sxs-lookup"><span data-stu-id="f556f-170">OUTPUTS</span></span>

### <span data-ttu-id="f556f-171">QueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f556f-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="f556f-172">名稱： SB-Queue_exampl1 位置：西 US LockDuration： AccessedAt： AutoDeleteOnIdle：10675199.02：48： 05.4775807 EntityAvailabilityStatus： CreatedAt： 1/20/2017 2:51:36 AM DefaultMessageTimeToLive：10675199.02：48： 05.4775807 DuplicateDetectionHistoryTimeWindow： EnableBatchedOperations： DeadLetteringOnMessageExpiration： EnableExpress： EnablePartitioning： 16384 IsAnonymousAccessible： MaxDeliveryCount： MaxSizeInMegabytes： MessageCount： false CountDetails： RequiresDuplicateDetection： RequiresSession： False SizeInBytes： false SupportOrdering： 1/20/2017 2:51:37 AM</span><span class="sxs-lookup"><span data-stu-id="f556f-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="f556f-173">筆記</span><span class="sxs-lookup"><span data-stu-id="f556f-173">NOTES</span></span>

## <span data-ttu-id="f556f-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="f556f-174">RELATED LINKS</span></span>

