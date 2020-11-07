---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793759"
---
# <span data-ttu-id="2b37e-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="2b37e-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="2b37e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b37e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b37e-103">從優惠中取消連結方案。</span><span class="sxs-lookup"><span data-stu-id="2b37e-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="2b37e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b37e-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b37e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b37e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b37e-106">從優惠中取消連結方案。</span><span class="sxs-lookup"><span data-stu-id="2b37e-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="2b37e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2b37e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b37e-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b37e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="2b37e-109">參數</span><span class="sxs-lookup"><span data-stu-id="2b37e-109">PARAMETERS</span></span>

### <span data-ttu-id="2b37e-110">-Force</span><span class="sxs-lookup"><span data-stu-id="2b37e-110">-Force</span></span>
<span data-ttu-id="2b37e-111">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="2b37e-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="2b37e-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="2b37e-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="2b37e-113">由訂閱者所取得的最大購置計數</span><span class="sxs-lookup"><span data-stu-id="2b37e-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37e-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="2b37e-114">-OfferName</span></span>
<span data-ttu-id="2b37e-115">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b37e-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37e-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="2b37e-116">-PlanLinkType</span></span>
<span data-ttu-id="2b37e-117">[方案] 連結的類型。</span><span class="sxs-lookup"><span data-stu-id="2b37e-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37e-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2b37e-118">-PlanName</span></span>
<span data-ttu-id="2b37e-119">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="2b37e-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b37e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b37e-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2b37e-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37e-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2b37e-122">-Confirm</span></span>
<span data-ttu-id="2b37e-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b37e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b37e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b37e-124">-WhatIf</span></span>
<span data-ttu-id="2b37e-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b37e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b37e-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b37e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b37e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b37e-127">CommonParameters</span></span>
<span data-ttu-id="2b37e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b37e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b37e-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b37e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b37e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2b37e-130">INPUTS</span></span>

## <span data-ttu-id="2b37e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2b37e-131">OUTPUTS</span></span>

## <span data-ttu-id="2b37e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2b37e-132">NOTES</span></span>

## <span data-ttu-id="2b37e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b37e-133">RELATED LINKS</span></span>

