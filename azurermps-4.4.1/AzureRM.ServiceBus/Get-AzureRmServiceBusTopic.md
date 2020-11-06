---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446667"
---
# <span data-ttu-id="6526c-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6526c-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="6526c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6526c-102">SYNOPSIS</span></span>
<span data-ttu-id="6526c-103">傳回指定服務匯流排主題的描述。</span><span class="sxs-lookup"><span data-stu-id="6526c-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6526c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6526c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6526c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6526c-105">DESCRIPTION</span></span>
<span data-ttu-id="6526c-106">**AzureRmServiceBusTopic** Cmdlet 會針對指定的服務匯流排命名空間傳回主題描述。</span><span class="sxs-lookup"><span data-stu-id="6526c-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6526c-107">示例</span><span class="sxs-lookup"><span data-stu-id="6526c-107">EXAMPLES</span></span>

### <span data-ttu-id="6526c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6526c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="6526c-109">針對指定的服務匯流排命名空間，返回指定主題的描述。</span><span class="sxs-lookup"><span data-stu-id="6526c-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="6526c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6526c-110">PARAMETERS</span></span>

### <span data-ttu-id="6526c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6526c-111">-DefaultProfile</span></span>
<span data-ttu-id="6526c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6526c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6526c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6526c-113">-Name</span></span>
<span data-ttu-id="6526c-114">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="6526c-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6526c-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6526c-115">-Namespace</span></span>
<span data-ttu-id="6526c-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6526c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6526c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6526c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6526c-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6526c-118">The name of the resource group</span></span>

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

### <span data-ttu-id="6526c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6526c-119">CommonParameters</span></span>
<span data-ttu-id="6526c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6526c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6526c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6526c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6526c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6526c-122">INPUTS</span></span>

### <span data-ttu-id="6526c-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6526c-123">-ResourceGroup</span></span>
 <span data-ttu-id="6526c-124">System.object</span><span class="sxs-lookup"><span data-stu-id="6526c-124">System.String</span></span>
 

### <span data-ttu-id="6526c-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6526c-125">-NamespaceName</span></span>
 <span data-ttu-id="6526c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="6526c-126">System.String</span></span>
 

### <span data-ttu-id="6526c-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6526c-127">-TopicName</span></span>
 <span data-ttu-id="6526c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="6526c-128">System.String</span></span>

## <span data-ttu-id="6526c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6526c-129">OUTPUTS</span></span>

### <span data-ttu-id="6526c-130">TopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6526c-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="6526c-131">名稱： SB-Topic_exampl1 位置：西美 Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 類型： AccessedAt： AutoDeleteOnIdle： 1/20/2017 3:18:54 AM/：10675199.02：48： 05.4775807 EntityAvailabilityStatus： CreatedAt： 1/20/2017 3:16:41 AM CountDetails：： MessageCountDetails DefaultMessageTimeToLive：10675199.02： True 05.4775807： false DuplicateDetectionHistoryTimeWindow： True EnableBatchedOperations： False EnableExpress： false EnablePartitioning： False EnableSubscriptionPartitioning： 16384 FilteringMessagesBeforePublishing： 1 IsAnonymousAccessible： False IsExpress： 1/20/2017 3:16:43 AM 的 MaxSizeInMegabytes： 1 RequiresDuplicateDetection： False SizeInBytes .. AM</span><span class="sxs-lookup"><span data-stu-id="6526c-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="6526c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6526c-132">NOTES</span></span>

## <span data-ttu-id="6526c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6526c-133">RELATED LINKS</span></span>

