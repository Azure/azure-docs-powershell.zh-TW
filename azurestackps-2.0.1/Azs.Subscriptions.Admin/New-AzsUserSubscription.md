---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966625"
---
# <span data-ttu-id="ead66-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ead66-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="ead66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ead66-102">SYNOPSIS</span></span>
<span data-ttu-id="ead66-103">建立或更新指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead66-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="ead66-104">句法</span><span class="sxs-lookup"><span data-stu-id="ead66-104">SYNTAX</span></span>

### <span data-ttu-id="ead66-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ead66-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ead66-106">建立</span><span class="sxs-lookup"><span data-stu-id="ead66-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ead66-107">說明</span><span class="sxs-lookup"><span data-stu-id="ead66-107">DESCRIPTION</span></span>
<span data-ttu-id="ead66-108">建立或更新指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead66-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="ead66-109">示例</span><span class="sxs-lookup"><span data-stu-id="ead66-109">EXAMPLES</span></span>

### <span data-ttu-id="ead66-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ead66-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="ead66-111">建立新的使用者訂閱</span><span class="sxs-lookup"><span data-stu-id="ead66-111">Creates a new user subscription</span></span>

## <span data-ttu-id="ead66-112">參數</span><span class="sxs-lookup"><span data-stu-id="ead66-112">PARAMETERS</span></span>

### <span data-ttu-id="ead66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead66-113">-DefaultProfile</span></span>
<span data-ttu-id="ead66-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead66-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ead66-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="ead66-116">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ead66-117">-DisplayName</span></span>
<span data-ttu-id="ead66-118">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="ead66-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="ead66-119">-ExternalReferenceId</span></span>
<span data-ttu-id="ead66-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-121">-Id</span></span>
<span data-ttu-id="ead66-122">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="ead66-123">-OfferId</span></span>
<span data-ttu-id="ead66-124">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-125">-擁有者</span><span class="sxs-lookup"><span data-stu-id="ead66-125">-Owner</span></span>
<span data-ttu-id="ead66-126">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="ead66-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="ead66-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="ead66-128">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="ead66-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-129">-State</span><span class="sxs-lookup"><span data-stu-id="ead66-129">-State</span></span>
<span data-ttu-id="ead66-130">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="ead66-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="ead66-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="ead66-132">訂閱物件屬性。</span><span class="sxs-lookup"><span data-stu-id="ead66-132">Subscription object properties.</span></span>
<span data-ttu-id="ead66-133">若要建立，請參閱 SUBSCRIPTIONDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="ead66-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ead66-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="ead66-135">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ead66-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ead66-136">-TenantId</span></span>
<span data-ttu-id="ead66-137">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ead66-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ead66-138">-Confirm</span></span>
<span data-ttu-id="ead66-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ead66-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead66-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead66-140">-WhatIf</span></span>
<span data-ttu-id="ead66-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ead66-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead66-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ead66-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead66-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead66-143">CommonParameters</span></span>
<span data-ttu-id="ead66-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ead66-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead66-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ead66-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead66-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ead66-146">INPUTS</span></span>

### <span data-ttu-id="ead66-147">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="ead66-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="ead66-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ead66-148">OUTPUTS</span></span>

### <span data-ttu-id="ead66-149">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="ead66-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="ead66-150">別名</span><span class="sxs-lookup"><span data-stu-id="ead66-150">ALIASES</span></span>

## <span data-ttu-id="ead66-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ead66-151">NOTES</span></span>

<span data-ttu-id="ead66-152">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ead66-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ead66-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ead66-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ead66-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> ：訂閱物件屬性。</span><span class="sxs-lookup"><span data-stu-id="ead66-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="ead66-155">`[DelegatedProviderSubscriptionId <String>]`：父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="ead66-156">`[DisplayName <String>]`：訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="ead66-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="ead66-157">`[ExternalReferenceId <String>]`：外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="ead66-158">`[Id <String>]`：完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="ead66-159">`[OfferId <String>]`：受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="ead66-160">`[Owner <String>]`：訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="ead66-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="ead66-161">`[RoutingResourceManagerType <ResourceManagerType?>]`：路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="ead66-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="ead66-162">`[State <SubscriptionState?>]`：訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="ead66-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="ead66-163">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="ead66-164">`[TenantId <String>]`：目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead66-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="ead66-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="ead66-165">RELATED LINKS</span></span>

