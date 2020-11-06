---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456663"
---
# <span data-ttu-id="62db9-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="62db9-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="62db9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62db9-102">SYNOPSIS</span></span>
<span data-ttu-id="62db9-103">針對指定的事件中心授權規則，建立新的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="62db9-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62db9-104">句法</span><span class="sxs-lookup"><span data-stu-id="62db9-104">SYNTAX</span></span>

### <span data-ttu-id="62db9-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62db9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62db9-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="62db9-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="62db9-107">說明</span><span class="sxs-lookup"><span data-stu-id="62db9-107">DESCRIPTION</span></span>
<span data-ttu-id="62db9-108">New-AzureRmEventHubKey Cmdlet 會為指定的事件中心授權規則重新產生主要或次要 SAS 金鑰。</span><span class="sxs-lookup"><span data-stu-id="62db9-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="62db9-109">示例</span><span class="sxs-lookup"><span data-stu-id="62db9-109">EXAMPLES</span></span>

### <span data-ttu-id="62db9-110">範例1。1</span><span class="sxs-lookup"><span data-stu-id="62db9-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="62db9-111">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="62db9-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="62db9-112">範例1。2</span><span class="sxs-lookup"><span data-stu-id="62db9-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="62db9-113">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="62db9-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="62db9-114">範例2。1</span><span class="sxs-lookup"><span data-stu-id="62db9-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="62db9-115">範例2。2</span><span class="sxs-lookup"><span data-stu-id="62db9-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="62db9-116">重新生成授權規則 MyAuthRuleName 的次要金鑰 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="62db9-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="62db9-117">參數</span><span class="sxs-lookup"><span data-stu-id="62db9-117">PARAMETERS</span></span>

### <span data-ttu-id="62db9-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="62db9-118">-RegenerateKey</span></span>
<span data-ttu-id="62db9-119">要重新產生： \` PrimaryKey \` 或 \` SecondaryKey \` 的按鍵。</span><span class="sxs-lookup"><span data-stu-id="62db9-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62db9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="62db9-120">-Confirm</span></span>
<span data-ttu-id="62db9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62db9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62db9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62db9-122">-WhatIf</span></span>
<span data-ttu-id="62db9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62db9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62db9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62db9-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62db9-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="62db9-125">-EventHub</span></span>
<span data-ttu-id="62db9-126">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="62db9-126">EventHub Name.</span></span>

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

### <span data-ttu-id="62db9-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="62db9-127">-Name</span></span>
<span data-ttu-id="62db9-128">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="62db9-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62db9-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="62db9-129">-Namespace</span></span>
<span data-ttu-id="62db9-130">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="62db9-130">Namespace Name.</span></span>

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

### <span data-ttu-id="62db9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62db9-131">-ResourceGroupName</span></span>
<span data-ttu-id="62db9-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="62db9-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="62db9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="62db9-133">INPUTS</span></span>

### <span data-ttu-id="62db9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="62db9-134">System.String</span></span>

## <span data-ttu-id="62db9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="62db9-135">OUTPUTS</span></span>

### <span data-ttu-id="62db9-136">ListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="62db9-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="62db9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="62db9-137">NOTES</span></span>

## <span data-ttu-id="62db9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="62db9-138">RELATED LINKS</span></span>

