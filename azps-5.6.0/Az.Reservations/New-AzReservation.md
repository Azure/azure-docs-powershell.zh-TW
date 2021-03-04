---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914505"
---
# <span data-ttu-id="16920-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="16920-101">New-AzReservation</span></span>

## <span data-ttu-id="16920-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16920-102">SYNOPSIS</span></span>
<span data-ttu-id="16920-103">購買預約</span><span class="sxs-lookup"><span data-stu-id="16920-103">Purchase a reservation</span></span>

## <span data-ttu-id="16920-104">語法</span><span class="sxs-lookup"><span data-stu-id="16920-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16920-105">描述</span><span class="sxs-lookup"><span data-stu-id="16920-105">DESCRIPTION</span></span>
<span data-ttu-id="16920-106">購買預約實例並取得權益</span><span class="sxs-lookup"><span data-stu-id="16920-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="16920-107">例子</span><span class="sxs-lookup"><span data-stu-id="16920-107">EXAMPLES</span></span>

### <span data-ttu-id="16920-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="16920-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="16920-109">計算價格之後，客戶可以計算Price 提供的價格來購買 RI 提供的價格</span><span class="sxs-lookup"><span data-stu-id="16920-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="16920-110">參數</span><span class="sxs-lookup"><span data-stu-id="16920-110">PARAMETERS</span></span>

### <span data-ttu-id="16920-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="16920-111">-AppliedScope</span></span>
<span data-ttu-id="16920-112">將適用權益的訂閱。</span><span class="sxs-lookup"><span data-stu-id="16920-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="16920-113">如果 --applied-scope-type 為 Single，則為必填項。</span><span class="sxs-lookup"><span data-stu-id="16920-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="16920-114">請勿指定 --applied-scope 類型是否為共用。</span><span class="sxs-lookup"><span data-stu-id="16920-114">Do not specify if --applied-scope-type is Shared.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="16920-115">-AppliedScopeType</span></span>
<span data-ttu-id="16920-116">以「單一」或「共用」更新預約的已使用範圍類型</span><span class="sxs-lookup"><span data-stu-id="16920-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="16920-117">-BillingPlan</span></span>
<span data-ttu-id="16920-118">此 SKU 可用的帳單方案選項。</span><span class="sxs-lookup"><span data-stu-id="16920-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="16920-119">「每月」或「預付」</span><span class="sxs-lookup"><span data-stu-id="16920-119">"Monthly" or "Upfront"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="16920-120">-BillingScopeId</span></span>
<span data-ttu-id="16920-121">將收取購買預約費用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="16920-121">Subscription that will be charged for purchasing Reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16920-122">-DefaultProfile</span></span>
<span data-ttu-id="16920-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16920-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="16920-124">-DisplayName</span></span>
<span data-ttu-id="16920-125">好用的名稱，讓使用者輕鬆識別預約。</span><span class="sxs-lookup"><span data-stu-id="16920-125">Friendly name for user to easily identified the reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="16920-126">-InstanceFlexibility</span></span>
<span data-ttu-id="16920-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="16920-127">{{ Fill InstanceFlexibility Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-128">-位置</span><span class="sxs-lookup"><span data-stu-id="16920-128">-Location</span></span>
<span data-ttu-id="16920-129">SKU 可用的位置。</span><span class="sxs-lookup"><span data-stu-id="16920-129">Location that the SKU is available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-130">-數量</span><span class="sxs-lookup"><span data-stu-id="16920-130">-Quantity</span></span>
<span data-ttu-id="16920-131">用於計算價格或購買的產品數量。</span><span class="sxs-lookup"><span data-stu-id="16920-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-132">-續約</span><span class="sxs-lookup"><span data-stu-id="16920-132">-Renew</span></span>
<span data-ttu-id="16920-133">設定為 True 時，系統會自動在到期日購買新的預約。</span><span class="sxs-lookup"><span data-stu-id="16920-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="16920-134">-ReservationOrderId</span></span>
<span data-ttu-id="16920-135">購買預約訂單的識別碼，由 az 預約預約訂單計算產生。</span><span class="sxs-lookup"><span data-stu-id="16920-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="16920-136">-ReservedResourceType</span></span>
<span data-ttu-id="16920-137">應提供 SKU 的資源類型。</span><span class="sxs-lookup"><span data-stu-id="16920-137">Type of the resource for which the skus should be provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="16920-138">-Sku</span></span>
<span data-ttu-id="16920-139">SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="16920-139">Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-140">-Term</span><span class="sxs-lookup"><span data-stu-id="16920-140">-Term</span></span>
<span data-ttu-id="16920-141">此資源的可用預約條款。</span><span class="sxs-lookup"><span data-stu-id="16920-141">Available reservation terms for this resource.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-142">-確認</span><span class="sxs-lookup"><span data-stu-id="16920-142">-Confirm</span></span>
<span data-ttu-id="16920-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="16920-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16920-144">-WhatIf</span></span>
<span data-ttu-id="16920-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16920-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16920-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16920-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16920-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16920-147">CommonParameters</span></span>
<span data-ttu-id="16920-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16920-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16920-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16920-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16920-150">輸入</span><span class="sxs-lookup"><span data-stu-id="16920-150">INPUTS</span></span>

### <span data-ttu-id="16920-151">沒有</span><span class="sxs-lookup"><span data-stu-id="16920-151">None</span></span>

## <span data-ttu-id="16920-152">輸出</span><span class="sxs-lookup"><span data-stu-id="16920-152">OUTPUTS</span></span>

### <span data-ttu-id="16920-153">Microsoft.Azure.management.Reservations.models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="16920-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="16920-154">筆記</span><span class="sxs-lookup"><span data-stu-id="16920-154">NOTES</span></span>

## <span data-ttu-id="16920-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="16920-155">RELATED LINKS</span></span>
