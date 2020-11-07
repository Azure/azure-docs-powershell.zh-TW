---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966559"
---
# <span data-ttu-id="a0805-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="a0805-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="a0805-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0805-102">SYNOPSIS</span></span>
<span data-ttu-id="a0805-103">刪除取得的方案。</span><span class="sxs-lookup"><span data-stu-id="a0805-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a0805-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0805-104">SYNTAX</span></span>

### <span data-ttu-id="a0805-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="a0805-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0805-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0805-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0805-107">說明</span><span class="sxs-lookup"><span data-stu-id="a0805-107">DESCRIPTION</span></span>
<span data-ttu-id="a0805-108">刪除取得的方案。</span><span class="sxs-lookup"><span data-stu-id="a0805-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a0805-109">示例</span><span class="sxs-lookup"><span data-stu-id="a0805-109">EXAMPLES</span></span>

### <span data-ttu-id="a0805-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="a0805-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="a0805-111">刪除取得的方案。</span><span class="sxs-lookup"><span data-stu-id="a0805-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="a0805-112">參數</span><span class="sxs-lookup"><span data-stu-id="a0805-112">PARAMETERS</span></span>

### <span data-ttu-id="a0805-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0805-113">-DefaultProfile</span></span>
<span data-ttu-id="a0805-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0805-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0805-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0805-115">-InputObject</span></span>
<span data-ttu-id="a0805-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0805-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a0805-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0805-117">-PassThru</span></span>
<span data-ttu-id="a0805-118">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="a0805-118">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0805-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a0805-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="a0805-120">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="a0805-120">The plan acquisition Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0805-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0805-121">-SubscriptionId</span></span>
<span data-ttu-id="a0805-122">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a0805-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0805-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0805-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="a0805-124">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a0805-124">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0805-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a0805-125">-Confirm</span></span>
<span data-ttu-id="a0805-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0805-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0805-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0805-127">-WhatIf</span></span>
<span data-ttu-id="a0805-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0805-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0805-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0805-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0805-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0805-130">CommonParameters</span></span>
<span data-ttu-id="a0805-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0805-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0805-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0805-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0805-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a0805-133">INPUTS</span></span>

### <span data-ttu-id="a0805-134">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="a0805-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="a0805-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a0805-135">OUTPUTS</span></span>

### <span data-ttu-id="a0805-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a0805-136">System.Boolean</span></span>

<span data-ttu-id="a0805-137">別名</span><span class="sxs-lookup"><span data-stu-id="a0805-137">ALIASES</span></span>

### <span data-ttu-id="a0805-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a0805-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a0805-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a0805-139">NOTES</span></span>

<span data-ttu-id="a0805-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a0805-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0805-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a0805-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a0805-142">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a0805-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0805-143">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0805-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="a0805-144">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0805-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="a0805-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a0805-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0805-146">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="a0805-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="a0805-147">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="a0805-148">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="a0805-149">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="a0805-150">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="a0805-151">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="a0805-152">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="a0805-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="a0805-153">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="a0805-154">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a0805-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="a0805-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a0805-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a0805-156">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a0805-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="a0805-157">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a0805-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="a0805-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0805-158">RELATED LINKS</span></span>

