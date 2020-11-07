---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793634"
---
# <span data-ttu-id="93541-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="93541-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="93541-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93541-102">SYNOPSIS</span></span>
<span data-ttu-id="93541-103">建立訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="93541-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="93541-104">句法</span><span class="sxs-lookup"><span data-stu-id="93541-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93541-105">說明</span><span class="sxs-lookup"><span data-stu-id="93541-105">DESCRIPTION</span></span>
<span data-ttu-id="93541-106">建立訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="93541-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="93541-107">示例</span><span class="sxs-lookup"><span data-stu-id="93541-107">EXAMPLES</span></span>

### <span data-ttu-id="93541-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="93541-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="93541-109">建立訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="93541-109">Create an subscription plan.</span></span>

## <span data-ttu-id="93541-110">參數</span><span class="sxs-lookup"><span data-stu-id="93541-110">PARAMETERS</span></span>

### <span data-ttu-id="93541-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="93541-111">-AcquisitionId</span></span>
<span data-ttu-id="93541-112">購置識別碼。</span><span class="sxs-lookup"><span data-stu-id="93541-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93541-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="93541-113">-PlanId</span></span>
<span data-ttu-id="93541-114">租使用者訂閱內容中的 [規劃識別碼]。</span><span class="sxs-lookup"><span data-stu-id="93541-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="93541-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93541-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="93541-116">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="93541-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93541-117">-確認</span><span class="sxs-lookup"><span data-stu-id="93541-117">-Confirm</span></span>
<span data-ttu-id="93541-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93541-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93541-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93541-119">-WhatIf</span></span>
<span data-ttu-id="93541-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93541-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93541-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93541-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93541-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93541-122">CommonParameters</span></span>
<span data-ttu-id="93541-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93541-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93541-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93541-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93541-125">輸入</span><span class="sxs-lookup"><span data-stu-id="93541-125">INPUTS</span></span>

## <span data-ttu-id="93541-126">輸出</span><span class="sxs-lookup"><span data-stu-id="93541-126">OUTPUTS</span></span>

### <span data-ttu-id="93541-127">AzureStack PlanAcquisition 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="93541-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="93541-128">筆記</span><span class="sxs-lookup"><span data-stu-id="93541-128">NOTES</span></span>

## <span data-ttu-id="93541-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="93541-129">RELATED LINKS</span></span>

