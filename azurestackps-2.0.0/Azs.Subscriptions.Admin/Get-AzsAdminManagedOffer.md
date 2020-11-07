---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966587"
---
# <span data-ttu-id="170cf-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="170cf-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="170cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="170cf-102">SYNOPSIS</span></span>
<span data-ttu-id="170cf-103">取得指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="170cf-103">Get the specified offer.</span></span>

## <span data-ttu-id="170cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="170cf-104">SYNTAX</span></span>

### <span data-ttu-id="170cf-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="170cf-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="170cf-106">獲取</span><span class="sxs-lookup"><span data-stu-id="170cf-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="170cf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="170cf-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="170cf-108">List1</span><span class="sxs-lookup"><span data-stu-id="170cf-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="170cf-109">說明</span><span class="sxs-lookup"><span data-stu-id="170cf-109">DESCRIPTION</span></span>
<span data-ttu-id="170cf-110">取得指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="170cf-110">Get the specified offer.</span></span>

## <span data-ttu-id="170cf-111">示例</span><span class="sxs-lookup"><span data-stu-id="170cf-111">EXAMPLES</span></span>

### <span data-ttu-id="170cf-112">範例1</span><span class="sxs-lookup"><span data-stu-id="170cf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="170cf-113">透過名稱和 ResourceGroupName 取得優惠</span><span class="sxs-lookup"><span data-stu-id="170cf-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="170cf-114">參數</span><span class="sxs-lookup"><span data-stu-id="170cf-114">PARAMETERS</span></span>

### <span data-ttu-id="170cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170cf-115">-DefaultProfile</span></span>
<span data-ttu-id="170cf-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="170cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="170cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="170cf-117">-InputObject</span></span>
<span data-ttu-id="170cf-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="170cf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="170cf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="170cf-119">-Name</span></span>
<span data-ttu-id="170cf-120">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-120">Name of an offer.</span></span>

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

### <span data-ttu-id="170cf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170cf-121">-ResourceGroupName</span></span>
<span data-ttu-id="170cf-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="170cf-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="170cf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="170cf-123">-SubscriptionId</span></span>
<span data-ttu-id="170cf-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="170cf-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="170cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170cf-125">CommonParameters</span></span>
<span data-ttu-id="170cf-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="170cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170cf-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="170cf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170cf-128">輸入</span><span class="sxs-lookup"><span data-stu-id="170cf-128">INPUTS</span></span>

### <span data-ttu-id="170cf-129">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="170cf-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="170cf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="170cf-130">OUTPUTS</span></span>

### <span data-ttu-id="170cf-131">IOffer （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="170cf-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="170cf-132">別名</span><span class="sxs-lookup"><span data-stu-id="170cf-132">ALIASES</span></span>

<span data-ttu-id="170cf-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="170cf-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="170cf-134">筆記</span><span class="sxs-lookup"><span data-stu-id="170cf-134">NOTES</span></span>

<span data-ttu-id="170cf-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="170cf-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="170cf-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="170cf-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="170cf-137">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="170cf-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="170cf-138">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="170cf-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="170cf-139">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="170cf-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="170cf-140">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="170cf-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="170cf-141">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="170cf-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="170cf-142">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="170cf-143">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="170cf-144">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="170cf-145">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="170cf-146">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="170cf-147">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="170cf-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="170cf-148">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="170cf-149">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="170cf-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="170cf-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="170cf-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="170cf-151">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="170cf-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="170cf-152">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="170cf-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="170cf-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="170cf-153">RELATED LINKS</span></span>

