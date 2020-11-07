---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968442"
---
# <span data-ttu-id="9333c-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="9333c-101">Get-AzsPlan</span></span>

## <span data-ttu-id="9333c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9333c-102">SYNOPSIS</span></span>
<span data-ttu-id="9333c-103">取得指定的方案。</span><span class="sxs-lookup"><span data-stu-id="9333c-103">Get the specified plan.</span></span>

## <span data-ttu-id="9333c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9333c-104">SYNTAX</span></span>

### <span data-ttu-id="9333c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9333c-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9333c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9333c-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9333c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9333c-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9333c-108">List1</span><span class="sxs-lookup"><span data-stu-id="9333c-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9333c-109">說明</span><span class="sxs-lookup"><span data-stu-id="9333c-109">DESCRIPTION</span></span>
<span data-ttu-id="9333c-110">取得指定的方案。</span><span class="sxs-lookup"><span data-stu-id="9333c-110">Get the specified plan.</span></span>

## <span data-ttu-id="9333c-111">示例</span><span class="sxs-lookup"><span data-stu-id="9333c-111">EXAMPLES</span></span>

### <span data-ttu-id="9333c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9333c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="9333c-113">在此訂閱下取得特定方案。</span><span class="sxs-lookup"><span data-stu-id="9333c-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="9333c-114">參數</span><span class="sxs-lookup"><span data-stu-id="9333c-114">PARAMETERS</span></span>

### <span data-ttu-id="9333c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9333c-115">-DefaultProfile</span></span>
<span data-ttu-id="9333c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9333c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9333c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9333c-117">-InputObject</span></span>
<span data-ttu-id="9333c-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9333c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9333c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9333c-119">-Name</span></span>
<span data-ttu-id="9333c-120">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-120">Name of the plan.</span></span>

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

### <span data-ttu-id="9333c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9333c-121">-ResourceGroupName</span></span>
<span data-ttu-id="9333c-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9333c-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9333c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9333c-123">-SubscriptionId</span></span>
<span data-ttu-id="9333c-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9333c-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9333c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9333c-125">CommonParameters</span></span>
<span data-ttu-id="9333c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9333c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9333c-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9333c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9333c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9333c-128">INPUTS</span></span>

### <span data-ttu-id="9333c-129">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="9333c-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9333c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9333c-130">OUTPUTS</span></span>

### <span data-ttu-id="9333c-131">IPlan （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="9333c-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="9333c-132">別名</span><span class="sxs-lookup"><span data-stu-id="9333c-132">ALIASES</span></span>

## <span data-ttu-id="9333c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9333c-133">NOTES</span></span>

<span data-ttu-id="9333c-134">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9333c-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9333c-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9333c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9333c-136">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9333c-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9333c-137">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9333c-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9333c-138">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9333c-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9333c-139">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9333c-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9333c-140">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="9333c-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9333c-141">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9333c-142">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9333c-143">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9333c-144">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9333c-145">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9333c-146">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="9333c-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9333c-147">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9333c-148">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9333c-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9333c-149">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9333c-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9333c-150">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9333c-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9333c-151">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9333c-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9333c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9333c-152">RELATED LINKS</span></span>

