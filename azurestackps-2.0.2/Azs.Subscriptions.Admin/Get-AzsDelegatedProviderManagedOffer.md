---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968599"
---
# <span data-ttu-id="9b03e-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="9b03e-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="9b03e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b03e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b03e-103">取得指定的委派提供者提供方案。</span><span class="sxs-lookup"><span data-stu-id="9b03e-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="9b03e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b03e-104">SYNTAX</span></span>

### <span data-ttu-id="9b03e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9b03e-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b03e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9b03e-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b03e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b03e-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b03e-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b03e-108">DESCRIPTION</span></span>
<span data-ttu-id="9b03e-109">取得指定的委派提供者提供方案。</span><span class="sxs-lookup"><span data-stu-id="9b03e-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="9b03e-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b03e-110">EXAMPLES</span></span>

### <span data-ttu-id="9b03e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9b03e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="9b03e-112">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="9b03e-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="9b03e-113">參數</span><span class="sxs-lookup"><span data-stu-id="9b03e-113">PARAMETERS</span></span>

### <span data-ttu-id="9b03e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b03e-114">-DefaultProfile</span></span>
<span data-ttu-id="9b03e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b03e-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b03e-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="9b03e-117">委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b03e-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9b03e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b03e-118">-InputObject</span></span>
<span data-ttu-id="9b03e-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9b03e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b03e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b03e-120">-Name</span></span>
<span data-ttu-id="9b03e-121">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-121">Name of an offer.</span></span>

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

### <span data-ttu-id="9b03e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b03e-122">-SubscriptionId</span></span>
<span data-ttu-id="9b03e-123">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9b03e-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b03e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b03e-124">CommonParameters</span></span>
<span data-ttu-id="9b03e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b03e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b03e-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b03e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b03e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b03e-127">INPUTS</span></span>

### <span data-ttu-id="9b03e-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="9b03e-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9b03e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9b03e-129">OUTPUTS</span></span>

### <span data-ttu-id="9b03e-130">IDelegatedProviderOffer （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="9b03e-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="9b03e-131">別名</span><span class="sxs-lookup"><span data-stu-id="9b03e-131">ALIASES</span></span>

## <span data-ttu-id="9b03e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9b03e-132">NOTES</span></span>

<span data-ttu-id="9b03e-133">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9b03e-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b03e-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9b03e-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9b03e-135">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9b03e-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b03e-136">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b03e-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9b03e-137">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b03e-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9b03e-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9b03e-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b03e-139">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="9b03e-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9b03e-140">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9b03e-141">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9b03e-142">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9b03e-143">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9b03e-144">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9b03e-145">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="9b03e-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9b03e-146">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9b03e-147">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9b03e-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9b03e-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9b03e-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9b03e-149">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b03e-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9b03e-150">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9b03e-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9b03e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b03e-151">RELATED LINKS</span></span>

