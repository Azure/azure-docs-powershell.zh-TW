---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958701"
---
# <span data-ttu-id="89717-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="89717-101">New-AzReservation</span></span>

## <span data-ttu-id="89717-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89717-102">SYNOPSIS</span></span>
<span data-ttu-id="89717-103">購買保留</span><span class="sxs-lookup"><span data-stu-id="89717-103">Purchase a reservation</span></span>

## <span data-ttu-id="89717-104">句法</span><span class="sxs-lookup"><span data-stu-id="89717-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89717-105">說明</span><span class="sxs-lookup"><span data-stu-id="89717-105">DESCRIPTION</span></span>
<span data-ttu-id="89717-106">購買保留實例並取得好處</span><span class="sxs-lookup"><span data-stu-id="89717-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="89717-107">示例</span><span class="sxs-lookup"><span data-stu-id="89717-107">EXAMPLES</span></span>

### <span data-ttu-id="89717-108">範例1</span><span class="sxs-lookup"><span data-stu-id="89717-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="89717-109">計算價格之後，客戶可以 purcahse RI 提供的 calculatePrice</span><span class="sxs-lookup"><span data-stu-id="89717-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="89717-110">參數</span><span class="sxs-lookup"><span data-stu-id="89717-110">PARAMETERS</span></span>

### <span data-ttu-id="89717-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="89717-111">-AppliedScope</span></span>
<span data-ttu-id="89717-112">將套用福利的訂閱。</span><span class="sxs-lookup"><span data-stu-id="89717-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="89717-113">如果已套用-作用欄位型別為 Single，則為必要。</span><span class="sxs-lookup"><span data-stu-id="89717-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="89717-114">請勿指定是否已共用套用範圍類型。</span><span class="sxs-lookup"><span data-stu-id="89717-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="89717-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="89717-115">-AppliedScopeType</span></span>
<span data-ttu-id="89717-116">已套用範圍的類型，以使用 "單一" 或 "Shared" 更新保留</span><span class="sxs-lookup"><span data-stu-id="89717-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="89717-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="89717-117">-BillingPlan</span></span>
<span data-ttu-id="89717-118">此 SKU 可用的帳單方案選項。</span><span class="sxs-lookup"><span data-stu-id="89717-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="89717-119">"每月" 或 "前期"</span><span class="sxs-lookup"><span data-stu-id="89717-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="89717-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="89717-120">-BillingScopeId</span></span>
<span data-ttu-id="89717-121">將針對採購預留付費的訂閱。</span><span class="sxs-lookup"><span data-stu-id="89717-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="89717-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89717-122">-DefaultProfile</span></span>
<span data-ttu-id="89717-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89717-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89717-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89717-124">-DisplayName</span></span>
<span data-ttu-id="89717-125">使用者的易記名稱，便於識別保留。</span><span class="sxs-lookup"><span data-stu-id="89717-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="89717-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="89717-126">-InstanceFlexibility</span></span>
<span data-ttu-id="89717-127">{{Fill InstanceFlexibility 說明}}</span><span class="sxs-lookup"><span data-stu-id="89717-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="89717-128">-位置</span><span class="sxs-lookup"><span data-stu-id="89717-128">-Location</span></span>
<span data-ttu-id="89717-129">提供 SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="89717-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="89717-130">數量</span><span class="sxs-lookup"><span data-stu-id="89717-130">-Quantity</span></span>
<span data-ttu-id="89717-131">計算價格或購買時所用的產品數量。</span><span class="sxs-lookup"><span data-stu-id="89717-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="89717-132">-續約</span><span class="sxs-lookup"><span data-stu-id="89717-132">-Renew</span></span>
<span data-ttu-id="89717-133">將此設定為 true 會在到期日期時間自動購買新的保留。</span><span class="sxs-lookup"><span data-stu-id="89717-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="89717-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="89717-134">-ReservationOrderId</span></span>
<span data-ttu-id="89717-135">要購買的預留單訂單識別碼，由 az 預留預留-訂單計算產生。</span><span class="sxs-lookup"><span data-stu-id="89717-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="89717-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="89717-136">-ReservedResourceType</span></span>
<span data-ttu-id="89717-137">應提供 sku 之資源的類型。</span><span class="sxs-lookup"><span data-stu-id="89717-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="89717-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="89717-138">-Sku</span></span>
<span data-ttu-id="89717-139">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="89717-139">Sku name</span></span>

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

### <span data-ttu-id="89717-140">-期限</span><span class="sxs-lookup"><span data-stu-id="89717-140">-Term</span></span>
<span data-ttu-id="89717-141">此資源的可用保留期限。</span><span class="sxs-lookup"><span data-stu-id="89717-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="89717-142">-確認</span><span class="sxs-lookup"><span data-stu-id="89717-142">-Confirm</span></span>
<span data-ttu-id="89717-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89717-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89717-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89717-144">-WhatIf</span></span>
<span data-ttu-id="89717-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89717-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89717-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89717-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89717-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89717-147">CommonParameters</span></span>
<span data-ttu-id="89717-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89717-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89717-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89717-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89717-150">輸入</span><span class="sxs-lookup"><span data-stu-id="89717-150">INPUTS</span></span>

### <span data-ttu-id="89717-151">所有</span><span class="sxs-lookup"><span data-stu-id="89717-151">None</span></span>

## <span data-ttu-id="89717-152">輸出</span><span class="sxs-lookup"><span data-stu-id="89717-152">OUTPUTS</span></span>

### <span data-ttu-id="89717-153">ReservationOrderResponse 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="89717-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="89717-154">筆記</span><span class="sxs-lookup"><span data-stu-id="89717-154">NOTES</span></span>

## <span data-ttu-id="89717-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="89717-155">RELATED LINKS</span></span>
