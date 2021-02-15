---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142517"
---
# <span data-ttu-id="57df9-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="57df9-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="57df9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57df9-102">SYNOPSIS</span></span>
<span data-ttu-id="57df9-103">傳回指定服務匯流排主題的描述。</span><span class="sxs-lookup"><span data-stu-id="57df9-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="57df9-104">句法</span><span class="sxs-lookup"><span data-stu-id="57df9-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57df9-105">說明</span><span class="sxs-lookup"><span data-stu-id="57df9-105">DESCRIPTION</span></span>
<span data-ttu-id="57df9-106">**AzServiceBusTopic** Cmdlet 會針對指定的服務匯流排命名空間傳回主題描述。</span><span class="sxs-lookup"><span data-stu-id="57df9-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="57df9-107">示例</span><span class="sxs-lookup"><span data-stu-id="57df9-107">EXAMPLES</span></span>

### <span data-ttu-id="57df9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="57df9-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="57df9-109">針對指定的服務匯流排命名空間，返回指定主題的描述。</span><span class="sxs-lookup"><span data-stu-id="57df9-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="57df9-110">範例2</span><span class="sxs-lookup"><span data-stu-id="57df9-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="57df9-111">傳回指定服務匯流排命名空間的主題清單。</span><span class="sxs-lookup"><span data-stu-id="57df9-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="57df9-112">根據預設，如果傳回100個以上的主題，則會傳回100主題，請使用-MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="57df9-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="57df9-113">範例3</span><span class="sxs-lookup"><span data-stu-id="57df9-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="57df9-114">傳回指定服務匯流排命名空間之第一個150主題的清單。</span><span class="sxs-lookup"><span data-stu-id="57df9-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="57df9-115">參數</span><span class="sxs-lookup"><span data-stu-id="57df9-115">PARAMETERS</span></span>

### <span data-ttu-id="57df9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57df9-116">-DefaultProfile</span></span>
<span data-ttu-id="57df9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57df9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57df9-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="57df9-118">-MaxCount</span></span>
<span data-ttu-id="57df9-119">決定要傳回的主題數目上限。</span><span class="sxs-lookup"><span data-stu-id="57df9-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="57df9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="57df9-120">-Name</span></span>
<span data-ttu-id="57df9-121">主題名稱</span><span class="sxs-lookup"><span data-stu-id="57df9-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57df9-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="57df9-122">-Namespace</span></span>
<span data-ttu-id="57df9-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="57df9-123">Namespace Name</span></span>

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

### <span data-ttu-id="57df9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57df9-124">-ResourceGroupName</span></span>
<span data-ttu-id="57df9-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="57df9-125">The name of the resource group</span></span>

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

### <span data-ttu-id="57df9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57df9-126">CommonParameters</span></span>
<span data-ttu-id="57df9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57df9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57df9-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57df9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57df9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="57df9-129">INPUTS</span></span>

### <span data-ttu-id="57df9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="57df9-130">System.String</span></span>

## <span data-ttu-id="57df9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="57df9-131">OUTPUTS</span></span>

### <span data-ttu-id="57df9-132">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="57df9-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="57df9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="57df9-133">NOTES</span></span>

## <span data-ttu-id="57df9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="57df9-134">RELATED LINKS</span></span>
