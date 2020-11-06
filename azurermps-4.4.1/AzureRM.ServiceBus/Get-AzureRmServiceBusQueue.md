---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455611"
---
# <span data-ttu-id="69ad2-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="69ad2-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="69ad2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="69ad2-103">傳回指定服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="69ad2-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ad2-104">句法</span><span class="sxs-lookup"><span data-stu-id="69ad2-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ad2-105">說明</span><span class="sxs-lookup"><span data-stu-id="69ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="69ad2-106">**AzureRmServiceBusQueue** Cmdlet 會傳回指定服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="69ad2-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="69ad2-107">示例</span><span class="sxs-lookup"><span data-stu-id="69ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="69ad2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="69ad2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="69ad2-109">傳回佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="69ad2-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="69ad2-110">參數</span><span class="sxs-lookup"><span data-stu-id="69ad2-110">PARAMETERS</span></span>

### <span data-ttu-id="69ad2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ad2-111">-DefaultProfile</span></span>
<span data-ttu-id="69ad2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69ad2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ad2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="69ad2-113">-Name</span></span>
<span data-ttu-id="69ad2-114">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="69ad2-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ad2-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="69ad2-115">-Namespace</span></span>
<span data-ttu-id="69ad2-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="69ad2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="69ad2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ad2-117">-ResourceGroupName</span></span>
<span data-ttu-id="69ad2-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="69ad2-118">The name of the resource group</span></span>

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

### <span data-ttu-id="69ad2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ad2-119">CommonParameters</span></span>
<span data-ttu-id="69ad2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69ad2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ad2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69ad2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ad2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="69ad2-122">INPUTS</span></span>

### <span data-ttu-id="69ad2-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69ad2-123">-ResourceGroup</span></span>
 <span data-ttu-id="69ad2-124">System.object</span><span class="sxs-lookup"><span data-stu-id="69ad2-124">System.String</span></span>
 

### <span data-ttu-id="69ad2-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="69ad2-125">-NamespaceName</span></span>
 <span data-ttu-id="69ad2-126">System.object</span><span class="sxs-lookup"><span data-stu-id="69ad2-126">System.String</span></span>
 

### <span data-ttu-id="69ad2-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="69ad2-127">-QueueName</span></span>
 <span data-ttu-id="69ad2-128">System.object</span><span class="sxs-lookup"><span data-stu-id="69ad2-128">System.String</span></span> 

## <span data-ttu-id="69ad2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="69ad2-129">OUTPUTS</span></span>

### <span data-ttu-id="69ad2-130">QueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="69ad2-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="69ad2-131">LockDuration： AccessedAt： 1/1/0001 12:00:00 AM AutoDeleteOnIdle：10675199.02：48： 05.4775807 EntityAvailabilityStatus： CreatedAt： 1/20/2017 2:51:35 AM DefaultMessageTimeToLive：10675199.02：48： 05.4775807 DuplicateDetectionHistoryTimeWindow： EnableBatchedOperations： True DeadLetteringOnMessageExpiration： false EnableExpress： EnablePartitioning： IsAnonymousAccessible： false MaxDeliveryCount： MaxSizeInMegabytes： 16384 MessageCount： CountDetails： MessageCountDetails： False RequiresDuplicateDetection： [RequiresSession SizeInBytes： false SupportOrdering： False UpdatedAt： 1/20/2017 2:51:37 AM Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 名稱： SB-Queue_example1 類型：（美國）</span><span class="sxs-lookup"><span data-stu-id="69ad2-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="69ad2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="69ad2-132">NOTES</span></span>

## <span data-ttu-id="69ad2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="69ad2-133">RELATED LINKS</span></span>

