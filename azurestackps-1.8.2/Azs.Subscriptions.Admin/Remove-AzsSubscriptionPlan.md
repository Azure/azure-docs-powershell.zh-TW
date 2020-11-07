---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968256"
---
# <span data-ttu-id="4b40e-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="4b40e-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="4b40e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b40e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b40e-103">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="4b40e-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="4b40e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b40e-104">SYNTAX</span></span>

### <span data-ttu-id="4b40e-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4b40e-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b40e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b40e-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b40e-107">說明</span><span class="sxs-lookup"><span data-stu-id="4b40e-107">DESCRIPTION</span></span>
<span data-ttu-id="4b40e-108">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="4b40e-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="4b40e-109">示例</span><span class="sxs-lookup"><span data-stu-id="4b40e-109">EXAMPLES</span></span>

### <span data-ttu-id="4b40e-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4b40e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="4b40e-111">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="4b40e-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="4b40e-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b40e-112">PARAMETERS</span></span>

### <span data-ttu-id="4b40e-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="4b40e-113">-AcquisitionId</span></span>
<span data-ttu-id="4b40e-114">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="4b40e-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b40e-115">-Force</span></span>
<span data-ttu-id="4b40e-116">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="4b40e-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="4b40e-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b40e-117">-ResourceId</span></span>
<span data-ttu-id="4b40e-118">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4b40e-118">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b40e-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b40e-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="4b40e-120">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4b40e-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4b40e-121">-Confirm</span></span>
<span data-ttu-id="4b40e-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b40e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b40e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b40e-123">-WhatIf</span></span>
<span data-ttu-id="4b40e-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b40e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b40e-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b40e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b40e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b40e-126">CommonParameters</span></span>
<span data-ttu-id="4b40e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b40e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b40e-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b40e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b40e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4b40e-129">INPUTS</span></span>

## <span data-ttu-id="4b40e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4b40e-130">OUTPUTS</span></span>

## <span data-ttu-id="4b40e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4b40e-131">NOTES</span></span>

## <span data-ttu-id="4b40e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b40e-132">RELATED LINKS</span></span>

