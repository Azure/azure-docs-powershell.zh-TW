---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793209"
---
# <span data-ttu-id="f1007-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f1007-101">Set-AzsOffer</span></span>

## <span data-ttu-id="f1007-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1007-102">SYNOPSIS</span></span>
<span data-ttu-id="f1007-103">更新優惠。</span><span class="sxs-lookup"><span data-stu-id="f1007-103">Update the offer.</span></span>

## <span data-ttu-id="f1007-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1007-104">SYNTAX</span></span>

### <span data-ttu-id="f1007-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="f1007-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1007-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1007-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1007-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1007-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1007-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1007-108">DESCRIPTION</span></span>
<span data-ttu-id="f1007-109">更新優惠。</span><span class="sxs-lookup"><span data-stu-id="f1007-109">Update the offer.</span></span>

## <span data-ttu-id="f1007-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1007-110">EXAMPLES</span></span>

### <span data-ttu-id="f1007-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1007-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="f1007-112">更新優惠。</span><span class="sxs-lookup"><span data-stu-id="f1007-112">Update the offer.</span></span>

## <span data-ttu-id="f1007-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1007-113">PARAMETERS</span></span>

### <span data-ttu-id="f1007-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f1007-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="f1007-115">提供給附加元件方案的參考，租使用者也可以選擇作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="f1007-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f1007-116">-BasePlanIds</span></span>
<span data-ttu-id="f1007-117">當租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1007-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-118">-描述</span><span class="sxs-lookup"><span data-stu-id="f1007-118">-Description</span></span>
<span data-ttu-id="f1007-119">優惠說明。</span><span class="sxs-lookup"><span data-stu-id="f1007-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1007-120">-DisplayName</span></span>
<span data-ttu-id="f1007-121">[優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="f1007-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f1007-122">-ExternalReferenceId</span></span>
<span data-ttu-id="f1007-123">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1007-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1007-124">-InputObject</span></span>
<span data-ttu-id="f1007-125">AzureStack 類型的輸入物件，其為 [系統管理]。</span><span class="sxs-lookup"><span data-stu-id="f1007-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-126">-位置</span><span class="sxs-lookup"><span data-stu-id="f1007-126">-Location</span></span>
<span data-ttu-id="f1007-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="f1007-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f1007-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f1007-129">每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="f1007-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1007-130">-Name</span></span>
<span data-ttu-id="f1007-131">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1007-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1007-132">-ResourceGroupName</span></span>
<span data-ttu-id="f1007-133">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f1007-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1007-134">-ResourceId</span></span>
<span data-ttu-id="f1007-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f1007-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-136">-State</span><span class="sxs-lookup"><span data-stu-id="f1007-136">-State</span></span>
<span data-ttu-id="f1007-137">提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="f1007-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f1007-138">-SubscriptionCount</span></span>
<span data-ttu-id="f1007-139">目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="f1007-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1007-140">-確認</span><span class="sxs-lookup"><span data-stu-id="f1007-140">-Confirm</span></span>
<span data-ttu-id="f1007-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1007-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1007-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1007-142">-WhatIf</span></span>
<span data-ttu-id="f1007-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1007-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1007-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1007-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1007-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1007-145">CommonParameters</span></span>
<span data-ttu-id="f1007-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1007-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1007-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1007-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1007-148">輸入</span><span class="sxs-lookup"><span data-stu-id="f1007-148">INPUTS</span></span>

## <span data-ttu-id="f1007-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f1007-149">OUTPUTS</span></span>

### <span data-ttu-id="f1007-150">AzureStack 的訂閱. 管理模型。</span><span class="sxs-lookup"><span data-stu-id="f1007-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="f1007-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f1007-151">NOTES</span></span>

## <span data-ttu-id="f1007-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1007-152">RELATED LINKS</span></span>

