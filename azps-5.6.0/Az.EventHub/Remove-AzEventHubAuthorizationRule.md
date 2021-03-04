---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912410"
---
# <span data-ttu-id="c9616-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9616-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c9616-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c9616-102">SYNOPSIS</span></span>
<span data-ttu-id="c9616-103">移除指定的事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="c9616-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="c9616-104">語法</span><span class="sxs-lookup"><span data-stu-id="c9616-104">SYNTAX</span></span>

### <span data-ttu-id="c9616-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c9616-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9616-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9616-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9616-107">描述</span><span class="sxs-lookup"><span data-stu-id="c9616-107">DESCRIPTION</span></span>
<span data-ttu-id="c9616-108">Cmdlet Remove-AzEventHubAuthorizationRule移除並刪除指定事件中樞的指定授權規則。</span><span class="sxs-lookup"><span data-stu-id="c9616-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="c9616-109">例子</span><span class="sxs-lookup"><span data-stu-id="c9616-109">EXAMPLES</span></span>

### <span data-ttu-id="c9616-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c9616-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c9616-111">從命名空間 \` MyNamespaceName 移除授權規則 \` \` MyAuthRuleName。 \`</span><span class="sxs-lookup"><span data-stu-id="c9616-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c9616-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c9616-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c9616-113">從事件中心 \` \` \` MyEventHubName 移除授權規則 MyAuthRuleName。 \`</span><span class="sxs-lookup"><span data-stu-id="c9616-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="c9616-114">參數</span><span class="sxs-lookup"><span data-stu-id="c9616-114">PARAMETERS</span></span>

### <span data-ttu-id="c9616-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9616-115">-DefaultProfile</span></span>
<span data-ttu-id="c9616-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9616-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9616-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c9616-117">-EventHub</span></span>
<span data-ttu-id="c9616-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="c9616-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9616-119">-強制</span><span class="sxs-lookup"><span data-stu-id="c9616-119">-Force</span></span>
<span data-ttu-id="c9616-120">請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="c9616-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9616-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9616-121">-Name</span></span>
<span data-ttu-id="c9616-122">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="c9616-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c9616-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c9616-123">-Namespace</span></span>
<span data-ttu-id="c9616-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c9616-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9616-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9616-125">-PassThru</span></span>
<span data-ttu-id="c9616-126">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c9616-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9616-127">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c9616-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9616-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9616-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9616-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="c9616-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c9616-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c9616-130">-Confirm</span></span>
<span data-ttu-id="c9616-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c9616-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9616-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9616-132">-WhatIf</span></span>
<span data-ttu-id="c9616-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9616-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9616-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9616-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9616-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9616-135">CommonParameters</span></span>
<span data-ttu-id="c9616-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c9616-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9616-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c9616-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9616-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c9616-138">INPUTS</span></span>

### <span data-ttu-id="c9616-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c9616-139">System.String</span></span>

## <span data-ttu-id="c9616-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c9616-140">OUTPUTS</span></span>

### <span data-ttu-id="c9616-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9616-141">System.Boolean</span></span>

## <span data-ttu-id="c9616-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c9616-142">NOTES</span></span>

## <span data-ttu-id="c9616-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9616-143">RELATED LINKS</span></span>
