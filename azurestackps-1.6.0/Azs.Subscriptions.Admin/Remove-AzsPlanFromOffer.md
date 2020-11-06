---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443396"
---
# <span data-ttu-id="435ef-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="435ef-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="435ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="435ef-102">SYNOPSIS</span></span>
<span data-ttu-id="435ef-103">從優惠中取消連結方案。</span><span class="sxs-lookup"><span data-stu-id="435ef-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="435ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="435ef-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435ef-105">說明</span><span class="sxs-lookup"><span data-stu-id="435ef-105">DESCRIPTION</span></span>
<span data-ttu-id="435ef-106">從優惠中取消連結方案。</span><span class="sxs-lookup"><span data-stu-id="435ef-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="435ef-107">示例</span><span class="sxs-lookup"><span data-stu-id="435ef-107">EXAMPLES</span></span>

### <span data-ttu-id="435ef-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="435ef-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="435ef-109">參數</span><span class="sxs-lookup"><span data-stu-id="435ef-109">PARAMETERS</span></span>

### <span data-ttu-id="435ef-110">-Force</span><span class="sxs-lookup"><span data-stu-id="435ef-110">-Force</span></span>
<span data-ttu-id="435ef-111">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="435ef-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="435ef-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="435ef-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="435ef-113">由訂閱者所取得的最大購置計數</span><span class="sxs-lookup"><span data-stu-id="435ef-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="435ef-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="435ef-114">-OfferName</span></span>
<span data-ttu-id="435ef-115">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="435ef-115">Name of an offer.</span></span>

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

### <span data-ttu-id="435ef-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="435ef-116">-PlanLinkType</span></span>
<span data-ttu-id="435ef-117">[方案] 連結的類型。</span><span class="sxs-lookup"><span data-stu-id="435ef-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="435ef-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="435ef-118">-PlanName</span></span>
<span data-ttu-id="435ef-119">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="435ef-119">Name of the plan.</span></span>

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

### <span data-ttu-id="435ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="435ef-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="435ef-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="435ef-122">-確認</span><span class="sxs-lookup"><span data-stu-id="435ef-122">-Confirm</span></span>
<span data-ttu-id="435ef-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="435ef-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435ef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435ef-124">-WhatIf</span></span>
<span data-ttu-id="435ef-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="435ef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435ef-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="435ef-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435ef-127">CommonParameters</span></span>
<span data-ttu-id="435ef-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="435ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435ef-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="435ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435ef-130">輸入</span><span class="sxs-lookup"><span data-stu-id="435ef-130">INPUTS</span></span>

## <span data-ttu-id="435ef-131">輸出</span><span class="sxs-lookup"><span data-stu-id="435ef-131">OUTPUTS</span></span>

## <span data-ttu-id="435ef-132">筆記</span><span class="sxs-lookup"><span data-stu-id="435ef-132">NOTES</span></span>

## <span data-ttu-id="435ef-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="435ef-133">RELATED LINKS</span></span>

