---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: eb04f3db26b7601b715369d695b21a234f2feb25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915858"
---
# <span data-ttu-id="5a82f-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a82f-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="5a82f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a82f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a82f-103">移除命名空間 NetworkRuleSet 的單一專用 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a82f-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="5a82f-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a82f-104">SYNTAX</span></span>

### <span data-ttu-id="5a82f-105">VirtualNetworkRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a82f-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a82f-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a82f-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a82f-107">描述</span><span class="sxs-lookup"><span data-stu-id="5a82f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a82f-108">移除命名空間 NetworkRuleSet 的單一專用 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a82f-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="5a82f-109">例子</span><span class="sxs-lookup"><span data-stu-id="5a82f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a82f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a82f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="5a82f-111">移除命名空間 NetworkRuleSet 的單一專用 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5a82f-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="5a82f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="5a82f-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="5a82f-113">移除$virtualruleset命名空間之 NetworkRuleSet 的</span><span class="sxs-lookup"><span data-stu-id="5a82f-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="5a82f-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a82f-114">PARAMETERS</span></span>

### <span data-ttu-id="5a82f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a82f-115">-AsJob</span></span>
<span data-ttu-id="5a82f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a82f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a82f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a82f-117">-DefaultProfile</span></span>
<span data-ttu-id="5a82f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a82f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a82f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a82f-119">-Name</span></span>
<span data-ttu-id="5a82f-120">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="5a82f-120">Namespace Name</span></span>

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

### <span data-ttu-id="5a82f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a82f-121">-PassThru</span></span>
<span data-ttu-id="5a82f-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5a82f-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5a82f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a82f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a82f-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="5a82f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5a82f-125">-子網Id</span><span class="sxs-lookup"><span data-stu-id="5a82f-125">-SubnetId</span></span>
<span data-ttu-id="5a82f-126">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5a82f-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a82f-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5a82f-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="5a82f-128">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="5a82f-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a82f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="5a82f-129">-Confirm</span></span>
<span data-ttu-id="5a82f-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a82f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a82f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a82f-131">-WhatIf</span></span>
<span data-ttu-id="5a82f-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a82f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a82f-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a82f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a82f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a82f-134">CommonParameters</span></span>
<span data-ttu-id="5a82f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a82f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5a82f-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5a82f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a82f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5a82f-137">INPUTS</span></span>

### <span data-ttu-id="5a82f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5a82f-138">System.String</span></span>

### <span data-ttu-id="5a82f-139">Microsoft.Azure.Commands.ServiceBus.models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5a82f-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="5a82f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5a82f-140">OUTPUTS</span></span>

### <span data-ttu-id="5a82f-141">Microsoft.Azure.Commands.ServiceBus.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5a82f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5a82f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5a82f-142">NOTES</span></span>

## <span data-ttu-id="5a82f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a82f-143">RELATED LINKS</span></span>
