---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624566"
---
# <span data-ttu-id="f104d-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f104d-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f104d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f104d-102">SYNOPSIS</span></span>
<span data-ttu-id="f104d-103">在指定的事件中樞命名空間上刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f104d-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f104d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f104d-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f104d-105">說明</span><span class="sxs-lookup"><span data-stu-id="f104d-105">DESCRIPTION</span></span>
<span data-ttu-id="f104d-106">Remove-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會在指定的事件中樞命名空間上移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f104d-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="f104d-107">示例</span><span class="sxs-lookup"><span data-stu-id="f104d-107">EXAMPLES</span></span>

### <span data-ttu-id="f104d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f104d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="f104d-109">\` \` 從命名空間 MyNamespaceName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f104d-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f104d-110">參數</span><span class="sxs-lookup"><span data-stu-id="f104d-110">PARAMETERS</span></span>

### <span data-ttu-id="f104d-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f104d-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="f104d-112">事件中心命名空間授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="f104d-112">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f104d-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f104d-113">-NamespaceName</span></span>
<span data-ttu-id="f104d-114">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f104d-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="f104d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f104d-115">-ResourceGroupName</span></span>
<span data-ttu-id="f104d-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f104d-116">Resource group name.</span></span>

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

### <span data-ttu-id="f104d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f104d-117">-Confirm</span></span>
<span data-ttu-id="f104d-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f104d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f104d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f104d-119">-WhatIf</span></span>
<span data-ttu-id="f104d-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f104d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f104d-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f104d-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f104d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f104d-122">INPUTS</span></span>

### <span data-ttu-id="f104d-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f104d-123">System.String</span></span>

## <span data-ttu-id="f104d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f104d-124">OUTPUTS</span></span>

### <span data-ttu-id="f104d-125">System.object</span><span class="sxs-lookup"><span data-stu-id="f104d-125">System.Boolean</span></span>

## <span data-ttu-id="f104d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f104d-126">NOTES</span></span>

## <span data-ttu-id="f104d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f104d-127">RELATED LINKS</span></span>

