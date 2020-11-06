---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622326"
---
# <span data-ttu-id="c268d-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c268d-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="c268d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c268d-102">SYNOPSIS</span></span>
<span data-ttu-id="c268d-103">取得事件訂閱的詳細資料，或取得目前 Azure 訂閱中的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="c268d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c268d-104">SYNTAX</span></span>

### <span data-ttu-id="c268d-105">EventSubscriptionTopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c268d-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c268d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c268d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c268d-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c268d-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c268d-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c268d-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c268d-109">說明</span><span class="sxs-lookup"><span data-stu-id="c268d-109">DESCRIPTION</span></span>
<span data-ttu-id="c268d-110">Get-AzEventGridSubscription Cmdlet 會取得指定事件格線訂閱的詳細資料，或目前 Azure 訂閱或資源群組中所有事件格線訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="c268d-111">如果提供了事件訂閱名稱，則會傳回單一事件格線訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c268d-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="c268d-112">如果未提供事件訂閱名稱，則會傳回所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="c268d-113">示例</span><span class="sxs-lookup"><span data-stu-id="c268d-113">EXAMPLES</span></span>

### <span data-ttu-id="c268d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c268d-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c268d-115">取得 \` \` \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的 \` \` 事件訂閱 EventSubscription1 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c268d-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c268d-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c268d-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="c268d-117">取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` \` \` ，包括完整的端點 URL （如果它是以 webhook 為基礎的事件訂閱）。</span><span class="sxs-lookup"><span data-stu-id="c268d-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="c268d-118">範例3</span><span class="sxs-lookup"><span data-stu-id="c268d-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="c268d-119">取得 \` \` 在資源群組 MyResourceGroupName 中針對主題 Topic1 所建立的所有活動訂閱 \` 清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="c268d-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c268d-120">範例4</span><span class="sxs-lookup"><span data-stu-id="c268d-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c268d-121">取得 \` \` 針對資源群組 MyResourceGroupName 建立的事件訂閱 EventSubscription1 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c268d-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c268d-122">範例5</span><span class="sxs-lookup"><span data-stu-id="c268d-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c268d-123">取得 \` \` 目前所選 Azure 訂閱所建立之事件訂閱 EventSubscription1 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c268d-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c268d-124">範例6</span><span class="sxs-lookup"><span data-stu-id="c268d-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c268d-125">取得在資源群組 MyResourceGroupName 下所建立的所有全域事件訂閱 \` 清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="c268d-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c268d-126">範例7</span><span class="sxs-lookup"><span data-stu-id="c268d-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="c268d-127">取得在目前選取的 Azure 訂閱中建立的所有全域事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c268d-128">範例8</span><span class="sxs-lookup"><span data-stu-id="c268d-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="c268d-129">取得在 \` \` 指定位置 westus2 中的 [資源群組 MyResourceGroupName] 下所建立的所有區域事件訂閱清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c268d-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="c268d-130">範例9</span><span class="sxs-lookup"><span data-stu-id="c268d-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="c268d-131">取得針對指定 EventHub 命名空間所建立之所有事件訂閱的清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="c268d-132">範例10</span><span class="sxs-lookup"><span data-stu-id="c268d-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="c268d-133">取得在指定位置 (EventHub 命名空間) 中為指定主題類型所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="c268d-134">範例11</span><span class="sxs-lookup"><span data-stu-id="c268d-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c268d-135">取得針對特定資源群組所建立的所有事件訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="c268d-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="c268d-136">參數</span><span class="sxs-lookup"><span data-stu-id="c268d-136">PARAMETERS</span></span>

### <span data-ttu-id="c268d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c268d-137">-DefaultProfile</span></span>
<span data-ttu-id="c268d-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c268d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c268d-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c268d-139">-EventSubscriptionName</span></span>
<span data-ttu-id="c268d-140">事件訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="c268d-140">The name of the event subscription</span></span>

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

### <span data-ttu-id="c268d-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c268d-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="c268d-142">包含事件訂閱目的地的完整端點 URL。</span><span class="sxs-lookup"><span data-stu-id="c268d-142">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="c268d-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c268d-143">-InputObject</span></span>
<span data-ttu-id="c268d-144">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="c268d-144">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c268d-145">-位置</span><span class="sxs-lookup"><span data-stu-id="c268d-145">-Location</span></span>
<span data-ttu-id="c268d-146">位於</span><span class="sxs-lookup"><span data-stu-id="c268d-146">Location</span></span>

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

### <span data-ttu-id="c268d-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c268d-147">-ResourceGroupName</span></span>
<span data-ttu-id="c268d-148">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c268d-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="c268d-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c268d-149">-ResourceId</span></span>
<span data-ttu-id="c268d-150">已建立事件訂閱之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c268d-150">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="c268d-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c268d-151">-TopicName</span></span>
<span data-ttu-id="c268d-152">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="c268d-152">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c268d-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="c268d-153">-TopicTypeName</span></span>
<span data-ttu-id="c268d-154">TopicType 名稱</span><span class="sxs-lookup"><span data-stu-id="c268d-154">TopicType name</span></span>

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

### <span data-ttu-id="c268d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c268d-155">CommonParameters</span></span>
<span data-ttu-id="c268d-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c268d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c268d-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c268d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c268d-158">輸入</span><span class="sxs-lookup"><span data-stu-id="c268d-158">INPUTS</span></span>

### <span data-ttu-id="c268d-159">System.object</span><span class="sxs-lookup"><span data-stu-id="c268d-159">System.String</span></span>

### <span data-ttu-id="c268d-160">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c268d-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c268d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="c268d-161">OUTPUTS</span></span>

### <span data-ttu-id="c268d-162">PSEventSubscription 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="c268d-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c268d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="c268d-163">NOTES</span></span>

## <span data-ttu-id="c268d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="c268d-164">RELATED LINKS</span></span>
