---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130759"
---
# <span data-ttu-id="dfef3-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="dfef3-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="dfef3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfef3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfef3-103">更新指定服務匯流排命名空間中服務匯流排主題的描述。</span><span class="sxs-lookup"><span data-stu-id="dfef3-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dfef3-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfef3-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfef3-105">說明</span><span class="sxs-lookup"><span data-stu-id="dfef3-105">DESCRIPTION</span></span>
<span data-ttu-id="dfef3-106">**AzServiceBusTopic** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排主題的描述物件。</span><span class="sxs-lookup"><span data-stu-id="dfef3-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dfef3-107">示例</span><span class="sxs-lookup"><span data-stu-id="dfef3-107">EXAMPLES</span></span>

### <span data-ttu-id="dfef3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dfef3-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

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

<span data-ttu-id="dfef3-109">使用指定命名空間中的新描述更新指定主題。</span><span class="sxs-lookup"><span data-stu-id="dfef3-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="dfef3-110">這個範例會將 **EnableExpress** 屬性更新為 **true**。</span><span class="sxs-lookup"><span data-stu-id="dfef3-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="dfef3-111">參數</span><span class="sxs-lookup"><span data-stu-id="dfef3-111">PARAMETERS</span></span>

### <span data-ttu-id="dfef3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfef3-112">-DefaultProfile</span></span>
<span data-ttu-id="dfef3-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfef3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfef3-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfef3-114">-InputObject</span></span>
<span data-ttu-id="dfef3-115">[上的] 主題定義。</span><span class="sxs-lookup"><span data-stu-id="dfef3-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="dfef3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfef3-116">-Name</span></span>
<span data-ttu-id="dfef3-117">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="dfef3-117">Topic Name.</span></span>

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

### <span data-ttu-id="dfef3-118">-命名空間</span><span class="sxs-lookup"><span data-stu-id="dfef3-118">-Namespace</span></span>
<span data-ttu-id="dfef3-119">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="dfef3-119">Namespace Name.</span></span>

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

### <span data-ttu-id="dfef3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfef3-120">-ResourceGroupName</span></span>
<span data-ttu-id="dfef3-121">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="dfef3-121">The name of the resource group</span></span>

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

### <span data-ttu-id="dfef3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="dfef3-122">-Confirm</span></span>
<span data-ttu-id="dfef3-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dfef3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfef3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfef3-124">-WhatIf</span></span>
<span data-ttu-id="dfef3-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dfef3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfef3-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfef3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfef3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfef3-127">CommonParameters</span></span>
<span data-ttu-id="dfef3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfef3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfef3-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dfef3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfef3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dfef3-130">INPUTS</span></span>

### <span data-ttu-id="dfef3-131">System.object</span><span class="sxs-lookup"><span data-stu-id="dfef3-131">System.String</span></span>

### <span data-ttu-id="dfef3-132">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dfef3-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="dfef3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="dfef3-133">OUTPUTS</span></span>

### <span data-ttu-id="dfef3-134">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dfef3-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="dfef3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dfef3-135">NOTES</span></span>

## <span data-ttu-id="dfef3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfef3-136">RELATED LINKS</span></span>
