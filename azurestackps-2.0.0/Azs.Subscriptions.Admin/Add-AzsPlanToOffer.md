---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966591"
---
# <span data-ttu-id="64689-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="64689-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="64689-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64689-102">SYNOPSIS</span></span>
<span data-ttu-id="64689-103">將計畫連結至優惠。</span><span class="sxs-lookup"><span data-stu-id="64689-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="64689-104">句法</span><span class="sxs-lookup"><span data-stu-id="64689-104">SYNTAX</span></span>

### <span data-ttu-id="64689-105">LinkExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="64689-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64689-106">鏈路</span><span class="sxs-lookup"><span data-stu-id="64689-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64689-107">LinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64689-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64689-108">LinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64689-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="64689-109">說明</span><span class="sxs-lookup"><span data-stu-id="64689-109">DESCRIPTION</span></span>
<span data-ttu-id="64689-110">將計畫連結至優惠。</span><span class="sxs-lookup"><span data-stu-id="64689-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="64689-111">示例</span><span class="sxs-lookup"><span data-stu-id="64689-111">EXAMPLES</span></span>

### <span data-ttu-id="64689-112">範例1</span><span class="sxs-lookup"><span data-stu-id="64689-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="64689-113">將計畫連結至優惠。</span><span class="sxs-lookup"><span data-stu-id="64689-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="64689-114">參數</span><span class="sxs-lookup"><span data-stu-id="64689-114">PARAMETERS</span></span>

### <span data-ttu-id="64689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64689-115">-DefaultProfile</span></span>
<span data-ttu-id="64689-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64689-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64689-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64689-117">-InputObject</span></span>
<span data-ttu-id="64689-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="64689-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="64689-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="64689-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="64689-120">由訂閱者所取得的最大購置計數</span><span class="sxs-lookup"><span data-stu-id="64689-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="64689-121">-OfferName</span></span>
<span data-ttu-id="64689-122">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="64689-123">-PlanLink</span></span>
<span data-ttu-id="64689-124">將方案連結和取消連結至提供的定義。</span><span class="sxs-lookup"><span data-stu-id="64689-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="64689-125">若要建立，請參閱 PLANLINK 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="64689-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="64689-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="64689-126">-PlanLinkType</span></span>
<span data-ttu-id="64689-127">[方案] 連結的類型。</span><span class="sxs-lookup"><span data-stu-id="64689-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="64689-128">-PlanName</span></span>
<span data-ttu-id="64689-129">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64689-130">-ResourceGroupName</span></span>
<span data-ttu-id="64689-131">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="64689-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64689-132">-SubscriptionId</span></span>
<span data-ttu-id="64689-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="64689-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64689-134">-確認</span><span class="sxs-lookup"><span data-stu-id="64689-134">-Confirm</span></span>
<span data-ttu-id="64689-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64689-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64689-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64689-136">-WhatIf</span></span>
<span data-ttu-id="64689-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64689-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64689-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64689-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64689-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64689-139">CommonParameters</span></span>
<span data-ttu-id="64689-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64689-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64689-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64689-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64689-142">輸入</span><span class="sxs-lookup"><span data-stu-id="64689-142">INPUTS</span></span>

### <span data-ttu-id="64689-143">IPlanLinkDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="64689-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="64689-144">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="64689-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="64689-145">輸出</span><span class="sxs-lookup"><span data-stu-id="64689-145">OUTPUTS</span></span>

### <span data-ttu-id="64689-146">IOffer （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="64689-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="64689-147">別名</span><span class="sxs-lookup"><span data-stu-id="64689-147">ALIASES</span></span>

## <span data-ttu-id="64689-148">筆記</span><span class="sxs-lookup"><span data-stu-id="64689-148">NOTES</span></span>

<span data-ttu-id="64689-149">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="64689-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64689-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="64689-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="64689-151">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="64689-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64689-152">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="64689-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="64689-153">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="64689-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="64689-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="64689-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64689-155">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="64689-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="64689-156">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="64689-157">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="64689-158">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="64689-159">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="64689-160">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="64689-161">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="64689-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="64689-162">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="64689-163">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="64689-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="64689-164">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="64689-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="64689-165">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="64689-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="64689-166">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="64689-167">PLANLINK <IPlanLinkDefinition> ：將方案連結和取消連結至提供的定義。</span><span class="sxs-lookup"><span data-stu-id="64689-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="64689-168">`[MaxAcquisitionCount <Int32?>]`：由訂閱者所取得的最大購置計數</span><span class="sxs-lookup"><span data-stu-id="64689-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="64689-169">`[PlanLinkType <PlanLinkType?>]`：方案連結的類型。</span><span class="sxs-lookup"><span data-stu-id="64689-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="64689-170">`[PlanName <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="64689-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="64689-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="64689-171">RELATED LINKS</span></span>

