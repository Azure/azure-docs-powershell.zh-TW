---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626661"
---
# <span data-ttu-id="25cdc-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="25cdc-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="25cdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="25cdc-103">取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="25cdc-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25cdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="25cdc-104">SYNTAX</span></span>

### <span data-ttu-id="25cdc-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="25cdc-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25cdc-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cdc-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25cdc-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cdc-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25cdc-108">說明</span><span class="sxs-lookup"><span data-stu-id="25cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="25cdc-109">Get-AzureRmEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="25cdc-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="25cdc-110">如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="25cdc-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="25cdc-111">如果未提供主題名稱，則會傳回主題的清單。</span><span class="sxs-lookup"><span data-stu-id="25cdc-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="25cdc-112">示例</span><span class="sxs-lookup"><span data-stu-id="25cdc-112">EXAMPLES</span></span>

### <span data-ttu-id="25cdc-113">範例1</span><span class="sxs-lookup"><span data-stu-id="25cdc-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="25cdc-114">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="25cdc-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="25cdc-115">範例2</span><span class="sxs-lookup"><span data-stu-id="25cdc-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="25cdc-116">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="25cdc-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="25cdc-117">範例3</span><span class="sxs-lookup"><span data-stu-id="25cdc-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="25cdc-118">列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="25cdc-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="25cdc-119">範例4</span><span class="sxs-lookup"><span data-stu-id="25cdc-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="25cdc-120">列出訂閱中的所有事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="25cdc-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="25cdc-121">參數</span><span class="sxs-lookup"><span data-stu-id="25cdc-121">PARAMETERS</span></span>

### <span data-ttu-id="25cdc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cdc-122">-DefaultProfile</span></span>
<span data-ttu-id="25cdc-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="25cdc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25cdc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="25cdc-124">-Name</span></span>
<span data-ttu-id="25cdc-125">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="25cdc-125">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cdc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cdc-126">-ResourceGroupName</span></span>
<span data-ttu-id="25cdc-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="25cdc-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cdc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25cdc-128">-ResourceId</span></span>
<span data-ttu-id="25cdc-129">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="25cdc-129">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cdc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cdc-130">CommonParameters</span></span>
<span data-ttu-id="25cdc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25cdc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cdc-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25cdc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cdc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="25cdc-133">INPUTS</span></span>

### <span data-ttu-id="25cdc-134">System.object</span><span class="sxs-lookup"><span data-stu-id="25cdc-134">System.String</span></span>
<span data-ttu-id="25cdc-135">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="25cdc-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="25cdc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="25cdc-136">OUTPUTS</span></span>

### <span data-ttu-id="25cdc-137">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="25cdc-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="25cdc-138">[System.object]。清單 ' 1 [EventGrid. PSTopicListInstance，EventGrid，版本 = 1.0.0.0，Culture = 非特定，PublicKeyToken = null]] （限）</span><span class="sxs-lookup"><span data-stu-id="25cdc-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="25cdc-139">筆記</span><span class="sxs-lookup"><span data-stu-id="25cdc-139">NOTES</span></span>

## <span data-ttu-id="25cdc-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="25cdc-140">RELATED LINKS</span></span>

