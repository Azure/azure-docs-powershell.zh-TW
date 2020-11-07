---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626301"
---
# <span data-ttu-id="7e339-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7e339-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="7e339-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e339-102">SYNOPSIS</span></span>
<span data-ttu-id="7e339-103">針對指定的事件中心建立新的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="7e339-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e339-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e339-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7e339-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e339-105">DESCRIPTION</span></span>
<span data-ttu-id="7e339-106">New-AzureRmEventHubConsumerGroup Cmdlet 會為指定的事件中樞建立新的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="7e339-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="7e339-107">示例</span><span class="sxs-lookup"><span data-stu-id="7e339-107">EXAMPLES</span></span>

### <span data-ttu-id="7e339-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7e339-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="7e339-109">\` \` 在 \` \` \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 的 \` 事件中心 MyEventHubName 中 \` 建立消費者群組 MyConsumerGroupName。</span><span class="sxs-lookup"><span data-stu-id="7e339-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7e339-110">參數</span><span class="sxs-lookup"><span data-stu-id="7e339-110">PARAMETERS</span></span>

### <span data-ttu-id="7e339-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e339-111">-ResourceGroupName</span></span>
<span data-ttu-id="7e339-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7e339-112">Resource group name.</span></span>

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

### <span data-ttu-id="7e339-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7e339-113">-UserMetadata</span></span>
<span data-ttu-id="7e339-114">消費者群組的使用者中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7e339-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e339-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7e339-115">-Confirm</span></span>
<span data-ttu-id="7e339-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e339-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e339-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e339-117">-WhatIf</span></span>
<span data-ttu-id="7e339-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e339-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e339-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e339-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e339-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7e339-120">-EventHub</span></span>
<span data-ttu-id="7e339-121">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="7e339-121">EventHub Name.</span></span>

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

### <span data-ttu-id="7e339-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e339-122">-Name</span></span>
<span data-ttu-id="7e339-123">ConsumerGroup [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7e339-123">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e339-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7e339-124">-Namespace</span></span>
<span data-ttu-id="7e339-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7e339-125">Namespace Name.</span></span>

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

## <span data-ttu-id="7e339-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7e339-126">INPUTS</span></span>

### <span data-ttu-id="7e339-127">System.object</span><span class="sxs-lookup"><span data-stu-id="7e339-127">System.String</span></span>

## <span data-ttu-id="7e339-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7e339-128">OUTPUTS</span></span>

### <span data-ttu-id="7e339-129">ConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="7e339-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="7e339-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7e339-130">NOTES</span></span>

## <span data-ttu-id="7e339-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e339-131">RELATED LINKS</span></span>

