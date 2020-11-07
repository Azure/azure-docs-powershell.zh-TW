---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626302"
---
# <span data-ttu-id="e1aa4-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e1aa4-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="e1aa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1aa4-103">取得 Eventubs 命名空間授權規則的詳細資料，或取得授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1aa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1aa4-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="e1aa4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="e1aa4-106">Get-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會取得指定事件中樞命名空間授權規則的詳細資料，或命名空間授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="e1aa4-107">如果提供授權規則名稱，則會傳回單一授權規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="e1aa4-108">如果未提供授權規則名稱，則會傳回命名空間中的所有授權規則清單。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="e1aa4-109">示例</span><span class="sxs-lookup"><span data-stu-id="e1aa4-109">EXAMPLES</span></span>

### <span data-ttu-id="e1aa4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e1aa4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="e1aa4-111">傳回 \` \` 事件中心命名空間 MyNamespaceName 中的授權規則 \` MyAuthRuleName \` （含資源群組 \` MyResourceGroupName） \` 。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e1aa4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="e1aa4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="e1aa4-113">傳回 [ \` \` 事件中心] 命名空間 MyNamespaceName 中的預設授權規則 RootManageSharedAccessKey \` \` ，其中包含 [資源群組 \` MyResourceGroupName] \` 。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e1aa4-114">範例3</span><span class="sxs-lookup"><span data-stu-id="e1aa4-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e1aa4-115">傳回 [事件中心] 命名空間 MyNamespaceName 中的所有授權規則 \` \` ，以及 [資源] 群組 \` MyResourceGroupName \` 。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e1aa4-116">參數</span><span class="sxs-lookup"><span data-stu-id="e1aa4-116">PARAMETERS</span></span>

### <span data-ttu-id="e1aa4-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e1aa4-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="e1aa4-118">事件中心命名空間授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1aa4-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e1aa4-119">-NamespaceName</span></span>
<span data-ttu-id="e1aa4-120">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-120">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1aa4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1aa4-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1aa4-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e1aa4-122">Resource group name.</span></span>

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

## <span data-ttu-id="e1aa4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e1aa4-123">INPUTS</span></span>

### <span data-ttu-id="e1aa4-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e1aa4-124">System.String</span></span>

## <span data-ttu-id="e1aa4-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e1aa4-125">OUTPUTS</span></span>

### <span data-ttu-id="e1aa4-126">[System.object]。清單 ' 1 [SharedAccessAuthorizationRuleAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="e1aa4-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e1aa4-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e1aa4-127">NOTES</span></span>

## <span data-ttu-id="e1aa4-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1aa4-128">RELATED LINKS</span></span>

