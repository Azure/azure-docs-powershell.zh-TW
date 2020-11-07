---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: bf6bd96314c8baf9e4d46b977b3f00457342db96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791038"
---
# <span data-ttu-id="e7afe-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e7afe-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="e7afe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7afe-102">SYNOPSIS</span></span>
<span data-ttu-id="e7afe-103">傳回指定主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="e7afe-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="e7afe-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7afe-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7afe-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7afe-105">DESCRIPTION</span></span>
<span data-ttu-id="e7afe-106">**AzServiceBusSubscription** Cmdlet 會針對指定的服務匯流排主題傳回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="e7afe-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="e7afe-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7afe-107">EXAMPLES</span></span>

### <span data-ttu-id="e7afe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e7afe-108">Example 1</span></span>
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

<span data-ttu-id="e7afe-109">針對指定的服務匯流排主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="e7afe-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="e7afe-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e7afe-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="e7afe-111">傳回指定服務匯流排主題的訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="e7afe-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="e7afe-112">根據預設，會傳回100訂閱，如需訂閱數，請使用-MaxCount 參數</span><span class="sxs-lookup"><span data-stu-id="e7afe-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="e7afe-113">範例3</span><span class="sxs-lookup"><span data-stu-id="e7afe-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="e7afe-114">傳回指定服務匯流排主題的前150訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="e7afe-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="e7afe-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7afe-115">PARAMETERS</span></span>

### <span data-ttu-id="e7afe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7afe-116">-DefaultProfile</span></span>
<span data-ttu-id="e7afe-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7afe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7afe-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e7afe-118">-MaxCount</span></span>
<span data-ttu-id="e7afe-119">決定要傳回的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="e7afe-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="e7afe-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7afe-120">-Name</span></span>
<span data-ttu-id="e7afe-121">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="e7afe-121">Subscription Name</span></span>

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

### <span data-ttu-id="e7afe-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e7afe-122">-Namespace</span></span>
<span data-ttu-id="e7afe-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e7afe-123">Namespace Name</span></span>

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

### <span data-ttu-id="e7afe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7afe-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7afe-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e7afe-125">The name of the resource group</span></span>

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

### <span data-ttu-id="e7afe-126">-主題</span><span class="sxs-lookup"><span data-stu-id="e7afe-126">-Topic</span></span>
<span data-ttu-id="e7afe-127">主題名稱</span><span class="sxs-lookup"><span data-stu-id="e7afe-127">Topic Name</span></span>

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

### <span data-ttu-id="e7afe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7afe-128">CommonParameters</span></span>
<span data-ttu-id="e7afe-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7afe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7afe-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7afe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7afe-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e7afe-131">INPUTS</span></span>

### <span data-ttu-id="e7afe-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e7afe-132">System.String</span></span>

## <span data-ttu-id="e7afe-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e7afe-133">OUTPUTS</span></span>

### <span data-ttu-id="e7afe-134">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7afe-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e7afe-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e7afe-135">NOTES</span></span>

## <span data-ttu-id="e7afe-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7afe-136">RELATED LINKS</span></span>
