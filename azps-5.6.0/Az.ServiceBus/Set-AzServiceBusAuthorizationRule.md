---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4e28f829a9daa17d5d6f44af10f21e8dc3b1f929
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917894"
---
# <span data-ttu-id="9fb2b-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fb2b-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="9fb2b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb2b-103">更新指定 Service Bus 命名空間或佇列或主題的指定授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="9fb2b-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fb2b-104">SYNTAX</span></span>

### <span data-ttu-id="9fb2b-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9fb2b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb2b-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fb2b-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb2b-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fb2b-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb2b-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9fb2b-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb2b-109">描述</span><span class="sxs-lookup"><span data-stu-id="9fb2b-109">DESCRIPTION</span></span>
<span data-ttu-id="9fb2b-110">**Set-AzServiceBusAuthorizationRule** Cmdlet 會更新指定 Service Bus 命名空間或佇列或主題中指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="9fb2b-111">例子</span><span class="sxs-lookup"><span data-stu-id="9fb2b-111">EXAMPLES</span></span>

### <span data-ttu-id="9fb2b-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="9fb2b-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="9fb2b-113">從 **命名空間** 中授權規則的存取許可權移除 `AuthoRule1` 管理 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="9fb2b-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="9fb2b-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="9fb2b-115">移除 **佇列中** 授權規則的存取 `AuthoRule1` 權中的管理 `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="9fb2b-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="9fb2b-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="9fb2b-117">移除 **主題** 中授權規則的存取權 `AuthoRule1` 中的管理 `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="9fb2b-118">參數</span><span class="sxs-lookup"><span data-stu-id="9fb2b-118">PARAMETERS</span></span>

### <span data-ttu-id="9fb2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb2b-119">-DefaultProfile</span></span>
<span data-ttu-id="9fb2b-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fb2b-121">-InputObject</span></span>
<span data-ttu-id="9fb2b-122">ServiceBus AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="9fb2b-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fb2b-123">-Name</span></span>
<span data-ttu-id="9fb2b-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="9fb2b-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9fb2b-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9fb2b-125">-Namespace</span></span>
<span data-ttu-id="9fb2b-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="9fb2b-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2b-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="9fb2b-127">-Queue</span></span>
<span data-ttu-id="9fb2b-128">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="9fb2b-128">Queue Name</span></span>

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

### <span data-ttu-id="9fb2b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb2b-129">-ResourceGroupName</span></span>
<span data-ttu-id="9fb2b-130">資源組名</span><span class="sxs-lookup"><span data-stu-id="9fb2b-130">Resource Group Name</span></span>

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

### <span data-ttu-id="9fb2b-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="9fb2b-131">-Rights</span></span>
<span data-ttu-id="9fb2b-132">許可權，例如 @ ("Listen"，"Send"，"Manage") </span><span class="sxs-lookup"><span data-stu-id="9fb2b-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb2b-133">-主題</span><span class="sxs-lookup"><span data-stu-id="9fb2b-133">-Topic</span></span>
<span data-ttu-id="9fb2b-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="9fb2b-134">Topic Name</span></span>

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

### <span data-ttu-id="9fb2b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="9fb2b-135">-Confirm</span></span>
<span data-ttu-id="9fb2b-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb2b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb2b-137">-WhatIf</span></span>
<span data-ttu-id="9fb2b-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb2b-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb2b-140">CommonParameters</span></span>
<span data-ttu-id="9fb2b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb2b-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9fb2b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb2b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9fb2b-143">INPUTS</span></span>

### <span data-ttu-id="9fb2b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9fb2b-144">System.String</span></span>

### <span data-ttu-id="9fb2b-145">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccesssAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9fb2b-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="9fb2b-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9fb2b-146">System.String[]</span></span>

## <span data-ttu-id="9fb2b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9fb2b-147">OUTPUTS</span></span>

### <span data-ttu-id="9fb2b-148">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccesssAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9fb2b-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9fb2b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9fb2b-149">NOTES</span></span>

## <span data-ttu-id="9fb2b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fb2b-150">RELATED LINKS</span></span>
