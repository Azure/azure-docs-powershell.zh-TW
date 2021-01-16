---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289132"
---
# <span data-ttu-id="65b40-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="65b40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65b40-102">SYNOPSIS</span></span>
<span data-ttu-id="65b40-103">移除指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="65b40-104">句法</span><span class="sxs-lookup"><span data-stu-id="65b40-104">SYNTAX</span></span>

### <span data-ttu-id="65b40-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="65b40-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b40-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65b40-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b40-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b40-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b40-108">說明</span><span class="sxs-lookup"><span data-stu-id="65b40-108">DESCRIPTION</span></span>
<span data-ttu-id="65b40-109">移除指定命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="65b40-110">示例</span><span class="sxs-lookup"><span data-stu-id="65b40-110">EXAMPLES</span></span>

### <span data-ttu-id="65b40-111">範例1</span><span class="sxs-lookup"><span data-stu-id="65b40-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="65b40-112">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="65b40-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="65b40-113">刪除給定「Eventhub-Namespace1-1375」命名空間的 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="65b40-114">範例2</span><span class="sxs-lookup"><span data-stu-id="65b40-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="65b40-115">使用 InputObject 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="65b40-116">範例3</span><span class="sxs-lookup"><span data-stu-id="65b40-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="65b40-117">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default 類型： NetworkRuleSet/命名空間/IpRules： VirtualNetworkRules：</span><span class="sxs-lookup"><span data-stu-id="65b40-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="65b40-118">使用命名空間的 ResourceId 刪除 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b40-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="65b40-119">參數</span><span class="sxs-lookup"><span data-stu-id="65b40-119">PARAMETERS</span></span>

### <span data-ttu-id="65b40-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65b40-120">-AsJob</span></span>
<span data-ttu-id="65b40-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="65b40-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65b40-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b40-122">-DefaultProfile</span></span>
<span data-ttu-id="65b40-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65b40-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b40-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65b40-124">-InputObject</span></span>
<span data-ttu-id="65b40-125">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="65b40-125">Namespace Object</span></span>

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

### <span data-ttu-id="65b40-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="65b40-126">-Name</span></span>
<span data-ttu-id="65b40-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="65b40-127">Namespace Name</span></span>

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

### <span data-ttu-id="65b40-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65b40-128">-PassThru</span></span>
<span data-ttu-id="65b40-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="65b40-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65b40-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b40-130">-ResourceGroupName</span></span>
<span data-ttu-id="65b40-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="65b40-131">Resource Group Name</span></span>

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

### <span data-ttu-id="65b40-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b40-132">-ResourceId</span></span>
<span data-ttu-id="65b40-133">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="65b40-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="65b40-134">-確認</span><span class="sxs-lookup"><span data-stu-id="65b40-134">-Confirm</span></span>
<span data-ttu-id="65b40-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65b40-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b40-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b40-136">-WhatIf</span></span>
<span data-ttu-id="65b40-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65b40-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b40-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65b40-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b40-139">CommonParameters</span></span>
<span data-ttu-id="65b40-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65b40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="65b40-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65b40-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b40-142">輸入</span><span class="sxs-lookup"><span data-stu-id="65b40-142">INPUTS</span></span>

### <span data-ttu-id="65b40-143">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="65b40-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="65b40-144">System.object</span><span class="sxs-lookup"><span data-stu-id="65b40-144">System.String</span></span>

## <span data-ttu-id="65b40-145">輸出</span><span class="sxs-lookup"><span data-stu-id="65b40-145">OUTPUTS</span></span>

### <span data-ttu-id="65b40-146">System.object</span><span class="sxs-lookup"><span data-stu-id="65b40-146">System.Boolean</span></span>

## <span data-ttu-id="65b40-147">筆記</span><span class="sxs-lookup"><span data-stu-id="65b40-147">NOTES</span></span>

## <span data-ttu-id="65b40-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="65b40-148">RELATED LINKS</span></span>