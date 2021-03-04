---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 5a33eae7e31ecdc793411bcddc2855d0dbcce8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904333"
---
# <span data-ttu-id="f0326-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f0326-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f0326-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0326-102">SYNOPSIS</span></span>
<span data-ttu-id="f0326-103">從指定的資源群組移除 Service Bus 命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f0326-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="f0326-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0326-104">SYNTAX</span></span>

### <span data-ttu-id="f0326-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0326-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0326-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0326-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0326-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0326-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0326-108">描述</span><span class="sxs-lookup"><span data-stu-id="f0326-108">DESCRIPTION</span></span>
<span data-ttu-id="f0326-109">**Remove-AzServiceBusAuthorizationRule** Cmdlet 會移除指定資源群組之 Service Bus 命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f0326-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="f0326-110">例子</span><span class="sxs-lookup"><span data-stu-id="f0326-110">EXAMPLES</span></span>

### <span data-ttu-id="f0326-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f0326-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f0326-112">從指定的資源群組 `SBAuthoRule1` 移除命名空間 `SB-Example1` 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f0326-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="f0326-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f0326-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f0326-114">從指定的資源群組 `SBAuthoRule1` 移除 `SBQueue` 佇列的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f0326-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="f0326-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="f0326-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f0326-116">從指定的資源群組 `SBAuthoRule1` 移除主題 `SBTopic` 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f0326-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="f0326-117">參數</span><span class="sxs-lookup"><span data-stu-id="f0326-117">PARAMETERS</span></span>

### <span data-ttu-id="f0326-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0326-118">-DefaultProfile</span></span>
<span data-ttu-id="f0326-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0326-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0326-120">-強制</span><span class="sxs-lookup"><span data-stu-id="f0326-120">-Force</span></span>
<span data-ttu-id="f0326-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="f0326-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f0326-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0326-122">-InputObject</span></span>
<span data-ttu-id="f0326-123">ServiceBus AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="f0326-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0326-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0326-124">-Name</span></span>
<span data-ttu-id="f0326-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="f0326-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0326-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f0326-126">-Namespace</span></span>
<span data-ttu-id="f0326-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f0326-127">Namespace Name</span></span>

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

### <span data-ttu-id="f0326-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0326-128">-PassThru</span></span>
<span data-ttu-id="f0326-129">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f0326-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0326-130">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f0326-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0326-131">-佇列</span><span class="sxs-lookup"><span data-stu-id="f0326-131">-Queue</span></span>
<span data-ttu-id="f0326-132">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="f0326-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0326-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0326-133">-ResourceGroupName</span></span>
<span data-ttu-id="f0326-134">資源組名</span><span class="sxs-lookup"><span data-stu-id="f0326-134">Resource Group Name</span></span>

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

### <span data-ttu-id="f0326-135">-主題</span><span class="sxs-lookup"><span data-stu-id="f0326-135">-Topic</span></span>
<span data-ttu-id="f0326-136">主題名稱</span><span class="sxs-lookup"><span data-stu-id="f0326-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0326-137">-確認</span><span class="sxs-lookup"><span data-stu-id="f0326-137">-Confirm</span></span>
<span data-ttu-id="f0326-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0326-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0326-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0326-139">-WhatIf</span></span>
<span data-ttu-id="f0326-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0326-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0326-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0326-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0326-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0326-142">CommonParameters</span></span>
<span data-ttu-id="f0326-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0326-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0326-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f0326-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0326-145">輸入</span><span class="sxs-lookup"><span data-stu-id="f0326-145">INPUTS</span></span>

### <span data-ttu-id="f0326-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f0326-146">System.String</span></span>

### <span data-ttu-id="f0326-147">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccesssAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f0326-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f0326-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f0326-148">OUTPUTS</span></span>

### <span data-ttu-id="f0326-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0326-149">System.Boolean</span></span>

## <span data-ttu-id="f0326-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f0326-150">NOTES</span></span>

## <span data-ttu-id="f0326-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0326-151">RELATED LINKS</span></span>
