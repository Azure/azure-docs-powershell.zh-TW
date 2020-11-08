---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968295"
---
# <span data-ttu-id="eccd4-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eccd4-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="eccd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eccd4-102">SYNOPSIS</span></span>
<span data-ttu-id="eccd4-103">取得指定的提供委派。</span><span class="sxs-lookup"><span data-stu-id="eccd4-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="eccd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="eccd4-104">SYNTAX</span></span>

### <span data-ttu-id="eccd4-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="eccd4-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eccd4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="eccd4-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eccd4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eccd4-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eccd4-108">說明</span><span class="sxs-lookup"><span data-stu-id="eccd4-108">DESCRIPTION</span></span>
<span data-ttu-id="eccd4-109">取得指定的提供委派。</span><span class="sxs-lookup"><span data-stu-id="eccd4-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="eccd4-110">示例</span><span class="sxs-lookup"><span data-stu-id="eccd4-110">EXAMPLES</span></span>

### <span data-ttu-id="eccd4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="eccd4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="eccd4-112">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="eccd4-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="eccd4-113">參數</span><span class="sxs-lookup"><span data-stu-id="eccd4-113">PARAMETERS</span></span>

### <span data-ttu-id="eccd4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccd4-114">-DefaultProfile</span></span>
<span data-ttu-id="eccd4-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eccd4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eccd4-116">-InputObject</span></span>
<span data-ttu-id="eccd4-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eccd4-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eccd4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="eccd4-118">-Name</span></span>
<span data-ttu-id="eccd4-119">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="eccd4-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="eccd4-120">-OfferName</span></span>
<span data-ttu-id="eccd4-121">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eccd4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccd4-122">-ResourceGroupName</span></span>
<span data-ttu-id="eccd4-123">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eccd4-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eccd4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eccd4-124">-SubscriptionId</span></span>
<span data-ttu-id="eccd4-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eccd4-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eccd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccd4-126">CommonParameters</span></span>
<span data-ttu-id="eccd4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eccd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccd4-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eccd4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccd4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="eccd4-129">INPUTS</span></span>

### <span data-ttu-id="eccd4-130">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="eccd4-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="eccd4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="eccd4-131">OUTPUTS</span></span>

### <span data-ttu-id="eccd4-132">IOfferDelegation （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="eccd4-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="eccd4-133">別名</span><span class="sxs-lookup"><span data-stu-id="eccd4-133">ALIASES</span></span>

## <span data-ttu-id="eccd4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="eccd4-134">NOTES</span></span>

<span data-ttu-id="eccd4-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="eccd4-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eccd4-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eccd4-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eccd4-137">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="eccd4-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eccd4-138">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="eccd4-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="eccd4-139">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="eccd4-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="eccd4-140">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="eccd4-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eccd4-141">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="eccd4-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="eccd4-142">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="eccd4-143">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="eccd4-144">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="eccd4-145">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="eccd4-146">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="eccd4-147">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="eccd4-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="eccd4-148">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="eccd4-149">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eccd4-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="eccd4-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eccd4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="eccd4-151">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="eccd4-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="eccd4-152">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="eccd4-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="eccd4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="eccd4-153">RELATED LINKS</span></span>
