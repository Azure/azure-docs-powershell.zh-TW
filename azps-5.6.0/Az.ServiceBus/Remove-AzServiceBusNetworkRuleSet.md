---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917918"
---
# <span data-ttu-id="67dfd-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="67dfd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="67dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="67dfd-103">移除給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="67dfd-104">語法</span><span class="sxs-lookup"><span data-stu-id="67dfd-104">SYNTAX</span></span>

### <span data-ttu-id="67dfd-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="67dfd-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67dfd-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67dfd-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67dfd-108">描述</span><span class="sxs-lookup"><span data-stu-id="67dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="67dfd-109">移除給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="67dfd-110">例子</span><span class="sxs-lookup"><span data-stu-id="67dfd-110">EXAMPLES</span></span>

### <span data-ttu-id="67dfd-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="67dfd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="67dfd-112">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourceGroups/resourceGroup/providers/Microsoft.ServiceBus/命名空間/ServiceBus-命名空間-1375/networkRuleSets/default Type ： Microsoft.ServiceBus/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="67dfd-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="67dfd-113">刪除 「ServiceBus-命名空間1-1375」命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="67dfd-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="67dfd-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="67dfd-115">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/命名空間/Eventhub-命名空間-1375/networkRuleSets/default Type ： Microsoft.EventHub/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="67dfd-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="67dfd-116">使用 InputObject 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="67dfd-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="67dfd-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="67dfd-118">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/命名空間/Eventhub-命名空間-1375/networkRuleSets/default Type ： Microsoft.EventHub/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="67dfd-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="67dfd-119">使用命名空間的 ResourceId 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dfd-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="67dfd-120">參數</span><span class="sxs-lookup"><span data-stu-id="67dfd-120">PARAMETERS</span></span>

### <span data-ttu-id="67dfd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67dfd-121">-AsJob</span></span>
<span data-ttu-id="67dfd-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67dfd-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67dfd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67dfd-123">-DefaultProfile</span></span>
<span data-ttu-id="67dfd-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="67dfd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67dfd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67dfd-125">-InputObject</span></span>
<span data-ttu-id="67dfd-126">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="67dfd-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67dfd-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="67dfd-127">-Name</span></span>
<span data-ttu-id="67dfd-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="67dfd-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dfd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67dfd-129">-PassThru</span></span>
<span data-ttu-id="67dfd-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="67dfd-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="67dfd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67dfd-131">-ResourceGroupName</span></span>
<span data-ttu-id="67dfd-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="67dfd-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dfd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67dfd-133">-ResourceId</span></span>
<span data-ttu-id="67dfd-134">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="67dfd-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67dfd-135">-確認</span><span class="sxs-lookup"><span data-stu-id="67dfd-135">-Confirm</span></span>
<span data-ttu-id="67dfd-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="67dfd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67dfd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67dfd-137">-WhatIf</span></span>
<span data-ttu-id="67dfd-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67dfd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67dfd-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67dfd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67dfd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dfd-140">CommonParameters</span></span>
<span data-ttu-id="67dfd-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="67dfd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="67dfd-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="67dfd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dfd-143">輸入</span><span class="sxs-lookup"><span data-stu-id="67dfd-143">INPUTS</span></span>

### <span data-ttu-id="67dfd-144">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="67dfd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="67dfd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="67dfd-145">System.String</span></span>

## <span data-ttu-id="67dfd-146">輸出</span><span class="sxs-lookup"><span data-stu-id="67dfd-146">OUTPUTS</span></span>

### <span data-ttu-id="67dfd-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67dfd-147">System.Boolean</span></span>

## <span data-ttu-id="67dfd-148">筆記</span><span class="sxs-lookup"><span data-stu-id="67dfd-148">NOTES</span></span>

## <span data-ttu-id="67dfd-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="67dfd-149">RELATED LINKS</span></span>
