---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456692"
---
# <span data-ttu-id="e9a08-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="e9a08-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="e9a08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9a08-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a08-103">取得單一事件中心的詳細資料，或取得事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="e9a08-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9a08-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9a08-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="e9a08-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9a08-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a08-106">Get-AzureRmEventHub Cmdlet 會傳回事件中心的詳細資料，或返回目前命名空間中所有事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="e9a08-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="e9a08-107">如果提供了事件中樞名稱，則會傳回單一事件中心的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e9a08-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="e9a08-108">如果未提供事件中樞名稱，則會傳回指定命名空間中的所有事件中心清單。</span><span class="sxs-lookup"><span data-stu-id="e9a08-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="e9a08-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9a08-109">EXAMPLES</span></span>

### <span data-ttu-id="e9a08-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e9a08-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e9a08-111">傳回事件中心 MyEventHubName 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="e9a08-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="e9a08-112">範例2</span><span class="sxs-lookup"><span data-stu-id="e9a08-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e9a08-113">傳回命名空間 MyNamespaceName 中的事件中心清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="e9a08-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e9a08-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9a08-114">PARAMETERS</span></span>

### <span data-ttu-id="e9a08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a08-115">-ResourceGroupName</span></span>
<span data-ttu-id="e9a08-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e9a08-116">Resource group name.</span></span>

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

### <span data-ttu-id="e9a08-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9a08-117">-Name</span></span>
<span data-ttu-id="e9a08-118">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="e9a08-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a08-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e9a08-119">-Namespace</span></span>
<span data-ttu-id="e9a08-120">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e9a08-120">Namespace Name.</span></span>

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

## <span data-ttu-id="e9a08-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e9a08-121">INPUTS</span></span>

### <span data-ttu-id="e9a08-122">System.object</span><span class="sxs-lookup"><span data-stu-id="e9a08-122">System.String</span></span>

## <span data-ttu-id="e9a08-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e9a08-123">OUTPUTS</span></span>

### <span data-ttu-id="e9a08-124">[System.object]。清單 ' 1 [EventHubAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="e9a08-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e9a08-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e9a08-125">NOTES</span></span>

## <span data-ttu-id="e9a08-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9a08-126">RELATED LINKS</span></span>

