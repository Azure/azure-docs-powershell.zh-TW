---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457600"
---
# <span data-ttu-id="a9ab3-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a9ab3-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a9ab3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ab3-103">更新指定事件中樞命名空間上的授權規則。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9ab3-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9ab3-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a9ab3-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ab3-106">Set-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會更新指定事件中樞命名空間上的授權規則。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a9ab3-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ab3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a9ab3-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="a9ab3-109">更新授權規則 \` MyAuthRuleName \` ，以授與管理許可權。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="a9ab3-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9ab3-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ab3-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a9ab3-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a9ab3-112">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-112">The authorization rule name.</span></span>
<span data-ttu-id="a9ab3-113">如果未指定-AuthruleObj，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab3-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a9ab3-114">-AuthRuleObj</span></span>
<span data-ttu-id="a9ab3-115">事件中心命名空間授權規則物件。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab3-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a9ab3-116">-NamespaceName</span></span>
<span data-ttu-id="a9ab3-117">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ab3-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9ab3-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-119">Resource group name.</span></span>

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

### <span data-ttu-id="a9ab3-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="a9ab3-120">-Rights</span></span>
<span data-ttu-id="a9ab3-121">如果未指定-AuthruleObj，則為必要。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="a9ab3-122">版權例如，@ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="a9ab3-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a9ab3-123">-Confirm</span></span>
<span data-ttu-id="a9ab3-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ab3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ab3-125">-WhatIf</span></span>
<span data-ttu-id="a9ab3-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ab3-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9ab3-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a9ab3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a9ab3-128">INPUTS</span></span>

### <span data-ttu-id="a9ab3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a9ab3-129">System.String</span></span>

## <span data-ttu-id="a9ab3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a9ab3-130">OUTPUTS</span></span>

### <span data-ttu-id="a9ab3-131">SharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="a9ab3-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a9ab3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a9ab3-132">NOTES</span></span>

## <span data-ttu-id="a9ab3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9ab3-133">RELATED LINKS</span></span>

