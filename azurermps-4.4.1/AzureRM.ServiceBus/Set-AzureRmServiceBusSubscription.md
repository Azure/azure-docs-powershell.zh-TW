---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625960"
---
# <span data-ttu-id="cc6c2-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="cc6c2-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="cc6c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6c2-103">更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc6c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc6c2-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc6c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc6c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc6c2-106">**AzureRmServiceBusSubscription** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="cc6c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc6c2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc6c2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cc6c2-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="cc6c2-109">針對指定的主題更新指定訂閱的描述。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="cc6c2-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **true** ，並將 **MaxDeliveryCount** 更新為9。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="cc6c2-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc6c2-111">PARAMETERS</span></span>

### <span data-ttu-id="cc6c2-112">-確認</span><span class="sxs-lookup"><span data-stu-id="cc6c2-112">-Confirm</span></span>
<span data-ttu-id="cc6c2-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc6c2-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc6c2-114">-WhatIf</span></span>
<span data-ttu-id="cc6c2-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc6c2-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc6c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6c2-117">-DefaultProfile</span></span>
<span data-ttu-id="cc6c2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc6c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc6c2-119">-InputObject</span></span>
<span data-ttu-id="cc6c2-120">已將訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6c2-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="cc6c2-121">-Namespace</span></span>
<span data-ttu-id="cc6c2-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-122">Namespace Name.</span></span>

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

### <span data-ttu-id="cc6c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc6c2-124">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="cc6c2-124">The name of the resource group</span></span>

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

### <span data-ttu-id="cc6c2-125">-主題</span><span class="sxs-lookup"><span data-stu-id="cc6c2-125">-Topic</span></span>
<span data-ttu-id="cc6c2-126">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-126">Topic Name.</span></span>

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

### <span data-ttu-id="cc6c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6c2-127">CommonParameters</span></span>
<span data-ttu-id="cc6c2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6c2-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc6c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6c2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cc6c2-130">INPUTS</span></span>

### <span data-ttu-id="cc6c2-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc6c2-131">-ResourceGroup</span></span>
 <span data-ttu-id="cc6c2-132">System.object</span><span class="sxs-lookup"><span data-stu-id="cc6c2-132">System.String</span></span>

### <span data-ttu-id="cc6c2-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cc6c2-133">-NamespaceName</span></span>
 <span data-ttu-id="cc6c2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cc6c2-134">System.String</span></span>

### <span data-ttu-id="cc6c2-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="cc6c2-135">-TopicName</span></span>
 <span data-ttu-id="cc6c2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="cc6c2-136">System.String</span></span>

### <span data-ttu-id="cc6c2-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="cc6c2-137">-SubscriptionObj</span></span>
 <span data-ttu-id="cc6c2-138">SubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cc6c2-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="cc6c2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="cc6c2-139">OUTPUTS</span></span>

### <span data-ttu-id="cc6c2-140">SubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cc6c2-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="cc6c2-141">名稱： SB-TopicSubscription-Example1 位置：美國西部 AccessedAt： 1/1/0001 12:00:00 AM AutoDeleteOnIdle：10675199.02：48： 05.4775807 CountDetails： CreatedAt： 1/20/2017 9:59:15 PM DefaultMessageTimeToLive：10675199.02：48： 05.4775807 DeadLetteringOnFilterEvaluationExceptions： True DeadLetteringOnMessageExpiration： False EnableBatchedOperations： True EntityAvailabilityStatus： IsReadOnly： LockDuration： 00:01:00 MaxDeliveryCount .. MessageCount： 0 RequiresSession： False 1/20/2017 9:59:15 狀態</span><span class="sxs-lookup"><span data-stu-id="cc6c2-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="cc6c2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cc6c2-142">NOTES</span></span>

## <span data-ttu-id="cc6c2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc6c2-143">RELATED LINKS</span></span>

