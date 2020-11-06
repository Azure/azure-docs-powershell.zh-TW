---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446671"
---
# <span data-ttu-id="d056b-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d056b-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="d056b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d056b-102">SYNOPSIS</span></span>
<span data-ttu-id="d056b-103">傳回指定主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d056b-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d056b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d056b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d056b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d056b-105">DESCRIPTION</span></span>
<span data-ttu-id="d056b-106">**AzureRmServiceBusSubscription** Cmdlet 會針對指定的服務匯流排主題傳回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d056b-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="d056b-107">示例</span><span class="sxs-lookup"><span data-stu-id="d056b-107">EXAMPLES</span></span>

### <span data-ttu-id="d056b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d056b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="d056b-109">針對指定的服務匯流排主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="d056b-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="d056b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d056b-110">PARAMETERS</span></span>

### <span data-ttu-id="d056b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d056b-111">-DefaultProfile</span></span>
<span data-ttu-id="d056b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d056b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d056b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d056b-113">-Name</span></span>
<span data-ttu-id="d056b-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="d056b-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d056b-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d056b-115">-Namespace</span></span>
<span data-ttu-id="d056b-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d056b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="d056b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d056b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d056b-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d056b-118">The name of the resource group</span></span>

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

### <span data-ttu-id="d056b-119">-主題</span><span class="sxs-lookup"><span data-stu-id="d056b-119">-Topic</span></span>
<span data-ttu-id="d056b-120">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="d056b-120">Topic Name.</span></span>

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

### <span data-ttu-id="d056b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d056b-121">CommonParameters</span></span>
<span data-ttu-id="d056b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d056b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d056b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d056b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d056b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d056b-124">INPUTS</span></span>

### <span data-ttu-id="d056b-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d056b-125">-ResourceGroup</span></span>
 <span data-ttu-id="d056b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="d056b-126">System.String</span></span>
 

### <span data-ttu-id="d056b-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d056b-127">-NamespaceName</span></span>
 <span data-ttu-id="d056b-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d056b-128">System.String</span></span>
 

### <span data-ttu-id="d056b-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d056b-129">-TopicName</span></span>
 <span data-ttu-id="d056b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d056b-130">System.String</span></span>
 

### <span data-ttu-id="d056b-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d056b-131">-SubscriptionName</span></span>
 <span data-ttu-id="d056b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d056b-132">System.String</span></span>
 

## <span data-ttu-id="d056b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d056b-133">OUTPUTS</span></span>

### <span data-ttu-id="d056b-134">SubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d056b-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="d056b-135">名稱： SB-TopicSubscription-Example1 位置：美國西部 AccessedAt： 1/20/2017 3:18:54 AM AutoDeleteOnIdle：10675199.02：48： 05.4775807 CountDetails： MessageCountDetails CreatedAt： 1/20/2017 3:18:52：48： DefaultMessageTimeToLive 10675199.02： True 05.4775807： DeadLetteringOnFilterEvaluationExceptions： 00:01:00 DeadLetteringOnMessageExpiration： 10 EnableBatchedOperations： 0 EntityAvailabilityStatus： False Status： IsReadOnly： 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="d056b-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="d056b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d056b-136">NOTES</span></span>

## <span data-ttu-id="d056b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d056b-137">RELATED LINKS</span></span>

