---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626300"
---
# <span data-ttu-id="759c9-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="759c9-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="759c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="759c9-102">SYNOPSIS</span></span>
<span data-ttu-id="759c9-103">建立事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="759c9-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="759c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="759c9-104">SYNTAX</span></span>

### <span data-ttu-id="759c9-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="759c9-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="759c9-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="759c9-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="759c9-107">說明</span><span class="sxs-lookup"><span data-stu-id="759c9-107">DESCRIPTION</span></span>
<span data-ttu-id="759c9-108">New-AzureRmEventHubNamespace Cmdlet 會建立一個類型事件中樞的新命名空間。</span><span class="sxs-lookup"><span data-stu-id="759c9-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="759c9-109">示例</span><span class="sxs-lookup"><span data-stu-id="759c9-109">EXAMPLES</span></span>

### <span data-ttu-id="759c9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="759c9-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="759c9-111">\` \` \` \` 在 [資源群組 MyResourceGroupName] 中，在指定的地理位置 MyLocation 中 \` \` 建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="759c9-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="759c9-112">範例2</span><span class="sxs-lookup"><span data-stu-id="759c9-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="759c9-113">在 \` MyNamespaceName \` 的 [ \` \` 資源群組] MyResourceGroupName 中， \` \` 以及 MaximumThroughputUnits 10 啟用 AutoInflate，在指定的地理位置 MyLocation 中建立事件中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="759c9-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="759c9-114">參數</span><span class="sxs-lookup"><span data-stu-id="759c9-114">PARAMETERS</span></span>

### <span data-ttu-id="759c9-115">-位置</span><span class="sxs-lookup"><span data-stu-id="759c9-115">-Location</span></span>
<span data-ttu-id="759c9-116">事件中心命名空間地理位置。</span><span class="sxs-lookup"><span data-stu-id="759c9-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="759c9-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="759c9-118">Resource group name.</span></span>

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

### <span data-ttu-id="759c9-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="759c9-119">-SkuCapacity</span></span>
<span data-ttu-id="759c9-120">事件中心輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="759c9-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="759c9-121">-SkuName</span></span>
<span data-ttu-id="759c9-122">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="759c9-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="759c9-123">-Tag</span></span>
<span data-ttu-id="759c9-124">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="759c9-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-125">-確認</span><span class="sxs-lookup"><span data-stu-id="759c9-125">-Confirm</span></span>
<span data-ttu-id="759c9-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="759c9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="759c9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759c9-127">-WhatIf</span></span>
<span data-ttu-id="759c9-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="759c9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="759c9-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="759c9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="759c9-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="759c9-130">-EnableAutoInflate</span></span>
<span data-ttu-id="759c9-131">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="759c9-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="759c9-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="759c9-133">輸送量單位的上限在啟用 AutoInflate 時，vaule 應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="759c9-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759c9-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="759c9-134">-Name</span></span>
<span data-ttu-id="759c9-135">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="759c9-135">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="759c9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="759c9-136">INPUTS</span></span>

### <span data-ttu-id="759c9-137">System.object</span><span class="sxs-lookup"><span data-stu-id="759c9-137">System.String</span></span>
<span data-ttu-id="759c9-138">可為 Null 的 \` 1 \[ \[ system （Int32），版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = B77a5c561934e089 \] \] System。可為 null \` 1 \[ \[ system. Boolean、mscorlib、Version = 4.0.0.0，Culture = 中立，版本 =，Culture = 中性，PublicKeyToken = b77a5c561934e089 \] \] System. Hashtable</span><span class="sxs-lookup"><span data-stu-id="759c9-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="759c9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="759c9-139">OUTPUTS</span></span>

### <span data-ttu-id="759c9-140">NamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="759c9-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="759c9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="759c9-141">NOTES</span></span>

## <span data-ttu-id="759c9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="759c9-142">RELATED LINKS</span></span>

