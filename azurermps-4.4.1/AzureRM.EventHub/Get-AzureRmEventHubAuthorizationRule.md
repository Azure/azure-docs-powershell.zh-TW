---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456688"
---
# <span data-ttu-id="0ae2a-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0ae2a-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="0ae2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ae2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae2a-103">取得授權規則的詳細資料，或取得授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ae2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ae2a-104">SYNTAX</span></span>

### <span data-ttu-id="0ae2a-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0ae2a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="0ae2a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ae2a-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="0ae2a-107">說明</span><span class="sxs-lookup"><span data-stu-id="0ae2a-107">DESCRIPTION</span></span>
<span data-ttu-id="0ae2a-108">Get-AzureRmEventHubAuthorizationRule Cmdlet 會取得授權規則的詳細資料，或指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="0ae2a-109">如果提供授權規則的名稱，則會傳回單一授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="0ae2a-110">如果未提供授權規則的名稱，則會傳回指定事件中心的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="0ae2a-111">示例</span><span class="sxs-lookup"><span data-stu-id="0ae2a-111">EXAMPLES</span></span>

### <span data-ttu-id="0ae2a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0ae2a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="0ae2a-113">取得 \` \` 事件中心 MyEventHubName 中的授權規則 MyAuthRuleName \` \` ，這是由命名空間 MyNamespaceName 所限定的 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="0ae2a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="0ae2a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="0ae2a-115">取得事件中心 MyEventHubName 中所有授權規則的清單 \` \` （由命名空間 MyNamespaceName 來限定） \` \` 。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="0ae2a-116">參數</span><span class="sxs-lookup"><span data-stu-id="0ae2a-116">PARAMETERS</span></span>

### <span data-ttu-id="0ae2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ae2a-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-118">Resource group name.</span></span>

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

### <span data-ttu-id="0ae2a-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="0ae2a-119">-Eventhub</span></span>
<span data-ttu-id="0ae2a-120">Eventhub Name。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="0ae2a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ae2a-121">-Name</span></span>
<span data-ttu-id="0ae2a-122">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae2a-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0ae2a-123">-Namespace</span></span>
<span data-ttu-id="0ae2a-124">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="0ae2a-124">Namespace Name.</span></span>

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

## <span data-ttu-id="0ae2a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0ae2a-125">INPUTS</span></span>

### <span data-ttu-id="0ae2a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="0ae2a-126">System.String</span></span>

## <span data-ttu-id="0ae2a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0ae2a-127">OUTPUTS</span></span>

### <span data-ttu-id="0ae2a-128">[System.object]。清單 ' 1 [SharedAccessAuthorizationRuleAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="0ae2a-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0ae2a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0ae2a-129">NOTES</span></span>

## <span data-ttu-id="0ae2a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ae2a-130">RELATED LINKS</span></span>

