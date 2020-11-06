---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442872"
---
# <span data-ttu-id="dc829-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="dc829-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="dc829-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc829-102">SYNOPSIS</span></span>
<span data-ttu-id="dc829-103">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="dc829-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="dc829-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc829-104">SYNTAX</span></span>

### <span data-ttu-id="dc829-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="dc829-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc829-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc829-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc829-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc829-107">DESCRIPTION</span></span>
<span data-ttu-id="dc829-108">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="dc829-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="dc829-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc829-109">EXAMPLES</span></span>

### <span data-ttu-id="dc829-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dc829-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="dc829-111">刪除訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="dc829-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="dc829-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc829-112">PARAMETERS</span></span>

### <span data-ttu-id="dc829-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="dc829-113">-AcquisitionId</span></span>
<span data-ttu-id="dc829-114">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="dc829-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="dc829-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dc829-115">-Force</span></span>
<span data-ttu-id="dc829-116">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="dc829-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="dc829-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc829-117">-ResourceId</span></span>
<span data-ttu-id="dc829-118">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dc829-118">The resource id.</span></span>

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

### <span data-ttu-id="dc829-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc829-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="dc829-120">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="dc829-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="dc829-121">-確認</span><span class="sxs-lookup"><span data-stu-id="dc829-121">-Confirm</span></span>
<span data-ttu-id="dc829-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc829-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc829-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc829-123">-WhatIf</span></span>
<span data-ttu-id="dc829-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc829-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc829-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc829-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc829-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc829-126">CommonParameters</span></span>
<span data-ttu-id="dc829-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc829-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc829-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc829-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc829-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dc829-129">INPUTS</span></span>

## <span data-ttu-id="dc829-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dc829-130">OUTPUTS</span></span>

## <span data-ttu-id="dc829-131">筆記</span><span class="sxs-lookup"><span data-stu-id="dc829-131">NOTES</span></span>

## <span data-ttu-id="dc829-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc829-132">RELATED LINKS</span></span>

