---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 9f8e7ee089972768053fd2873be22ed31dab206c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912585"
---
# <span data-ttu-id="61049-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="61049-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="61049-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61049-102">SYNOPSIS</span></span>
<span data-ttu-id="61049-103">會針對指定的 Service Bus 主題，返回描述。</span><span class="sxs-lookup"><span data-stu-id="61049-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="61049-104">語法</span><span class="sxs-lookup"><span data-stu-id="61049-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61049-105">描述</span><span class="sxs-lookup"><span data-stu-id="61049-105">DESCRIPTION</span></span>
<span data-ttu-id="61049-106">**Get-AzServiceBusTopic** Cmdlet 會針對指定的 Service Bus 命名空間，會返回主題描述。</span><span class="sxs-lookup"><span data-stu-id="61049-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="61049-107">例子</span><span class="sxs-lookup"><span data-stu-id="61049-107">EXAMPLES</span></span>

### <span data-ttu-id="61049-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="61049-108">Example 1</span></span>
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

<span data-ttu-id="61049-109">會針對指定的 Service Bus 命名空間，返回指定主題的描述。</span><span class="sxs-lookup"><span data-stu-id="61049-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="61049-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="61049-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="61049-111">針對給定 Service Bus 命名空間，會返回主題清單。</span><span class="sxs-lookup"><span data-stu-id="61049-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="61049-112">根據預設，會退回 100 個主題，如果要退回的主題超過 100 個，請使用 -MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="61049-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="61049-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="61049-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="61049-114">針對給定 Service Bus 命名空間，會返回前 150 個主題的清單。</span><span class="sxs-lookup"><span data-stu-id="61049-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="61049-115">參數</span><span class="sxs-lookup"><span data-stu-id="61049-115">PARAMETERS</span></span>

### <span data-ttu-id="61049-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61049-116">-DefaultProfile</span></span>
<span data-ttu-id="61049-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61049-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61049-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="61049-118">-MaxCount</span></span>
<span data-ttu-id="61049-119">決定要退回的主題數量上限。</span><span class="sxs-lookup"><span data-stu-id="61049-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="61049-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="61049-120">-Name</span></span>
<span data-ttu-id="61049-121">主題名稱</span><span class="sxs-lookup"><span data-stu-id="61049-121">Topic Name</span></span>

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

### <span data-ttu-id="61049-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="61049-122">-Namespace</span></span>
<span data-ttu-id="61049-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="61049-123">Namespace Name</span></span>

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

### <span data-ttu-id="61049-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61049-124">-ResourceGroupName</span></span>
<span data-ttu-id="61049-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="61049-125">The name of the resource group</span></span>

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

### <span data-ttu-id="61049-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61049-126">CommonParameters</span></span>
<span data-ttu-id="61049-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61049-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61049-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="61049-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61049-129">輸入</span><span class="sxs-lookup"><span data-stu-id="61049-129">INPUTS</span></span>

### <span data-ttu-id="61049-130">System.String</span><span class="sxs-lookup"><span data-stu-id="61049-130">System.String</span></span>

## <span data-ttu-id="61049-131">輸出</span><span class="sxs-lookup"><span data-stu-id="61049-131">OUTPUTS</span></span>

### <span data-ttu-id="61049-132">Microsoft.Azure.Commands.ServiceBus.models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="61049-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="61049-133">筆記</span><span class="sxs-lookup"><span data-stu-id="61049-133">NOTES</span></span>

## <span data-ttu-id="61049-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="61049-134">RELATED LINKS</span></span>
