---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273403"
---
# <span data-ttu-id="efa94-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="efa94-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="efa94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efa94-102">SYNOPSIS</span></span>
<span data-ttu-id="efa94-103">取得授權規則的詳細資料，或取得授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="efa94-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="efa94-104">句法</span><span class="sxs-lookup"><span data-stu-id="efa94-104">SYNTAX</span></span>

### <span data-ttu-id="efa94-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="efa94-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efa94-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="efa94-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efa94-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="efa94-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efa94-108">說明</span><span class="sxs-lookup"><span data-stu-id="efa94-108">DESCRIPTION</span></span>
<span data-ttu-id="efa94-109">Get-AzEventHubAuthorizationRule Cmdlet 會取得授權規則的詳細資料，或指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="efa94-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="efa94-110">如果提供授權規則的名稱，則會傳回單一授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="efa94-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="efa94-111">如果未提供授權規則的名稱，則會傳回指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="efa94-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="efa94-112">如果提供 (災害復原) 的別名名稱，則會傳回設定別名之命名空間之授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="efa94-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="efa94-113">示例</span><span class="sxs-lookup"><span data-stu-id="efa94-113">EXAMPLES</span></span>

### <span data-ttu-id="efa94-114">範例1： AuthorizationRule 命名空間</span><span class="sxs-lookup"><span data-stu-id="efa94-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="efa94-115">取得 \` \` 命名空間 MyNamespaceName 中的授權規則 \` MyAuthRuleName \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="efa94-116">範例2： AuthorizationRules 命名空間</span><span class="sxs-lookup"><span data-stu-id="efa94-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="efa94-117">取得命名空間 MyNamespaceName 中所有授權規則的清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="efa94-118">範例3： EventHub 的 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="efa94-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="efa94-119">取得 \` \` 事件中心 MyEventHubName 中的授權規則 MyAuthRuleName \` \` ，這是由命名空間 MyNamespaceName 所限定的 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="efa94-120">範例4： EventHub 的 AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="efa94-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="efa94-121">取得 [事件中心 MyEventHubName] 中的清單授權規則 \` \` ，其範圍是由命名空間 \` MyNamespaceName 決定 \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="efa94-122">範例5： AuthorizationRule 的別名 (GeoRecovery 配置) </span><span class="sxs-lookup"><span data-stu-id="efa94-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="efa94-123">取得 \` \` 命名空間 MyNamespaceName 中的授權規則 \` MyAuthRuleName \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="efa94-124">範例6： AuthorizationRules 的別名 (GeoRecovery 配置) </span><span class="sxs-lookup"><span data-stu-id="efa94-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="efa94-125">取得 \` \` 命名空間 MyNamespaceName 中所有授權規則 MyAuthRuleName 的清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="efa94-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="efa94-126">參數</span><span class="sxs-lookup"><span data-stu-id="efa94-126">PARAMETERS</span></span>

### <span data-ttu-id="efa94-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="efa94-127">-AliasName</span></span>
<span data-ttu-id="efa94-128">別名名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-128">Alias Name</span></span>

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

### <span data-ttu-id="efa94-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa94-129">-DefaultProfile</span></span>
<span data-ttu-id="efa94-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efa94-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa94-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="efa94-131">-Eventhub</span></span>
<span data-ttu-id="efa94-132">Eventhub 名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-132">Eventhub Name</span></span>

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

### <span data-ttu-id="efa94-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-133">-Name</span></span>
<span data-ttu-id="efa94-134">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="efa94-135">-命名空間</span><span class="sxs-lookup"><span data-stu-id="efa94-135">-Namespace</span></span>
<span data-ttu-id="efa94-136">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-136">Namespace Name</span></span>

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

### <span data-ttu-id="efa94-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa94-137">-ResourceGroupName</span></span>
<span data-ttu-id="efa94-138">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="efa94-138">Resource Group Name</span></span>

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

### <span data-ttu-id="efa94-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa94-139">CommonParameters</span></span>
<span data-ttu-id="efa94-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efa94-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa94-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efa94-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa94-142">輸入</span><span class="sxs-lookup"><span data-stu-id="efa94-142">INPUTS</span></span>

### <span data-ttu-id="efa94-143">System.object</span><span class="sxs-lookup"><span data-stu-id="efa94-143">System.String</span></span>

## <span data-ttu-id="efa94-144">輸出</span><span class="sxs-lookup"><span data-stu-id="efa94-144">OUTPUTS</span></span>

### <span data-ttu-id="efa94-145">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="efa94-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="efa94-146">筆記</span><span class="sxs-lookup"><span data-stu-id="efa94-146">NOTES</span></span>

## <span data-ttu-id="efa94-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="efa94-147">RELATED LINKS</span></span>
