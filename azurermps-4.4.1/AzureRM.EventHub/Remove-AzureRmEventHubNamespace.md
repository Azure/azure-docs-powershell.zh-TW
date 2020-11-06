---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451699"
---
# <span data-ttu-id="53c1b-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="53c1b-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="53c1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="53c1b-103">移除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="53c1b-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53c1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="53c1b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="53c1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="53c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="53c1b-106">Remove-AzureRmEventHubNamespace Cmdlet 會移除並刪除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="53c1b-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="53c1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="53c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="53c1b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53c1b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="53c1b-109">移除 \` \` 資源群組 MyResourceGroupName 中的 [事件中心] 命名空間 MyNamespaceName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="53c1b-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="53c1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="53c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="53c1b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c1b-111">-ResourceGroupName</span></span>
<span data-ttu-id="53c1b-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="53c1b-112">Resource group name.</span></span>

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

### <span data-ttu-id="53c1b-113">-確認</span><span class="sxs-lookup"><span data-stu-id="53c1b-113">-Confirm</span></span>
<span data-ttu-id="53c1b-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53c1b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c1b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c1b-115">-WhatIf</span></span>
<span data-ttu-id="53c1b-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53c1b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c1b-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53c1b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c1b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="53c1b-118">-Name</span></span>
<span data-ttu-id="53c1b-119">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="53c1b-119">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="53c1b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="53c1b-120">INPUTS</span></span>

### <span data-ttu-id="53c1b-121">System.object</span><span class="sxs-lookup"><span data-stu-id="53c1b-121">System.String</span></span>

## <span data-ttu-id="53c1b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="53c1b-122">OUTPUTS</span></span>

### <span data-ttu-id="53c1b-123">System.object</span><span class="sxs-lookup"><span data-stu-id="53c1b-123">System.Object</span></span>

## <span data-ttu-id="53c1b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="53c1b-124">NOTES</span></span>

## <span data-ttu-id="53c1b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="53c1b-125">RELATED LINKS</span></span>

