---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625247"
---
# <span data-ttu-id="29828-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29828-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="29828-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29828-102">SYNOPSIS</span></span>
<span data-ttu-id="29828-103">針對指定的服務匯流排命名空間或佇列或主題更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="29828-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29828-104">句法</span><span class="sxs-lookup"><span data-stu-id="29828-104">SYNTAX</span></span>

### <span data-ttu-id="29828-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29828-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29828-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29828-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29828-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29828-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29828-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29828-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29828-109">說明</span><span class="sxs-lookup"><span data-stu-id="29828-109">DESCRIPTION</span></span>
<span data-ttu-id="29828-110">**AzureRmServiceBusAuthorizationRule** Cmdlet 會在指定的服務匯流排命名空間或佇列或主題中，更新指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="29828-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="29828-111">示例</span><span class="sxs-lookup"><span data-stu-id="29828-111">EXAMPLES</span></span>

### <span data-ttu-id="29828-112">範例1</span><span class="sxs-lookup"><span data-stu-id="29828-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="29828-113">從命名空間中授權規則的存取許可權中移除 [ **管理** ] `AuthoRule1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="29828-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="29828-114">範例2</span><span class="sxs-lookup"><span data-stu-id="29828-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="29828-115">從佇列中授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="29828-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="29828-116">範例2</span><span class="sxs-lookup"><span data-stu-id="29828-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="29828-117">從主題中的授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="29828-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="29828-118">參數</span><span class="sxs-lookup"><span data-stu-id="29828-118">PARAMETERS</span></span>

### <span data-ttu-id="29828-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29828-119">-DefaultProfile</span></span>
<span data-ttu-id="29828-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29828-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29828-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29828-121">-InputObject</span></span>
<span data-ttu-id="29828-122">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="29828-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="29828-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="29828-123">-Name</span></span>
<span data-ttu-id="29828-124">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="29828-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="29828-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="29828-125">-Namespace</span></span>
<span data-ttu-id="29828-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="29828-126">Namespace Name</span></span>

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

### <span data-ttu-id="29828-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="29828-127">-Queue</span></span>
<span data-ttu-id="29828-128">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="29828-128">Queue Name</span></span>

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

### <span data-ttu-id="29828-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29828-129">-ResourceGroupName</span></span>
<span data-ttu-id="29828-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="29828-130">Resource Group Name</span></span>

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

### <span data-ttu-id="29828-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="29828-131">-Rights</span></span>
<span data-ttu-id="29828-132">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="29828-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="29828-133">-主題</span><span class="sxs-lookup"><span data-stu-id="29828-133">-Topic</span></span>
<span data-ttu-id="29828-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="29828-134">Topic Name</span></span>

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

### <span data-ttu-id="29828-135">-確認</span><span class="sxs-lookup"><span data-stu-id="29828-135">-Confirm</span></span>
<span data-ttu-id="29828-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29828-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29828-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29828-137">-WhatIf</span></span>
<span data-ttu-id="29828-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29828-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29828-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29828-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29828-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29828-140">CommonParameters</span></span>
<span data-ttu-id="29828-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29828-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29828-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29828-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29828-143">輸入</span><span class="sxs-lookup"><span data-stu-id="29828-143">INPUTS</span></span>

### <span data-ttu-id="29828-144">System.object</span><span class="sxs-lookup"><span data-stu-id="29828-144">System.String</span></span>

### <span data-ttu-id="29828-145">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29828-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="29828-146">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="29828-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="29828-147">System.object []</span><span class="sxs-lookup"><span data-stu-id="29828-147">System.String[]</span></span>

## <span data-ttu-id="29828-148">輸出</span><span class="sxs-lookup"><span data-stu-id="29828-148">OUTPUTS</span></span>

### <span data-ttu-id="29828-149">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29828-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="29828-150">筆記</span><span class="sxs-lookup"><span data-stu-id="29828-150">NOTES</span></span>

## <span data-ttu-id="29828-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="29828-151">RELATED LINKS</span></span>
