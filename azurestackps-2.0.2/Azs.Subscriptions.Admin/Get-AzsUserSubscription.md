---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968513"
---
# <span data-ttu-id="9b442-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="9b442-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="9b442-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b442-102">SYNOPSIS</span></span>
<span data-ttu-id="9b442-103">取得指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b442-103">Get a specified subscription.</span></span>

## <span data-ttu-id="9b442-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b442-104">SYNTAX</span></span>

### <span data-ttu-id="9b442-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9b442-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b442-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9b442-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b442-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b442-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b442-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b442-108">DESCRIPTION</span></span>
<span data-ttu-id="9b442-109">取得指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b442-109">Get a specified subscription.</span></span>

## <span data-ttu-id="9b442-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b442-110">EXAMPLES</span></span>

### <span data-ttu-id="9b442-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9b442-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="9b442-112">取得使用者訂閱清單做為操作員。</span><span class="sxs-lookup"><span data-stu-id="9b442-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="9b442-113">參數</span><span class="sxs-lookup"><span data-stu-id="9b442-113">PARAMETERS</span></span>

### <span data-ttu-id="9b442-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b442-114">-DefaultProfile</span></span>
<span data-ttu-id="9b442-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b442-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b442-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="9b442-116">-Filter</span></span>
<span data-ttu-id="9b442-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="9b442-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b442-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b442-118">-InputObject</span></span>
<span data-ttu-id="9b442-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9b442-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9b442-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b442-120">-SubscriptionId</span></span>
<span data-ttu-id="9b442-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9b442-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b442-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b442-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="9b442-123">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b442-123">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b442-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b442-124">CommonParameters</span></span>
<span data-ttu-id="9b442-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b442-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b442-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b442-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b442-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b442-127">INPUTS</span></span>

### <span data-ttu-id="9b442-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="9b442-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9b442-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9b442-129">OUTPUTS</span></span>

### <span data-ttu-id="9b442-130">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="9b442-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="9b442-131">別名</span><span class="sxs-lookup"><span data-stu-id="9b442-131">ALIASES</span></span>

## <span data-ttu-id="9b442-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9b442-132">NOTES</span></span>

<span data-ttu-id="9b442-133">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9b442-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b442-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9b442-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9b442-135">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9b442-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b442-136">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b442-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9b442-137">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b442-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9b442-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9b442-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b442-139">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="9b442-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9b442-140">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9b442-141">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9b442-142">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9b442-143">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9b442-144">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9b442-145">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="9b442-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9b442-146">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9b442-147">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9b442-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9b442-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9b442-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9b442-149">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b442-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9b442-150">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9b442-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9b442-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b442-151">RELATED LINKS</span></span>

