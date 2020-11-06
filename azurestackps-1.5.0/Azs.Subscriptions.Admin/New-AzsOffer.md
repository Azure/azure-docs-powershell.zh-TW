---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442684"
---
# <span data-ttu-id="38c0f-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="38c0f-101">New-AzsOffer</span></span>

## <span data-ttu-id="38c0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="38c0f-103">建立新的優惠。</span><span class="sxs-lookup"><span data-stu-id="38c0f-103">Creates a new offer.</span></span>

## <span data-ttu-id="38c0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="38c0f-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="38c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="38c0f-106">建立或更新優惠。</span><span class="sxs-lookup"><span data-stu-id="38c0f-106">Create or update the offer.</span></span>

## <span data-ttu-id="38c0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="38c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="38c0f-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="38c0f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="38c0f-109">建立新的優惠。</span><span class="sxs-lookup"><span data-stu-id="38c0f-109">Creates a new offer.</span></span>

## <span data-ttu-id="38c0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="38c0f-110">PARAMETERS</span></span>

### <span data-ttu-id="38c0f-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="38c0f-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="38c0f-112">提供給附加元件方案的參考，租使用者也可以選擇作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="38c0f-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="38c0f-113">-BasePlanIds</span></span>
<span data-ttu-id="38c0f-114">當租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="38c0f-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-115">-描述</span><span class="sxs-lookup"><span data-stu-id="38c0f-115">-Description</span></span>
<span data-ttu-id="38c0f-116">優惠說明。</span><span class="sxs-lookup"><span data-stu-id="38c0f-116">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="38c0f-117">-DisplayName</span></span>
<span data-ttu-id="38c0f-118">[優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="38c0f-118">Display name of offer.</span></span>

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

### <span data-ttu-id="38c0f-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="38c0f-119">-ExternalReferenceId</span></span>
<span data-ttu-id="38c0f-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="38c0f-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-121">-位置</span><span class="sxs-lookup"><span data-stu-id="38c0f-121">-Location</span></span>
<span data-ttu-id="38c0f-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="38c0f-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="38c0f-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="38c0f-124">每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="38c0f-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="38c0f-125">-Name</span></span>
<span data-ttu-id="38c0f-126">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="38c0f-126">Name of an offer.</span></span>

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

### <span data-ttu-id="38c0f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c0f-127">-ResourceGroupName</span></span>
<span data-ttu-id="38c0f-128">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="38c0f-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="38c0f-129">-State</span><span class="sxs-lookup"><span data-stu-id="38c0f-129">-State</span></span>
<span data-ttu-id="38c0f-130">提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="38c0f-130">Offer accessibility state.</span></span>
<span data-ttu-id="38c0f-131">預設值為 [私人]。</span><span class="sxs-lookup"><span data-stu-id="38c0f-131">Default value is Private.</span></span>
<span data-ttu-id="38c0f-132">未來版本中將會棄用此參數</span><span class="sxs-lookup"><span data-stu-id="38c0f-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="38c0f-133">-SubscriptionCount</span></span>
<span data-ttu-id="38c0f-134">目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="38c0f-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c0f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="38c0f-135">-Confirm</span></span>
<span data-ttu-id="38c0f-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38c0f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c0f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c0f-137">-WhatIf</span></span>
<span data-ttu-id="38c0f-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38c0f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c0f-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38c0f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c0f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c0f-140">CommonParameters</span></span>
<span data-ttu-id="38c0f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38c0f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c0f-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38c0f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c0f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="38c0f-143">INPUTS</span></span>

## <span data-ttu-id="38c0f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="38c0f-144">OUTPUTS</span></span>

### <span data-ttu-id="38c0f-145">AzureStack 的訂閱. 管理模型。</span><span class="sxs-lookup"><span data-stu-id="38c0f-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="38c0f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="38c0f-146">NOTES</span></span>

## <span data-ttu-id="38c0f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="38c0f-147">RELATED LINKS</span></span>

