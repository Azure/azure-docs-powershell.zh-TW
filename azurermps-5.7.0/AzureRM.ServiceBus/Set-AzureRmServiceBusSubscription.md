---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 6bb5b6e8ea96f0852747c00ac4ef5ac11208e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623801"
---
# <span data-ttu-id="320d9-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="320d9-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="320d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="320d9-102">SYNOPSIS</span></span>
<span data-ttu-id="320d9-103">更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="320d9-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="320d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="320d9-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="320d9-105">DESCRIPTION</span></span>
<span data-ttu-id="320d9-106">**AzureRmServiceBusSubscription** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="320d9-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="320d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="320d9-107">EXAMPLES</span></span>

### <span data-ttu-id="320d9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="320d9-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="320d9-109">針對指定的主題更新指定訂閱的描述。</span><span class="sxs-lookup"><span data-stu-id="320d9-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="320d9-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **true** ，並將 **MaxDeliveryCount** 更新為9。</span><span class="sxs-lookup"><span data-stu-id="320d9-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="320d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="320d9-111">PARAMETERS</span></span>

### <span data-ttu-id="320d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320d9-112">-DefaultProfile</span></span>
<span data-ttu-id="320d9-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="320d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="320d9-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="320d9-114">-InputObject</span></span>
<span data-ttu-id="320d9-115">已將訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="320d9-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320d9-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="320d9-116">-Namespace</span></span>
<span data-ttu-id="320d9-117">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="320d9-117">Namespace Name.</span></span>

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

### <span data-ttu-id="320d9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320d9-118">-ResourceGroupName</span></span>
<span data-ttu-id="320d9-119">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="320d9-119">The name of the resource group</span></span>

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

### <span data-ttu-id="320d9-120">-主題</span><span class="sxs-lookup"><span data-stu-id="320d9-120">-Topic</span></span>
<span data-ttu-id="320d9-121">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="320d9-121">Topic Name.</span></span>

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

### <span data-ttu-id="320d9-122">-確認</span><span class="sxs-lookup"><span data-stu-id="320d9-122">-Confirm</span></span>
<span data-ttu-id="320d9-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="320d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320d9-124">-WhatIf</span></span>
<span data-ttu-id="320d9-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="320d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320d9-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="320d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320d9-127">CommonParameters</span></span>
<span data-ttu-id="320d9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="320d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320d9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="320d9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320d9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="320d9-130">INPUTS</span></span>

### <span data-ttu-id="320d9-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="320d9-131">-ResourceGroup</span></span>
 <span data-ttu-id="320d9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="320d9-132">System.String</span></span>

### <span data-ttu-id="320d9-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="320d9-133">-NamespaceName</span></span>
 <span data-ttu-id="320d9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="320d9-134">System.String</span></span>

### <span data-ttu-id="320d9-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="320d9-135">-TopicName</span></span>
 <span data-ttu-id="320d9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="320d9-136">System.String</span></span>

### <span data-ttu-id="320d9-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="320d9-137">-SubscriptionObj</span></span>
 <span data-ttu-id="320d9-138">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="320d9-138">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="320d9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="320d9-139">OUTPUTS</span></span>

### <span data-ttu-id="320d9-140">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="320d9-140">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="320d9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="320d9-141">NOTES</span></span>

## <span data-ttu-id="320d9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="320d9-142">RELATED LINKS</span></span>

