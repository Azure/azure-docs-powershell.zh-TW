---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 99993a92179da1adaba068ae7bb525b5b2cca5df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612387"
---
# <span data-ttu-id="c49ea-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c49ea-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="c49ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c49ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c49ea-103">更新指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="c49ea-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c49ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="c49ea-104">SYNTAX</span></span>

### <span data-ttu-id="c49ea-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c49ea-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c49ea-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c49ea-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c49ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="c49ea-107">DESCRIPTION</span></span>
<span data-ttu-id="c49ea-108">Set-AzEventHubNamespace Cmdlet 會更新指定事件中樞命名空間的屬性。</span><span class="sxs-lookup"><span data-stu-id="c49ea-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c49ea-109">示例</span><span class="sxs-lookup"><span data-stu-id="c49ea-109">EXAMPLES</span></span>

### <span data-ttu-id="c49ea-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c49ea-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="c49ea-111">更新要建立之命名空間 MyNamespaceName 的標記 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c49ea-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="c49ea-112">範例2</span><span class="sxs-lookup"><span data-stu-id="c49ea-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="c49ea-113">\` \` 使用 AutoInflate = Enabled 和 MaximumThroughputUnits = 10 更新命名空間 MyNamespaceName 的狀態</span><span class="sxs-lookup"><span data-stu-id="c49ea-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="c49ea-114">參數</span><span class="sxs-lookup"><span data-stu-id="c49ea-114">PARAMETERS</span></span>

### <span data-ttu-id="c49ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49ea-115">-DefaultProfile</span></span>
<span data-ttu-id="c49ea-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c49ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c49ea-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c49ea-117">-EnableAutoInflate</span></span>
<span data-ttu-id="c49ea-118">指出是否已啟用 AutoInflate</span><span class="sxs-lookup"><span data-stu-id="c49ea-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="c49ea-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="c49ea-119">-EnableKafka</span></span>
<span data-ttu-id="c49ea-120">啟用或停用命名空間的 Kafka</span><span class="sxs-lookup"><span data-stu-id="c49ea-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="c49ea-121">-位置</span><span class="sxs-lookup"><span data-stu-id="c49ea-121">-Location</span></span>
<span data-ttu-id="c49ea-122">EventHub 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="c49ea-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="c49ea-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c49ea-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c49ea-124">啟用 AutoInflate 時的輸送量單位上限，值應該在0到20輸送量單位內。</span><span class="sxs-lookup"><span data-stu-id="c49ea-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="c49ea-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c49ea-125">-Name</span></span>
<span data-ttu-id="c49ea-126">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="c49ea-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="c49ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="c49ea-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c49ea-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="c49ea-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c49ea-129">-SkuCapacity</span></span>
<span data-ttu-id="c49ea-130">Eventhub 輸送量單位。</span><span class="sxs-lookup"><span data-stu-id="c49ea-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="c49ea-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c49ea-131">-SkuName</span></span>
<span data-ttu-id="c49ea-132">命名空間 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="c49ea-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="c49ea-133">-State</span><span class="sxs-lookup"><span data-stu-id="c49ea-133">-State</span></span>
<span data-ttu-id="c49ea-134">停用/啟用命名空間。</span><span class="sxs-lookup"><span data-stu-id="c49ea-134">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="c49ea-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c49ea-135">-Tag</span></span>
<span data-ttu-id="c49ea-136">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="c49ea-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="c49ea-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c49ea-137">-Confirm</span></span>
<span data-ttu-id="c49ea-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c49ea-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c49ea-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c49ea-139">-WhatIf</span></span>
<span data-ttu-id="c49ea-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c49ea-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c49ea-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c49ea-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c49ea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49ea-142">CommonParameters</span></span>
<span data-ttu-id="c49ea-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c49ea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49ea-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c49ea-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49ea-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c49ea-145">INPUTS</span></span>

### <span data-ttu-id="c49ea-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c49ea-146">System.String</span></span>

### <span data-ttu-id="c49ea-147">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c49ea-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c49ea-148">"NamespaceState" 1 [[1.3.0.0]、[]、[]、[Culture = 中性]、[PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="c49ea-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c49ea-149">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c49ea-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c49ea-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c49ea-150">OUTPUTS</span></span>

### <span data-ttu-id="c49ea-151">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="c49ea-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c49ea-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c49ea-152">NOTES</span></span>

## <span data-ttu-id="c49ea-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c49ea-153">RELATED LINKS</span></span>
