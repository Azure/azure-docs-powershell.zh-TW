---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966603"
---
# <span data-ttu-id="6dfc9-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="6dfc9-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="6dfc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfc9-103">取得使用優惠之訂閱所取得的指定方案。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="6dfc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dfc9-104">SYNTAX</span></span>

### <span data-ttu-id="6dfc9-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="6dfc9-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfc9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="6dfc9-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6dfc9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6dfc9-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dfc9-108">說明</span><span class="sxs-lookup"><span data-stu-id="6dfc9-108">DESCRIPTION</span></span>
<span data-ttu-id="6dfc9-109">取得使用優惠之訂閱所取得的指定方案。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="6dfc9-110">示例</span><span class="sxs-lookup"><span data-stu-id="6dfc9-110">EXAMPLES</span></span>

### <span data-ttu-id="6dfc9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6dfc9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="6dfc9-112">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="6dfc9-113">參數</span><span class="sxs-lookup"><span data-stu-id="6dfc9-113">PARAMETERS</span></span>

### <span data-ttu-id="6dfc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfc9-114">-DefaultProfile</span></span>
<span data-ttu-id="6dfc9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfc9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dfc9-116">-InputObject</span></span>
<span data-ttu-id="6dfc9-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6dfc9-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="6dfc9-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="6dfc9-119">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="6dfc9-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="6dfc9-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dfc9-120">-SubscriptionId</span></span>
<span data-ttu-id="6dfc9-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6dfc9-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dfc9-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="6dfc9-123">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="6dfc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfc9-124">CommonParameters</span></span>
<span data-ttu-id="6dfc9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfc9-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfc9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6dfc9-127">INPUTS</span></span>

### <span data-ttu-id="6dfc9-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="6dfc9-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="6dfc9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6dfc9-129">OUTPUTS</span></span>

### <span data-ttu-id="6dfc9-130">IPlanAcquisition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="6dfc9-131">別名</span><span class="sxs-lookup"><span data-stu-id="6dfc9-131">ALIASES</span></span>

<span data-ttu-id="6dfc9-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="6dfc9-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="6dfc9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6dfc9-133">NOTES</span></span>

<span data-ttu-id="6dfc9-134">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6dfc9-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6dfc9-136">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6dfc9-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6dfc9-137">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="6dfc9-138">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="6dfc9-139">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6dfc9-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6dfc9-140">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="6dfc9-141">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="6dfc9-142">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="6dfc9-143">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="6dfc9-144">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="6dfc9-145">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="6dfc9-146">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="6dfc9-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="6dfc9-147">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="6dfc9-148">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="6dfc9-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6dfc9-150">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="6dfc9-151">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6dfc9-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="6dfc9-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dfc9-152">RELATED LINKS</span></span>

