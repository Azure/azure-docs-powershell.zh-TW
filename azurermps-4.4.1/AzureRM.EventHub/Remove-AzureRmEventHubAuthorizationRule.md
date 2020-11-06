---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456655"
---
# <span data-ttu-id="5c165-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c165-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="5c165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c165-102">SYNOPSIS</span></span>
<span data-ttu-id="5c165-103">移除指定的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="5c165-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c165-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c165-104">SYNTAX</span></span>

### <span data-ttu-id="5c165-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c165-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5c165-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c165-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5c165-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c165-107">DESCRIPTION</span></span>
<span data-ttu-id="5c165-108">Remove-AzureRmEventHubAuthorizationRule Cmdlet 會從指定的事件中樞中移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="5c165-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="5c165-109">示例</span><span class="sxs-lookup"><span data-stu-id="5c165-109">EXAMPLES</span></span>

### <span data-ttu-id="5c165-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5c165-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="5c165-111">範例2</span><span class="sxs-lookup"><span data-stu-id="5c165-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="5c165-112">\` \` 從事件中心 MyEventHubName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="5c165-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="5c165-113">參數</span><span class="sxs-lookup"><span data-stu-id="5c165-113">PARAMETERS</span></span>

### <span data-ttu-id="5c165-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c165-114">-ResourceGroupName</span></span>
<span data-ttu-id="5c165-115">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5c165-115">Resource group name.</span></span>

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

### <span data-ttu-id="5c165-116">-確認</span><span class="sxs-lookup"><span data-stu-id="5c165-116">-Confirm</span></span>
<span data-ttu-id="5c165-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c165-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c165-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c165-118">-WhatIf</span></span>
<span data-ttu-id="5c165-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c165-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c165-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c165-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c165-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5c165-121">-EventHub</span></span>
<span data-ttu-id="5c165-122">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="5c165-122">EventHub Name.</span></span>

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

### <span data-ttu-id="5c165-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5c165-123">-Force</span></span>
<span data-ttu-id="5c165-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="5c165-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c165-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c165-125">-Name</span></span>
<span data-ttu-id="5c165-126">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="5c165-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="5c165-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5c165-127">-Namespace</span></span>
<span data-ttu-id="5c165-128">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5c165-128">Namespace Name.</span></span>

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

### <span data-ttu-id="5c165-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c165-129">-PassThru</span></span>
<span data-ttu-id="5c165-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="5c165-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5c165-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5c165-131">INPUTS</span></span>

### <span data-ttu-id="5c165-132">System.object</span><span class="sxs-lookup"><span data-stu-id="5c165-132">System.String</span></span>

## <span data-ttu-id="5c165-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5c165-133">OUTPUTS</span></span>

### <span data-ttu-id="5c165-134">System.object</span><span class="sxs-lookup"><span data-stu-id="5c165-134">System.Boolean</span></span>

## <span data-ttu-id="5c165-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5c165-135">NOTES</span></span>

## <span data-ttu-id="5c165-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c165-136">RELATED LINKS</span></span>

