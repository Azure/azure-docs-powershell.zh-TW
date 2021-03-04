---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 3fdd10ea83efb68b33d6936a84d32e940df71e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909333"
---
# <span data-ttu-id="81d6b-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="81d6b-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="81d6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="81d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="81d6b-103">更新指定 Service Bus 命名空間中服務母線佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="81d6b-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="81d6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="81d6b-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d6b-105">描述</span><span class="sxs-lookup"><span data-stu-id="81d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="81d6b-106">**Set-AzServiceBusQueue** Cmdlet 會更新指定 Service Bus 命名空間中服務Bus佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="81d6b-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="81d6b-107">例子</span><span class="sxs-lookup"><span data-stu-id="81d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="81d6b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="81d6b-108">Example 1</span></span>
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

<span data-ttu-id="81d6b-109">使用指定命名空間中的新描述更新指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="81d6b-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="81d6b-110">此範例將 **DeadLetteringOnMessageExpiration** 屬性更新為 **True，** 而 **SupportOrdering 更新為** **True。**</span><span class="sxs-lookup"><span data-stu-id="81d6b-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="81d6b-111">參數</span><span class="sxs-lookup"><span data-stu-id="81d6b-111">PARAMETERS</span></span>

### <span data-ttu-id="81d6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d6b-112">-DefaultProfile</span></span>
<span data-ttu-id="81d6b-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="81d6b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d6b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d6b-114">-InputObject</span></span>
<span data-ttu-id="81d6b-115">ServiceBus 定義。</span><span class="sxs-lookup"><span data-stu-id="81d6b-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="81d6b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="81d6b-116">-Name</span></span>
<span data-ttu-id="81d6b-117">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="81d6b-117">Queue Name.</span></span>

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

### <span data-ttu-id="81d6b-118">-命名空間</span><span class="sxs-lookup"><span data-stu-id="81d6b-118">-Namespace</span></span>
<span data-ttu-id="81d6b-119">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="81d6b-119">Namespace Name.</span></span>

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

### <span data-ttu-id="81d6b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d6b-120">-ResourceGroupName</span></span>
<span data-ttu-id="81d6b-121">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="81d6b-121">The name of the resource group</span></span>

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

### <span data-ttu-id="81d6b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="81d6b-122">-Confirm</span></span>
<span data-ttu-id="81d6b-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="81d6b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d6b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d6b-124">-WhatIf</span></span>
<span data-ttu-id="81d6b-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81d6b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d6b-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81d6b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d6b-127">CommonParameters</span></span>
<span data-ttu-id="81d6b-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="81d6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d6b-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="81d6b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d6b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="81d6b-130">INPUTS</span></span>

### <span data-ttu-id="81d6b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="81d6b-131">System.String</span></span>

### <span data-ttu-id="81d6b-132">Microsoft.Azure.Commands.ServiceBus.models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="81d6b-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="81d6b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="81d6b-133">OUTPUTS</span></span>

### <span data-ttu-id="81d6b-134">Microsoft.Azure.Commands.ServiceBus.models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="81d6b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="81d6b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="81d6b-135">NOTES</span></span>

## <span data-ttu-id="81d6b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="81d6b-136">RELATED LINKS</span></span>
