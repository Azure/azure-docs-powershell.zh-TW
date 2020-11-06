---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620608"
---
# <span data-ttu-id="b7246-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="b7246-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7246-102">SYNOPSIS</span></span>
<span data-ttu-id="b7246-103">移除指定命名空間的 NetwrokRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="b7246-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7246-104">SYNTAX</span></span>

### <span data-ttu-id="b7246-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b7246-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7246-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b7246-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7246-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7246-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7246-108">說明</span><span class="sxs-lookup"><span data-stu-id="b7246-108">DESCRIPTION</span></span>
<span data-ttu-id="b7246-109">移除指定命名空間的 NetwrokRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="b7246-110">示例</span><span class="sxs-lookup"><span data-stu-id="b7246-110">EXAMPLES</span></span>

### <span data-ttu-id="b7246-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b7246-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="b7246-112">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="b7246-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="b7246-113">刪除指定「Namespace1-1375」的 NetwrokRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="b7246-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b7246-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="b7246-115">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="b7246-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="b7246-116">使用 InputObject 刪除 NetwrokRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="b7246-117">範例3</span><span class="sxs-lookup"><span data-stu-id="b7246-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="b7246-118">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="b7246-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="b7246-119">使用 Namepsace 的 ResourceId 刪除 NetwrokRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7246-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="b7246-120">參數</span><span class="sxs-lookup"><span data-stu-id="b7246-120">PARAMETERS</span></span>

### <span data-ttu-id="b7246-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7246-121">-AsJob</span></span>
<span data-ttu-id="b7246-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7246-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7246-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7246-123">-DefaultProfile</span></span>
<span data-ttu-id="b7246-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7246-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7246-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7246-125">-InputObject</span></span>
<span data-ttu-id="b7246-126">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="b7246-126">Namespace Object</span></span>

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

### <span data-ttu-id="b7246-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7246-127">-Name</span></span>
<span data-ttu-id="b7246-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b7246-128">Namespace Name</span></span>

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

### <span data-ttu-id="b7246-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7246-129">-PassThru</span></span>
<span data-ttu-id="b7246-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b7246-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7246-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7246-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7246-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b7246-132">Resource Group Name</span></span>

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

### <span data-ttu-id="b7246-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7246-133">-ResourceId</span></span>
<span data-ttu-id="b7246-134">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b7246-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b7246-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b7246-135">-Confirm</span></span>
<span data-ttu-id="b7246-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7246-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7246-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7246-137">-WhatIf</span></span>
<span data-ttu-id="b7246-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7246-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7246-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7246-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7246-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7246-140">CommonParameters</span></span>
<span data-ttu-id="b7246-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7246-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7246-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7246-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7246-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b7246-143">INPUTS</span></span>

### <span data-ttu-id="b7246-144">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7246-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="b7246-145">System.object</span><span class="sxs-lookup"><span data-stu-id="b7246-145">System.String</span></span>

## <span data-ttu-id="b7246-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b7246-146">OUTPUTS</span></span>

### <span data-ttu-id="b7246-147">System.object</span><span class="sxs-lookup"><span data-stu-id="b7246-147">System.Boolean</span></span>

## <span data-ttu-id="b7246-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b7246-148">NOTES</span></span>

## <span data-ttu-id="b7246-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7246-149">RELATED LINKS</span></span>
