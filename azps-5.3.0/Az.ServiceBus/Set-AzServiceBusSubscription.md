---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448323"
---
# <span data-ttu-id="36301-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="36301-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="36301-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36301-102">SYNOPSIS</span></span>
<span data-ttu-id="36301-103">更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="36301-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="36301-104">句法</span><span class="sxs-lookup"><span data-stu-id="36301-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36301-105">說明</span><span class="sxs-lookup"><span data-stu-id="36301-105">DESCRIPTION</span></span>
<span data-ttu-id="36301-106">**AzServiceBusSubscription** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="36301-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="36301-107">示例</span><span class="sxs-lookup"><span data-stu-id="36301-107">EXAMPLES</span></span>

### <span data-ttu-id="36301-108">範例1</span><span class="sxs-lookup"><span data-stu-id="36301-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="36301-109">針對指定的主題更新指定訂閱的描述。</span><span class="sxs-lookup"><span data-stu-id="36301-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="36301-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **true** ，並將 **MaxDeliveryCount** 更新為9。</span><span class="sxs-lookup"><span data-stu-id="36301-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="36301-111">參數</span><span class="sxs-lookup"><span data-stu-id="36301-111">PARAMETERS</span></span>

### <span data-ttu-id="36301-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36301-112">-DefaultProfile</span></span>
<span data-ttu-id="36301-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36301-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36301-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36301-114">-InputObject</span></span>
<span data-ttu-id="36301-115">已將訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="36301-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="36301-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="36301-116">-Namespace</span></span>
<span data-ttu-id="36301-117">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="36301-117">Namespace Name.</span></span>

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

### <span data-ttu-id="36301-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36301-118">-ResourceGroupName</span></span>
<span data-ttu-id="36301-119">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="36301-119">The name of the resource group</span></span>

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

### <span data-ttu-id="36301-120">-主題</span><span class="sxs-lookup"><span data-stu-id="36301-120">-Topic</span></span>
<span data-ttu-id="36301-121">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="36301-121">Topic Name.</span></span>

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

### <span data-ttu-id="36301-122">-確認</span><span class="sxs-lookup"><span data-stu-id="36301-122">-Confirm</span></span>
<span data-ttu-id="36301-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36301-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36301-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36301-124">-WhatIf</span></span>
<span data-ttu-id="36301-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36301-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36301-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36301-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36301-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36301-127">CommonParameters</span></span>
<span data-ttu-id="36301-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36301-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36301-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36301-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36301-130">輸入</span><span class="sxs-lookup"><span data-stu-id="36301-130">INPUTS</span></span>

### <span data-ttu-id="36301-131">System.object</span><span class="sxs-lookup"><span data-stu-id="36301-131">System.String</span></span>

### <span data-ttu-id="36301-132">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="36301-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="36301-133">輸出</span><span class="sxs-lookup"><span data-stu-id="36301-133">OUTPUTS</span></span>

### <span data-ttu-id="36301-134">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="36301-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="36301-135">筆記</span><span class="sxs-lookup"><span data-stu-id="36301-135">NOTES</span></span>

## <span data-ttu-id="36301-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="36301-136">RELATED LINKS</span></span>
