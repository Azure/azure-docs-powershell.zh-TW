---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: b08b4d9bd201f8a29ef878a4aaa73c926eb47151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449740"
---
# <span data-ttu-id="7ca90-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7ca90-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7ca90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ca90-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca90-103">更新指定服務匯流排命名空間中服務匯流排主題的描述。</span><span class="sxs-lookup"><span data-stu-id="7ca90-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ca90-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ca90-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ca90-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ca90-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca90-106">**AzureRmServiceBusTopic** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的描述物件。</span><span class="sxs-lookup"><span data-stu-id="7ca90-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7ca90-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ca90-107">EXAMPLES</span></span>

### <span data-ttu-id="7ca90-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7ca90-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="7ca90-109">使用指定命名空間中的新描述更新指定主題。</span><span class="sxs-lookup"><span data-stu-id="7ca90-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="7ca90-110">這個範例會將 **EnableExpress** 屬性更新為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="7ca90-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="7ca90-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ca90-111">PARAMETERS</span></span>

### <span data-ttu-id="7ca90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca90-112">-DefaultProfile</span></span>
<span data-ttu-id="7ca90-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ca90-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca90-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca90-114">-InputObject</span></span>
<span data-ttu-id="7ca90-115">[上的] 主題定義。</span><span class="sxs-lookup"><span data-stu-id="7ca90-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca90-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ca90-116">-Name</span></span>
<span data-ttu-id="7ca90-117">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="7ca90-117">Topic Name.</span></span>

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

### <span data-ttu-id="7ca90-118">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7ca90-118">-Namespace</span></span>
<span data-ttu-id="7ca90-119">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7ca90-119">Namespace Name.</span></span>

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

### <span data-ttu-id="7ca90-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca90-120">-ResourceGroupName</span></span>
<span data-ttu-id="7ca90-121">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7ca90-121">The name of the resource group</span></span>

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

### <span data-ttu-id="7ca90-122">-確認</span><span class="sxs-lookup"><span data-stu-id="7ca90-122">-Confirm</span></span>
<span data-ttu-id="7ca90-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ca90-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca90-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca90-124">-WhatIf</span></span>
<span data-ttu-id="7ca90-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ca90-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca90-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ca90-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca90-127">CommonParameters</span></span>
<span data-ttu-id="7ca90-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ca90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca90-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ca90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca90-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7ca90-130">INPUTS</span></span>

### <span data-ttu-id="7ca90-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7ca90-131">System.String</span></span>

### <span data-ttu-id="7ca90-132">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ca90-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="7ca90-133">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7ca90-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7ca90-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7ca90-134">OUTPUTS</span></span>

### <span data-ttu-id="7ca90-135">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ca90-135">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="7ca90-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7ca90-136">NOTES</span></span>

## <span data-ttu-id="7ca90-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ca90-137">RELATED LINKS</span></span>
