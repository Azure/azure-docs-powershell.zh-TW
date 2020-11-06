---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453520"
---
# <span data-ttu-id="1f380-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="1f380-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="1f380-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f380-102">SYNOPSIS</span></span>
<span data-ttu-id="1f380-103">取得事件格線主題的詳細資料，或取得目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="1f380-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f380-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f380-104">SYNTAX</span></span>

### <span data-ttu-id="1f380-105">ResourceGroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f380-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f380-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f380-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f380-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f380-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f380-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f380-108">DESCRIPTION</span></span>
<span data-ttu-id="1f380-109">Get-AzureRmEventGridTopic Cmdlet 會取得指定事件格線主題的詳細資料，或目前 Azure 訂閱中所有事件格線主題的清單。</span><span class="sxs-lookup"><span data-stu-id="1f380-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="1f380-110">如果提供主題名稱，則會傳回單一事件格線主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1f380-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="1f380-111">如果未提供主題名稱，則會傳回主題的清單。</span><span class="sxs-lookup"><span data-stu-id="1f380-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="1f380-112">示例</span><span class="sxs-lookup"><span data-stu-id="1f380-112">EXAMPLES</span></span>

### <span data-ttu-id="1f380-113">範例1</span><span class="sxs-lookup"><span data-stu-id="1f380-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="1f380-114">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="1f380-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1f380-115">範例2</span><span class="sxs-lookup"><span data-stu-id="1f380-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="1f380-116">取得 \` \` 資源群組 MyResourceGroupName 中 Topic1 事件網格主題的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="1f380-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1f380-117">範例3</span><span class="sxs-lookup"><span data-stu-id="1f380-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="1f380-118">列出 [資源群組 MyResourceGroupName] 中的所有事件格線主題 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="1f380-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1f380-119">範例4</span><span class="sxs-lookup"><span data-stu-id="1f380-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="1f380-120">列出訂閱中的所有事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="1f380-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="1f380-121">參數</span><span class="sxs-lookup"><span data-stu-id="1f380-121">PARAMETERS</span></span>

### <span data-ttu-id="1f380-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f380-122">-Name</span></span>
<span data-ttu-id="1f380-123">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="1f380-123">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="1f380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f380-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f380-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1f380-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f380-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f380-126">-ResourceId</span></span>
<span data-ttu-id="1f380-127">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f380-127">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="1f380-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f380-128">-DefaultProfile</span></span>
<span data-ttu-id="1f380-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f380-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f380-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f380-130">CommonParameters</span></span>
<span data-ttu-id="1f380-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f380-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f380-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f380-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f380-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1f380-133">INPUTS</span></span>

### <span data-ttu-id="1f380-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1f380-134">System.String</span></span>
<span data-ttu-id="1f380-135">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="1f380-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="1f380-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1f380-136">OUTPUTS</span></span>

### <span data-ttu-id="1f380-137">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="1f380-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="1f380-138">[System.object]。清單 ' 1 [EventGrid. PSTopicListInstance，EventGrid，版本 = 1.0.0.0，Culture = 非特定，PublicKeyToken = null]] （限）</span><span class="sxs-lookup"><span data-stu-id="1f380-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1f380-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1f380-139">NOTES</span></span>

## <span data-ttu-id="1f380-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f380-140">RELATED LINKS</span></span>

