---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968563"
---
# <span data-ttu-id="cd6dd-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="cd6dd-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="cd6dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6dd-103">檢查身分識別健康情況</span><span class="sxs-lookup"><span data-stu-id="cd6dd-103">Checks the identity health</span></span>

## <span data-ttu-id="cd6dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd6dd-104">SYNTAX</span></span>

### <span data-ttu-id="cd6dd-105">檢查 (預設) </span><span class="sxs-lookup"><span data-stu-id="cd6dd-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cd6dd-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd6dd-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd6dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="cd6dd-107">DESCRIPTION</span></span>
<span data-ttu-id="cd6dd-108">檢查身分識別健康情況</span><span class="sxs-lookup"><span data-stu-id="cd6dd-108">Checks the identity health</span></span>

## <span data-ttu-id="cd6dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="cd6dd-109">EXAMPLES</span></span>

### <span data-ttu-id="cd6dd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cd6dd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="cd6dd-111">取得身分識別健康情況的狀態。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="cd6dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="cd6dd-112">PARAMETERS</span></span>

### <span data-ttu-id="cd6dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6dd-113">-DefaultProfile</span></span>
<span data-ttu-id="cd6dd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6dd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd6dd-115">-InputObject</span></span>
<span data-ttu-id="cd6dd-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cd6dd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd6dd-117">-SubscriptionId</span></span>
<span data-ttu-id="cd6dd-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd6dd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cd6dd-119">-Confirm</span></span>
<span data-ttu-id="cd6dd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd6dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6dd-121">-WhatIf</span></span>
<span data-ttu-id="cd6dd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd6dd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd6dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6dd-124">CommonParameters</span></span>
<span data-ttu-id="cd6dd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6dd-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6dd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cd6dd-127">INPUTS</span></span>

### <span data-ttu-id="cd6dd-128">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cd6dd-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="cd6dd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cd6dd-129">OUTPUTS</span></span>

### <span data-ttu-id="cd6dd-130">IIdentityHealthCheckReportDefinition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="cd6dd-131">別名</span><span class="sxs-lookup"><span data-stu-id="cd6dd-131">ALIASES</span></span>

## <span data-ttu-id="cd6dd-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cd6dd-132">NOTES</span></span>

<span data-ttu-id="cd6dd-133">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd6dd-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cd6dd-135">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cd6dd-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd6dd-136">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="cd6dd-137">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="cd6dd-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cd6dd-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd6dd-139">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="cd6dd-140">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="cd6dd-141">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="cd6dd-142">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="cd6dd-143">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="cd6dd-144">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="cd6dd-145">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="cd6dd-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="cd6dd-146">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cd6dd-147">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="cd6dd-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cd6dd-149">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="cd6dd-150">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="cd6dd-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="cd6dd-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd6dd-151">RELATED LINKS</span></span>

