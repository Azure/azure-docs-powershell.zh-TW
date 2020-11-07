---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968391"
---
# <span data-ttu-id="94f3c-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="94f3c-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="94f3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="94f3c-103">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f3c-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="94f3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="94f3c-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="94f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="94f3c-106">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f3c-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="94f3c-107">示例</span><span class="sxs-lookup"><span data-stu-id="94f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="94f3c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="94f3c-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="94f3c-109">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f3c-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="94f3c-110">參數</span><span class="sxs-lookup"><span data-stu-id="94f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="94f3c-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94f3c-111">-SubscriptionId</span></span>
<span data-ttu-id="94f3c-112">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="94f3c-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="94f3c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="94f3c-113">-Force</span></span>
<span data-ttu-id="94f3c-114">在不提示的情況下移除訂閱</span><span class="sxs-lookup"><span data-stu-id="94f3c-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="94f3c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f3c-115">-WhatIf</span></span>
<span data-ttu-id="94f3c-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f3c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f3c-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f3c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f3c-118">-確認</span><span class="sxs-lookup"><span data-stu-id="94f3c-118">-Confirm</span></span>
<span data-ttu-id="94f3c-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94f3c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f3c-120">CommonParameters</span></span>
<span data-ttu-id="94f3c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94f3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f3c-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94f3c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f3c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="94f3c-123">INPUTS</span></span>

## <span data-ttu-id="94f3c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="94f3c-124">OUTPUTS</span></span>

## <span data-ttu-id="94f3c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="94f3c-125">NOTES</span></span>

## <span data-ttu-id="94f3c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f3c-126">RELATED LINKS</span></span>
