---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622255"
---
# <span data-ttu-id="6f954-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6f954-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="6f954-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f954-102">SYNOPSIS</span></span>
<span data-ttu-id="6f954-103">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="6f954-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="6f954-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f954-104">SYNTAX</span></span>

### <span data-ttu-id="6f954-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f954-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f954-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f954-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f954-107">DESCRIPTION</span></span>
<span data-ttu-id="6f954-108">Set-AzEventHubNamespace Cmdlet 會更新指定事件中樞命名空間的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f954-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="6f954-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f954-109">EXAMPLES</span></span>

### <span data-ttu-id="6f954-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6f954-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="6f954-111">更新要建立的命名空間 MyNamespaceName 的狀態 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="6f954-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="6f954-112">範例2</span><span class="sxs-lookup"><span data-stu-id="6f954-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="6f954-113">\` \` 使用 AutoInflate = Enabled 和 MaximumThroughputUnits = 10 更新命名空間 MyNamespaceName 的狀態</span><span class="sxs-lookup"><span data-stu-id="6f954-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="6f954-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f954-114">PARAMETERS</span></span>

### <span data-ttu-id="6f954-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f954-115">-DefaultProfile</span></span>
<span data-ttu-id="6f954-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f954-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f954-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="6f954-117">-EnableAutoInflate</span></span>
<span data-ttu-id="6f954-118">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="6f954-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="6f954-119">-位置</span><span class="sxs-lookup"><span data-stu-id="6f954-119">-Location</span></span>
<span data-ttu-id="6f954-120">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="6f954-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="6f954-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="6f954-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="6f954-122">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="6f954-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f954-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f954-123">-Name</span></span>
<span data-ttu-id="6f954-124">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6f954-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="6f954-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f954-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f954-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6f954-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="6f954-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6f954-127">-SkuCapacity</span></span>
<span data-ttu-id="6f954-128">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="6f954-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="6f954-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6f954-129">-SkuName</span></span>
<span data-ttu-id="6f954-130">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="6f954-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="6f954-131">-State</span><span class="sxs-lookup"><span data-stu-id="6f954-131">-State</span></span>
<span data-ttu-id="6f954-132">停用/啟用命名空間。</span><span class="sxs-lookup"><span data-stu-id="6f954-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f954-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f954-133">-Tag</span></span>
<span data-ttu-id="6f954-134">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="6f954-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f954-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6f954-135">-Confirm</span></span>
<span data-ttu-id="6f954-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f954-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f954-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f954-137">-WhatIf</span></span>
<span data-ttu-id="6f954-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f954-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f954-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f954-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f954-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f954-140">CommonParameters</span></span>
<span data-ttu-id="6f954-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f954-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f954-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f954-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f954-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6f954-143">INPUTS</span></span>

### <span data-ttu-id="6f954-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6f954-144">System.String</span></span>

### <span data-ttu-id="6f954-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f954-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6f954-146">"NamespaceState" 1 [.... eventhub. eventhub. EventHub，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="6f954-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6f954-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f954-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6f954-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6f954-148">OUTPUTS</span></span>

### <span data-ttu-id="6f954-149">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="6f954-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6f954-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6f954-150">NOTES</span></span>

## <span data-ttu-id="6f954-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f954-151">RELATED LINKS</span></span>
