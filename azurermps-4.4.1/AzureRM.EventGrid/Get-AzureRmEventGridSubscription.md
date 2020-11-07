---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 26e306c80f18f3e7d14ca073cfdedfbdc9e6567b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624825"
---
# <span data-ttu-id="57cfe-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="57cfe-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="57cfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="57cfe-103">取得事件訂閱的詳細資料，或取得目前 Azure 訂閱中的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57cfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="57cfe-104">SYNTAX</span></span>

### <span data-ttu-id="57cfe-105">EventSubscriptionTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57cfe-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57cfe-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cfe-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57cfe-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57cfe-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57cfe-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57cfe-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57cfe-109">說明</span><span class="sxs-lookup"><span data-stu-id="57cfe-109">DESCRIPTION</span></span>
<span data-ttu-id="57cfe-110">Get-AzureRmEventGridSubscription Cmdlet 會取得指定事件格線訂閱的詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="57cfe-111">如果提供了事件訂閱名稱，則會傳回單一事件格線訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57cfe-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="57cfe-112">如果未提供事件訂閱名稱，則會傳回所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="57cfe-113">示例</span><span class="sxs-lookup"><span data-stu-id="57cfe-113">EXAMPLES</span></span>

### <span data-ttu-id="57cfe-114">範例1</span><span class="sxs-lookup"><span data-stu-id="57cfe-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="57cfe-115">取得 \` \` \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的 \` \` 事件訂閱 EventSubscription1 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57cfe-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="57cfe-116">範例2</span><span class="sxs-lookup"><span data-stu-id="57cfe-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="57cfe-117">取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` \` \` ，包括完整的端點 URL （如果它是以 webhook 為基礎的事件訂閱）。</span><span class="sxs-lookup"><span data-stu-id="57cfe-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="57cfe-118">範例3</span><span class="sxs-lookup"><span data-stu-id="57cfe-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="57cfe-119">取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 所建立的所有活動訂閱 \` 清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="57cfe-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="57cfe-120">範例4</span><span class="sxs-lookup"><span data-stu-id="57cfe-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="57cfe-121">取得 \` \` 針對資源群組 MyResourceGroupName 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="57cfe-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="57cfe-122">範例5</span><span class="sxs-lookup"><span data-stu-id="57cfe-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="57cfe-123">取得 \` \` 目前所選 Azure 訂閱所建立之事件訂閱 EventSubscription1 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57cfe-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="57cfe-124">範例6</span><span class="sxs-lookup"><span data-stu-id="57cfe-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="57cfe-125">取得在資源群組 MyResourceGroupName 下所建立的所有全域事件訂閱 \` 清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="57cfe-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="57cfe-126">範例7</span><span class="sxs-lookup"><span data-stu-id="57cfe-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="57cfe-127">取得在目前選取的 Azure 訂閱中建立的所有全域事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="57cfe-128">範例8</span><span class="sxs-lookup"><span data-stu-id="57cfe-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="57cfe-129">取得在 \` \` 指定位置 westus2 中的 [資源群組 MyResourceGroupName] 下所建立的所有區域事件訂閱清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="57cfe-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="57cfe-130">範例9</span><span class="sxs-lookup"><span data-stu-id="57cfe-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="57cfe-131">取得針對指定 EventHub 命名空間所建立之所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="57cfe-132">範例10</span><span class="sxs-lookup"><span data-stu-id="57cfe-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="57cfe-133">取得在指定位置 (EventHub 命名空間) 中為指定主題類型所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="57cfe-134">範例11</span><span class="sxs-lookup"><span data-stu-id="57cfe-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="57cfe-135">取得針對特定資源群組所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="57cfe-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="57cfe-136">參數</span><span class="sxs-lookup"><span data-stu-id="57cfe-136">PARAMETERS</span></span>

### <span data-ttu-id="57cfe-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="57cfe-137">-EventSubscriptionName</span></span>
<span data-ttu-id="57cfe-138">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="57cfe-138">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-139">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="57cfe-139">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="57cfe-140">包含事件訂閱目的地的完整端點 URL。</span><span class="sxs-lookup"><span data-stu-id="57cfe-140">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57cfe-141">-InputObject</span></span>
<span data-ttu-id="57cfe-142">EventGrid 事件訂閱物件。</span><span class="sxs-lookup"><span data-stu-id="57cfe-142">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="57cfe-143">-位置</span><span class="sxs-lookup"><span data-stu-id="57cfe-143">-Location</span></span>
<span data-ttu-id="57cfe-144">位於</span><span class="sxs-lookup"><span data-stu-id="57cfe-144">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57cfe-145">-ResourceGroupName</span></span>
<span data-ttu-id="57cfe-146">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="57cfe-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57cfe-147">-ResourceId</span></span>
<span data-ttu-id="57cfe-148">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57cfe-148">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="57cfe-149">-TopicName</span></span>
<span data-ttu-id="57cfe-150">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="57cfe-150">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-151">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="57cfe-151">-TopicTypeName</span></span>
<span data-ttu-id="57cfe-152">TopicType 名稱</span><span class="sxs-lookup"><span data-stu-id="57cfe-152">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57cfe-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cfe-153">-DefaultProfile</span></span>
<span data-ttu-id="57cfe-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57cfe-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57cfe-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cfe-155">CommonParameters</span></span>
<span data-ttu-id="57cfe-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57cfe-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cfe-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57cfe-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cfe-158">輸入</span><span class="sxs-lookup"><span data-stu-id="57cfe-158">INPUTS</span></span>

### <span data-ttu-id="57cfe-159">System.object</span><span class="sxs-lookup"><span data-stu-id="57cfe-159">System.String</span></span>
<span data-ttu-id="57cfe-160">PSEventSubscription EventGrid. SwitchParameter （）的功能。</span><span class="sxs-lookup"><span data-stu-id="57cfe-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57cfe-161">輸出</span><span class="sxs-lookup"><span data-stu-id="57cfe-161">OUTPUTS</span></span>

### <span data-ttu-id="57cfe-162">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="57cfe-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="57cfe-163">[System.object]。清單 ' 1 [EventGrid. PSEventSubscriptionListInstance，EventGrid，版本 = 1.0.0.0，Culture = 非特定，PublicKeyToken = null]] （限）</span><span class="sxs-lookup"><span data-stu-id="57cfe-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="57cfe-164">筆記</span><span class="sxs-lookup"><span data-stu-id="57cfe-164">NOTES</span></span>

## <span data-ttu-id="57cfe-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="57cfe-165">RELATED LINKS</span></span>

