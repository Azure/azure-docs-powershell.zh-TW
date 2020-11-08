---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128644"
---
# <span data-ttu-id="c9eeb-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="c9eeb-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="c9eeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eeb-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="c9eeb-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="c9eeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9eeb-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9eeb-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eeb-106">計算放置預留訂單的價格。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="c9eeb-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eeb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c9eeb-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="c9eeb-109">取得目錄之後，客戶可以根據位置取得 differe 產品。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="c9eeb-110">使用這些資訊，可以正確檢查價格</span><span class="sxs-lookup"><span data-stu-id="c9eeb-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="c9eeb-111">參數</span><span class="sxs-lookup"><span data-stu-id="c9eeb-111">PARAMETERS</span></span>

### <span data-ttu-id="c9eeb-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="c9eeb-112">-AppliedScope</span></span>
<span data-ttu-id="c9eeb-113">將套用福利的訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="c9eeb-114">如果已套用-作用欄位型別為 Single，則為必要。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="c9eeb-115">請勿指定是否已共用套用範圍類型。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="c9eeb-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="c9eeb-116">-AppliedScopeType</span></span>
<span data-ttu-id="c9eeb-117">已套用範圍的類型，以使用 "單一" 或 "Shared" 更新保留</span><span class="sxs-lookup"><span data-stu-id="c9eeb-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="c9eeb-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="c9eeb-118">-BillingPlan</span></span>
<span data-ttu-id="c9eeb-119">此 SKU 可用的帳單方案選項。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="c9eeb-120">"每月" 或 "前期"</span><span class="sxs-lookup"><span data-stu-id="c9eeb-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="c9eeb-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="c9eeb-121">-BillingScopeId</span></span>
<span data-ttu-id="c9eeb-122">將針對採購預留付費的訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="c9eeb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eeb-123">-DefaultProfile</span></span>
<span data-ttu-id="c9eeb-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9eeb-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c9eeb-125">-DisplayName</span></span>
<span data-ttu-id="c9eeb-126">使用者的易記名稱，便於識別保留。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="c9eeb-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="c9eeb-127">-InstanceFlexibility</span></span>
<span data-ttu-id="c9eeb-128">用來更新保留的實例彈性類型。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="c9eeb-129">-位置</span><span class="sxs-lookup"><span data-stu-id="c9eeb-129">-Location</span></span>
<span data-ttu-id="c9eeb-130">提供 SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="c9eeb-131">數量</span><span class="sxs-lookup"><span data-stu-id="c9eeb-131">-Quantity</span></span>
<span data-ttu-id="c9eeb-132">計算價格或購買時所用的產品數量。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="c9eeb-133">-續約</span><span class="sxs-lookup"><span data-stu-id="c9eeb-133">-Renew</span></span>
<span data-ttu-id="c9eeb-134">將此設定為 true 會在到期日期時間自動購買新的保留。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="c9eeb-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="c9eeb-135">-ReservedResourceType</span></span>
<span data-ttu-id="c9eeb-136">應提供 sku 之資源的類型。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="c9eeb-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="c9eeb-137">-Sku</span></span>
<span data-ttu-id="c9eeb-138">Sku 名稱，請使用命令 az 保留目錄顯示來取得 sku 清單</span><span class="sxs-lookup"><span data-stu-id="c9eeb-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="c9eeb-139">-期限</span><span class="sxs-lookup"><span data-stu-id="c9eeb-139">-Term</span></span>
<span data-ttu-id="c9eeb-140">此資源的可用保留期限。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="c9eeb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eeb-141">CommonParameters</span></span>
<span data-ttu-id="c9eeb-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eeb-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9eeb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eeb-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c9eeb-144">INPUTS</span></span>

### <span data-ttu-id="c9eeb-145">所有</span><span class="sxs-lookup"><span data-stu-id="c9eeb-145">None</span></span>

## <span data-ttu-id="c9eeb-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c9eeb-146">OUTPUTS</span></span>

### <span data-ttu-id="c9eeb-147">CalculatePriceResponse 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="c9eeb-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="c9eeb-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c9eeb-148">NOTES</span></span>

## <span data-ttu-id="c9eeb-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9eeb-149">RELATED LINKS</span></span>