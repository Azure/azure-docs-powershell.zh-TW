---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793610"
---
# <span data-ttu-id="57476-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="57476-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="57476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57476-102">SYNOPSIS</span></span>
<span data-ttu-id="57476-103">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="57476-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="57476-104">句法</span><span class="sxs-lookup"><span data-stu-id="57476-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57476-105">說明</span><span class="sxs-lookup"><span data-stu-id="57476-105">DESCRIPTION</span></span>
<span data-ttu-id="57476-106">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="57476-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="57476-107">示例</span><span class="sxs-lookup"><span data-stu-id="57476-107">EXAMPLES</span></span>

### <span data-ttu-id="57476-108">範例1</span><span class="sxs-lookup"><span data-stu-id="57476-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="57476-109">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="57476-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="57476-110">參數</span><span class="sxs-lookup"><span data-stu-id="57476-110">PARAMETERS</span></span>

### <span data-ttu-id="57476-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57476-111">-SubscriptionId</span></span>
<span data-ttu-id="57476-112">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="57476-112">Id of the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57476-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57476-113">-Force</span></span>
<span data-ttu-id="57476-114">在不提示的情況下移除訂閱</span><span class="sxs-lookup"><span data-stu-id="57476-114">Remove subscription without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57476-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57476-115">-WhatIf</span></span>
<span data-ttu-id="57476-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57476-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57476-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57476-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57476-118">-確認</span><span class="sxs-lookup"><span data-stu-id="57476-118">-Confirm</span></span>
<span data-ttu-id="57476-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57476-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57476-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57476-120">CommonParameters</span></span>
<span data-ttu-id="57476-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57476-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57476-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57476-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57476-123">輸入</span><span class="sxs-lookup"><span data-stu-id="57476-123">INPUTS</span></span>

## <span data-ttu-id="57476-124">輸出</span><span class="sxs-lookup"><span data-stu-id="57476-124">OUTPUTS</span></span>

## <span data-ttu-id="57476-125">筆記</span><span class="sxs-lookup"><span data-stu-id="57476-125">NOTES</span></span>

## <span data-ttu-id="57476-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="57476-126">RELATED LINKS</span></span>
