---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624663"
---
# <span data-ttu-id="17221-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="17221-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="17221-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17221-102">SYNOPSIS</span></span>
<span data-ttu-id="17221-103">建立指定服務匯流排主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="17221-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17221-104">句法</span><span class="sxs-lookup"><span data-stu-id="17221-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17221-105">說明</span><span class="sxs-lookup"><span data-stu-id="17221-105">DESCRIPTION</span></span>
<span data-ttu-id="17221-106">**新的-AzureRmServiceBusSubscription** Cmdlet 會在指定的服務匯流排主題中建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="17221-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="17221-107">示例</span><span class="sxs-lookup"><span data-stu-id="17221-107">EXAMPLES</span></span>

### <span data-ttu-id="17221-108">範例1</span><span class="sxs-lookup"><span data-stu-id="17221-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="17221-109">`SB-TopicSubscription-Example1`針對指定的服務匯流排主題建立訂閱 `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="17221-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="17221-110">參數</span><span class="sxs-lookup"><span data-stu-id="17221-110">PARAMETERS</span></span>

### <span data-ttu-id="17221-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="17221-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="17221-112">指定將自動刪除訂閱之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="17221-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="17221-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="17221-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="17221-114">-確認</span><span class="sxs-lookup"><span data-stu-id="17221-114">-Confirm</span></span>
<span data-ttu-id="17221-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17221-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17221-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="17221-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="17221-117">指示訂閱在篩選評估例外狀況上是否有死信支援的值。</span><span class="sxs-lookup"><span data-stu-id="17221-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="17221-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="17221-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="17221-119">郵件到期時的死字母</span><span class="sxs-lookup"><span data-stu-id="17221-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="17221-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="17221-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="17221-121">Timespan 到 [即時] 值。</span><span class="sxs-lookup"><span data-stu-id="17221-121">Timespan to live value.</span></span>
<span data-ttu-id="17221-122">這是郵件到期後的持續時間，從郵件傳送到服務匯流排的那一段開始。</span><span class="sxs-lookup"><span data-stu-id="17221-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="17221-123">這是未在郵件本身設定 TimeToLive 時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="17221-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="17221-124">標準 = Timespan.zero. Max 和 Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="17221-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="17221-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17221-125">-DefaultProfile</span></span>
<span data-ttu-id="17221-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17221-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17221-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="17221-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="17221-128">啟用成批次工作-值，指出是否已啟用伺服器端批次作業</span><span class="sxs-lookup"><span data-stu-id="17221-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="17221-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="17221-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="17221-130">[佇列]/[主題名稱]，轉寄死信訊息</span><span class="sxs-lookup"><span data-stu-id="17221-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="17221-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="17221-131">-ForwardTo</span></span>
<span data-ttu-id="17221-132">[佇列]/[主題名稱] 來轉寄郵件</span><span class="sxs-lookup"><span data-stu-id="17221-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="17221-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="17221-133">-LockDuration</span></span>
<span data-ttu-id="17221-134">鎖定持續時間</span><span class="sxs-lookup"><span data-stu-id="17221-134">Lock Duration</span></span>

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

### <span data-ttu-id="17221-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="17221-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="17221-136">MaxDeliveryCount-最大傳送計數。</span><span class="sxs-lookup"><span data-stu-id="17221-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="17221-137">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="17221-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="17221-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="17221-138">-Name</span></span>
<span data-ttu-id="17221-139">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="17221-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17221-140">-命名空間</span><span class="sxs-lookup"><span data-stu-id="17221-140">-Namespace</span></span>
<span data-ttu-id="17221-141">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="17221-141">Namespace Name</span></span>

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

### <span data-ttu-id="17221-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="17221-142">-RequiresSession</span></span>
<span data-ttu-id="17221-143">RequiresSession-指出此佇列是否需要重複偵測的值。</span><span class="sxs-lookup"><span data-stu-id="17221-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="17221-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17221-144">-ResourceGroupName</span></span>
<span data-ttu-id="17221-145">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="17221-145">The name of the resource group</span></span>

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

### <span data-ttu-id="17221-146">-主題</span><span class="sxs-lookup"><span data-stu-id="17221-146">-Topic</span></span>
<span data-ttu-id="17221-147">主題名稱</span><span class="sxs-lookup"><span data-stu-id="17221-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17221-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17221-148">-WhatIf</span></span>
<span data-ttu-id="17221-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17221-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17221-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17221-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17221-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17221-151">CommonParameters</span></span>
<span data-ttu-id="17221-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17221-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="17221-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17221-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17221-154">輸入</span><span class="sxs-lookup"><span data-stu-id="17221-154">INPUTS</span></span>

### <span data-ttu-id="17221-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17221-155">-ResourceGroup</span></span>
 <span data-ttu-id="17221-156">System.object</span><span class="sxs-lookup"><span data-stu-id="17221-156">System.String</span></span>
 

### <span data-ttu-id="17221-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="17221-157">-NamespaceName</span></span>
 <span data-ttu-id="17221-158">System.object</span><span class="sxs-lookup"><span data-stu-id="17221-158">System.String</span></span>
 

### <span data-ttu-id="17221-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="17221-159">-TopicName</span></span>
 <span data-ttu-id="17221-160">System.object</span><span class="sxs-lookup"><span data-stu-id="17221-160">System.String</span></span>
 

### <span data-ttu-id="17221-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="17221-161">-SubscriptionName</span></span>
 <span data-ttu-id="17221-162">System.object</span><span class="sxs-lookup"><span data-stu-id="17221-162">System.String</span></span>


## <span data-ttu-id="17221-163">輸出</span><span class="sxs-lookup"><span data-stu-id="17221-163">OUTPUTS</span></span>

### <span data-ttu-id="17221-164">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="17221-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="17221-165">筆記</span><span class="sxs-lookup"><span data-stu-id="17221-165">NOTES</span></span>

## <span data-ttu-id="17221-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="17221-166">RELATED LINKS</span></span>
