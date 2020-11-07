---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 25a64b352622cf9c057ce0e3f38bc3e4e122e22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624344"
---
# <span data-ttu-id="47de4-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="47de4-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="47de4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47de4-102">SYNOPSIS</span></span>
<span data-ttu-id="47de4-103">傳回指定服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="47de4-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47de4-104">句法</span><span class="sxs-lookup"><span data-stu-id="47de4-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47de4-105">說明</span><span class="sxs-lookup"><span data-stu-id="47de4-105">DESCRIPTION</span></span>
<span data-ttu-id="47de4-106">傳回指定服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="47de4-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="47de4-107">示例</span><span class="sxs-lookup"><span data-stu-id="47de4-107">EXAMPLES</span></span>

### <span data-ttu-id="47de4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="47de4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="47de4-109">傳回佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="47de4-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="47de4-110">範例2</span><span class="sxs-lookup"><span data-stu-id="47de4-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="47de4-111">傳回指定命名空間的佇列清單：預設會傳回100佇列（如果傳回超過100個佇列），請使用-MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="47de4-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="47de4-112">範例3</span><span class="sxs-lookup"><span data-stu-id="47de4-112">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="47de4-113">傳回指定命名空間之前150佇列的清單</span><span class="sxs-lookup"><span data-stu-id="47de4-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="47de4-114">參數</span><span class="sxs-lookup"><span data-stu-id="47de4-114">PARAMETERS</span></span>

### <span data-ttu-id="47de4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47de4-115">-DefaultProfile</span></span>
<span data-ttu-id="47de4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47de4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47de4-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="47de4-117">-MaxCount</span></span>
<span data-ttu-id="47de4-118">決定要傳回的佇列數目上限。</span><span class="sxs-lookup"><span data-stu-id="47de4-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="47de4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="47de4-119">-Name</span></span>
<span data-ttu-id="47de4-120">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="47de4-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47de4-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="47de4-121">-Namespace</span></span>
<span data-ttu-id="47de4-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="47de4-122">Namespace Name</span></span>

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

### <span data-ttu-id="47de4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47de4-123">-ResourceGroupName</span></span>
<span data-ttu-id="47de4-124">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="47de4-124">The name of the resource group</span></span>

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

### <span data-ttu-id="47de4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47de4-125">CommonParameters</span></span>
<span data-ttu-id="47de4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47de4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47de4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47de4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47de4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="47de4-128">INPUTS</span></span>

### <span data-ttu-id="47de4-129">System.object</span><span class="sxs-lookup"><span data-stu-id="47de4-129">System.String</span></span>

## <span data-ttu-id="47de4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="47de4-130">OUTPUTS</span></span>

### <span data-ttu-id="47de4-131">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="47de4-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="47de4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="47de4-132">NOTES</span></span>

## <span data-ttu-id="47de4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="47de4-133">RELATED LINKS</span></span>
