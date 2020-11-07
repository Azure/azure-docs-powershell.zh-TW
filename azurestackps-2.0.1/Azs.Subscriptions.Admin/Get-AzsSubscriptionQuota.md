---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966703"
---
# <span data-ttu-id="b03ba-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="b03ba-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="b03ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b03ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b03ba-103">依名稱取得配額。</span><span class="sxs-lookup"><span data-stu-id="b03ba-103">Gets a quota by name.</span></span>

## <span data-ttu-id="b03ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b03ba-104">SYNTAX</span></span>

### <span data-ttu-id="b03ba-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b03ba-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03ba-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b03ba-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b03ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b03ba-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b03ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="b03ba-108">DESCRIPTION</span></span>
<span data-ttu-id="b03ba-109">依名稱取得配額。</span><span class="sxs-lookup"><span data-stu-id="b03ba-109">Gets a quota by name.</span></span>

## <span data-ttu-id="b03ba-110">示例</span><span class="sxs-lookup"><span data-stu-id="b03ba-110">EXAMPLES</span></span>

### <span data-ttu-id="b03ba-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b03ba-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="b03ba-112">取得訂閱資源提供者配額的清單。</span><span class="sxs-lookup"><span data-stu-id="b03ba-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="b03ba-113">參數</span><span class="sxs-lookup"><span data-stu-id="b03ba-113">PARAMETERS</span></span>

### <span data-ttu-id="b03ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03ba-114">-DefaultProfile</span></span>
<span data-ttu-id="b03ba-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03ba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03ba-116">-InputObject</span></span>
<span data-ttu-id="b03ba-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b03ba-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b03ba-118">-位置</span><span class="sxs-lookup"><span data-stu-id="b03ba-118">-Location</span></span>
<span data-ttu-id="b03ba-119">AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="b03ba-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b03ba-120">-配額</span><span class="sxs-lookup"><span data-stu-id="b03ba-120">-Quota</span></span>
<span data-ttu-id="b03ba-121">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-121">Name of the quota.</span></span>

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

### <span data-ttu-id="b03ba-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b03ba-122">-SubscriptionId</span></span>
<span data-ttu-id="b03ba-123">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b03ba-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b03ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03ba-124">CommonParameters</span></span>
<span data-ttu-id="b03ba-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b03ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03ba-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b03ba-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03ba-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b03ba-127">INPUTS</span></span>

### <span data-ttu-id="b03ba-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="b03ba-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b03ba-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b03ba-129">OUTPUTS</span></span>

### <span data-ttu-id="b03ba-130">IQuota （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="b03ba-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="b03ba-131">別名</span><span class="sxs-lookup"><span data-stu-id="b03ba-131">ALIASES</span></span>

<span data-ttu-id="b03ba-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="b03ba-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="b03ba-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b03ba-133">NOTES</span></span>

<span data-ttu-id="b03ba-134">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b03ba-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b03ba-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b03ba-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b03ba-136">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b03ba-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b03ba-137">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b03ba-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b03ba-138">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b03ba-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b03ba-139">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b03ba-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b03ba-140">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="b03ba-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b03ba-141">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b03ba-142">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b03ba-143">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b03ba-144">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b03ba-145">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b03ba-146">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="b03ba-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b03ba-147">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b03ba-148">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b03ba-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b03ba-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b03ba-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b03ba-150">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b03ba-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b03ba-151">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b03ba-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b03ba-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b03ba-152">RELATED LINKS</span></span>

