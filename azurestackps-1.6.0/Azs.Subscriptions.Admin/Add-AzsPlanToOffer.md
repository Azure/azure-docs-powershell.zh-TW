---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442752"
---
# <span data-ttu-id="25735-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="25735-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="25735-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25735-102">SYNOPSIS</span></span>
<span data-ttu-id="25735-103">將計畫連結至優惠。</span><span class="sxs-lookup"><span data-stu-id="25735-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="25735-104">句法</span><span class="sxs-lookup"><span data-stu-id="25735-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25735-105">說明</span><span class="sxs-lookup"><span data-stu-id="25735-105">DESCRIPTION</span></span>
<span data-ttu-id="25735-106">將計畫連結至優惠。</span><span class="sxs-lookup"><span data-stu-id="25735-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="25735-107">示例</span><span class="sxs-lookup"><span data-stu-id="25735-107">EXAMPLES</span></span>

### <span data-ttu-id="25735-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25735-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="25735-109">參數</span><span class="sxs-lookup"><span data-stu-id="25735-109">PARAMETERS</span></span>

### <span data-ttu-id="25735-110">-Force</span><span class="sxs-lookup"><span data-stu-id="25735-110">-Force</span></span>
<span data-ttu-id="25735-111">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="25735-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="25735-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="25735-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="25735-113">由訂閱者所取得的最大購置計數</span><span class="sxs-lookup"><span data-stu-id="25735-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25735-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="25735-114">-OfferName</span></span>
<span data-ttu-id="25735-115">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="25735-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25735-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="25735-116">-PlanLinkType</span></span>
<span data-ttu-id="25735-117">[方案] 連結的類型。</span><span class="sxs-lookup"><span data-stu-id="25735-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25735-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="25735-118">-PlanName</span></span>
<span data-ttu-id="25735-119">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="25735-119">Name of the plan.</span></span>

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

### <span data-ttu-id="25735-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25735-120">-ResourceGroupName</span></span>
<span data-ttu-id="25735-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="25735-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25735-122">-確認</span><span class="sxs-lookup"><span data-stu-id="25735-122">-Confirm</span></span>
<span data-ttu-id="25735-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25735-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25735-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25735-124">-WhatIf</span></span>
<span data-ttu-id="25735-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25735-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25735-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25735-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25735-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25735-127">CommonParameters</span></span>
<span data-ttu-id="25735-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25735-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25735-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25735-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25735-130">輸入</span><span class="sxs-lookup"><span data-stu-id="25735-130">INPUTS</span></span>

## <span data-ttu-id="25735-131">輸出</span><span class="sxs-lookup"><span data-stu-id="25735-131">OUTPUTS</span></span>

## <span data-ttu-id="25735-132">筆記</span><span class="sxs-lookup"><span data-stu-id="25735-132">NOTES</span></span>

## <span data-ttu-id="25735-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="25735-133">RELATED LINKS</span></span>

