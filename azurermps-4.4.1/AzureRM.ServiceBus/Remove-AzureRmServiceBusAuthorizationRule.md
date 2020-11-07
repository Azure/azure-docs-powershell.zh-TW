---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623854"
---
# <span data-ttu-id="99751-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="99751-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="99751-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99751-102">SYNOPSIS</span></span>
<span data-ttu-id="99751-103">從指定的資源群組中移除服務匯流排命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99751-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99751-104">句法</span><span class="sxs-lookup"><span data-stu-id="99751-104">SYNTAX</span></span>

### <span data-ttu-id="99751-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="99751-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99751-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99751-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99751-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99751-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="99751-108">說明</span><span class="sxs-lookup"><span data-stu-id="99751-108">DESCRIPTION</span></span>
<span data-ttu-id="99751-109">**AzureRmServiceBusAuthorizationRule** Cmdlet 會移除指定資源群組的服務匯流排命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99751-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="99751-110">示例</span><span class="sxs-lookup"><span data-stu-id="99751-110">EXAMPLES</span></span>

### <span data-ttu-id="99751-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99751-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="99751-112">`SBAuthoRule1` `SB-Example1` 從指定的資源群組中移除命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99751-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="99751-113">範例2</span><span class="sxs-lookup"><span data-stu-id="99751-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="99751-114">`SBAuthoRule1` `SBQueue` 從指定的資源群組移除佇列的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99751-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="99751-115">範例3</span><span class="sxs-lookup"><span data-stu-id="99751-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="99751-116">`SBAuthoRule1` `SBTopic` 從指定的資源群組中移除主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="99751-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="99751-117">參數</span><span class="sxs-lookup"><span data-stu-id="99751-117">PARAMETERS</span></span>

### <span data-ttu-id="99751-118">-確認</span><span class="sxs-lookup"><span data-stu-id="99751-118">-Confirm</span></span>
<span data-ttu-id="99751-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99751-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99751-120">-Force</span><span class="sxs-lookup"><span data-stu-id="99751-120">-Force</span></span>
<span data-ttu-id="99751-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="99751-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99751-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="99751-122">-Name</span></span>
<span data-ttu-id="99751-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="99751-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99751-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="99751-124">-Namespace</span></span>
<span data-ttu-id="99751-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="99751-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99751-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99751-126">-PassThru</span></span>
<span data-ttu-id="99751-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="99751-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99751-128">-佇列</span><span class="sxs-lookup"><span data-stu-id="99751-128">-Queue</span></span>
<span data-ttu-id="99751-129">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="99751-129">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99751-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99751-130">-ResourceGroupName</span></span>
<span data-ttu-id="99751-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="99751-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="99751-132">-主題</span><span class="sxs-lookup"><span data-stu-id="99751-132">-Topic</span></span>
<span data-ttu-id="99751-133">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="99751-133">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99751-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99751-134">-WhatIf</span></span>
<span data-ttu-id="99751-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99751-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99751-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99751-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="99751-137">輸入</span><span class="sxs-lookup"><span data-stu-id="99751-137">INPUTS</span></span>

### <span data-ttu-id="99751-138">System.object</span><span class="sxs-lookup"><span data-stu-id="99751-138">System.String</span></span>


## <span data-ttu-id="99751-139">輸出</span><span class="sxs-lookup"><span data-stu-id="99751-139">OUTPUTS</span></span>

### <span data-ttu-id="99751-140">System.object</span><span class="sxs-lookup"><span data-stu-id="99751-140">System.Boolean</span></span>


## <span data-ttu-id="99751-141">筆記</span><span class="sxs-lookup"><span data-stu-id="99751-141">NOTES</span></span>

## <span data-ttu-id="99751-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="99751-142">RELATED LINKS</span></span>

