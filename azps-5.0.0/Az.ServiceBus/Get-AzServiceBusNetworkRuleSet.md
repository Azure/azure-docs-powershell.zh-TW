---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137991"
---
# <span data-ttu-id="b22b3-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b22b3-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="b22b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b22b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b22b3-103">取得目前 Azure 訂閱中的命名空間事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b22b3-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b22b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b22b3-104">SYNTAX</span></span>

### <span data-ttu-id="b22b3-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b22b3-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22b3-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b22b3-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22b3-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22b3-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b22b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="b22b3-108">DESCRIPTION</span></span>
<span data-ttu-id="b22b3-109">取得目前 Azure 訂閱中的命名空間事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b22b3-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b22b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="b22b3-110">EXAMPLES</span></span>

### <span data-ttu-id="b22b3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b22b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="b22b3-112">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {1.1.1.1，Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，False}</span><span class="sxs-lookup"><span data-stu-id="b22b3-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="b22b3-113">使用 ResourceGroup 和命名空間參數，取得命名空間之事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b22b3-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="b22b3-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b22b3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="b22b3-115">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {1.1.1.1，Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，False}</span><span class="sxs-lookup"><span data-stu-id="b22b3-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="b22b3-116">使用目前訂閱中的命名空間來取得 namespace 事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b22b3-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="b22b3-117">範例3</span><span class="sxs-lookup"><span data-stu-id="b22b3-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="b22b3-118">名稱：預設 DefaultAction： Allow Id：/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default 類型：/命名空間/NetworkRuleSet IpRules： {1.1.1.1，Allow} VirtualNetworkRules： {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default，False}</span><span class="sxs-lookup"><span data-stu-id="b22b3-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="b22b3-119">使用其他命名空間的資源識別碼來取得命名空間之事件中心 NetworkruleSet 的詳細資料</span><span class="sxs-lookup"><span data-stu-id="b22b3-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="b22b3-120">參數</span><span class="sxs-lookup"><span data-stu-id="b22b3-120">PARAMETERS</span></span>

### <span data-ttu-id="b22b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22b3-121">-DefaultProfile</span></span>
<span data-ttu-id="b22b3-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b22b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22b3-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b22b3-123">-Namespace</span></span>
<span data-ttu-id="b22b3-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b22b3-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22b3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22b3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b22b3-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b22b3-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22b3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b22b3-127">-ResourceId</span></span>
<span data-ttu-id="b22b3-128">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b22b3-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b22b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22b3-129">CommonParameters</span></span>
<span data-ttu-id="b22b3-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b22b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b22b3-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b22b3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22b3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b22b3-132">INPUTS</span></span>

### <span data-ttu-id="b22b3-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b22b3-133">System.String</span></span>

## <span data-ttu-id="b22b3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b22b3-134">OUTPUTS</span></span>

### <span data-ttu-id="b22b3-135">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b22b3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b22b3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b22b3-136">NOTES</span></span>

## <span data-ttu-id="b22b3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b22b3-137">RELATED LINKS</span></span>