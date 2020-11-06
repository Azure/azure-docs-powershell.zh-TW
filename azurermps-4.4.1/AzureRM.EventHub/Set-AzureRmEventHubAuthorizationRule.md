---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451692"
---
# <span data-ttu-id="f9d3b-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9d3b-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f9d3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d3b-103">更新事件中樞上的指定授權規則。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9d3b-104">SYNTAX</span></span>

### <span data-ttu-id="f9d3b-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9d3b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f9d3b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9d3b-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f9d3b-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9d3b-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f9d3b-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f9d3b-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="f9d3b-109">說明</span><span class="sxs-lookup"><span data-stu-id="f9d3b-109">DESCRIPTION</span></span>
<span data-ttu-id="f9d3b-110">Set-AzureRmEventHubAuthorizationRule Cmdlet 會在指定的事件中樞上更新指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="f9d3b-111">示例</span><span class="sxs-lookup"><span data-stu-id="f9d3b-111">EXAMPLES</span></span>

### <span data-ttu-id="f9d3b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f9d3b-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="f9d3b-113">更新授權規則 \` MyAuthRuleName \` ，以授予對事件中心 MyEventHubName 的管理 \` 許可權 \` （依命名空間 MyNamespaceName 的範圍） \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f9d3b-114">參數</span><span class="sxs-lookup"><span data-stu-id="f9d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="f9d3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9d3b-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-116">Resource group name.</span></span>

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

### <span data-ttu-id="f9d3b-117">-許可權</span><span class="sxs-lookup"><span data-stu-id="f9d3b-117">-Rights</span></span>
<span data-ttu-id="f9d3b-118">如果未指定 ' AuthruleObj」，則為必要。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="f9d3b-119">版權例如，@ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="f9d3b-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f9d3b-120">-Confirm</span></span>
<span data-ttu-id="f9d3b-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d3b-122">-WhatIf</span></span>
<span data-ttu-id="f9d3b-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d3b-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f9d3b-125">-EventHub</span></span>
<span data-ttu-id="f9d3b-126">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d3b-127">-InputObject</span></span>
<span data-ttu-id="f9d3b-128">{{Fill InputObject 描述}}</span><span class="sxs-lookup"><span data-stu-id="f9d3b-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9d3b-129">-Name</span></span>
<span data-ttu-id="f9d3b-130">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-130">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d3b-131">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f9d3b-131">-Namespace</span></span>
<span data-ttu-id="f9d3b-132">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-132">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f9d3b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f9d3b-133">INPUTS</span></span>

### <span data-ttu-id="f9d3b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="f9d3b-134">System.String</span></span>

## <span data-ttu-id="f9d3b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f9d3b-135">OUTPUTS</span></span>

### <span data-ttu-id="f9d3b-136">SharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9d3b-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f9d3b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f9d3b-137">NOTES</span></span>

## <span data-ttu-id="f9d3b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9d3b-138">RELATED LINKS</span></span>

