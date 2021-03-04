---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 842b48e1645bb141650c2a53dc86bbb5e79acb80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906222"
---
# <span data-ttu-id="4e61f-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e61f-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4e61f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e61f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e61f-103">獲得授權規則的詳細資訊，或獲得授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="4e61f-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="4e61f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e61f-104">SYNTAX</span></span>

### <span data-ttu-id="4e61f-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e61f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e61f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e61f-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e61f-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e61f-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e61f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4e61f-108">DESCRIPTION</span></span>
<span data-ttu-id="4e61f-109">Cmdlet Get-AzEventHubAuthorizationRule會獲得授權規則的詳細資訊，或指定事件中樞的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="4e61f-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="4e61f-110">如果提供授權規則的名稱，系統即會返回該單一授權規則的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4e61f-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="4e61f-111">如果未提供授權規則的名稱，會針對指定的事件中樞，會返回所有授權規則的清單。</span><span class="sxs-lookup"><span data-stu-id="4e61f-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="4e61f-112">如果 (復原) 別名名稱，則系統會針對已配置的別名命名空間，返回授權規則的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4e61f-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="4e61f-113">例子</span><span class="sxs-lookup"><span data-stu-id="4e61f-113">EXAMPLES</span></span>

### <span data-ttu-id="4e61f-114">範例 1：命名空間的 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e61f-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="4e61f-115">在命名空間 \` MyNamespaceName 中 \` ，獲得 \` 授權規則 MyAuthRuleName。 \`</span><span class="sxs-lookup"><span data-stu-id="4e61f-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4e61f-116">範例 2：命名空間的授權規則</span><span class="sxs-lookup"><span data-stu-id="4e61f-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4e61f-117">在命名空間 MyNamespaceName 中，獲得所有 \` 授權規則的清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="4e61f-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4e61f-118">範例 3：EventHub 的授權規則</span><span class="sxs-lookup"><span data-stu-id="4e61f-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="4e61f-119">在事件中樞 MyEventHubName 中，獲得授權規則 \` \` \` MyAuthRuleName，此名稱以 \` 命名空間 \` MyNamespaceName 為範圍 \` 。</span><span class="sxs-lookup"><span data-stu-id="4e61f-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4e61f-120">範例 4：EventHub 的授權規則</span><span class="sxs-lookup"><span data-stu-id="4e61f-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4e61f-121">在事件中樞 \` MyEventHubName 中獲得清單授權規則 \` ，此名稱以命名空間 \` MyNamespaceName 為範圍 \` 。</span><span class="sxs-lookup"><span data-stu-id="4e61f-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4e61f-122">範例 5：Alias 的 AuthorizationRule (GeoRecovery Configuration) </span><span class="sxs-lookup"><span data-stu-id="4e61f-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="4e61f-123">在命名空間 \` MyNamespaceName 中 \` ，獲得 \` 授權規則 MyAuthRuleName。 \`</span><span class="sxs-lookup"><span data-stu-id="4e61f-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4e61f-124">範例 6：Alias 的 AuthorizationRules (GeoRecovery Configuration) </span><span class="sxs-lookup"><span data-stu-id="4e61f-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="4e61f-125">在命名空間 \` MyNamespaceName 中，獲得所有授權規則 \` \` MyAuthRuleName 的清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="4e61f-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4e61f-126">參數</span><span class="sxs-lookup"><span data-stu-id="4e61f-126">PARAMETERS</span></span>

### <span data-ttu-id="4e61f-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4e61f-127">-AliasName</span></span>
<span data-ttu-id="4e61f-128">別名名稱</span><span class="sxs-lookup"><span data-stu-id="4e61f-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e61f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e61f-129">-DefaultProfile</span></span>
<span data-ttu-id="4e61f-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e61f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e61f-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="4e61f-131">-Eventhub</span></span>
<span data-ttu-id="4e61f-132">Eventhub 名稱</span><span class="sxs-lookup"><span data-stu-id="4e61f-132">Eventhub Name</span></span>

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

### <span data-ttu-id="4e61f-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e61f-133">-Name</span></span>
<span data-ttu-id="4e61f-134">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="4e61f-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e61f-135">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4e61f-135">-Namespace</span></span>
<span data-ttu-id="4e61f-136">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="4e61f-136">Namespace Name</span></span>

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

### <span data-ttu-id="4e61f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e61f-137">-ResourceGroupName</span></span>
<span data-ttu-id="4e61f-138">資源組名</span><span class="sxs-lookup"><span data-stu-id="4e61f-138">Resource Group Name</span></span>

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

### <span data-ttu-id="4e61f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e61f-139">CommonParameters</span></span>
<span data-ttu-id="4e61f-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e61f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e61f-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4e61f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e61f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4e61f-142">INPUTS</span></span>

### <span data-ttu-id="4e61f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4e61f-143">System.String</span></span>

## <span data-ttu-id="4e61f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4e61f-144">OUTPUTS</span></span>

### <span data-ttu-id="4e61f-145">Microsoft.Azure.Commands.EventHub.models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4e61f-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4e61f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4e61f-146">NOTES</span></span>

## <span data-ttu-id="4e61f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e61f-147">RELATED LINKS</span></span>
