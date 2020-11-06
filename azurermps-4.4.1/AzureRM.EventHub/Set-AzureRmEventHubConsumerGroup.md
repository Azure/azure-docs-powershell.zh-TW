---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453516"
---
# <span data-ttu-id="ab059-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ab059-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="ab059-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab059-102">SYNOPSIS</span></span>
<span data-ttu-id="ab059-103">更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="ab059-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab059-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab059-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ab059-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab059-105">DESCRIPTION</span></span>
<span data-ttu-id="ab059-106">Set-AzureRmEventHubConsumerGroup Cmdlet 會更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="ab059-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="ab059-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab059-107">EXAMPLES</span></span>

### <span data-ttu-id="ab059-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ab059-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="ab059-109">將消費者群組 MyConsumerGroupName 的使用者中繼資料 \` 設定 \` 為「測試」。</span><span class="sxs-lookup"><span data-stu-id="ab059-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="ab059-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab059-110">PARAMETERS</span></span>

### <span data-ttu-id="ab059-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab059-111">-ResourceGroupName</span></span>
<span data-ttu-id="ab059-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ab059-112">Resource group name.</span></span>

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

### <span data-ttu-id="ab059-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ab059-113">-UserMetadata</span></span>
<span data-ttu-id="ab059-114">消費者群組的使用者中繼資料 (選用的) 。</span><span class="sxs-lookup"><span data-stu-id="ab059-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="ab059-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ab059-115">-Confirm</span></span>
<span data-ttu-id="ab059-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab059-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab059-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab059-117">-WhatIf</span></span>
<span data-ttu-id="ab059-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab059-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab059-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab059-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab059-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ab059-120">-EventHub</span></span>
<span data-ttu-id="ab059-121">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="ab059-121">EventHub Name.</span></span>

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

### <span data-ttu-id="ab059-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab059-122">-Name</span></span>
<span data-ttu-id="ab059-123">ConsumerGroup [名稱]。</span><span class="sxs-lookup"><span data-stu-id="ab059-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="ab059-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ab059-124">-Namespace</span></span>
<span data-ttu-id="ab059-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ab059-125">Namespace Name.</span></span>

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

## <span data-ttu-id="ab059-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ab059-126">INPUTS</span></span>

### <span data-ttu-id="ab059-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ab059-127">System.String</span></span>

## <span data-ttu-id="ab059-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ab059-128">OUTPUTS</span></span>

### <span data-ttu-id="ab059-129">ConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab059-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="ab059-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ab059-130">NOTES</span></span>

## <span data-ttu-id="ab059-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab059-131">RELATED LINKS</span></span>

