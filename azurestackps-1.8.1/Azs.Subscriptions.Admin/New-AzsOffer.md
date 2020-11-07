---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793808"
---
# <span data-ttu-id="dd107-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="dd107-101">New-AzsOffer</span></span>

## <span data-ttu-id="dd107-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd107-102">SYNOPSIS</span></span>
<span data-ttu-id="dd107-103">建立新的優惠。</span><span class="sxs-lookup"><span data-stu-id="dd107-103">Creates a new offer.</span></span>

## <span data-ttu-id="dd107-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd107-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd107-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd107-105">DESCRIPTION</span></span>
<span data-ttu-id="dd107-106">建立或更新優惠。</span><span class="sxs-lookup"><span data-stu-id="dd107-106">Create or update the offer.</span></span>

## <span data-ttu-id="dd107-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd107-107">EXAMPLES</span></span>

### <span data-ttu-id="dd107-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd107-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="dd107-109">建立新的優惠。</span><span class="sxs-lookup"><span data-stu-id="dd107-109">Creates a new offer.</span></span>

## <span data-ttu-id="dd107-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd107-110">PARAMETERS</span></span>

### <span data-ttu-id="dd107-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="dd107-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="dd107-112">提供給附加元件方案的參考，租使用者也可以選擇作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="dd107-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="dd107-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="dd107-113">-BasePlanIds</span></span>
<span data-ttu-id="dd107-114">當租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd107-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="dd107-115">-描述</span><span class="sxs-lookup"><span data-stu-id="dd107-115">-Description</span></span>
<span data-ttu-id="dd107-116">優惠說明。</span><span class="sxs-lookup"><span data-stu-id="dd107-116">Description of offer.</span></span>

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

### <span data-ttu-id="dd107-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd107-117">-DisplayName</span></span>
<span data-ttu-id="dd107-118">[優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="dd107-118">Display name of offer.</span></span>

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

### <span data-ttu-id="dd107-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="dd107-119">-ExternalReferenceId</span></span>
<span data-ttu-id="dd107-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd107-120">External reference identifier.</span></span>

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

### <span data-ttu-id="dd107-121">-位置</span><span class="sxs-lookup"><span data-stu-id="dd107-121">-Location</span></span>
<span data-ttu-id="dd107-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dd107-122">Location of the resource.</span></span>

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

### <span data-ttu-id="dd107-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="dd107-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="dd107-124">每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="dd107-124">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="dd107-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd107-125">-Name</span></span>
<span data-ttu-id="dd107-126">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd107-126">Name of an offer.</span></span>

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

### <span data-ttu-id="dd107-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd107-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd107-128">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="dd107-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="dd107-129">-State</span><span class="sxs-lookup"><span data-stu-id="dd107-129">-State</span></span>
<span data-ttu-id="dd107-130">提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="dd107-130">Offer accessibility state.</span></span>
<span data-ttu-id="dd107-131">預設值為 [私人]。</span><span class="sxs-lookup"><span data-stu-id="dd107-131">Default value is Private.</span></span>
<span data-ttu-id="dd107-132">未來版本中將會棄用此參數</span><span class="sxs-lookup"><span data-stu-id="dd107-132">This parameter will be deprecated in a future release</span></span>

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

### <span data-ttu-id="dd107-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="dd107-133">-SubscriptionCount</span></span>
<span data-ttu-id="dd107-134">目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="dd107-134">Current subscription count.</span></span>

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

### <span data-ttu-id="dd107-135">-確認</span><span class="sxs-lookup"><span data-stu-id="dd107-135">-Confirm</span></span>
<span data-ttu-id="dd107-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd107-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd107-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd107-137">-WhatIf</span></span>
<span data-ttu-id="dd107-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd107-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd107-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd107-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd107-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd107-140">CommonParameters</span></span>
<span data-ttu-id="dd107-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd107-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd107-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd107-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd107-143">輸入</span><span class="sxs-lookup"><span data-stu-id="dd107-143">INPUTS</span></span>

## <span data-ttu-id="dd107-144">輸出</span><span class="sxs-lookup"><span data-stu-id="dd107-144">OUTPUTS</span></span>

### <span data-ttu-id="dd107-145">AzureStack 的訂閱. 管理模型。</span><span class="sxs-lookup"><span data-stu-id="dd107-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="dd107-146">筆記</span><span class="sxs-lookup"><span data-stu-id="dd107-146">NOTES</span></span>

## <span data-ttu-id="dd107-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd107-147">RELATED LINKS</span></span>

