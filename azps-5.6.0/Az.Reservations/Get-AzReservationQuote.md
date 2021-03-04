---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 3a06de95cedd0ea38fa38b2fb8784e553ae6f4d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914518"
---
# <span data-ttu-id="d61f3-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="d61f3-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="d61f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d61f3-102">SYNOPSIS</span></span>
<span data-ttu-id="d61f3-103">取得預約的報價。</span><span class="sxs-lookup"><span data-stu-id="d61f3-103">Get a quote for the reservation.</span></span> <span data-ttu-id="d61f3-104">這會傳遞至 `New-AzReservation` 購買。</span><span class="sxs-lookup"><span data-stu-id="d61f3-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="d61f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="d61f3-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d61f3-106">描述</span><span class="sxs-lookup"><span data-stu-id="d61f3-106">DESCRIPTION</span></span>
<span data-ttu-id="d61f3-107">計算下預約訂單的價格。</span><span class="sxs-lookup"><span data-stu-id="d61f3-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="d61f3-108">例子</span><span class="sxs-lookup"><span data-stu-id="d61f3-108">EXAMPLES</span></span>

### <span data-ttu-id="d61f3-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="d61f3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="d61f3-110">取得目錄之後，客戶就可以根據位置取得不同的產品。</span><span class="sxs-lookup"><span data-stu-id="d61f3-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="d61f3-111">使用這些資訊，正確檢查價格</span><span class="sxs-lookup"><span data-stu-id="d61f3-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="d61f3-112">參數</span><span class="sxs-lookup"><span data-stu-id="d61f3-112">PARAMETERS</span></span>

### <span data-ttu-id="d61f3-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d61f3-113">-AppliedScope</span></span>
<span data-ttu-id="d61f3-114">將適用權益的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d61f3-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="d61f3-115">如果 --applied-scope-type 為 Single，則為必填項。</span><span class="sxs-lookup"><span data-stu-id="d61f3-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="d61f3-116">請勿指定 --applied-scope 類型是否為共用。</span><span class="sxs-lookup"><span data-stu-id="d61f3-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="d61f3-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d61f3-117">-AppliedScopeType</span></span>
<span data-ttu-id="d61f3-118">以「單一」或「共用」更新預約的已使用範圍類型</span><span class="sxs-lookup"><span data-stu-id="d61f3-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="d61f3-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="d61f3-119">-BillingPlan</span></span>
<span data-ttu-id="d61f3-120">此 SKU 可用的帳單方案選項。</span><span class="sxs-lookup"><span data-stu-id="d61f3-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="d61f3-121">「每月」或「預付」</span><span class="sxs-lookup"><span data-stu-id="d61f3-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="d61f3-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="d61f3-122">-BillingScopeId</span></span>
<span data-ttu-id="d61f3-123">將收取購買預約費用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d61f3-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="d61f3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61f3-124">-DefaultProfile</span></span>
<span data-ttu-id="d61f3-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d61f3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d61f3-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d61f3-126">-DisplayName</span></span>
<span data-ttu-id="d61f3-127">好用的名稱，讓使用者輕鬆識別預約。</span><span class="sxs-lookup"><span data-stu-id="d61f3-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="d61f3-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="d61f3-128">-InstanceFlexibility</span></span>
<span data-ttu-id="d61f3-129">更新預約的實例彈性類型。</span><span class="sxs-lookup"><span data-stu-id="d61f3-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="d61f3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="d61f3-130">-Location</span></span>
<span data-ttu-id="d61f3-131">SKU 可用的位置。</span><span class="sxs-lookup"><span data-stu-id="d61f3-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="d61f3-132">-數量</span><span class="sxs-lookup"><span data-stu-id="d61f3-132">-Quantity</span></span>
<span data-ttu-id="d61f3-133">用於計算價格或購買的產品數量。</span><span class="sxs-lookup"><span data-stu-id="d61f3-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="d61f3-134">-續約</span><span class="sxs-lookup"><span data-stu-id="d61f3-134">-Renew</span></span>
<span data-ttu-id="d61f3-135">設定為 True 時，系統會自動在到期日購買新的預約。</span><span class="sxs-lookup"><span data-stu-id="d61f3-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="d61f3-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="d61f3-136">-ReservedResourceType</span></span>
<span data-ttu-id="d61f3-137">應提供 SKU 的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d61f3-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="d61f3-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d61f3-138">-Sku</span></span>
<span data-ttu-id="d61f3-139">SKU 名稱，使用命令 az 預約目錄顯示來取得 SKU 清單</span><span class="sxs-lookup"><span data-stu-id="d61f3-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="d61f3-140">-Term</span><span class="sxs-lookup"><span data-stu-id="d61f3-140">-Term</span></span>
<span data-ttu-id="d61f3-141">此資源的可用預約條款。</span><span class="sxs-lookup"><span data-stu-id="d61f3-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="d61f3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61f3-142">CommonParameters</span></span>
<span data-ttu-id="d61f3-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d61f3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61f3-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d61f3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61f3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d61f3-145">INPUTS</span></span>

### <span data-ttu-id="d61f3-146">沒有</span><span class="sxs-lookup"><span data-stu-id="d61f3-146">None</span></span>

## <span data-ttu-id="d61f3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d61f3-147">OUTPUTS</span></span>

### <span data-ttu-id="d61f3-148">Microsoft.Azure.management.Reservations.models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="d61f3-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="d61f3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d61f3-149">NOTES</span></span>

## <span data-ttu-id="d61f3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d61f3-150">RELATED LINKS</span></span>
