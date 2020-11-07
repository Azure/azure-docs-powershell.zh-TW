---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968110"
---
# <span data-ttu-id="74d2d-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="74d2d-101">Set-AzsOffer</span></span>

## <span data-ttu-id="74d2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="74d2d-103">建立或更新優惠。</span><span class="sxs-lookup"><span data-stu-id="74d2d-103">Create or update the offer.</span></span>

## <span data-ttu-id="74d2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="74d2d-104">SYNTAX</span></span>

### <span data-ttu-id="74d2d-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="74d2d-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74d2d-106">時更新</span><span class="sxs-lookup"><span data-stu-id="74d2d-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74d2d-107">說明</span><span class="sxs-lookup"><span data-stu-id="74d2d-107">DESCRIPTION</span></span>
<span data-ttu-id="74d2d-108">建立或更新優惠。</span><span class="sxs-lookup"><span data-stu-id="74d2d-108">Create or update the offer.</span></span>

## <span data-ttu-id="74d2d-109">示例</span><span class="sxs-lookup"><span data-stu-id="74d2d-109">EXAMPLES</span></span>

### <span data-ttu-id="74d2d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="74d2d-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="74d2d-111">更新促銷活動。</span><span class="sxs-lookup"><span data-stu-id="74d2d-111">Update an offer.</span></span>

## <span data-ttu-id="74d2d-112">參數</span><span class="sxs-lookup"><span data-stu-id="74d2d-112">PARAMETERS</span></span>

### <span data-ttu-id="74d2d-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="74d2d-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="74d2d-114">提供給附加元件方案的參考，租使用者也可以選擇作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="74d2d-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="74d2d-115">若要建立，請參閱 ADDONPLANDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="74d2d-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="74d2d-116">-BasePlanIds</span></span>
<span data-ttu-id="74d2d-117">當租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d2d-118">-DefaultProfile</span></span>
<span data-ttu-id="74d2d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74d2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-120">-描述</span><span class="sxs-lookup"><span data-stu-id="74d2d-120">-Description</span></span>
<span data-ttu-id="74d2d-121">優惠說明。</span><span class="sxs-lookup"><span data-stu-id="74d2d-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="74d2d-122">-DisplayName</span></span>
<span data-ttu-id="74d2d-123">[優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="74d2d-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="74d2d-124">-ExternalReferenceId</span></span>
<span data-ttu-id="74d2d-125">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-126">-位置</span><span class="sxs-lookup"><span data-stu-id="74d2d-126">-Location</span></span>
<span data-ttu-id="74d2d-127">資源的位置</span><span class="sxs-lookup"><span data-stu-id="74d2d-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="74d2d-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="74d2d-129">每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="74d2d-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="74d2d-130">-Name</span></span>
<span data-ttu-id="74d2d-131">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d2d-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="74d2d-132">-OfferDefinition</span></span>
<span data-ttu-id="74d2d-133">代表可建立訂閱的服務產品。</span><span class="sxs-lookup"><span data-stu-id="74d2d-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="74d2d-134">若要建立，請參閱 OFFERDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="74d2d-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="74d2d-135">-PropertiesName</span></span>
<span data-ttu-id="74d2d-136">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d2d-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d2d-137">-ResourceGroupName</span></span>
<span data-ttu-id="74d2d-138">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="74d2d-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-139">-State</span><span class="sxs-lookup"><span data-stu-id="74d2d-139">-State</span></span>
<span data-ttu-id="74d2d-140">提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="74d2d-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="74d2d-141">-SubscriptionCount</span></span>
<span data-ttu-id="74d2d-142">目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="74d2d-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74d2d-143">-SubscriptionId</span></span>
<span data-ttu-id="74d2d-144">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="74d2d-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74d2d-145">-確認</span><span class="sxs-lookup"><span data-stu-id="74d2d-145">-Confirm</span></span>
<span data-ttu-id="74d2d-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74d2d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d2d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d2d-147">-WhatIf</span></span>
<span data-ttu-id="74d2d-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74d2d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d2d-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74d2d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d2d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d2d-150">CommonParameters</span></span>
<span data-ttu-id="74d2d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74d2d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d2d-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74d2d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d2d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="74d2d-153">INPUTS</span></span>

### <span data-ttu-id="74d2d-154">IOffer （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="74d2d-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="74d2d-155">輸出</span><span class="sxs-lookup"><span data-stu-id="74d2d-155">OUTPUTS</span></span>

### <span data-ttu-id="74d2d-156">IOffer （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="74d2d-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="74d2d-157">別名</span><span class="sxs-lookup"><span data-stu-id="74d2d-157">ALIASES</span></span>

## <span data-ttu-id="74d2d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="74d2d-158">NOTES</span></span>

<span data-ttu-id="74d2d-159">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="74d2d-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74d2d-160">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="74d2d-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="74d2d-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >：針對附加元件方案的參考，租使用者可以選擇將它作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="74d2d-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="74d2d-162">`[MaxAcquisitionCount <Int32?>]`：單一訂閱可以取得的實例數目上限。</span><span class="sxs-lookup"><span data-stu-id="74d2d-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="74d2d-163">如果未指定，則假設值為1。</span><span class="sxs-lookup"><span data-stu-id="74d2d-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="74d2d-164">`[PlanId <String>]`：規劃識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="74d2d-165">OFFERDEFINITION <IOffer> ：代表可建立訂閱的服務選項。</span><span class="sxs-lookup"><span data-stu-id="74d2d-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="74d2d-166">`[Location <String>]`：資源的位置</span><span class="sxs-lookup"><span data-stu-id="74d2d-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="74d2d-167">`[AddonPlans <IAddonPlanDefinition[]>]`：對附加元件方案的參照，租使用者也可以選擇取得該優惠的一部分。</span><span class="sxs-lookup"><span data-stu-id="74d2d-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="74d2d-168">`[MaxAcquisitionCount <Int32?>]`：單一訂閱可以取得的實例數目上限。</span><span class="sxs-lookup"><span data-stu-id="74d2d-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="74d2d-169">如果未指定，則假設值為1。</span><span class="sxs-lookup"><span data-stu-id="74d2d-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="74d2d-170">`[PlanId <String>]`：規劃識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="74d2d-171">`[BasePlanIds <String[]>]`：租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="74d2d-172">`[Description <String>]`：優惠的描述。</span><span class="sxs-lookup"><span data-stu-id="74d2d-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="74d2d-173">`[DisplayName <String>]`： [優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="74d2d-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="74d2d-174">`[ExternalReferenceId <String>]`：外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="74d2d-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="74d2d-175">`[MaxSubscriptionsPerAccount <Int32?>]`：每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="74d2d-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="74d2d-176">`[PropertiesName <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d2d-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="74d2d-177">`[State <AccessibilityState?>]`：提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="74d2d-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="74d2d-178">`[SubscriptionCount <Int32?>]`：目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="74d2d-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="74d2d-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="74d2d-179">RELATED LINKS</span></span>

