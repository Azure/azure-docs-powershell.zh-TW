---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968179"
---
# <span data-ttu-id="2023c-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="2023c-101">Get-AzsLocation</span></span>

## <span data-ttu-id="2023c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2023c-102">SYNOPSIS</span></span>
<span data-ttu-id="2023c-103">取得指定的位置。</span><span class="sxs-lookup"><span data-stu-id="2023c-103">Get the specified location.</span></span>

## <span data-ttu-id="2023c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2023c-104">SYNTAX</span></span>

### <span data-ttu-id="2023c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2023c-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2023c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2023c-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2023c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2023c-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2023c-108">說明</span><span class="sxs-lookup"><span data-stu-id="2023c-108">DESCRIPTION</span></span>
<span data-ttu-id="2023c-109">取得指定的位置。</span><span class="sxs-lookup"><span data-stu-id="2023c-109">Get the specified location.</span></span>

## <span data-ttu-id="2023c-110">示例</span><span class="sxs-lookup"><span data-stu-id="2023c-110">EXAMPLES</span></span>

### <span data-ttu-id="2023c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2023c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="2023c-112">取得所有 AzureStack 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="2023c-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="2023c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2023c-113">PARAMETERS</span></span>

### <span data-ttu-id="2023c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2023c-114">-DefaultProfile</span></span>
<span data-ttu-id="2023c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2023c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2023c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2023c-116">-InputObject</span></span>
<span data-ttu-id="2023c-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2023c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2023c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2023c-118">-Name</span></span>
<span data-ttu-id="2023c-119">AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="2023c-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2023c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2023c-120">-SubscriptionId</span></span>
<span data-ttu-id="2023c-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2023c-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2023c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2023c-122">CommonParameters</span></span>
<span data-ttu-id="2023c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2023c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2023c-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2023c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2023c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2023c-125">INPUTS</span></span>

### <span data-ttu-id="2023c-126">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="2023c-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="2023c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2023c-127">OUTPUTS</span></span>

### <span data-ttu-id="2023c-128">ILocation （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="2023c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="2023c-129">別名</span><span class="sxs-lookup"><span data-stu-id="2023c-129">ALIASES</span></span>

## <span data-ttu-id="2023c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2023c-130">NOTES</span></span>

<span data-ttu-id="2023c-131">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2023c-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2023c-132">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2023c-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2023c-133">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2023c-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2023c-134">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2023c-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="2023c-135">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2023c-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="2023c-136">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2023c-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2023c-137">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="2023c-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="2023c-138">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="2023c-139">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="2023c-140">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="2023c-141">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="2023c-142">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2023c-143">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="2023c-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="2023c-144">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2023c-145">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2023c-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="2023c-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2023c-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2023c-147">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2023c-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="2023c-148">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2023c-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="2023c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2023c-149">RELATED LINKS</span></span>

