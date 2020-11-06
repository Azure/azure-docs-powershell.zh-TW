---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456656"
---
# <span data-ttu-id="93690-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="93690-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="93690-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93690-102">SYNOPSIS</span></span>
<span data-ttu-id="93690-103">移除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="93690-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93690-104">句法</span><span class="sxs-lookup"><span data-stu-id="93690-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="93690-105">說明</span><span class="sxs-lookup"><span data-stu-id="93690-105">DESCRIPTION</span></span>
<span data-ttu-id="93690-106">Remove-AzureRmEventHub Cmdlet 會從指定的命名空間中移除並刪除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="93690-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="93690-107">示例</span><span class="sxs-lookup"><span data-stu-id="93690-107">EXAMPLES</span></span>

### <span data-ttu-id="93690-108">範例1</span><span class="sxs-lookup"><span data-stu-id="93690-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="93690-109">移除事件中心 \` MyEventHubName \` 。</span><span class="sxs-lookup"><span data-stu-id="93690-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="93690-110">參數</span><span class="sxs-lookup"><span data-stu-id="93690-110">PARAMETERS</span></span>

### <span data-ttu-id="93690-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93690-111">-ResourceGroupName</span></span>
<span data-ttu-id="93690-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="93690-112">Resource group name.</span></span>

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

### <span data-ttu-id="93690-113">-確認</span><span class="sxs-lookup"><span data-stu-id="93690-113">-Confirm</span></span>
<span data-ttu-id="93690-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93690-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93690-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93690-115">-WhatIf</span></span>
<span data-ttu-id="93690-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93690-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93690-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93690-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93690-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="93690-118">-Name</span></span>
<span data-ttu-id="93690-119">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="93690-119">EventHub Name.</span></span>

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

### <span data-ttu-id="93690-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="93690-120">-Namespace</span></span>
<span data-ttu-id="93690-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="93690-121">Namespace Name.</span></span>

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

## <span data-ttu-id="93690-122">輸入</span><span class="sxs-lookup"><span data-stu-id="93690-122">INPUTS</span></span>

### <span data-ttu-id="93690-123">System.object</span><span class="sxs-lookup"><span data-stu-id="93690-123">System.String</span></span>

## <span data-ttu-id="93690-124">輸出</span><span class="sxs-lookup"><span data-stu-id="93690-124">OUTPUTS</span></span>

### <span data-ttu-id="93690-125">System.object</span><span class="sxs-lookup"><span data-stu-id="93690-125">System.Object</span></span>

## <span data-ttu-id="93690-126">筆記</span><span class="sxs-lookup"><span data-stu-id="93690-126">NOTES</span></span>

## <span data-ttu-id="93690-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="93690-127">RELATED LINKS</span></span>

