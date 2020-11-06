---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454243"
---
# <span data-ttu-id="c99d6-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c99d6-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c99d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c99d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c99d6-103">取得授權規則的詳細資料，或取得授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="c99d6-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c99d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c99d6-104">SYNTAX</span></span>

### <span data-ttu-id="c99d6-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c99d6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99d6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c99d6-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99d6-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c99d6-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99d6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c99d6-108">DESCRIPTION</span></span>
<span data-ttu-id="c99d6-109">Get-AzureRmEventHubAuthorizationRule Cmdlet 會取得授權規則的詳細資料，或指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="c99d6-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="c99d6-110">如果提供授權規則的名稱，則會傳回單一授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c99d6-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="c99d6-111">如果未提供授權規則的名稱，則會傳回指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="c99d6-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="c99d6-112">如果提供 (災害復原) 的別名名稱，則會傳回設定別名之命名空間之授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c99d6-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="c99d6-113">示例</span><span class="sxs-lookup"><span data-stu-id="c99d6-113">EXAMPLES</span></span>

### <span data-ttu-id="c99d6-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c99d6-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="c99d6-115">取得 \` \` 事件中心 MyEventHubName 中的授權規則 MyAuthRuleName \` \` ，這是由命名空間 MyNamespaceName 所限定的 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c99d6-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c99d6-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c99d6-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c99d6-117">取得事件中心 MyEventHubName 中所有授權規則的清單 \` \` （由命名空間 MyNamespaceName 來限定） \` \` 。</span><span class="sxs-lookup"><span data-stu-id="c99d6-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c99d6-118">範例3</span><span class="sxs-lookup"><span data-stu-id="c99d6-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="c99d6-119">取得 \` \` 命名空間 MyNamespaceName 中的授權規則 \` MyAuthRuleName \` 。</span><span class="sxs-lookup"><span data-stu-id="c99d6-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c99d6-120">參數</span><span class="sxs-lookup"><span data-stu-id="c99d6-120">PARAMETERS</span></span>

### <span data-ttu-id="c99d6-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c99d6-121">-AliasName</span></span>
<span data-ttu-id="c99d6-122">別名名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99d6-123">-DefaultProfile</span></span>
<span data-ttu-id="c99d6-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c99d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99d6-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="c99d6-125">-Eventhub</span></span>
<span data-ttu-id="c99d6-126">Eventhub 名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-126">Eventhub Name</span></span>

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

### <span data-ttu-id="c99d6-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-127">-Name</span></span>
<span data-ttu-id="c99d6-128">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99d6-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c99d6-129">-Namespace</span></span>
<span data-ttu-id="c99d6-130">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99d6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99d6-131">-ResourceGroupName</span></span>
<span data-ttu-id="c99d6-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c99d6-132">Resource Group Name</span></span>

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

### <span data-ttu-id="c99d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99d6-133">CommonParameters</span></span>
<span data-ttu-id="c99d6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c99d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c99d6-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c99d6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99d6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c99d6-136">INPUTS</span></span>

### <span data-ttu-id="c99d6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c99d6-137">System.String</span></span>


## <span data-ttu-id="c99d6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c99d6-138">OUTPUTS</span></span>

### <span data-ttu-id="c99d6-139">[System.object]。清單 ' 1 [PSSharedAccessAuthorizationRuleAttributes，0.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="c99d6-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="c99d6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c99d6-140">NOTES</span></span>

## <span data-ttu-id="c99d6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c99d6-141">RELATED LINKS</span></span>
