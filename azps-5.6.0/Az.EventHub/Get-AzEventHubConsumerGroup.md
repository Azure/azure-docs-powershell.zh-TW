---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 4b34731c0cd0c2d49a7c26112d370d8d4a2f948e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903241"
---
# <span data-ttu-id="e83b9-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e83b9-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e83b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e83b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e83b9-103">獲得指定的事件中樞消費者群組詳細資料，或獲得事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="e83b9-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="e83b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e83b9-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e83b9-105">描述</span><span class="sxs-lookup"><span data-stu-id="e83b9-105">DESCRIPTION</span></span>
<span data-ttu-id="e83b9-106">Cmdlet Get-AzEventHubConsumerGroup會獲得指定的事件中樞消費者群組詳細資料，或特定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="e83b9-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="e83b9-107">如果提供消費者群組的名稱，則會返回單一消費者群組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e83b9-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="e83b9-108">如果未提供消費者群組的名稱，則會返回指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="e83b9-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="e83b9-109">例子</span><span class="sxs-lookup"><span data-stu-id="e83b9-109">EXAMPLES</span></span>

### <span data-ttu-id="e83b9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e83b9-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e83b9-111">在事件中樞 MyEventHubName 中，獲得消費者群組 \` MyConsumerGroupName，此名稱存在於命名空間 \` \` \` \` MyNamespaceName 與資源群組 \` \` MyResourceGroupName \` 中。</span><span class="sxs-lookup"><span data-stu-id="e83b9-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e83b9-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e83b9-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e83b9-113">在事件中樞 MyEventHubName 中，獲得消費者群組的清單，此名稱存在於命名空間 MyNamespaceName 與資源群組 \` \` \` \` \` MyResourceGroupName \` 中。</span><span class="sxs-lookup"><span data-stu-id="e83b9-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e83b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="e83b9-114">PARAMETERS</span></span>

### <span data-ttu-id="e83b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83b9-115">-DefaultProfile</span></span>
<span data-ttu-id="e83b9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e83b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e83b9-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e83b9-117">-EventHub</span></span>
<span data-ttu-id="e83b9-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="e83b9-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83b9-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e83b9-119">-MaxCount</span></span>
<span data-ttu-id="e83b9-120">決定要退回的 ConsumerGroup 數量上限。</span><span class="sxs-lookup"><span data-stu-id="e83b9-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e83b9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e83b9-121">-Name</span></span>
<span data-ttu-id="e83b9-122">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="e83b9-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83b9-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e83b9-123">-Namespace</span></span>
<span data-ttu-id="e83b9-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e83b9-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e83b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e83b9-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="e83b9-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83b9-127">CommonParameters</span></span>
<span data-ttu-id="e83b9-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e83b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83b9-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e83b9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83b9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e83b9-130">INPUTS</span></span>

### <span data-ttu-id="e83b9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e83b9-131">System.String</span></span>

## <span data-ttu-id="e83b9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e83b9-132">OUTPUTS</span></span>

### <span data-ttu-id="e83b9-133">Microsoft.Azure.Commands.EventHub.models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e83b9-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e83b9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e83b9-134">NOTES</span></span>

## <span data-ttu-id="e83b9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e83b9-135">RELATED LINKS</span></span>
