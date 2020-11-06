---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449744"
---
# <span data-ttu-id="9ca89-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9ca89-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="9ca89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ca89-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca89-103">從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="9ca89-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ca89-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ca89-104">SYNTAX</span></span>

### <span data-ttu-id="9ca89-105">QueuePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ca89-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca89-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ca89-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca89-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ca89-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca89-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ca89-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca89-109">**AzureRmServiceBusQueue** Cmdlet 會從指定的服務匯流排命名空間中移除佇列。</span><span class="sxs-lookup"><span data-stu-id="9ca89-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9ca89-110">示例</span><span class="sxs-lookup"><span data-stu-id="9ca89-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca89-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9ca89-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="9ca89-112">從命名空間移除服務匯流排佇列 `SB-Queue_exampl1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="9ca89-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="9ca89-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="9ca89-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="9ca89-114">移除在-InputObject 參數 $inputobject 中提供的服務匯流排佇列</span><span class="sxs-lookup"><span data-stu-id="9ca89-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="9ca89-115">範例 2.1-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="9ca89-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="9ca89-116">範例 3.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="9ca89-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="9ca89-117">移除 $resourceid/string 中的 ARM id 提供的服務匯流排佇列（在 ResourceId 參數中）</span><span class="sxs-lookup"><span data-stu-id="9ca89-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="9ca89-118">範例 3.2-ResourceId-passign as 字串：</span><span class="sxs-lookup"><span data-stu-id="9ca89-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="9ca89-119">參數</span><span class="sxs-lookup"><span data-stu-id="9ca89-119">PARAMETERS</span></span>

### <span data-ttu-id="9ca89-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ca89-120">-AsJob</span></span>
<span data-ttu-id="9ca89-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ca89-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ca89-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca89-122">-DefaultProfile</span></span>
<span data-ttu-id="9ca89-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ca89-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca89-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca89-124">-InputObject</span></span>
<span data-ttu-id="9ca89-125">服務匯流排佇列物件</span><span class="sxs-lookup"><span data-stu-id="9ca89-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="9ca89-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ca89-126">-Name</span></span>
<span data-ttu-id="9ca89-127">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="9ca89-127">Queue Name</span></span>

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

### <span data-ttu-id="9ca89-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9ca89-128">-Namespace</span></span>
<span data-ttu-id="9ca89-129">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="9ca89-129">Namespace Name</span></span>

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

### <span data-ttu-id="9ca89-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ca89-130">-PassThru</span></span>
<span data-ttu-id="9ca89-131">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="9ca89-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9ca89-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca89-132">-ResourceGroupName</span></span>
<span data-ttu-id="9ca89-133">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9ca89-133">The name of the resource group</span></span>

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

### <span data-ttu-id="9ca89-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca89-134">-ResourceId</span></span>
<span data-ttu-id="9ca89-135">服務匯流排佇列資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9ca89-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="9ca89-136">-確認</span><span class="sxs-lookup"><span data-stu-id="9ca89-136">-Confirm</span></span>
<span data-ttu-id="9ca89-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ca89-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca89-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca89-138">-WhatIf</span></span>
<span data-ttu-id="9ca89-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ca89-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca89-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ca89-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca89-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca89-141">CommonParameters</span></span>
<span data-ttu-id="9ca89-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ca89-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca89-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ca89-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca89-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9ca89-144">INPUTS</span></span>

### <span data-ttu-id="9ca89-145">System.object</span><span class="sxs-lookup"><span data-stu-id="9ca89-145">System.String</span></span>

### <span data-ttu-id="9ca89-146">PSQueueAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ca89-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="9ca89-147">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9ca89-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9ca89-148">輸出</span><span class="sxs-lookup"><span data-stu-id="9ca89-148">OUTPUTS</span></span>

### <span data-ttu-id="9ca89-149">System.object</span><span class="sxs-lookup"><span data-stu-id="9ca89-149">System.Boolean</span></span>

## <span data-ttu-id="9ca89-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9ca89-150">NOTES</span></span>

## <span data-ttu-id="9ca89-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ca89-151">RELATED LINKS</span></span>