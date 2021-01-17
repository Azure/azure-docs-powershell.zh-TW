---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448400"
---
# <span data-ttu-id="679ea-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="679ea-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="679ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="679ea-102">SYNOPSIS</span></span>
<span data-ttu-id="679ea-103">建立指定服務匯流排主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="679ea-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="679ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="679ea-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="679ea-105">DESCRIPTION</span></span>
<span data-ttu-id="679ea-106">**新的-AzServiceBusSubscription** Cmdlet 會在指定的服務匯流排主題中建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="679ea-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="679ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="679ea-107">EXAMPLES</span></span>

### <span data-ttu-id="679ea-108">範例1</span><span class="sxs-lookup"><span data-stu-id="679ea-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="679ea-109">`SB-TopicSubscription-Example1`針對指定的服務匯流排主題建立訂閱 `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="679ea-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="679ea-110">參數</span><span class="sxs-lookup"><span data-stu-id="679ea-110">PARAMETERS</span></span>

### <span data-ttu-id="679ea-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="679ea-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="679ea-112">指定將自動刪除訂閱之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="679ea-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="679ea-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="679ea-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="679ea-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="679ea-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="679ea-115">指示訂閱在篩選評估例外狀況上是否有死信支援的值。</span><span class="sxs-lookup"><span data-stu-id="679ea-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="679ea-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="679ea-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="679ea-117">郵件到期時的死字母</span><span class="sxs-lookup"><span data-stu-id="679ea-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="679ea-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="679ea-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="679ea-119">Timespan 到 [即時] 值。</span><span class="sxs-lookup"><span data-stu-id="679ea-119">Timespan to live value.</span></span>
<span data-ttu-id="679ea-120">這是郵件到期後的持續時間，從郵件傳送到服務匯流排的那一段開始。</span><span class="sxs-lookup"><span data-stu-id="679ea-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="679ea-121">這是未在郵件本身設定 TimeToLive 時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="679ea-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="679ea-122">標準 = Timespan.zero，Max 和 Basic = 14 天</span><span class="sxs-lookup"><span data-stu-id="679ea-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="679ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679ea-123">-DefaultProfile</span></span>
<span data-ttu-id="679ea-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="679ea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679ea-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="679ea-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="679ea-126">啟用成批次工作-值，指出是否已啟用伺服器端批次作業</span><span class="sxs-lookup"><span data-stu-id="679ea-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="679ea-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="679ea-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="679ea-128">[佇列]/[主題名稱]，轉寄死信訊息</span><span class="sxs-lookup"><span data-stu-id="679ea-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="679ea-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="679ea-129">-ForwardTo</span></span>
<span data-ttu-id="679ea-130">[佇列]/[主題名稱] 來轉寄郵件</span><span class="sxs-lookup"><span data-stu-id="679ea-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="679ea-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="679ea-131">-LockDuration</span></span>
<span data-ttu-id="679ea-132">鎖定持續時間</span><span class="sxs-lookup"><span data-stu-id="679ea-132">Lock Duration</span></span>

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

### <span data-ttu-id="679ea-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="679ea-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="679ea-134">MaxDeliveryCount-最大傳送計數。</span><span class="sxs-lookup"><span data-stu-id="679ea-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="679ea-135">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="679ea-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="679ea-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="679ea-136">-Name</span></span>
<span data-ttu-id="679ea-137">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="679ea-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="679ea-138">-命名空間</span><span class="sxs-lookup"><span data-stu-id="679ea-138">-Namespace</span></span>
<span data-ttu-id="679ea-139">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="679ea-139">Namespace Name</span></span>

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

### <span data-ttu-id="679ea-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="679ea-140">-RequiresSession</span></span>
<span data-ttu-id="679ea-141">RequiresSession-指出此佇列是否需要重複偵測的值。</span><span class="sxs-lookup"><span data-stu-id="679ea-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="679ea-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679ea-142">-ResourceGroupName</span></span>
<span data-ttu-id="679ea-143">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="679ea-143">The name of the resource group</span></span>

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

### <span data-ttu-id="679ea-144">-主題</span><span class="sxs-lookup"><span data-stu-id="679ea-144">-Topic</span></span>
<span data-ttu-id="679ea-145">主題名稱</span><span class="sxs-lookup"><span data-stu-id="679ea-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="679ea-146">-確認</span><span class="sxs-lookup"><span data-stu-id="679ea-146">-Confirm</span></span>
<span data-ttu-id="679ea-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="679ea-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679ea-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679ea-148">-WhatIf</span></span>
<span data-ttu-id="679ea-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="679ea-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679ea-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="679ea-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679ea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679ea-151">CommonParameters</span></span>
<span data-ttu-id="679ea-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="679ea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679ea-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="679ea-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679ea-154">輸入</span><span class="sxs-lookup"><span data-stu-id="679ea-154">INPUTS</span></span>

### <span data-ttu-id="679ea-155">System.object</span><span class="sxs-lookup"><span data-stu-id="679ea-155">System.String</span></span>

### <span data-ttu-id="679ea-156">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="679ea-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="679ea-157">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="679ea-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="679ea-158">輸出</span><span class="sxs-lookup"><span data-stu-id="679ea-158">OUTPUTS</span></span>

### <span data-ttu-id="679ea-159">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="679ea-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="679ea-160">筆記</span><span class="sxs-lookup"><span data-stu-id="679ea-160">NOTES</span></span>

## <span data-ttu-id="679ea-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="679ea-161">RELATED LINKS</span></span>
