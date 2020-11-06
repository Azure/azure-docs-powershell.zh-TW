---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455604"
---
# <span data-ttu-id="d4f79-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4f79-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d4f79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4f79-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f79-103">針對指定的服務匯流排命名空間或佇列或主題更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="d4f79-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f79-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4f79-104">SYNTAX</span></span>

### <span data-ttu-id="d4f79-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d4f79-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f79-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f79-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f79-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4f79-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f79-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4f79-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f79-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d4f79-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4f79-110">說明</span><span class="sxs-lookup"><span data-stu-id="d4f79-110">DESCRIPTION</span></span>
<span data-ttu-id="d4f79-111">**AzureRmServiceBusAuthorizationRule** Cmdlet 會在指定的服務匯流排命名空間或佇列或主題中，更新指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="d4f79-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="d4f79-112">示例</span><span class="sxs-lookup"><span data-stu-id="d4f79-112">EXAMPLES</span></span>

### <span data-ttu-id="d4f79-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d4f79-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f79-114">從命名空間中授權規則的存取許可權中移除 [ **管理** ] `AuthoRule1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="d4f79-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d4f79-115">範例2</span><span class="sxs-lookup"><span data-stu-id="d4f79-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f79-116">從佇列中授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBQueue` 。</span><span class="sxs-lookup"><span data-stu-id="d4f79-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="d4f79-117">範例2</span><span class="sxs-lookup"><span data-stu-id="d4f79-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d4f79-118">從主題中的授權規則的存取權中移除 [ **管理** ] `AuthoRule1` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="d4f79-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="d4f79-119">參數</span><span class="sxs-lookup"><span data-stu-id="d4f79-119">PARAMETERS</span></span>

### <span data-ttu-id="d4f79-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d4f79-120">-Confirm</span></span>
<span data-ttu-id="d4f79-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4f79-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f79-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4f79-122">-InputObject</span></span>
<span data-ttu-id="d4f79-123">AuthorizationRule 物件。</span><span class="sxs-lookup"><span data-stu-id="d4f79-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f79-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4f79-124">-Name</span></span>
<span data-ttu-id="d4f79-125">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="d4f79-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d4f79-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d4f79-126">-Namespace</span></span>
<span data-ttu-id="d4f79-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d4f79-127">Namespace Name.</span></span>

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

### <span data-ttu-id="d4f79-128">-佇列</span><span class="sxs-lookup"><span data-stu-id="d4f79-128">-Queue</span></span>
<span data-ttu-id="d4f79-129">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="d4f79-129">Queue Name.</span></span>

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

### <span data-ttu-id="d4f79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f79-130">-ResourceGroupName</span></span>
<span data-ttu-id="d4f79-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d4f79-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4f79-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="d4f79-132">-Rights</span></span>
<span data-ttu-id="d4f79-133">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="d4f79-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f79-134">-主題</span><span class="sxs-lookup"><span data-stu-id="d4f79-134">-Topic</span></span>
<span data-ttu-id="d4f79-135">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="d4f79-135">Topic Name.</span></span>

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

### <span data-ttu-id="d4f79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f79-136">-WhatIf</span></span>
<span data-ttu-id="d4f79-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4f79-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f79-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4f79-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f79-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f79-139">-DefaultProfile</span></span>
<span data-ttu-id="d4f79-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4f79-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4f79-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f79-141">CommonParameters</span></span>
<span data-ttu-id="d4f79-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4f79-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f79-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4f79-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f79-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d4f79-144">INPUTS</span></span>

### <span data-ttu-id="d4f79-145">System.object</span><span class="sxs-lookup"><span data-stu-id="d4f79-145">System.String</span></span>
<span data-ttu-id="d4f79-146">SharedAccessAuthorizationRuleAttributes [] （.... "</span><span class="sxs-lookup"><span data-stu-id="d4f79-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="d4f79-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d4f79-147">OUTPUTS</span></span>

### <span data-ttu-id="d4f79-148">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4f79-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d4f79-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d4f79-149">NOTES</span></span>

## <span data-ttu-id="d4f79-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4f79-150">RELATED LINKS</span></span>

