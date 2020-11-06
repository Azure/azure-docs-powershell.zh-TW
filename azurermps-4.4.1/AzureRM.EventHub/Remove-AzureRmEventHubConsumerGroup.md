---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451700"
---
# <span data-ttu-id="6ff35-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6ff35-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="6ff35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ff35-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff35-103">刪除指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="6ff35-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff35-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ff35-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6ff35-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ff35-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff35-106">Remove-AzureRmEventHubConsumerGroup Cmdlet 會從指定的事件中心移除並刪除指定的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="6ff35-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="6ff35-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ff35-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff35-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6ff35-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="6ff35-109">從事件中心 MyEventHubName 中刪除消費者群組 \` MyConsumerGroupName \` \` \` ，並將其範圍設定為 \` MyNamespaceName \` 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6ff35-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="6ff35-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ff35-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff35-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff35-111">-ResourceGroupName</span></span>
<span data-ttu-id="6ff35-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff35-112">Resource group name.</span></span>

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

### <span data-ttu-id="6ff35-113">-確認</span><span class="sxs-lookup"><span data-stu-id="6ff35-113">-Confirm</span></span>
<span data-ttu-id="6ff35-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ff35-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff35-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff35-115">-WhatIf</span></span>
<span data-ttu-id="6ff35-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ff35-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff35-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ff35-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff35-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6ff35-118">-EventHub</span></span>
<span data-ttu-id="6ff35-119">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="6ff35-119">EventHub Name.</span></span>

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

### <span data-ttu-id="6ff35-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ff35-120">-Name</span></span>
<span data-ttu-id="6ff35-121">ConsumerGroup [名稱]。</span><span class="sxs-lookup"><span data-stu-id="6ff35-121">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="6ff35-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6ff35-122">-Namespace</span></span>
<span data-ttu-id="6ff35-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff35-123">Namespace Name.</span></span>

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

## <span data-ttu-id="6ff35-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6ff35-124">INPUTS</span></span>

### <span data-ttu-id="6ff35-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6ff35-125">System.String</span></span>

## <span data-ttu-id="6ff35-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6ff35-126">OUTPUTS</span></span>

### <span data-ttu-id="6ff35-127">System.object</span><span class="sxs-lookup"><span data-stu-id="6ff35-127">System.Object</span></span>

## <span data-ttu-id="6ff35-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6ff35-128">NOTES</span></span>

## <span data-ttu-id="6ff35-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ff35-129">RELATED LINKS</span></span>

