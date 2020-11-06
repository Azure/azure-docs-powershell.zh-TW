---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 739d027d095810ae33f90a7b5cc1ad7caf148081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448677"
---
# <span data-ttu-id="617c3-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="617c3-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="617c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="617c3-102">SYNOPSIS</span></span>
<span data-ttu-id="617c3-103">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="617c3-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="617c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="617c3-104">SYNTAX</span></span>

### <span data-ttu-id="617c3-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="617c3-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617c3-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="617c3-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="617c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="617c3-107">DESCRIPTION</span></span>
<span data-ttu-id="617c3-108">Set-AzureRmEventHubNamespace Cmdlet 會更新指定事件中樞命名空間的屬性。</span><span class="sxs-lookup"><span data-stu-id="617c3-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="617c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="617c3-109">EXAMPLES</span></span>

### <span data-ttu-id="617c3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="617c3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="617c3-111">更新要建立的命名空間 MyNamespaceName 的狀態 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="617c3-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="617c3-112">範例2</span><span class="sxs-lookup"><span data-stu-id="617c3-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="617c3-113">\` \` 使用 AutoInflate = Enabled 和 MaximumThroughputUnits = 10 更新命名空間 MyNamespaceName 的狀態</span><span class="sxs-lookup"><span data-stu-id="617c3-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="617c3-114">參數</span><span class="sxs-lookup"><span data-stu-id="617c3-114">PARAMETERS</span></span>

### <span data-ttu-id="617c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617c3-115">-DefaultProfile</span></span>
<span data-ttu-id="617c3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="617c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="617c3-117">-EnableAutoInflate</span></span>
<span data-ttu-id="617c3-118">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="617c3-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="617c3-119">-Location</span></span>
<span data-ttu-id="617c3-120">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="617c3-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="617c3-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="617c3-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="617c3-122">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="617c3-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="617c3-123">-Name</span></span>
<span data-ttu-id="617c3-124">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="617c3-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="617c3-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="617c3-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="617c3-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="617c3-127">-SkuCapacity</span></span>
<span data-ttu-id="617c3-128">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="617c3-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="617c3-129">-SkuName</span></span>
<span data-ttu-id="617c3-130">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="617c3-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="617c3-131">-State</span><span class="sxs-lookup"><span data-stu-id="617c3-131">-State</span></span>
<span data-ttu-id="617c3-132">停用/啟用命名空間。</span><span class="sxs-lookup"><span data-stu-id="617c3-132">Disable/Enable Namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="617c3-133">-Tag</span></span>
<span data-ttu-id="617c3-134">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="617c3-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="617c3-135">-Confirm</span></span>
<span data-ttu-id="617c3-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="617c3-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617c3-137">-WhatIf</span></span>
<span data-ttu-id="617c3-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="617c3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617c3-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="617c3-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617c3-140">CommonParameters</span></span>
<span data-ttu-id="617c3-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="617c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="617c3-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="617c3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617c3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="617c3-143">INPUTS</span></span>

### <span data-ttu-id="617c3-144">System.object</span><span class="sxs-lookup"><span data-stu-id="617c3-144">System.String</span></span>
<span data-ttu-id="617c3-145">`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`NamespaceState null 1 [[0.5.0.0]。 eventhub、Version =、Culture = 中性、PublicKeyToken = null]] System. Hashtable = null]] 系統. Hashtable</span><span class="sxs-lookup"><span data-stu-id="617c3-145">System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="617c3-146">輸出</span><span class="sxs-lookup"><span data-stu-id="617c3-146">OUTPUTS</span></span>

### <span data-ttu-id="617c3-147">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="617c3-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="617c3-148">筆記</span><span class="sxs-lookup"><span data-stu-id="617c3-148">NOTES</span></span>

## <span data-ttu-id="617c3-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="617c3-149">RELATED LINKS</span></span>
