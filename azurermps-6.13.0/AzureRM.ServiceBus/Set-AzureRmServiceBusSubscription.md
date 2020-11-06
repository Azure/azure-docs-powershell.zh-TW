---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: dbc3acdf65f97e5fa46d9359f1f7af43c2c137d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449741"
---
# <span data-ttu-id="e94fa-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e94fa-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="e94fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e94fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e94fa-103">更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="e94fa-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e94fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="e94fa-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e94fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="e94fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e94fa-106">**AzureRmServiceBusSubscription** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="e94fa-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e94fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="e94fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e94fa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e94fa-108">Example 1</span></span>
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

<span data-ttu-id="e94fa-109">針對指定的主題更新指定訂閱的描述。</span><span class="sxs-lookup"><span data-stu-id="e94fa-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="e94fa-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **true** ，並將 **MaxDeliveryCount** 更新為9。</span><span class="sxs-lookup"><span data-stu-id="e94fa-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="e94fa-111">參數</span><span class="sxs-lookup"><span data-stu-id="e94fa-111">PARAMETERS</span></span>

### <span data-ttu-id="e94fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94fa-112">-DefaultProfile</span></span>
<span data-ttu-id="e94fa-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e94fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e94fa-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e94fa-114">-InputObject</span></span>
<span data-ttu-id="e94fa-115">已將訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="e94fa-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e94fa-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e94fa-116">-Namespace</span></span>
<span data-ttu-id="e94fa-117">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e94fa-117">Namespace Name.</span></span>

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

### <span data-ttu-id="e94fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="e94fa-119">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e94fa-119">The name of the resource group</span></span>

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

### <span data-ttu-id="e94fa-120">-主題</span><span class="sxs-lookup"><span data-stu-id="e94fa-120">-Topic</span></span>
<span data-ttu-id="e94fa-121">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="e94fa-121">Topic Name.</span></span>

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

### <span data-ttu-id="e94fa-122">-確認</span><span class="sxs-lookup"><span data-stu-id="e94fa-122">-Confirm</span></span>
<span data-ttu-id="e94fa-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e94fa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94fa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94fa-124">-WhatIf</span></span>
<span data-ttu-id="e94fa-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e94fa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94fa-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e94fa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94fa-127">CommonParameters</span></span>
<span data-ttu-id="e94fa-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e94fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94fa-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e94fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94fa-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e94fa-130">INPUTS</span></span>

### <span data-ttu-id="e94fa-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e94fa-131">System.String</span></span>

### <span data-ttu-id="e94fa-132">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e94fa-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="e94fa-133">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e94fa-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e94fa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e94fa-134">OUTPUTS</span></span>

### <span data-ttu-id="e94fa-135">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e94fa-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e94fa-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e94fa-136">NOTES</span></span>

## <span data-ttu-id="e94fa-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e94fa-137">RELATED LINKS</span></span>
