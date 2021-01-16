---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280704"
---
# <span data-ttu-id="442e6-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="442e6-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="442e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="442e6-102">SYNOPSIS</span></span>
<span data-ttu-id="442e6-103">更新事件中樞上的指定授權規則。</span><span class="sxs-lookup"><span data-stu-id="442e6-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="442e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="442e6-104">SYNTAX</span></span>

### <span data-ttu-id="442e6-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="442e6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="442e6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="442e6-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="442e6-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="442e6-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442e6-108">說明</span><span class="sxs-lookup"><span data-stu-id="442e6-108">DESCRIPTION</span></span>
<span data-ttu-id="442e6-109">Set-AzEventHubAuthorizationRule Cmdlet 會在指定的事件中樞上更新指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="442e6-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="442e6-110">示例</span><span class="sxs-lookup"><span data-stu-id="442e6-110">EXAMPLES</span></span>

### <span data-ttu-id="442e6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="442e6-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="442e6-112">更新授權規則 \` MyAuthRuleName \` ，以授予對事件中心 MyEventHubName 的管理 \` 許可權 \` （依命名空間 MyNamespaceName 的範圍） \` \` 。</span><span class="sxs-lookup"><span data-stu-id="442e6-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="442e6-113">參數</span><span class="sxs-lookup"><span data-stu-id="442e6-113">PARAMETERS</span></span>

### <span data-ttu-id="442e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442e6-114">-DefaultProfile</span></span>
<span data-ttu-id="442e6-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="442e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442e6-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="442e6-116">-EventHub</span></span>
<span data-ttu-id="442e6-117">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="442e6-117">EventHub Name</span></span>

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

### <span data-ttu-id="442e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="442e6-118">-InputObject</span></span>
<span data-ttu-id="442e6-119">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="442e6-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="442e6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="442e6-120">-Name</span></span>
<span data-ttu-id="442e6-121">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="442e6-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="442e6-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="442e6-122">-Namespace</span></span>
<span data-ttu-id="442e6-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="442e6-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="442e6-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="442e6-125">Resource Group Name</span></span>

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

### <span data-ttu-id="442e6-126">-許可權</span><span class="sxs-lookup"><span data-stu-id="442e6-126">-Rights</span></span>
<span data-ttu-id="442e6-127">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="442e6-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442e6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="442e6-128">-Confirm</span></span>
<span data-ttu-id="442e6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="442e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442e6-130">-WhatIf</span></span>
<span data-ttu-id="442e6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="442e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="442e6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="442e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442e6-133">CommonParameters</span></span>
<span data-ttu-id="442e6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="442e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442e6-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="442e6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442e6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="442e6-136">INPUTS</span></span>

### <span data-ttu-id="442e6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="442e6-137">System.String</span></span>

### <span data-ttu-id="442e6-138">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="442e6-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="442e6-139">System.object []</span><span class="sxs-lookup"><span data-stu-id="442e6-139">System.String[]</span></span>

## <span data-ttu-id="442e6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="442e6-140">OUTPUTS</span></span>

### <span data-ttu-id="442e6-141">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="442e6-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="442e6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="442e6-142">NOTES</span></span>

## <span data-ttu-id="442e6-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="442e6-143">RELATED LINKS</span></span>
