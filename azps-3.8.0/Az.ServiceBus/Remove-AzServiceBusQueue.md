---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 6a2ba59acb8148cc3640582b57772a68014177ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957234"
---
# <span data-ttu-id="ca85a-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ca85a-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="ca85a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca85a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca85a-103">從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="ca85a-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca85a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca85a-104">SYNTAX</span></span>

### <span data-ttu-id="ca85a-105">QueuePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca85a-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca85a-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca85a-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca85a-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca85a-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca85a-108">說明</span><span class="sxs-lookup"><span data-stu-id="ca85a-108">DESCRIPTION</span></span>
<span data-ttu-id="ca85a-109">**AzServiceBusQueue** Cmdlet 會從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="ca85a-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca85a-110">示例</span><span class="sxs-lookup"><span data-stu-id="ca85a-110">EXAMPLES</span></span>

### <span data-ttu-id="ca85a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ca85a-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="ca85a-112">從命名空間移除服務匯流排佇列 `SB-Queue_exampl1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="ca85a-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ca85a-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="ca85a-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="ca85a-114">移除在-InputObject 參數 $inputobject 中提供的服務匯流排佇列</span><span class="sxs-lookup"><span data-stu-id="ca85a-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="ca85a-115">範例 2.1-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="ca85a-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="ca85a-116">範例 3.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="ca85a-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="ca85a-117">移除 $resourceid/string 中的 ARM id 提供的服務匯流排佇列（在 ResourceId 參數中）</span><span class="sxs-lookup"><span data-stu-id="ca85a-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="ca85a-118">範例 3.2-ResourceId-傳遞成字串：</span><span class="sxs-lookup"><span data-stu-id="ca85a-118">Example 3.2 - ResourceId - passing as string:</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="ca85a-119">參數</span><span class="sxs-lookup"><span data-stu-id="ca85a-119">PARAMETERS</span></span>

### <span data-ttu-id="ca85a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca85a-120">-AsJob</span></span>
<span data-ttu-id="ca85a-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca85a-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca85a-122">-DefaultProfile</span></span>
<span data-ttu-id="ca85a-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca85a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca85a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca85a-124">-InputObject</span></span>
<span data-ttu-id="ca85a-125">服務匯流排佇列物件</span><span class="sxs-lookup"><span data-stu-id="ca85a-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca85a-126">-Name</span></span>
<span data-ttu-id="ca85a-127">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="ca85a-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ca85a-128">-Namespace</span></span>
<span data-ttu-id="ca85a-129">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="ca85a-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca85a-130">-PassThru</span></span>
<span data-ttu-id="ca85a-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ca85a-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca85a-132">-ResourceGroupName</span></span>
<span data-ttu-id="ca85a-133">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ca85a-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca85a-134">-ResourceId</span></span>
<span data-ttu-id="ca85a-135">服務匯流排佇列資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ca85a-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="ca85a-136">-Confirm</span></span>
<span data-ttu-id="ca85a-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca85a-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca85a-138">-WhatIf</span></span>
<span data-ttu-id="ca85a-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca85a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca85a-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca85a-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca85a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca85a-141">CommonParameters</span></span>
<span data-ttu-id="ca85a-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca85a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca85a-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca85a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca85a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ca85a-144">INPUTS</span></span>

### <span data-ttu-id="ca85a-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ca85a-145">System.String</span></span>

### <span data-ttu-id="ca85a-146">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca85a-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ca85a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ca85a-147">OUTPUTS</span></span>

### <span data-ttu-id="ca85a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="ca85a-148">System.Boolean</span></span>

## <span data-ttu-id="ca85a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="ca85a-149">NOTES</span></span>

## <span data-ttu-id="ca85a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca85a-150">RELATED LINKS</span></span>
