---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966593"
---
# <span data-ttu-id="27e03-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="27e03-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="27e03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27e03-102">SYNOPSIS</span></span>
<span data-ttu-id="27e03-103">在委派的提供者優惠之間移動訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e03-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="27e03-104">句法</span><span class="sxs-lookup"><span data-stu-id="27e03-104">SYNTAX</span></span>

### <span data-ttu-id="27e03-105">MoveExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="27e03-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27e03-106">把</span><span class="sxs-lookup"><span data-stu-id="27e03-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="27e03-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27e03-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27e03-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="27e03-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27e03-109">說明</span><span class="sxs-lookup"><span data-stu-id="27e03-109">DESCRIPTION</span></span>
<span data-ttu-id="27e03-110">在委派的提供者優惠之間移動訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e03-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="27e03-111">示例</span><span class="sxs-lookup"><span data-stu-id="27e03-111">EXAMPLES</span></span>

### <span data-ttu-id="27e03-112">範例1</span><span class="sxs-lookup"><span data-stu-id="27e03-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="27e03-113">將使用者訂閱移至委派提供者優惠。</span><span class="sxs-lookup"><span data-stu-id="27e03-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="27e03-114">範例2</span><span class="sxs-lookup"><span data-stu-id="27e03-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="27e03-115">將來自委派提供者的使用者訂閱移至預設提供者。</span><span class="sxs-lookup"><span data-stu-id="27e03-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="27e03-116">參數</span><span class="sxs-lookup"><span data-stu-id="27e03-116">PARAMETERS</span></span>

### <span data-ttu-id="27e03-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27e03-117">-AsJob</span></span>
<span data-ttu-id="27e03-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="27e03-118">Run the command as a job</span></span>

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

### <span data-ttu-id="27e03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e03-119">-DefaultProfile</span></span>
<span data-ttu-id="27e03-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e03-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27e03-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="27e03-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="27e03-122">委派提供者提供的識別碼 (從系統管理內容) 要移至的訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e03-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e03-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27e03-123">-InputObject</span></span>
<span data-ttu-id="27e03-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="27e03-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="27e03-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="27e03-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="27e03-126">要構造的移動訂閱動作定義，請參閱 MOVESUBSCRIPTIONSDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="27e03-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="27e03-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="27e03-127">-NoWait</span></span>
<span data-ttu-id="27e03-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="27e03-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27e03-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27e03-129">-PassThru</span></span>
<span data-ttu-id="27e03-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="27e03-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="27e03-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e03-131">-ResourceId</span></span>
<span data-ttu-id="27e03-132">要移至目標委派提供者優惠的訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="27e03-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e03-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27e03-133">-SubscriptionId</span></span>
<span data-ttu-id="27e03-134">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="27e03-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e03-135">-確認</span><span class="sxs-lookup"><span data-stu-id="27e03-135">-Confirm</span></span>
<span data-ttu-id="27e03-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27e03-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27e03-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e03-137">-WhatIf</span></span>
<span data-ttu-id="27e03-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27e03-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27e03-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27e03-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27e03-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e03-140">CommonParameters</span></span>
<span data-ttu-id="27e03-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27e03-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e03-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27e03-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e03-143">輸入</span><span class="sxs-lookup"><span data-stu-id="27e03-143">INPUTS</span></span>

### <span data-ttu-id="27e03-144">IMoveSubscriptionsDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="27e03-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="27e03-145">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="27e03-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="27e03-146">輸出</span><span class="sxs-lookup"><span data-stu-id="27e03-146">OUTPUTS</span></span>

### <span data-ttu-id="27e03-147">System.object</span><span class="sxs-lookup"><span data-stu-id="27e03-147">System.Boolean</span></span>

<span data-ttu-id="27e03-148">別名</span><span class="sxs-lookup"><span data-stu-id="27e03-148">ALIASES</span></span>

## <span data-ttu-id="27e03-149">筆記</span><span class="sxs-lookup"><span data-stu-id="27e03-149">NOTES</span></span>

<span data-ttu-id="27e03-150">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="27e03-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27e03-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="27e03-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="27e03-152">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="27e03-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27e03-153">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="27e03-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="27e03-154">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="27e03-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="27e03-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="27e03-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27e03-156">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="27e03-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="27e03-157">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="27e03-158">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="27e03-159">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="27e03-160">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="27e03-161">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="27e03-162">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="27e03-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="27e03-163">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="27e03-164">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="27e03-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="27e03-165">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="27e03-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="27e03-166">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="27e03-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="27e03-167">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="27e03-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="27e03-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> ：移動訂閱動作定義</span><span class="sxs-lookup"><span data-stu-id="27e03-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="27e03-169">`Resources <String[]>`：要移至目標委派提供者優惠的訂閱集合。</span><span class="sxs-lookup"><span data-stu-id="27e03-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="27e03-170">`[TargetDelegatedProviderOffer <String>]`：委派提供者提供的識別碼 (從系統管理內容) 要移至的訂閱。</span><span class="sxs-lookup"><span data-stu-id="27e03-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="27e03-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="27e03-171">RELATED LINKS</span></span>

