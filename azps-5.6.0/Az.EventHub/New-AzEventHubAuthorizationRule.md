---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903210"
---
# <span data-ttu-id="28702-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="28702-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="28702-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28702-102">SYNOPSIS</span></span>
<span data-ttu-id="28702-103">為命名空間或事件中心建立新事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="28702-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="28702-104">語法</span><span class="sxs-lookup"><span data-stu-id="28702-104">SYNTAX</span></span>

### <span data-ttu-id="28702-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28702-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28702-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="28702-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28702-107">描述</span><span class="sxs-lookup"><span data-stu-id="28702-107">DESCRIPTION</span></span>
<span data-ttu-id="28702-108">Cmdlet New-AzEventHubAuthorizationRule會建立新的事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="28702-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="28702-109">例子</span><span class="sxs-lookup"><span data-stu-id="28702-109">EXAMPLES</span></span>

### <span data-ttu-id="28702-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="28702-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="28702-111">使用資源群組 \` \` \` \` \` MyResourceGroupName 建立授權規則 MyAuthRuleName，授予命名空間 MyNamespaceName 的聆聽和傳送許可權 \` 。</span><span class="sxs-lookup"><span data-stu-id="28702-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="28702-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="28702-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="28702-113">使用資源群組 \` \` \` \` \` \` MyResourceGroupName，在命名空間 MyNamespaceName 中建立授權規則 MyAuthRuleName，將聆聽和傳送許可權授予事件中樞 \` MyEventHubName。 \`</span><span class="sxs-lookup"><span data-stu-id="28702-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="28702-114">參數</span><span class="sxs-lookup"><span data-stu-id="28702-114">PARAMETERS</span></span>

### <span data-ttu-id="28702-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28702-115">-DefaultProfile</span></span>
<span data-ttu-id="28702-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28702-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28702-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="28702-117">-EventHub</span></span>
<span data-ttu-id="28702-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="28702-118">EventHub Name</span></span>

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

### <span data-ttu-id="28702-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="28702-119">-Name</span></span>
<span data-ttu-id="28702-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="28702-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="28702-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="28702-121">-Namespace</span></span>
<span data-ttu-id="28702-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="28702-122">Namespace Name</span></span>

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

### <span data-ttu-id="28702-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28702-123">-ResourceGroupName</span></span>
<span data-ttu-id="28702-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="28702-124">Resource Group Name</span></span>

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

### <span data-ttu-id="28702-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="28702-125">-Rights</span></span>
<span data-ttu-id="28702-126">許可權，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="28702-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28702-127">-確認</span><span class="sxs-lookup"><span data-stu-id="28702-127">-Confirm</span></span>
<span data-ttu-id="28702-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28702-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28702-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28702-129">-WhatIf</span></span>
<span data-ttu-id="28702-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28702-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28702-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28702-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28702-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28702-132">CommonParameters</span></span>
<span data-ttu-id="28702-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28702-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28702-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="28702-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28702-135">輸入</span><span class="sxs-lookup"><span data-stu-id="28702-135">INPUTS</span></span>

### <span data-ttu-id="28702-136">System.String</span><span class="sxs-lookup"><span data-stu-id="28702-136">System.String</span></span>

### <span data-ttu-id="28702-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="28702-137">System.String[]</span></span>

## <span data-ttu-id="28702-138">輸出</span><span class="sxs-lookup"><span data-stu-id="28702-138">OUTPUTS</span></span>

### <span data-ttu-id="28702-139">Microsoft.Azure.Commands.EventHub.models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="28702-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="28702-140">筆記</span><span class="sxs-lookup"><span data-stu-id="28702-140">NOTES</span></span>

## <span data-ttu-id="28702-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="28702-141">RELATED LINKS</span></span>
