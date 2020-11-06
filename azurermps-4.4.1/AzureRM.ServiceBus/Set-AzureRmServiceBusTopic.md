---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449504"
---
# <span data-ttu-id="9c6de-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="9c6de-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="9c6de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c6de-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6de-103">更新指定服務匯流排命名空間中服務匯流排主題的描述。</span><span class="sxs-lookup"><span data-stu-id="9c6de-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c6de-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c6de-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c6de-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c6de-105">DESCRIPTION</span></span>
<span data-ttu-id="9c6de-106">**AzureRmServiceBusTopic** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的描述物件。</span><span class="sxs-lookup"><span data-stu-id="9c6de-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9c6de-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c6de-107">EXAMPLES</span></span>

### <span data-ttu-id="9c6de-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9c6de-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="9c6de-109">使用指定命名空間中的新描述更新指定主題。</span><span class="sxs-lookup"><span data-stu-id="9c6de-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="9c6de-110">這個範例會將 **EnableExpress** 屬性更新為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="9c6de-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="9c6de-111">參數</span><span class="sxs-lookup"><span data-stu-id="9c6de-111">PARAMETERS</span></span>

### <span data-ttu-id="9c6de-112">-確認</span><span class="sxs-lookup"><span data-stu-id="9c6de-112">-Confirm</span></span>
<span data-ttu-id="9c6de-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c6de-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c6de-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c6de-114">-WhatIf</span></span>
<span data-ttu-id="9c6de-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c6de-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c6de-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c6de-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c6de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6de-117">-DefaultProfile</span></span>
<span data-ttu-id="9c6de-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c6de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c6de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c6de-119">-InputObject</span></span>
<span data-ttu-id="9c6de-120">[上的] 主題定義。</span><span class="sxs-lookup"><span data-stu-id="9c6de-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c6de-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c6de-121">-Name</span></span>
<span data-ttu-id="9c6de-122">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="9c6de-122">Topic Name.</span></span>

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

### <span data-ttu-id="9c6de-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9c6de-123">-Namespace</span></span>
<span data-ttu-id="9c6de-124">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="9c6de-124">Namespace Name.</span></span>

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

### <span data-ttu-id="9c6de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c6de-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c6de-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9c6de-126">The name of the resource group</span></span>

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

### <span data-ttu-id="9c6de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6de-127">CommonParameters</span></span>
<span data-ttu-id="9c6de-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c6de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6de-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c6de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6de-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9c6de-130">INPUTS</span></span>

### <span data-ttu-id="9c6de-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c6de-131">-ResourceGroup</span></span>
 <span data-ttu-id="9c6de-132">System.object</span><span class="sxs-lookup"><span data-stu-id="9c6de-132">System.String</span></span>

### <span data-ttu-id="9c6de-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9c6de-133">-NamespaceName</span></span>
 <span data-ttu-id="9c6de-134">System.object</span><span class="sxs-lookup"><span data-stu-id="9c6de-134">System.String</span></span>

### <span data-ttu-id="9c6de-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="9c6de-135">-TopicName</span></span>
 <span data-ttu-id="9c6de-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9c6de-136">System.String</span></span>

### <span data-ttu-id="9c6de-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="9c6de-137">-TopicObj</span></span>
 <span data-ttu-id="9c6de-138">TopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9c6de-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="9c6de-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9c6de-139">OUTPUTS</span></span>

### <span data-ttu-id="9c6de-140">TopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9c6de-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="9c6de-141">名稱： SB-Topic_exampl1 位置：美國西部 Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1 類型： AccessedAt： AutoDeleteOnIdle： 1/20/2017 3:18:54 AM：10675199.02：48： 05.4775807 EntityAvailabilityStatus： CreatedAt： 1/20/2017 3:16:41 AM CountDetails：： MessageCountDetails DefaultMessageTimeToLive：10675199.02： True 05.4775807： False DuplicateDetectionHistoryTimeWindow： True EnableBatchedOperations： False EnableExpress： 16384 EnablePartitioning： false EnableSubscriptionPartitioning： False FilteringMessagesBeforePublishing： IsAnonymousAccessible： 1 IsExpress： False MaxSizeInMegabytes： 1/20/2017 7:12:16 PM （假）： RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="9c6de-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="9c6de-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9c6de-142">NOTES</span></span>

## <span data-ttu-id="9c6de-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c6de-143">RELATED LINKS</span></span>

