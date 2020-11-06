---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443288"
---
# <span data-ttu-id="f478a-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="f478a-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="f478a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f478a-102">SYNOPSIS</span></span>
<span data-ttu-id="f478a-103">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f478a-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="f478a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f478a-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f478a-105">說明</span><span class="sxs-lookup"><span data-stu-id="f478a-105">DESCRIPTION</span></span>
<span data-ttu-id="f478a-106">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f478a-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="f478a-107">示例</span><span class="sxs-lookup"><span data-stu-id="f478a-107">EXAMPLES</span></span>

### <span data-ttu-id="f478a-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f478a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="f478a-109">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f478a-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="f478a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f478a-110">PARAMETERS</span></span>

### <span data-ttu-id="f478a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f478a-111">-Force</span></span>
<span data-ttu-id="f478a-112">在不提示的情況下移除訂閱</span><span class="sxs-lookup"><span data-stu-id="f478a-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="f478a-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f478a-113">-SubscriptionId</span></span>
<span data-ttu-id="f478a-114">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="f478a-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="f478a-115">-確認</span><span class="sxs-lookup"><span data-stu-id="f478a-115">-Confirm</span></span>
<span data-ttu-id="f478a-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f478a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f478a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f478a-117">-WhatIf</span></span>
<span data-ttu-id="f478a-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f478a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f478a-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f478a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f478a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f478a-120">CommonParameters</span></span>
<span data-ttu-id="f478a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f478a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f478a-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f478a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f478a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f478a-123">INPUTS</span></span>

## <span data-ttu-id="f478a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f478a-124">OUTPUTS</span></span>

## <span data-ttu-id="f478a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f478a-125">NOTES</span></span>

## <span data-ttu-id="f478a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f478a-126">RELATED LINKS</span></span>

