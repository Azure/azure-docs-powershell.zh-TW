---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966581"
---
# <span data-ttu-id="0cb05-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="0cb05-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="0cb05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cb05-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb05-103">取得指定的委派提供者。</span><span class="sxs-lookup"><span data-stu-id="0cb05-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="0cb05-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cb05-104">SYNTAX</span></span>

### <span data-ttu-id="0cb05-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0cb05-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0cb05-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0cb05-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0cb05-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0cb05-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cb05-108">說明</span><span class="sxs-lookup"><span data-stu-id="0cb05-108">DESCRIPTION</span></span>
<span data-ttu-id="0cb05-109">取得指定的委派提供者。</span><span class="sxs-lookup"><span data-stu-id="0cb05-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="0cb05-110">示例</span><span class="sxs-lookup"><span data-stu-id="0cb05-110">EXAMPLES</span></span>

### <span data-ttu-id="0cb05-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0cb05-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="0cb05-112">取得特定的委派提供者。</span><span class="sxs-lookup"><span data-stu-id="0cb05-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="0cb05-113">參數</span><span class="sxs-lookup"><span data-stu-id="0cb05-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb05-114">-DefaultProfile</span></span>
<span data-ttu-id="0cb05-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cb05-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="0cb05-116">-DelegatedProviderId</span></span>
<span data-ttu-id="0cb05-117">DelegatedProvider 識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0cb05-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="0cb05-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cb05-118">-InputObject</span></span>
<span data-ttu-id="0cb05-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0cb05-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0cb05-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0cb05-120">-SubscriptionId</span></span>
<span data-ttu-id="0cb05-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0cb05-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0cb05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb05-122">CommonParameters</span></span>
<span data-ttu-id="0cb05-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cb05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb05-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0cb05-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb05-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0cb05-125">INPUTS</span></span>

### <span data-ttu-id="0cb05-126">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="0cb05-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="0cb05-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0cb05-127">OUTPUTS</span></span>

### <span data-ttu-id="0cb05-128">ISubscriptionDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="0cb05-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="0cb05-129">別名</span><span class="sxs-lookup"><span data-stu-id="0cb05-129">ALIASES</span></span>

## <span data-ttu-id="0cb05-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0cb05-130">NOTES</span></span>

<span data-ttu-id="0cb05-131">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0cb05-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0cb05-132">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0cb05-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0cb05-133">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0cb05-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0cb05-134">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cb05-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="0cb05-135">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cb05-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="0cb05-136">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0cb05-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0cb05-137">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="0cb05-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="0cb05-138">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="0cb05-139">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="0cb05-140">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="0cb05-141">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="0cb05-142">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="0cb05-143">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="0cb05-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="0cb05-144">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0cb05-145">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0cb05-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="0cb05-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0cb05-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0cb05-147">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0cb05-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="0cb05-148">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="0cb05-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="0cb05-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cb05-149">RELATED LINKS</span></span>

