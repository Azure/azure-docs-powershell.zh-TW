---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456660"
---
# <span data-ttu-id="e7d35-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e7d35-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="e7d35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7d35-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d35-103">針對指定事件中樞命名空間上的授權規則，建立新的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="e7d35-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d35-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7d35-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e7d35-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7d35-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d35-106">New-AzureRmEventHubNamespaceKey Cmdlet 會針對指定事件中樞命名空間上的指定授權規則，重新生成主要或輔助金鑰。</span><span class="sxs-lookup"><span data-stu-id="e7d35-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e7d35-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7d35-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d35-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e7d35-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="e7d35-109">\` \` 在事件中心命名空間 \` MyNamespaceName 中 \` ，使用資源群組 \` MyResourceGroupName \` 重新產生授權規則 MyAuthRuleName 的主鍵。</span><span class="sxs-lookup"><span data-stu-id="e7d35-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e7d35-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7d35-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d35-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e7d35-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="e7d35-112">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e7d35-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d35-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e7d35-113">-NamespaceName</span></span>
<span data-ttu-id="e7d35-114">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e7d35-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="e7d35-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e7d35-115">-RegenerateKeys</span></span>
<span data-ttu-id="e7d35-116">要重新產生： \` PrimaryKey \` 或 \` SecondaryKey \` 的按鍵。</span><span class="sxs-lookup"><span data-stu-id="e7d35-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d35-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7d35-117">-ResourceGroup</span></span>
<span data-ttu-id="e7d35-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7d35-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7d35-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e7d35-119">-Confirm</span></span>
<span data-ttu-id="e7d35-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7d35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d35-121">-WhatIf</span></span>
<span data-ttu-id="e7d35-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7d35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d35-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7d35-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="e7d35-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e7d35-124">INPUTS</span></span>

### <span data-ttu-id="e7d35-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e7d35-125">System.String</span></span>

## <span data-ttu-id="e7d35-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e7d35-126">OUTPUTS</span></span>

### <span data-ttu-id="e7d35-127">ListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7d35-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="e7d35-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e7d35-128">NOTES</span></span>

## <span data-ttu-id="e7d35-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7d35-129">RELATED LINKS</span></span>

