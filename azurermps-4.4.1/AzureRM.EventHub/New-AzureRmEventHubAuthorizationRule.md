---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624823"
---
# <span data-ttu-id="f2289-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f2289-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f2289-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2289-102">SYNOPSIS</span></span>
<span data-ttu-id="f2289-103">為 namespace 或 eventhub 建立新的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="f2289-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2289-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2289-104">SYNTAX</span></span>

### <span data-ttu-id="f2289-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2289-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f2289-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f2289-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f2289-107">說明</span><span class="sxs-lookup"><span data-stu-id="f2289-107">DESCRIPTION</span></span>
<span data-ttu-id="f2289-108">New-AzureRmEventHubAuthorizationRule Cmdlet 會建立新的事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="f2289-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f2289-109">示例</span><span class="sxs-lookup"><span data-stu-id="f2289-109">EXAMPLES</span></span>

### <span data-ttu-id="f2289-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f2289-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f2289-111">\` \` \` \` 使用資源群組 MyResourceGroupName，建立授權規則 MyAuthRuleName，將偵聽和傳送許可權授予命名空間 \` MyNamespaceName \` 。</span><span class="sxs-lookup"><span data-stu-id="f2289-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f2289-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f2289-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f2289-113">\` \` \` \` 在 \` \` 使用資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中，建立 \` MyAuthRuleName 的偵聽和傳送權利給事件中心 MyEventHubName 的 \` 授權規則。</span><span class="sxs-lookup"><span data-stu-id="f2289-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f2289-114">參數</span><span class="sxs-lookup"><span data-stu-id="f2289-114">PARAMETERS</span></span>

### <span data-ttu-id="f2289-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2289-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2289-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f2289-116">Resource group name.</span></span>

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

### <span data-ttu-id="f2289-117">-許可權</span><span class="sxs-lookup"><span data-stu-id="f2289-117">-Rights</span></span>
<span data-ttu-id="f2289-118">版權例如 @ ( 「聆聽」、「傳送」、「管理」 ) 。</span><span class="sxs-lookup"><span data-stu-id="f2289-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2289-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f2289-119">-Confirm</span></span>
<span data-ttu-id="f2289-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2289-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2289-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2289-121">-WhatIf</span></span>
<span data-ttu-id="f2289-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2289-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2289-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2289-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2289-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f2289-124">-EventHub</span></span>
<span data-ttu-id="f2289-125">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="f2289-125">EventHub Name.</span></span>

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

### <span data-ttu-id="f2289-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2289-126">-Name</span></span>
<span data-ttu-id="f2289-127">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="f2289-127">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f2289-128">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f2289-128">-Namespace</span></span>
<span data-ttu-id="f2289-129">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f2289-129">Namespace Name.</span></span>

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

## <span data-ttu-id="f2289-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f2289-130">INPUTS</span></span>

### <span data-ttu-id="f2289-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f2289-131">System.String</span></span>

## <span data-ttu-id="f2289-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f2289-132">OUTPUTS</span></span>

### <span data-ttu-id="f2289-133">SharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2289-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f2289-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f2289-134">NOTES</span></span>

## <span data-ttu-id="f2289-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2289-135">RELATED LINKS</span></span>

