---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968320"
---
# <span data-ttu-id="f6369-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="f6369-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="f6369-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6369-102">SYNOPSIS</span></span>
<span data-ttu-id="f6369-103">依名稱取得目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="f6369-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="f6369-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6369-104">SYNTAX</span></span>

### <span data-ttu-id="f6369-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f6369-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6369-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f6369-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6369-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6369-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6369-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6369-108">DESCRIPTION</span></span>
<span data-ttu-id="f6369-109">依名稱取得目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="f6369-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="f6369-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6369-110">EXAMPLES</span></span>

### <span data-ttu-id="f6369-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f6369-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="f6369-112">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="f6369-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="f6369-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6369-113">PARAMETERS</span></span>

### <span data-ttu-id="f6369-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6369-114">-DefaultProfile</span></span>
<span data-ttu-id="f6369-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6369-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6369-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6369-116">-InputObject</span></span>
<span data-ttu-id="f6369-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6369-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6369-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6369-118">-Name</span></span>
<span data-ttu-id="f6369-119">目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="f6369-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6369-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6369-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f6369-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f6369-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6369-122">-SubscriptionId</span></span>
<span data-ttu-id="f6369-123">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f6369-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6369-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6369-124">CommonParameters</span></span>
<span data-ttu-id="f6369-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6369-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6369-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6369-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6369-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f6369-127">INPUTS</span></span>

### <span data-ttu-id="f6369-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="f6369-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f6369-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f6369-129">OUTPUTS</span></span>

### <span data-ttu-id="f6369-130">IDirectoryTenant （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="f6369-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="f6369-131">別名</span><span class="sxs-lookup"><span data-stu-id="f6369-131">ALIASES</span></span>

## <span data-ttu-id="f6369-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f6369-132">NOTES</span></span>

<span data-ttu-id="f6369-133">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f6369-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6369-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6369-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f6369-135">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6369-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6369-136">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6369-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f6369-137">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6369-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f6369-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6369-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6369-139">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="f6369-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f6369-140">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f6369-141">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f6369-142">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f6369-143">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f6369-144">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f6369-145">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="f6369-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f6369-146">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f6369-147">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f6369-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f6369-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f6369-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f6369-149">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f6369-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f6369-150">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f6369-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f6369-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6369-151">RELATED LINKS</span></span>

