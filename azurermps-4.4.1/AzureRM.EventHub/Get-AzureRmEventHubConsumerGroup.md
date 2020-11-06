---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456680"
---
# <span data-ttu-id="47f41-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47f41-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="47f41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47f41-102">SYNOPSIS</span></span>
<span data-ttu-id="47f41-103">取得指定事件中樞消費者群組的詳細資料，或取得事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="47f41-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47f41-104">句法</span><span class="sxs-lookup"><span data-stu-id="47f41-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="47f41-105">說明</span><span class="sxs-lookup"><span data-stu-id="47f41-105">DESCRIPTION</span></span>
<span data-ttu-id="47f41-106">Get-AzureRmEventHubConsumerGroup Cmdlet 會取得指定事件中樞消費者群組的詳細資料，或指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="47f41-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="47f41-107">如果提供消費者群組的名稱，則會傳回單一消費者群組詳細資料的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="47f41-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="47f41-108">如果未提供消費者群組的名稱，則會傳回指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="47f41-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="47f41-109">示例</span><span class="sxs-lookup"><span data-stu-id="47f41-109">EXAMPLES</span></span>

### <span data-ttu-id="47f41-110">範例1</span><span class="sxs-lookup"><span data-stu-id="47f41-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="47f41-111">\` \` 在事件中心 MyEventHubName 中取得消費者群組 MyConsumerGroupName，該活動中心已 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="47f41-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="47f41-112">範例2</span><span class="sxs-lookup"><span data-stu-id="47f41-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="47f41-113">在事件中心 MyEventHubName 中取得消費者群組的清單，該使用者群組 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="47f41-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="47f41-114">參數</span><span class="sxs-lookup"><span data-stu-id="47f41-114">PARAMETERS</span></span>

### <span data-ttu-id="47f41-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f41-115">-ResourceGroupName</span></span>
<span data-ttu-id="47f41-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="47f41-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f41-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="47f41-117">-EventHub</span></span>
<span data-ttu-id="47f41-118">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="47f41-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f41-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="47f41-119">-Name</span></span>
<span data-ttu-id="47f41-120">ConsumerGroup [名稱]。</span><span class="sxs-lookup"><span data-stu-id="47f41-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f41-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="47f41-121">-Namespace</span></span>
<span data-ttu-id="47f41-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="47f41-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="47f41-123">輸入</span><span class="sxs-lookup"><span data-stu-id="47f41-123">INPUTS</span></span>

### <span data-ttu-id="47f41-124">System.object</span><span class="sxs-lookup"><span data-stu-id="47f41-124">System.String</span></span>

## <span data-ttu-id="47f41-125">輸出</span><span class="sxs-lookup"><span data-stu-id="47f41-125">OUTPUTS</span></span>

### <span data-ttu-id="47f41-126">[System.object]。清單 ' 1 [ConsumerGroupAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="47f41-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="47f41-127">筆記</span><span class="sxs-lookup"><span data-stu-id="47f41-127">NOTES</span></span>

## <span data-ttu-id="47f41-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="47f41-128">RELATED LINKS</span></span>

