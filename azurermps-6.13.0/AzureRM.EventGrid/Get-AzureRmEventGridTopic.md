---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 2d18e923e14caf4c0048575465e9f52fb14596f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445612"
---
# <span data-ttu-id="cf589-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="cf589-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="cf589-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf589-102">SYNOPSIS</span></span>
<span data-ttu-id="cf589-103">取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="cf589-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf589-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf589-104">SYNTAX</span></span>

### <span data-ttu-id="cf589-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf589-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf589-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf589-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf589-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf589-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf589-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf589-108">DESCRIPTION</span></span>
<span data-ttu-id="cf589-109">Get-AzureRmEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="cf589-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="cf589-110">如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf589-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="cf589-111">如果未提供主題名稱，則會傳回主題的清單。</span><span class="sxs-lookup"><span data-stu-id="cf589-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="cf589-112">示例</span><span class="sxs-lookup"><span data-stu-id="cf589-112">EXAMPLES</span></span>

### <span data-ttu-id="cf589-113">範例1</span><span class="sxs-lookup"><span data-stu-id="cf589-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="cf589-114">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="cf589-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cf589-115">範例2</span><span class="sxs-lookup"><span data-stu-id="cf589-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="cf589-116">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="cf589-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cf589-117">範例3</span><span class="sxs-lookup"><span data-stu-id="cf589-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="cf589-118">列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="cf589-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cf589-119">範例4</span><span class="sxs-lookup"><span data-stu-id="cf589-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="cf589-120">列出訂閱中的所有事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="cf589-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="cf589-121">參數</span><span class="sxs-lookup"><span data-stu-id="cf589-121">PARAMETERS</span></span>

### <span data-ttu-id="cf589-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf589-122">-DefaultProfile</span></span>
<span data-ttu-id="cf589-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf589-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf589-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf589-124">-Name</span></span>
<span data-ttu-id="cf589-125">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="cf589-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="cf589-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf589-126">-ResourceGroupName</span></span>
<span data-ttu-id="cf589-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cf589-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cf589-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf589-128">-ResourceId</span></span>
<span data-ttu-id="cf589-129">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf589-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="cf589-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf589-130">CommonParameters</span></span>
<span data-ttu-id="cf589-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf589-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf589-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf589-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf589-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cf589-133">INPUTS</span></span>

### <span data-ttu-id="cf589-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cf589-134">System.String</span></span>

## <span data-ttu-id="cf589-135">輸出</span><span class="sxs-lookup"><span data-stu-id="cf589-135">OUTPUTS</span></span>

### <span data-ttu-id="cf589-136">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="cf589-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="cf589-137">PSTopicListInstance 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="cf589-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="cf589-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cf589-138">NOTES</span></span>

## <span data-ttu-id="cf589-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf589-139">RELATED LINKS</span></span>
