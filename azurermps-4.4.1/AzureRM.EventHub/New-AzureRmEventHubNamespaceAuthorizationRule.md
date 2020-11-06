---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456664"
---
# <span data-ttu-id="266e9-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="266e9-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="266e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="266e9-102">SYNOPSIS</span></span>
<span data-ttu-id="266e9-103">在指定的命名空間上建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="266e9-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="266e9-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="266e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="266e9-105">DESCRIPTION</span></span>
<span data-ttu-id="266e9-106">New-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會在指定的事件中樞命名空間上建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="266e9-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="266e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="266e9-107">EXAMPLES</span></span>

### <span data-ttu-id="266e9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="266e9-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="266e9-109">\` \` \` 在 [ \` 資源群組 MyResourceGroupName] 中，為事件中樞命名空間 MyNamespaceName 建立具有偵聽和傳送許可權 \` 的授權規則 MyAuthRuleName \` 。</span><span class="sxs-lookup"><span data-stu-id="266e9-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="266e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="266e9-110">PARAMETERS</span></span>

### <span data-ttu-id="266e9-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="266e9-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="266e9-112">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="266e9-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="266e9-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="266e9-113">-NamespaceName</span></span>
<span data-ttu-id="266e9-114">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="266e9-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="266e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="266e9-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="266e9-116">Resource group name.</span></span>

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

### <span data-ttu-id="266e9-117">-許可權</span><span class="sxs-lookup"><span data-stu-id="266e9-117">-Rights</span></span>
<span data-ttu-id="266e9-118">權力; 例如，@ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="266e9-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="266e9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="266e9-119">-Confirm</span></span>
<span data-ttu-id="266e9-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="266e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="266e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266e9-121">-WhatIf</span></span>
<span data-ttu-id="266e9-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="266e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266e9-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="266e9-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="266e9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="266e9-124">INPUTS</span></span>

### <span data-ttu-id="266e9-125">System.object</span><span class="sxs-lookup"><span data-stu-id="266e9-125">System.String</span></span>

## <span data-ttu-id="266e9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="266e9-126">OUTPUTS</span></span>

### <span data-ttu-id="266e9-127">SharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="266e9-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="266e9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="266e9-128">NOTES</span></span>

## <span data-ttu-id="266e9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="266e9-129">RELATED LINKS</span></span>

