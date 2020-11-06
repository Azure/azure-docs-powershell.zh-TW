---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449507"
---
# <span data-ttu-id="28189-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="28189-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="28189-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28189-102">SYNOPSIS</span></span>
<span data-ttu-id="28189-103">建立指定服務匯流排主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="28189-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28189-104">句法</span><span class="sxs-lookup"><span data-stu-id="28189-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28189-105">說明</span><span class="sxs-lookup"><span data-stu-id="28189-105">DESCRIPTION</span></span>
<span data-ttu-id="28189-106">**新的-AzureRmServiceBusSubscription** Cmdlet 會在指定的服務匯流排主題中建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="28189-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="28189-107">示例</span><span class="sxs-lookup"><span data-stu-id="28189-107">EXAMPLES</span></span>

### <span data-ttu-id="28189-108">範例1</span><span class="sxs-lookup"><span data-stu-id="28189-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="28189-109">`SB-TopicSubscription-Example1`針對指定的服務匯流排主題建立訂閱 `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="28189-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="28189-110">參數</span><span class="sxs-lookup"><span data-stu-id="28189-110">PARAMETERS</span></span>

### <span data-ttu-id="28189-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="28189-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="28189-112">指定將自動刪除訂閱之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔。</span><span class="sxs-lookup"><span data-stu-id="28189-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="28189-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="28189-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="28189-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="28189-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="28189-115">表示訂閱在篩選評估例外狀況上是否有死信支援。</span><span class="sxs-lookup"><span data-stu-id="28189-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="28189-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="28189-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="28189-117">指示在郵件到期時，訂閱是否有 deadletter 支援。</span><span class="sxs-lookup"><span data-stu-id="28189-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="28189-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="28189-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="28189-119">指出是否已啟用伺服器端批次作業。</span><span class="sxs-lookup"><span data-stu-id="28189-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="28189-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="28189-120">-IsReadOnly</span></span>
<span data-ttu-id="28189-121">指示實體描述是否為唯讀</span><span class="sxs-lookup"><span data-stu-id="28189-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="28189-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="28189-122">-LockDuration</span></span>
<span data-ttu-id="28189-123">指定訂閱的鎖定持續時間範圍。</span><span class="sxs-lookup"><span data-stu-id="28189-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="28189-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="28189-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="28189-125">指定最大遞送數。</span><span class="sxs-lookup"><span data-stu-id="28189-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="28189-126">在遞送此數之後，就會自動 deadlettered 訊息。</span><span class="sxs-lookup"><span data-stu-id="28189-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="28189-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="28189-127">-RequiresSession</span></span>
<span data-ttu-id="28189-128">指定訂閱是否支援會話的概念。</span><span class="sxs-lookup"><span data-stu-id="28189-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="28189-129">-確認</span><span class="sxs-lookup"><span data-stu-id="28189-129">-Confirm</span></span>
<span data-ttu-id="28189-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28189-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28189-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28189-131">-WhatIf</span></span>
<span data-ttu-id="28189-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28189-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28189-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28189-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28189-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="28189-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="28189-135">Timespan 到 [即時] 值。</span><span class="sxs-lookup"><span data-stu-id="28189-135">Timespan to live value.</span></span> <span data-ttu-id="28189-136">這是郵件到期後的持續時間，從郵件傳送到服務匯流排的那一段開始。</span><span class="sxs-lookup"><span data-stu-id="28189-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="28189-137">這是未在郵件本身設定 TimeToLive 時所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="28189-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="28189-138">標準 = Timespan.zero. Max 和 Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="28189-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="28189-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28189-139">-DefaultProfile</span></span>
<span data-ttu-id="28189-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28189-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28189-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="28189-141">-Name</span></span>
<span data-ttu-id="28189-142">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="28189-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28189-143">-命名空間</span><span class="sxs-lookup"><span data-stu-id="28189-143">-Namespace</span></span>
<span data-ttu-id="28189-144">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="28189-144">Namespace Name.</span></span>

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

### <span data-ttu-id="28189-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28189-145">-ResourceGroupName</span></span>
<span data-ttu-id="28189-146">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="28189-146">The name of the resource group</span></span>

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

### <span data-ttu-id="28189-147">-主題</span><span class="sxs-lookup"><span data-stu-id="28189-147">-Topic</span></span>
<span data-ttu-id="28189-148">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="28189-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28189-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28189-149">CommonParameters</span></span>
<span data-ttu-id="28189-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28189-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28189-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28189-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28189-152">輸入</span><span class="sxs-lookup"><span data-stu-id="28189-152">INPUTS</span></span>

### <span data-ttu-id="28189-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28189-153">-ResourceGroup</span></span>
 <span data-ttu-id="28189-154">System.object</span><span class="sxs-lookup"><span data-stu-id="28189-154">System.String</span></span>
 

### <span data-ttu-id="28189-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="28189-155">-NamespaceName</span></span>
 <span data-ttu-id="28189-156">System.object</span><span class="sxs-lookup"><span data-stu-id="28189-156">System.String</span></span>
 

### <span data-ttu-id="28189-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="28189-157">-TopicName</span></span>
 <span data-ttu-id="28189-158">System.object</span><span class="sxs-lookup"><span data-stu-id="28189-158">System.String</span></span>
 

### <span data-ttu-id="28189-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="28189-159">-SubscriptionName</span></span>
 <span data-ttu-id="28189-160">System.object</span><span class="sxs-lookup"><span data-stu-id="28189-160">System.String</span></span>

## <span data-ttu-id="28189-161">輸出</span><span class="sxs-lookup"><span data-stu-id="28189-161">OUTPUTS</span></span>

### <span data-ttu-id="28189-162">SubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="28189-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="28189-163">名稱： SB-TopicSubscription-Example1 位置：美國西部 AccessedAt： 1/20/2017 3:18:54 AM AutoDeleteOnIdle：10675199.02：48： 05.4775807 CountDetails： MessageCountDetails CreatedAt： 1/20/2017 3:18:52：48： DefaultMessageTimeToLive 10675199.02： True 05.4775807： DeadLetteringOnFilterEvaluationExceptions： 00:01:00 DeadLetteringOnMessageExpiration： 10 EnableBatchedOperations： 0 EntityAvailabilityStatus： False Status： IsReadOnly： 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="28189-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="28189-164">筆記</span><span class="sxs-lookup"><span data-stu-id="28189-164">NOTES</span></span>

## <span data-ttu-id="28189-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="28189-165">RELATED LINKS</span></span>

