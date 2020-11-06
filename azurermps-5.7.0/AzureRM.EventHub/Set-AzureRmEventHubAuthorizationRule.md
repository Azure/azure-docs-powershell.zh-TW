---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449366"
---
# <span data-ttu-id="78cd5-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="78cd5-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="78cd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="78cd5-103">更新事件中樞上的指定授權規則。</span><span class="sxs-lookup"><span data-stu-id="78cd5-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78cd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="78cd5-104">SYNTAX</span></span>

### <span data-ttu-id="78cd5-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78cd5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78cd5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="78cd5-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78cd5-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78cd5-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78cd5-108">說明</span><span class="sxs-lookup"><span data-stu-id="78cd5-108">DESCRIPTION</span></span>
<span data-ttu-id="78cd5-109">Set-AzureRmEventHubAuthorizationRule Cmdlet 會在指定的事件中樞上更新指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="78cd5-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="78cd5-110">示例</span><span class="sxs-lookup"><span data-stu-id="78cd5-110">EXAMPLES</span></span>

### <span data-ttu-id="78cd5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="78cd5-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="78cd5-112">更新授權規則 \` MyAuthRuleName \` ，以授予對事件中心 MyEventHubName 的管理 \` 許可權 \` （依命名空間 MyNamespaceName 的範圍） \` \` 。</span><span class="sxs-lookup"><span data-stu-id="78cd5-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="78cd5-113">參數</span><span class="sxs-lookup"><span data-stu-id="78cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="78cd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cd5-114">-DefaultProfile</span></span>
<span data-ttu-id="78cd5-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78cd5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="78cd5-116">-EventHub</span></span>
<span data-ttu-id="78cd5-117">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="78cd5-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78cd5-118">-InputObject</span></span>
<span data-ttu-id="78cd5-119">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="78cd5-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="78cd5-120">-Name</span></span>
<span data-ttu-id="78cd5-121">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="78cd5-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="78cd5-122">-Namespace</span></span>
<span data-ttu-id="78cd5-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="78cd5-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cd5-124">-ResourceGroupName</span></span>
<span data-ttu-id="78cd5-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="78cd5-125">Resource Group Name</span></span>

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

### <span data-ttu-id="78cd5-126">-許可權</span><span class="sxs-lookup"><span data-stu-id="78cd5-126">-Rights</span></span>
<span data-ttu-id="78cd5-127">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="78cd5-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="78cd5-128">-Confirm</span></span>
<span data-ttu-id="78cd5-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78cd5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78cd5-130">-WhatIf</span></span>
<span data-ttu-id="78cd5-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78cd5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78cd5-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78cd5-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cd5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cd5-133">CommonParameters</span></span>
<span data-ttu-id="78cd5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78cd5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="78cd5-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78cd5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cd5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="78cd5-136">INPUTS</span></span>

### <span data-ttu-id="78cd5-137">System.object</span><span class="sxs-lookup"><span data-stu-id="78cd5-137">System.String</span></span>
<span data-ttu-id="78cd5-138">PSSharedAccessAuthorizationRuleAttributes [] 的 [System.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="78cd5-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="78cd5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="78cd5-139">OUTPUTS</span></span>

### <span data-ttu-id="78cd5-140">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="78cd5-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="78cd5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="78cd5-141">NOTES</span></span>

## <span data-ttu-id="78cd5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="78cd5-142">RELATED LINKS</span></span>
