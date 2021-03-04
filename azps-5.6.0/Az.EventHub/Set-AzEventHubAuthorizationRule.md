---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: ef71b8ce2f90fb6275c3bd658289f4e32579cd69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915493"
---
# <span data-ttu-id="1a219-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1a219-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="1a219-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a219-102">SYNOPSIS</span></span>
<span data-ttu-id="1a219-103">更新事件中樞上指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="1a219-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="1a219-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a219-104">SYNTAX</span></span>

### <span data-ttu-id="1a219-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1a219-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a219-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1a219-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a219-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1a219-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a219-108">描述</span><span class="sxs-lookup"><span data-stu-id="1a219-108">DESCRIPTION</span></span>
<span data-ttu-id="1a219-109">此Set-AzEventHubAuthorizationRule Cmdlet 會更新指定事件中樞上的指定授權規則。</span><span class="sxs-lookup"><span data-stu-id="1a219-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="1a219-110">例子</span><span class="sxs-lookup"><span data-stu-id="1a219-110">EXAMPLES</span></span>

### <span data-ttu-id="1a219-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1a219-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="1a219-112">更新授權規則 \` MyAuthRuleName，以將管理許可權授予事件 \` 中樞 \` MyEventHubName \` ，以命名空間 \` MyNamespaceName 為範圍 \` 。</span><span class="sxs-lookup"><span data-stu-id="1a219-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="1a219-113">參數</span><span class="sxs-lookup"><span data-stu-id="1a219-113">PARAMETERS</span></span>

### <span data-ttu-id="1a219-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a219-114">-DefaultProfile</span></span>
<span data-ttu-id="1a219-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a219-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a219-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1a219-116">-EventHub</span></span>
<span data-ttu-id="1a219-117">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="1a219-117">EventHub Name</span></span>

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

### <span data-ttu-id="1a219-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a219-118">-InputObject</span></span>
<span data-ttu-id="1a219-119">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="1a219-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="1a219-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a219-120">-Name</span></span>
<span data-ttu-id="1a219-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="1a219-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1a219-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1a219-122">-Namespace</span></span>
<span data-ttu-id="1a219-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="1a219-123">Namespace Name</span></span>

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

### <span data-ttu-id="1a219-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a219-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a219-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="1a219-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1a219-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="1a219-126">-Rights</span></span>
<span data-ttu-id="1a219-127">許可權，例如 @ ("Listen"，"Send"，"Manage") </span><span class="sxs-lookup"><span data-stu-id="1a219-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="1a219-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1a219-128">-Confirm</span></span>
<span data-ttu-id="1a219-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1a219-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a219-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a219-130">-WhatIf</span></span>
<span data-ttu-id="1a219-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a219-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a219-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a219-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a219-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a219-133">CommonParameters</span></span>
<span data-ttu-id="1a219-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a219-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a219-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1a219-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a219-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1a219-136">INPUTS</span></span>

### <span data-ttu-id="1a219-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1a219-137">System.String</span></span>

### <span data-ttu-id="1a219-138">Microsoft.Azure.Commands.EventHub.models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1a219-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="1a219-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1a219-139">System.String[]</span></span>

## <span data-ttu-id="1a219-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1a219-140">OUTPUTS</span></span>

### <span data-ttu-id="1a219-141">Microsoft.Azure.Commands.EventHub.models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1a219-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1a219-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1a219-142">NOTES</span></span>

## <span data-ttu-id="1a219-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a219-143">RELATED LINKS</span></span>
