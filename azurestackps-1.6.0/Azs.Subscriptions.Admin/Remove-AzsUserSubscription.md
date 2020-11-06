---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623179"
---
# <span data-ttu-id="58374-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="58374-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="58374-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58374-102">SYNOPSIS</span></span>
<span data-ttu-id="58374-103">移除指定的租使用者訂閱。</span><span class="sxs-lookup"><span data-stu-id="58374-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="58374-104">句法</span><span class="sxs-lookup"><span data-stu-id="58374-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58374-105">說明</span><span class="sxs-lookup"><span data-stu-id="58374-105">DESCRIPTION</span></span>
<span data-ttu-id="58374-106">移除指定的租使用者訂閱。</span><span class="sxs-lookup"><span data-stu-id="58374-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="58374-107">示例</span><span class="sxs-lookup"><span data-stu-id="58374-107">EXAMPLES</span></span>

### <span data-ttu-id="58374-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="58374-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="58374-109">移除指定的租使用者訂閱。</span><span class="sxs-lookup"><span data-stu-id="58374-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="58374-110">參數</span><span class="sxs-lookup"><span data-stu-id="58374-110">PARAMETERS</span></span>

### <span data-ttu-id="58374-111">-Force</span><span class="sxs-lookup"><span data-stu-id="58374-111">-Force</span></span>
<span data-ttu-id="58374-112">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="58374-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="58374-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58374-113">-SubscriptionId</span></span>
<span data-ttu-id="58374-114">[訂閱識別碼] 參數。</span><span class="sxs-lookup"><span data-stu-id="58374-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58374-115">-確認</span><span class="sxs-lookup"><span data-stu-id="58374-115">-Confirm</span></span>
<span data-ttu-id="58374-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58374-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58374-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58374-117">-WhatIf</span></span>
<span data-ttu-id="58374-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58374-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58374-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58374-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58374-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58374-120">CommonParameters</span></span>
<span data-ttu-id="58374-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58374-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58374-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58374-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58374-123">輸入</span><span class="sxs-lookup"><span data-stu-id="58374-123">INPUTS</span></span>

## <span data-ttu-id="58374-124">輸出</span><span class="sxs-lookup"><span data-stu-id="58374-124">OUTPUTS</span></span>

## <span data-ttu-id="58374-125">筆記</span><span class="sxs-lookup"><span data-stu-id="58374-125">NOTES</span></span>

## <span data-ttu-id="58374-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="58374-126">RELATED LINKS</span></span>

