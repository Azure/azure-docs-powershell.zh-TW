---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968590"
---
# <span data-ttu-id="12424-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="12424-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="12424-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12424-102">SYNOPSIS</span></span>
<span data-ttu-id="12424-103">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="12424-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="12424-104">句法</span><span class="sxs-lookup"><span data-stu-id="12424-104">SYNTAX</span></span>

### <span data-ttu-id="12424-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="12424-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12424-106">確認</span><span class="sxs-lookup"><span data-stu-id="12424-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12424-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12424-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12424-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="12424-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12424-109">說明</span><span class="sxs-lookup"><span data-stu-id="12424-109">DESCRIPTION</span></span>
<span data-ttu-id="12424-110">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="12424-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="12424-111">示例</span><span class="sxs-lookup"><span data-stu-id="12424-111">EXAMPLES</span></span>

### <span data-ttu-id="12424-112">範例1</span><span class="sxs-lookup"><span data-stu-id="12424-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="12424-113">傳回指定訂閱資源類型和名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="12424-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="12424-114">參數</span><span class="sxs-lookup"><span data-stu-id="12424-114">PARAMETERS</span></span>

### <span data-ttu-id="12424-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12424-115">-DefaultProfile</span></span>
<span data-ttu-id="12424-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12424-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12424-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12424-117">-InputObject</span></span>
<span data-ttu-id="12424-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="12424-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="12424-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="12424-119">-Name</span></span>
<span data-ttu-id="12424-120">要驗證的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12424-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="12424-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="12424-122">檢查名稱可用性動作定義。</span><span class="sxs-lookup"><span data-stu-id="12424-122">The check name availability action definition.</span></span>
<span data-ttu-id="12424-123">若要建立，請參閱 NAMEAVAILABILITYDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="12424-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="12424-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="12424-124">-ResourceType</span></span>
<span data-ttu-id="12424-125">要驗證的資源類型。</span><span class="sxs-lookup"><span data-stu-id="12424-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12424-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12424-126">-SubscriptionId</span></span>
<span data-ttu-id="12424-127">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12424-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12424-128">-確認</span><span class="sxs-lookup"><span data-stu-id="12424-128">-Confirm</span></span>
<span data-ttu-id="12424-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12424-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12424-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12424-130">-WhatIf</span></span>
<span data-ttu-id="12424-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12424-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12424-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12424-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12424-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12424-133">CommonParameters</span></span>
<span data-ttu-id="12424-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12424-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12424-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12424-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12424-136">輸入</span><span class="sxs-lookup"><span data-stu-id="12424-136">INPUTS</span></span>

### <span data-ttu-id="12424-137">ICheckNameAvailabilityDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="12424-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="12424-138">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="12424-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="12424-139">輸出</span><span class="sxs-lookup"><span data-stu-id="12424-139">OUTPUTS</span></span>

### <span data-ttu-id="12424-140">ICheckNameAvailabilityResponse （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="12424-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="12424-141">別名</span><span class="sxs-lookup"><span data-stu-id="12424-141">ALIASES</span></span>

## <span data-ttu-id="12424-142">筆記</span><span class="sxs-lookup"><span data-stu-id="12424-142">NOTES</span></span>

<span data-ttu-id="12424-143">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="12424-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12424-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="12424-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="12424-145">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="12424-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12424-146">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="12424-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="12424-147">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="12424-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="12424-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="12424-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12424-149">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="12424-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="12424-150">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="12424-151">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="12424-152">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="12424-153">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="12424-154">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="12424-155">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="12424-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="12424-156">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="12424-157">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="12424-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="12424-158">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12424-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="12424-159">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="12424-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="12424-160">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="12424-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> ：檢查名稱可用性動作定義。</span><span class="sxs-lookup"><span data-stu-id="12424-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="12424-162">`[Name <String>]`：要驗證的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="12424-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="12424-163">`[ResourceType <String>]`：要驗證的資源類型。</span><span class="sxs-lookup"><span data-stu-id="12424-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="12424-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="12424-164">RELATED LINKS</span></span>

