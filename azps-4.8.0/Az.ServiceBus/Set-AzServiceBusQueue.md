---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969051"
---
# <span data-ttu-id="ab8df-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ab8df-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="ab8df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab8df-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8df-103">更新指定服務匯流排命名空間中服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="ab8df-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ab8df-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab8df-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab8df-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab8df-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8df-106">**AzServiceBusQueue** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="ab8df-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ab8df-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab8df-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8df-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ab8df-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="ab8df-109">使用指定命名空間中的新描述更新指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="ab8df-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="ab8df-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **True** ，然後 **SupportOrdering** 為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="ab8df-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="ab8df-111">參數</span><span class="sxs-lookup"><span data-stu-id="ab8df-111">PARAMETERS</span></span>

### <span data-ttu-id="ab8df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8df-112">-DefaultProfile</span></span>
<span data-ttu-id="ab8df-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab8df-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab8df-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab8df-114">-InputObject</span></span>
<span data-ttu-id="ab8df-115">未定義的定義。</span><span class="sxs-lookup"><span data-stu-id="ab8df-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8df-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab8df-116">-Name</span></span>
<span data-ttu-id="ab8df-117">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="ab8df-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8df-118">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ab8df-118">-Namespace</span></span>
<span data-ttu-id="ab8df-119">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ab8df-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ab8df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8df-120">-ResourceGroupName</span></span>
<span data-ttu-id="ab8df-121">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ab8df-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ab8df-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ab8df-122">-Confirm</span></span>
<span data-ttu-id="ab8df-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab8df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8df-124">-WhatIf</span></span>
<span data-ttu-id="ab8df-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab8df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab8df-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab8df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8df-127">CommonParameters</span></span>
<span data-ttu-id="ab8df-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab8df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8df-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab8df-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8df-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ab8df-130">INPUTS</span></span>

### <span data-ttu-id="ab8df-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ab8df-131">System.String</span></span>

### <span data-ttu-id="ab8df-132">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab8df-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ab8df-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ab8df-133">OUTPUTS</span></span>

### <span data-ttu-id="ab8df-134">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab8df-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ab8df-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ab8df-135">NOTES</span></span>

## <span data-ttu-id="ab8df-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab8df-136">RELATED LINKS</span></span>