---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622324"
---
# <span data-ttu-id="24421-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="24421-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="24421-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24421-102">SYNOPSIS</span></span>
<span data-ttu-id="24421-103">取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="24421-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="24421-104">句法</span><span class="sxs-lookup"><span data-stu-id="24421-104">SYNTAX</span></span>

### <span data-ttu-id="24421-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24421-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24421-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24421-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24421-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24421-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24421-108">說明</span><span class="sxs-lookup"><span data-stu-id="24421-108">DESCRIPTION</span></span>
<span data-ttu-id="24421-109">Get-AzEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="24421-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="24421-110">如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="24421-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="24421-111">如果未提供主題名稱，則會傳回主題的清單。</span><span class="sxs-lookup"><span data-stu-id="24421-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="24421-112">示例</span><span class="sxs-lookup"><span data-stu-id="24421-112">EXAMPLES</span></span>

### <span data-ttu-id="24421-113">範例1</span><span class="sxs-lookup"><span data-stu-id="24421-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="24421-114">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="24421-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="24421-115">範例2</span><span class="sxs-lookup"><span data-stu-id="24421-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="24421-116">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="24421-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="24421-117">範例3</span><span class="sxs-lookup"><span data-stu-id="24421-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="24421-118">列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="24421-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="24421-119">範例4</span><span class="sxs-lookup"><span data-stu-id="24421-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="24421-120">列出訂閱中的所有事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="24421-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="24421-121">參數</span><span class="sxs-lookup"><span data-stu-id="24421-121">PARAMETERS</span></span>

### <span data-ttu-id="24421-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24421-122">-DefaultProfile</span></span>
<span data-ttu-id="24421-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="24421-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24421-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="24421-124">-Name</span></span>
<span data-ttu-id="24421-125">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="24421-125">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24421-126">-ResourceGroupName</span></span>
<span data-ttu-id="24421-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="24421-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24421-128">-ResourceId</span></span>
<span data-ttu-id="24421-129">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24421-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="24421-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24421-130">CommonParameters</span></span>
<span data-ttu-id="24421-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24421-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24421-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24421-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24421-133">輸入</span><span class="sxs-lookup"><span data-stu-id="24421-133">INPUTS</span></span>

### <span data-ttu-id="24421-134">System.object</span><span class="sxs-lookup"><span data-stu-id="24421-134">System.String</span></span>

## <span data-ttu-id="24421-135">輸出</span><span class="sxs-lookup"><span data-stu-id="24421-135">OUTPUTS</span></span>

### <span data-ttu-id="24421-136">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="24421-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="24421-137">PSTopicListInstance 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="24421-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="24421-138">筆記</span><span class="sxs-lookup"><span data-stu-id="24421-138">NOTES</span></span>

## <span data-ttu-id="24421-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="24421-139">RELATED LINKS</span></span>
