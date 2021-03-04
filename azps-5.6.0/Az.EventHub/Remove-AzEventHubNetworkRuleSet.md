---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9f82f3ac02e9acaf7e715ffb1eeb8c15fa4af3b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916961"
---
# <span data-ttu-id="54a4a-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="54a4a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="54a4a-103">移除給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="54a4a-104">語法</span><span class="sxs-lookup"><span data-stu-id="54a4a-104">SYNTAX</span></span>

### <span data-ttu-id="54a4a-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="54a4a-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54a4a-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54a4a-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a4a-108">描述</span><span class="sxs-lookup"><span data-stu-id="54a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="54a4a-109">移除給定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="54a4a-110">例子</span><span class="sxs-lookup"><span data-stu-id="54a4a-110">EXAMPLES</span></span>

### <span data-ttu-id="54a4a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="54a4a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="54a4a-112">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourceGroups/resourceGroup/providers/Microsoft.EventHub/命名空間/EventHub-命名空間-1375/networkRuleSets/default Type ： Microsoft.EventHub/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="54a4a-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="54a4a-113">刪除 「Eventhub-命名空間1-1375」命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="54a4a-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="54a4a-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="54a4a-115">使用 InputObject 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="54a4a-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="54a4a-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="54a4a-117">名稱 ： default DefaultAction ： Allow Id ： /subscriptions/subscriptionId/resourceGroups/resourceGroup/providers/Microsoft.EventHub/命名空間/EventHub-命名空間-1375/networkRuleSets/default Type ： Microsoft.EventHub/命名空間/NetworkRuleSet IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="54a4a-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="54a4a-118">使用命名空間的 ResourceId 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54a4a-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="54a4a-119">參數</span><span class="sxs-lookup"><span data-stu-id="54a4a-119">PARAMETERS</span></span>

### <span data-ttu-id="54a4a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54a4a-120">-AsJob</span></span>
<span data-ttu-id="54a4a-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54a4a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54a4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a4a-122">-DefaultProfile</span></span>
<span data-ttu-id="54a4a-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54a4a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a4a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54a4a-124">-InputObject</span></span>
<span data-ttu-id="54a4a-125">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="54a4a-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54a4a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="54a4a-126">-Name</span></span>
<span data-ttu-id="54a4a-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="54a4a-127">Namespace Name</span></span>

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

### <span data-ttu-id="54a4a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54a4a-128">-PassThru</span></span>
<span data-ttu-id="54a4a-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="54a4a-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="54a4a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a4a-130">-ResourceGroupName</span></span>
<span data-ttu-id="54a4a-131">資源組名</span><span class="sxs-lookup"><span data-stu-id="54a4a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="54a4a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a4a-132">-ResourceId</span></span>
<span data-ttu-id="54a4a-133">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="54a4a-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="54a4a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="54a4a-134">-Confirm</span></span>
<span data-ttu-id="54a4a-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54a4a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a4a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a4a-136">-WhatIf</span></span>
<span data-ttu-id="54a4a-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54a4a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a4a-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54a4a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54a4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a4a-139">CommonParameters</span></span>
<span data-ttu-id="54a4a-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54a4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="54a4a-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="54a4a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a4a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="54a4a-142">INPUTS</span></span>

### <span data-ttu-id="54a4a-143">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="54a4a-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="54a4a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="54a4a-144">System.String</span></span>

## <span data-ttu-id="54a4a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="54a4a-145">OUTPUTS</span></span>

### <span data-ttu-id="54a4a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54a4a-146">System.Boolean</span></span>

## <span data-ttu-id="54a4a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="54a4a-147">NOTES</span></span>

## <span data-ttu-id="54a4a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="54a4a-148">RELATED LINKS</span></span>