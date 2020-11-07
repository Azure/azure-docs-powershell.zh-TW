---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 2ceed94c800a53bae98a3d6ba93dc5cc722cc4e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787865"
---
# <span data-ttu-id="d10e5-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d10e5-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="d10e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d10e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d10e5-103">建立事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="d10e5-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="d10e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d10e5-104">SYNTAX</span></span>

### <span data-ttu-id="d10e5-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d10e5-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d10e5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d10e5-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="d10e5-107">DESCRIPTION</span></span>
<span data-ttu-id="d10e5-108">New-AzEventHubNamespace Cmdlet 會建立一個類型事件中樞的新命名空間。</span><span class="sxs-lookup"><span data-stu-id="d10e5-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="d10e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="d10e5-109">EXAMPLES</span></span>

### <span data-ttu-id="d10e5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d10e5-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="d10e5-111">\` \` \` \` 在 [資源群組 MyResourceGroupName] 中，在指定的地理位置 MyLocation 中 \` \` 建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="d10e5-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d10e5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d10e5-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="d10e5-113">在 \` MyNamespaceName \` 的 [ \` \` 資源群組] MyResourceGroupName 中， \` \` 以及 MaximumThroughputUnits 10 啟用 AutoInflate，在指定的地理位置 MyLocation 中建立事件中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="d10e5-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="d10e5-114">範例 3-Kafka 已啟用的命名空間</span><span class="sxs-lookup"><span data-stu-id="d10e5-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="d10e5-115">\` \` \` \` 在 \` \` 已啟用 Kafka 和 AutoInflate 的 [資源群組] MyResourceGroupName 中，在指定的地理位置 MyLocation 中建立事件中心命名空間 MyNamespaceName。</span><span class="sxs-lookup"><span data-stu-id="d10e5-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="d10e5-116">參數</span><span class="sxs-lookup"><span data-stu-id="d10e5-116">PARAMETERS</span></span>

### <span data-ttu-id="d10e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10e5-117">-DefaultProfile</span></span>
<span data-ttu-id="d10e5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d10e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d10e5-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="d10e5-119">-EnableAutoInflate</span></span>
<span data-ttu-id="d10e5-120">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="d10e5-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="d10e5-121">-EnableKafka</span></span>
<span data-ttu-id="d10e5-122">啟用或停用命名空間的 Kafka</span><span class="sxs-lookup"><span data-stu-id="d10e5-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-123">-位置</span><span class="sxs-lookup"><span data-stu-id="d10e5-123">-Location</span></span>
<span data-ttu-id="d10e5-124">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="d10e5-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="d10e5-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="d10e5-126">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="d10e5-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="d10e5-127">-Name</span></span>
<span data-ttu-id="d10e5-128">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d10e5-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="d10e5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10e5-129">-ResourceGroupName</span></span>
<span data-ttu-id="d10e5-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d10e5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="d10e5-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d10e5-131">-SkuCapacity</span></span>
<span data-ttu-id="d10e5-132">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="d10e5-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d10e5-133">-SkuName</span></span>
<span data-ttu-id="d10e5-134">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="d10e5-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d10e5-135">-Tag</span></span>
<span data-ttu-id="d10e5-136">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="d10e5-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-137">-確認</span><span class="sxs-lookup"><span data-stu-id="d10e5-137">-Confirm</span></span>
<span data-ttu-id="d10e5-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d10e5-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10e5-139">-WhatIf</span></span>
<span data-ttu-id="d10e5-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d10e5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d10e5-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d10e5-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10e5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10e5-142">CommonParameters</span></span>
<span data-ttu-id="d10e5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d10e5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10e5-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d10e5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10e5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d10e5-145">INPUTS</span></span>

### <span data-ttu-id="d10e5-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d10e5-146">System.String</span></span>

### <span data-ttu-id="d10e5-147">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d10e5-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d10e5-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d10e5-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d10e5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="d10e5-149">OUTPUTS</span></span>

### <span data-ttu-id="d10e5-150">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="d10e5-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d10e5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="d10e5-151">NOTES</span></span>

## <span data-ttu-id="d10e5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d10e5-152">RELATED LINKS</span></span>
