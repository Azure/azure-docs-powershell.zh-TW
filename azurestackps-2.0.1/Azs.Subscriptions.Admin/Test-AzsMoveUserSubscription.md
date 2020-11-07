---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966726"
---
# <span data-ttu-id="19266-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="19266-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="19266-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19266-102">SYNOPSIS</span></span>
<span data-ttu-id="19266-103">確認使用者訂閱可以在委派的提供者提供的服務之間移動。</span><span class="sxs-lookup"><span data-stu-id="19266-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="19266-104">句法</span><span class="sxs-lookup"><span data-stu-id="19266-104">SYNTAX</span></span>

### <span data-ttu-id="19266-105">ValidateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="19266-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19266-106">核實</span><span class="sxs-lookup"><span data-stu-id="19266-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="19266-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19266-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19266-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="19266-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19266-109">說明</span><span class="sxs-lookup"><span data-stu-id="19266-109">DESCRIPTION</span></span>
<span data-ttu-id="19266-110">確認使用者訂閱可以在委派的提供者提供的服務之間移動。</span><span class="sxs-lookup"><span data-stu-id="19266-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="19266-111">示例</span><span class="sxs-lookup"><span data-stu-id="19266-111">EXAMPLES</span></span>

### <span data-ttu-id="19266-112">範例1</span><span class="sxs-lookup"><span data-stu-id="19266-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="19266-113">測試使用者訂閱是否可移至委派提供者優惠。</span><span class="sxs-lookup"><span data-stu-id="19266-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="19266-114">範例2</span><span class="sxs-lookup"><span data-stu-id="19266-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="19266-115">測試使用者訂閱可以從委派的提供者移至預設提供者。</span><span class="sxs-lookup"><span data-stu-id="19266-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="19266-116">參數</span><span class="sxs-lookup"><span data-stu-id="19266-116">PARAMETERS</span></span>

### <span data-ttu-id="19266-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19266-117">-AsJob</span></span>
<span data-ttu-id="19266-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="19266-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19266-119">-DefaultProfile</span></span>
<span data-ttu-id="19266-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19266-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19266-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="19266-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="19266-122">委派提供者提供的識別碼 (從系統管理內容) 要移至的訂閱。</span><span class="sxs-lookup"><span data-stu-id="19266-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19266-123">-InputObject</span></span>
<span data-ttu-id="19266-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="19266-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="19266-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="19266-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="19266-126">要構造的移動訂閱動作定義，請參閱 MOVESUBSCRIPTIONSDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="19266-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="19266-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19266-127">-NoWait</span></span>
<span data-ttu-id="19266-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="19266-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19266-129">-PassThru</span></span>
<span data-ttu-id="19266-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="19266-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19266-131">-ResourceId</span></span>
<span data-ttu-id="19266-132">要移至目標委派提供者優惠的訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="19266-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19266-133">-SubscriptionId</span></span>
<span data-ttu-id="19266-134">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="19266-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19266-135">-確認</span><span class="sxs-lookup"><span data-stu-id="19266-135">-Confirm</span></span>
<span data-ttu-id="19266-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="19266-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19266-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19266-137">-WhatIf</span></span>
<span data-ttu-id="19266-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="19266-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19266-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19266-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19266-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19266-140">CommonParameters</span></span>
<span data-ttu-id="19266-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19266-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19266-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="19266-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19266-143">輸入</span><span class="sxs-lookup"><span data-stu-id="19266-143">INPUTS</span></span>

### <span data-ttu-id="19266-144">IMoveSubscriptionsDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="19266-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="19266-145">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="19266-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="19266-146">輸出</span><span class="sxs-lookup"><span data-stu-id="19266-146">OUTPUTS</span></span>

### <span data-ttu-id="19266-147">System.object</span><span class="sxs-lookup"><span data-stu-id="19266-147">System.Boolean</span></span>

<span data-ttu-id="19266-148">別名</span><span class="sxs-lookup"><span data-stu-id="19266-148">ALIASES</span></span>

### <span data-ttu-id="19266-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="19266-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="19266-150">筆記</span><span class="sxs-lookup"><span data-stu-id="19266-150">NOTES</span></span>

<span data-ttu-id="19266-151">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="19266-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19266-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="19266-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="19266-153">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="19266-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19266-154">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="19266-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="19266-155">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="19266-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="19266-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="19266-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19266-157">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="19266-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="19266-158">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="19266-159">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="19266-160">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="19266-161">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="19266-162">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="19266-163">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="19266-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="19266-164">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="19266-165">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="19266-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="19266-166">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="19266-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="19266-167">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="19266-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="19266-168">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="19266-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="19266-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> ：移動訂閱動作定義</span><span class="sxs-lookup"><span data-stu-id="19266-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="19266-170">`Resources <String[]>`：要移至目標委派提供者優惠的訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="19266-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="19266-171">`[TargetDelegatedProviderOffer <String>]`：委派提供者提供的識別碼 (從系統管理內容) 要移至的訂閱。</span><span class="sxs-lookup"><span data-stu-id="19266-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="19266-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="19266-172">RELATED LINKS</span></span>

