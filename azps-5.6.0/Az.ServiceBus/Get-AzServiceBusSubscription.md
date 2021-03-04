---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: c68764d0dfd2d496d5ead3a2e9631d29979194e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912586"
---
# <span data-ttu-id="d6684-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d6684-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="d6684-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6684-102">SYNOPSIS</span></span>
<span data-ttu-id="d6684-103">會針對指定的主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d6684-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="d6684-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6684-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6684-105">描述</span><span class="sxs-lookup"><span data-stu-id="d6684-105">DESCRIPTION</span></span>
<span data-ttu-id="d6684-106">**Get-AzServiceBusSubscription** Cmdlet 會針對指定的 Service Bus 主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d6684-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="d6684-107">例子</span><span class="sxs-lookup"><span data-stu-id="d6684-107">EXAMPLES</span></span>

### <span data-ttu-id="d6684-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6684-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="d6684-109">會針對指定的 Service Bus 主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d6684-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="d6684-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="d6684-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="d6684-111">針對指定的 Service Bus 主題，會返回訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="d6684-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="d6684-112">根據預設，將會退回 100 個訂閱，針對訂閱數目，請使用 -MaxCount 參數</span><span class="sxs-lookup"><span data-stu-id="d6684-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="d6684-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="d6684-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="d6684-114">針對指定的 Service Bus 主題，會返回前 150 個訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="d6684-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="d6684-115">參數</span><span class="sxs-lookup"><span data-stu-id="d6684-115">PARAMETERS</span></span>

### <span data-ttu-id="d6684-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6684-116">-DefaultProfile</span></span>
<span data-ttu-id="d6684-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6684-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6684-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d6684-118">-MaxCount</span></span>
<span data-ttu-id="d6684-119">決定要退回的訂閱數量上限。</span><span class="sxs-lookup"><span data-stu-id="d6684-119">Determine the maximum number of Subscriptions to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6684-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6684-120">-Name</span></span>
<span data-ttu-id="d6684-121">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="d6684-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6684-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d6684-122">-Namespace</span></span>
<span data-ttu-id="d6684-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="d6684-123">Namespace Name</span></span>

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

### <span data-ttu-id="d6684-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6684-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6684-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="d6684-125">The name of the resource group</span></span>

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

### <span data-ttu-id="d6684-126">-主題</span><span class="sxs-lookup"><span data-stu-id="d6684-126">-Topic</span></span>
<span data-ttu-id="d6684-127">主題名稱</span><span class="sxs-lookup"><span data-stu-id="d6684-127">Topic Name</span></span>

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

### <span data-ttu-id="d6684-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6684-128">CommonParameters</span></span>
<span data-ttu-id="d6684-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6684-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6684-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d6684-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6684-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d6684-131">INPUTS</span></span>

### <span data-ttu-id="d6684-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6684-132">System.String</span></span>

## <span data-ttu-id="d6684-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d6684-133">OUTPUTS</span></span>

### <span data-ttu-id="d6684-134">Microsoft.Azure.Commands.ServiceBus.models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="d6684-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="d6684-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d6684-135">NOTES</span></span>

## <span data-ttu-id="d6684-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6684-136">RELATED LINKS</span></span>
