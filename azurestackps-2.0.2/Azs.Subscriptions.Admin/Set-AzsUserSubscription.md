---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968603"
---
# <span data-ttu-id="bbdfd-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="bbdfd-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="bbdfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdfd-103">建立或更新指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="bbdfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbdfd-104">SYNTAX</span></span>

### <span data-ttu-id="bbdfd-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="bbdfd-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbdfd-106">時更新</span><span class="sxs-lookup"><span data-stu-id="bbdfd-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbdfd-107">說明</span><span class="sxs-lookup"><span data-stu-id="bbdfd-107">DESCRIPTION</span></span>
<span data-ttu-id="bbdfd-108">建立或更新指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="bbdfd-109">示例</span><span class="sxs-lookup"><span data-stu-id="bbdfd-109">EXAMPLES</span></span>

### <span data-ttu-id="bbdfd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bbdfd-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="bbdfd-111">更新訂閱</span><span class="sxs-lookup"><span data-stu-id="bbdfd-111">Updates a subscription</span></span>

## <span data-ttu-id="bbdfd-112">參數</span><span class="sxs-lookup"><span data-stu-id="bbdfd-112">PARAMETERS</span></span>

### <span data-ttu-id="bbdfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdfd-113">-DefaultProfile</span></span>
<span data-ttu-id="bbdfd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbdfd-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="bbdfd-116">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="bbdfd-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bbdfd-117">-DisplayName</span></span>
<span data-ttu-id="bbdfd-118">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-118">Subscription name.</span></span>

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

### <span data-ttu-id="bbdfd-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-119">-ExternalReferenceId</span></span>
<span data-ttu-id="bbdfd-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-120">External reference identifier.</span></span>

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

### <span data-ttu-id="bbdfd-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="bbdfd-121">-Id</span></span>
<span data-ttu-id="bbdfd-122">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="bbdfd-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-123">-OfferId</span></span>
<span data-ttu-id="bbdfd-124">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="bbdfd-125">-擁有者</span><span class="sxs-lookup"><span data-stu-id="bbdfd-125">-Owner</span></span>
<span data-ttu-id="bbdfd-126">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-126">Subscription owner.</span></span>

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

### <span data-ttu-id="bbdfd-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="bbdfd-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="bbdfd-128">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bbdfd-129">-State</span><span class="sxs-lookup"><span data-stu-id="bbdfd-129">-State</span></span>
<span data-ttu-id="bbdfd-130">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bbdfd-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="bbdfd-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="bbdfd-132">訂閱物件屬性。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-132">Subscription object properties.</span></span>
<span data-ttu-id="bbdfd-133">若要建立，請參閱 SUBSCRIPTIONDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bbdfd-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-134">-SubscriptionId</span></span>
<span data-ttu-id="bbdfd-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bbdfd-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="bbdfd-136">-SubscriptionId1</span></span>
<span data-ttu-id="bbdfd-137">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="bbdfd-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="bbdfd-139">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="bbdfd-140">-TenantId</span><span class="sxs-lookup"><span data-stu-id="bbdfd-140">-TenantId</span></span>
<span data-ttu-id="bbdfd-141">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="bbdfd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="bbdfd-142">-Confirm</span></span>
<span data-ttu-id="bbdfd-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdfd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdfd-144">-WhatIf</span></span>
<span data-ttu-id="bbdfd-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdfd-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdfd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdfd-147">CommonParameters</span></span>
<span data-ttu-id="bbdfd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdfd-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdfd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="bbdfd-150">INPUTS</span></span>

### <span data-ttu-id="bbdfd-151">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="bbdfd-152">輸出</span><span class="sxs-lookup"><span data-stu-id="bbdfd-152">OUTPUTS</span></span>

### <span data-ttu-id="bbdfd-153">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="bbdfd-154">別名</span><span class="sxs-lookup"><span data-stu-id="bbdfd-154">ALIASES</span></span>

## <span data-ttu-id="bbdfd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="bbdfd-155">NOTES</span></span>

<span data-ttu-id="bbdfd-156">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbdfd-157">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bbdfd-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> ：訂閱物件屬性。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="bbdfd-159">`[DelegatedProviderSubscriptionId <String>]`：父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="bbdfd-160">`[DisplayName <String>]`：訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="bbdfd-161">`[ExternalReferenceId <String>]`：外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="bbdfd-162">`[Id <String>]`：完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="bbdfd-163">`[OfferId <String>]`：受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="bbdfd-164">`[Owner <String>]`：訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="bbdfd-165">`[RoutingResourceManagerType <ResourceManagerType?>]`：路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="bbdfd-166">`[State <SubscriptionState?>]`：訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="bbdfd-167">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="bbdfd-168">`[TenantId <String>]`：目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbdfd-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="bbdfd-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbdfd-169">RELATED LINKS</span></span>

