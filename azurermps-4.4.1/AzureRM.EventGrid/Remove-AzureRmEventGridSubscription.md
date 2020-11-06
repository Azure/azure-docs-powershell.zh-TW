---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456700"
---
# <span data-ttu-id="496c5-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="496c5-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="496c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="496c5-102">SYNOPSIS</span></span>
<span data-ttu-id="496c5-103">移除 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="496c5-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="496c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="496c5-104">SYNTAX</span></span>

### <span data-ttu-id="496c5-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="496c5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496c5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="496c5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496c5-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="496c5-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496c5-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="496c5-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="496c5-109">說明</span><span class="sxs-lookup"><span data-stu-id="496c5-109">DESCRIPTION</span></span>
<span data-ttu-id="496c5-110">移除 Azure 事件格線主題、資源、Azure 訂閱或資源群組的 Azure 事件格線事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="496c5-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="496c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="496c5-111">EXAMPLES</span></span>

### <span data-ttu-id="496c5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="496c5-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="496c5-113">移除 [ \` \` \` 資源群組 MyResourceGroupName] 中 Topic1 Azure 事件格線主題的事件訂閱 EventSubscription1 \` \` \` 。</span><span class="sxs-lookup"><span data-stu-id="496c5-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="496c5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="496c5-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="496c5-115">移除 \` \` 資源群組 MyResourceGroupName 的事件訂閱 EventSubscription1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="496c5-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="496c5-116">範例3</span><span class="sxs-lookup"><span data-stu-id="496c5-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="496c5-117">移除 \` 預設 Azure 訂閱 EventSubscription1 的事件訂閱 \` 。</span><span class="sxs-lookup"><span data-stu-id="496c5-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="496c5-118">範例4</span><span class="sxs-lookup"><span data-stu-id="496c5-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="496c5-119">移除 \` \` 事件中心命名空間的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="496c5-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="496c5-120">範例5</span><span class="sxs-lookup"><span data-stu-id="496c5-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="496c5-121">移除 \` \` 事件格線主題的事件訂閱 EventSubscription1。</span><span class="sxs-lookup"><span data-stu-id="496c5-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="496c5-122">參數</span><span class="sxs-lookup"><span data-stu-id="496c5-122">PARAMETERS</span></span>

### <span data-ttu-id="496c5-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="496c5-123">-EventSubscriptionName</span></span>
<span data-ttu-id="496c5-124">需要移除之事件訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="496c5-124">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496c5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="496c5-125">-InputObject</span></span>
<span data-ttu-id="496c5-126">EventGrid EventSubscription 物件。</span><span class="sxs-lookup"><span data-stu-id="496c5-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="496c5-127">-PassThru</span></span>
<span data-ttu-id="496c5-128">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="496c5-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="496c5-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="496c5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="496c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="496c5-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="496c5-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496c5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="496c5-132">-ResourceId</span></span>
<span data-ttu-id="496c5-133">需要移除其事件訂閱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="496c5-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496c5-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="496c5-134">-TopicName</span></span>
<span data-ttu-id="496c5-135">事件格線主題名稱。</span><span class="sxs-lookup"><span data-stu-id="496c5-135">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496c5-136">-確認</span><span class="sxs-lookup"><span data-stu-id="496c5-136">-Confirm</span></span>
<span data-ttu-id="496c5-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="496c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496c5-138">-WhatIf</span></span>
<span data-ttu-id="496c5-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="496c5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496c5-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="496c5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496c5-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496c5-141">-DefaultProfile</span></span>
<span data-ttu-id="496c5-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="496c5-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="496c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496c5-143">CommonParameters</span></span>
<span data-ttu-id="496c5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="496c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496c5-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="496c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496c5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="496c5-146">INPUTS</span></span>

### <span data-ttu-id="496c5-147">System.object</span><span class="sxs-lookup"><span data-stu-id="496c5-147">System.String</span></span>
<span data-ttu-id="496c5-148">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="496c5-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="496c5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="496c5-149">OUTPUTS</span></span>

### <span data-ttu-id="496c5-150">System.object</span><span class="sxs-lookup"><span data-stu-id="496c5-150">System.Object</span></span>

## <span data-ttu-id="496c5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="496c5-151">NOTES</span></span>

## <span data-ttu-id="496c5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="496c5-152">RELATED LINKS</span></span>

