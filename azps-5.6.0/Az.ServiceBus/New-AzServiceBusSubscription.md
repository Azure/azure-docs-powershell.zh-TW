---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: b0ce7f5190ea36727c8d5b3182515c8b7917071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914386"
---
# <span data-ttu-id="4baea-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4baea-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="4baea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4baea-102">SYNOPSIS</span></span>
<span data-ttu-id="4baea-103">建立指定 Service Bus 主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4baea-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4baea-104">語法</span><span class="sxs-lookup"><span data-stu-id="4baea-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4baea-105">描述</span><span class="sxs-lookup"><span data-stu-id="4baea-105">DESCRIPTION</span></span>
<span data-ttu-id="4baea-106">**New-AzServiceBusSubscription** Cmdlet 會建立指定 Service Bus 主題的新訂閱。</span><span class="sxs-lookup"><span data-stu-id="4baea-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4baea-107">例子</span><span class="sxs-lookup"><span data-stu-id="4baea-107">EXAMPLES</span></span>

### <span data-ttu-id="4baea-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4baea-108">Example 1</span></span>
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

<span data-ttu-id="4baea-109">建立指定 `SB-TopicSubscription-Example1` Service Bus 主題的訂閱 `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="4baea-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="4baea-110">參數</span><span class="sxs-lookup"><span data-stu-id="4baea-110">PARAMETERS</span></span>

### <span data-ttu-id="4baea-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="4baea-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="4baea-112">指定 [時間間隔，](https://msdn.microsoft.com/library/system.timespan.aspx) 之後會自動刪除訂閱。</span><span class="sxs-lookup"><span data-stu-id="4baea-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="4baea-113">最短持續時間為 5 分鐘。</span><span class="sxs-lookup"><span data-stu-id="4baea-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="4baea-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="4baea-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="4baea-115">指出訂閱是否支援篩選評估例外情形的值。</span><span class="sxs-lookup"><span data-stu-id="4baea-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="4baea-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="4baea-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="4baea-117">郵件到期時出現信號失效</span><span class="sxs-lookup"><span data-stu-id="4baea-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="4baea-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="4baea-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="4baea-119">時間窗格為即時值。</span><span class="sxs-lookup"><span data-stu-id="4baea-119">Timespan to live value.</span></span>
<span data-ttu-id="4baea-120">這是郵件到期的持續時間，從郵件送到 Service Bus 的時間開始。</span><span class="sxs-lookup"><span data-stu-id="4baea-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="4baea-121">這是 TimeToLive 未在郵件本身上設定時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="4baea-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="4baea-122">標準 = Timespan.Max 和 Basic = 14 天</span><span class="sxs-lookup"><span data-stu-id="4baea-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="4baea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4baea-123">-DefaultProfile</span></span>
<span data-ttu-id="4baea-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4baea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4baea-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="4baea-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="4baea-126">啟用批次處理作業 - 指出是否已啟用伺服器端批次處理作業的值</span><span class="sxs-lookup"><span data-stu-id="4baea-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="4baea-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="4baea-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="4baea-128">佇列/主題名稱以轉寄已信的訊息</span><span class="sxs-lookup"><span data-stu-id="4baea-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="4baea-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="4baea-129">-ForwardTo</span></span>
<span data-ttu-id="4baea-130">佇列/主題名稱以轉轉郵件</span><span class="sxs-lookup"><span data-stu-id="4baea-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="4baea-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="4baea-131">-LockDuration</span></span>
<span data-ttu-id="4baea-132">鎖定持續時間</span><span class="sxs-lookup"><span data-stu-id="4baea-132">Lock Duration</span></span>

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

### <span data-ttu-id="4baea-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4baea-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="4baea-134">MaxDeliveryCount - 最大傳遞計數。</span><span class="sxs-lookup"><span data-stu-id="4baea-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="4baea-135">郵件會在此數目的傳遞後自動刪除。</span><span class="sxs-lookup"><span data-stu-id="4baea-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="4baea-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="4baea-136">-Name</span></span>
<span data-ttu-id="4baea-137">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="4baea-137">Subscription Name</span></span>

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

### <span data-ttu-id="4baea-138">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4baea-138">-Namespace</span></span>
<span data-ttu-id="4baea-139">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="4baea-139">Namespace Name</span></span>

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

### <span data-ttu-id="4baea-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="4baea-140">-RequiresSession</span></span>
<span data-ttu-id="4baea-141">需要Session - 指出此佇列需要重複偵測的值。</span><span class="sxs-lookup"><span data-stu-id="4baea-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="4baea-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4baea-142">-ResourceGroupName</span></span>
<span data-ttu-id="4baea-143">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4baea-143">The name of the resource group</span></span>

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

### <span data-ttu-id="4baea-144">-主題</span><span class="sxs-lookup"><span data-stu-id="4baea-144">-Topic</span></span>
<span data-ttu-id="4baea-145">主題名稱</span><span class="sxs-lookup"><span data-stu-id="4baea-145">Topic Name</span></span>

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

### <span data-ttu-id="4baea-146">-確認</span><span class="sxs-lookup"><span data-stu-id="4baea-146">-Confirm</span></span>
<span data-ttu-id="4baea-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4baea-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4baea-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4baea-148">-WhatIf</span></span>
<span data-ttu-id="4baea-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4baea-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4baea-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4baea-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4baea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4baea-151">CommonParameters</span></span>
<span data-ttu-id="4baea-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4baea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4baea-153">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4baea-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4baea-154">輸入</span><span class="sxs-lookup"><span data-stu-id="4baea-154">INPUTS</span></span>

### <span data-ttu-id="4baea-155">System.String</span><span class="sxs-lookup"><span data-stu-id="4baea-155">System.String</span></span>

### <span data-ttu-id="4baea-156">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4baea-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4baea-157">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4baea-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4baea-158">輸出</span><span class="sxs-lookup"><span data-stu-id="4baea-158">OUTPUTS</span></span>

### <span data-ttu-id="4baea-159">Microsoft.Azure.Commands.ServiceBus.models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4baea-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4baea-160">筆記</span><span class="sxs-lookup"><span data-stu-id="4baea-160">NOTES</span></span>

## <span data-ttu-id="4baea-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="4baea-161">RELATED LINKS</span></span>
