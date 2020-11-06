---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446813"
---
# <span data-ttu-id="bd5c1-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bd5c1-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="bd5c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5c1-103">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd5c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd5c1-104">SYNTAX</span></span>

### <span data-ttu-id="bd5c1-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd5c1-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bd5c1-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd5c1-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="bd5c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd5c1-107">DESCRIPTION</span></span>
<span data-ttu-id="bd5c1-108">Set-AzureRmEventHubNamespace Cmdlet 會更新指定事件中樞命名空間的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="bd5c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="bd5c1-109">EXAMPLES</span></span>

### <span data-ttu-id="bd5c1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bd5c1-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="bd5c1-111">更新要建立的命名空間 MyNamespaceName 的狀態 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="bd5c1-112">範例2</span><span class="sxs-lookup"><span data-stu-id="bd5c1-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="bd5c1-113">\` \` 使用 AutoInflate = Enabled 和 MaximumThroughputUnits = 10 更新命名空間 MyNamespaceName 的狀態</span><span class="sxs-lookup"><span data-stu-id="bd5c1-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="bd5c1-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd5c1-114">PARAMETERS</span></span>

### <span data-ttu-id="bd5c1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="bd5c1-115">-Location</span></span>
<span data-ttu-id="bd5c1-116">事件中心命名空間地理位置。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="bd5c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd5c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd5c1-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-118">Resource group name.</span></span>

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

### <span data-ttu-id="bd5c1-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bd5c1-119">-SkuCapacity</span></span>
<span data-ttu-id="bd5c1-120">事件中心輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="bd5c1-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bd5c1-121">-SkuName</span></span>
<span data-ttu-id="bd5c1-122">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c1-123">-State</span><span class="sxs-lookup"><span data-stu-id="bd5c1-123">-State</span></span>
<span data-ttu-id="bd5c1-124">指定命名空間 (停用或啟用) 狀態。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd5c1-125">-Tag</span></span>
<span data-ttu-id="bd5c1-126">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="bd5c1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="bd5c1-127">-Confirm</span></span>
<span data-ttu-id="bd5c1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5c1-129">-WhatIf</span></span>
<span data-ttu-id="bd5c1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd5c1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5c1-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="bd5c1-132">-EnableAutoInflate</span></span>
<span data-ttu-id="bd5c1-133">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="bd5c1-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="bd5c1-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="bd5c1-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="bd5c1-135">輸送量單位的上限在啟用 AutoInflate 時，vaule 應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="bd5c1-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd5c1-136">-Name</span></span>
<span data-ttu-id="bd5c1-137">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="bd5c1-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="bd5c1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bd5c1-138">INPUTS</span></span>

### <span data-ttu-id="bd5c1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bd5c1-139">System.String</span></span>

### <span data-ttu-id="bd5c1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bd5c1-140">System.Int32</span></span>

### <span data-ttu-id="bd5c1-141">NamespaceState 中的 [管理]</span><span class="sxs-lookup"><span data-stu-id="bd5c1-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="bd5c1-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd5c1-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd5c1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="bd5c1-143">OUTPUTS</span></span>

### <span data-ttu-id="bd5c1-144">NamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd5c1-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="bd5c1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="bd5c1-145">NOTES</span></span>

## <span data-ttu-id="bd5c1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd5c1-146">RELATED LINKS</span></span>

