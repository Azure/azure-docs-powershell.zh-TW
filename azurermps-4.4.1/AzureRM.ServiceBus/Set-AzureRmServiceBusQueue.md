---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455595"
---
# <span data-ttu-id="ec47c-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ec47c-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="ec47c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec47c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec47c-103">更新指定服務匯流排命名空間中服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="ec47c-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec47c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec47c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec47c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec47c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec47c-106">**AzureRmServiceBusQueue** Cmdlet 會更新指定服務匯流排命名空間中服務匯流排佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="ec47c-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ec47c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec47c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec47c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ec47c-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="ec47c-109">使用指定命名空間中的新描述更新指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="ec47c-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="ec47c-110">這個範例會將 **DeadLetteringOnMessageExpiration** 屬性更新為 **True** ，然後 **SupportOrdering** 為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="ec47c-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="ec47c-111">參數</span><span class="sxs-lookup"><span data-stu-id="ec47c-111">PARAMETERS</span></span>

### <span data-ttu-id="ec47c-112">-確認</span><span class="sxs-lookup"><span data-stu-id="ec47c-112">-Confirm</span></span>
<span data-ttu-id="ec47c-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec47c-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec47c-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec47c-114">-WhatIf</span></span>
<span data-ttu-id="ec47c-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec47c-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec47c-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec47c-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec47c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec47c-117">-DefaultProfile</span></span>
<span data-ttu-id="ec47c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec47c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec47c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec47c-119">-InputObject</span></span>
<span data-ttu-id="ec47c-120">未定義的定義。</span><span class="sxs-lookup"><span data-stu-id="ec47c-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec47c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec47c-121">-Name</span></span>
<span data-ttu-id="ec47c-122">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="ec47c-122">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec47c-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ec47c-123">-Namespace</span></span>
<span data-ttu-id="ec47c-124">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ec47c-124">Namespace Name.</span></span>

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

### <span data-ttu-id="ec47c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec47c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec47c-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ec47c-126">The name of the resource group</span></span>

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

### <span data-ttu-id="ec47c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec47c-127">CommonParameters</span></span>
<span data-ttu-id="ec47c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec47c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec47c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec47c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec47c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ec47c-130">INPUTS</span></span>

### <span data-ttu-id="ec47c-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec47c-131">-ResourceGroup</span></span>
 <span data-ttu-id="ec47c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ec47c-132">System.String</span></span>

### <span data-ttu-id="ec47c-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ec47c-133">-NamespaceName</span></span>
 <span data-ttu-id="ec47c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ec47c-134">System.String</span></span>

### <span data-ttu-id="ec47c-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="ec47c-135">-QueueName</span></span>
 <span data-ttu-id="ec47c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ec47c-136">System.String</span></span>

### <span data-ttu-id="ec47c-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="ec47c-137">-QueueObj</span></span>
 <span data-ttu-id="ec47c-138">QueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec47c-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="ec47c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ec47c-139">OUTPUTS</span></span>

### <span data-ttu-id="ec47c-140">QueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec47c-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="ec47c-141">名稱： SB-Queue_exampl1 位置：美國西部 LockDuration： AccessedAt： 1/1/0001 12:00:00 AM AutoDeleteOnIdle：10675199.02：48： 1/20/2017 2:51:34 EntityAvailabilityStatus： CreatedAt： AM DefaultMessageTimeToLive： False 10675199.02： False 05.4775807： True DuplicateDetectionHistoryTimeWindow： False EnableBatchedOperations： DeadLetteringOnMessageExpiration： 16384 EnableExpress： EnablePartitioning： IsAnonymousAccessible： False MaxDeliveryCount： Status： MaxSizeInMegabytes： False MessageCount： 1/20/2017 6:16:18 PM</span><span class="sxs-lookup"><span data-stu-id="ec47c-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="ec47c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ec47c-142">NOTES</span></span>

## <span data-ttu-id="ec47c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec47c-143">RELATED LINKS</span></span>
