---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792097"
---
# <span data-ttu-id="394ea-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="394ea-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="394ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="394ea-102">SYNOPSIS</span></span>
<span data-ttu-id="394ea-103">針對指定的服務匯流排命名空間或佇列或主題更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="394ea-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="394ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="394ea-104">SYNTAX</span></span>

### <span data-ttu-id="394ea-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="394ea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="394ea-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="394ea-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="394ea-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="394ea-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="394ea-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="394ea-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="394ea-109">說明</span><span class="sxs-lookup"><span data-stu-id="394ea-109">DESCRIPTION</span></span>
<span data-ttu-id="394ea-110">**AzServiceBusAuthorizationRule** Cmdlet 會在指定的服務匯流排命名空間或佇列或主題中，更新指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="394ea-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="394ea-111">示例</span><span class="sxs-lookup"><span data-stu-id="394ea-111">EXAMPLES</span></span>

### <span data-ttu-id="394ea-112">範例1</span><span class="sxs-lookup"><span data-stu-id="394ea-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="394ea-113">從命名空間中授權規則的存取許可權中移除 [ **管理** ] `AuthoRule1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="394ea-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="394ea-114">範例2</span><span class="sxs-lookup"><span data-stu-id="394ea-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="394ea-115">從佇列中授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="394ea-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="394ea-116">範例2</span><span class="sxs-lookup"><span data-stu-id="394ea-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="394ea-117">從主題中的授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="394ea-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="394ea-118">參數</span><span class="sxs-lookup"><span data-stu-id="394ea-118">PARAMETERS</span></span>

### <span data-ttu-id="394ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394ea-119">-DefaultProfile</span></span>
<span data-ttu-id="394ea-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="394ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="394ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="394ea-121">-InputObject</span></span>
<span data-ttu-id="394ea-122">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="394ea-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="394ea-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-123">-Name</span></span>
<span data-ttu-id="394ea-124">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="394ea-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="394ea-125">-Namespace</span></span>
<span data-ttu-id="394ea-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-126">Namespace Name</span></span>

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

### <span data-ttu-id="394ea-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="394ea-127">-Queue</span></span>
<span data-ttu-id="394ea-128">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-128">Queue Name</span></span>

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

### <span data-ttu-id="394ea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="394ea-129">-ResourceGroupName</span></span>
<span data-ttu-id="394ea-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-130">Resource Group Name</span></span>

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

### <span data-ttu-id="394ea-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="394ea-131">-Rights</span></span>
<span data-ttu-id="394ea-132">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="394ea-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="394ea-133">-主題</span><span class="sxs-lookup"><span data-stu-id="394ea-133">-Topic</span></span>
<span data-ttu-id="394ea-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="394ea-134">Topic Name</span></span>

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

### <span data-ttu-id="394ea-135">-確認</span><span class="sxs-lookup"><span data-stu-id="394ea-135">-Confirm</span></span>
<span data-ttu-id="394ea-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="394ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="394ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="394ea-137">-WhatIf</span></span>
<span data-ttu-id="394ea-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="394ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="394ea-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="394ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="394ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394ea-140">CommonParameters</span></span>
<span data-ttu-id="394ea-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="394ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394ea-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="394ea-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394ea-143">輸入</span><span class="sxs-lookup"><span data-stu-id="394ea-143">INPUTS</span></span>

### <span data-ttu-id="394ea-144">System.object</span><span class="sxs-lookup"><span data-stu-id="394ea-144">System.String</span></span>

### <span data-ttu-id="394ea-145">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="394ea-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="394ea-146">System.object []</span><span class="sxs-lookup"><span data-stu-id="394ea-146">System.String[]</span></span>

## <span data-ttu-id="394ea-147">輸出</span><span class="sxs-lookup"><span data-stu-id="394ea-147">OUTPUTS</span></span>

### <span data-ttu-id="394ea-148">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="394ea-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="394ea-149">筆記</span><span class="sxs-lookup"><span data-stu-id="394ea-149">NOTES</span></span>

## <span data-ttu-id="394ea-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="394ea-150">RELATED LINKS</span></span>