---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966560"
---
# <span data-ttu-id="4dad2-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="4dad2-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="4dad2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4dad2-102">SYNOPSIS</span></span>
<span data-ttu-id="4dad2-103">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="4dad2-103">Delete the specified offer.</span></span>

## <span data-ttu-id="4dad2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4dad2-104">SYNTAX</span></span>

### <span data-ttu-id="4dad2-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4dad2-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4dad2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4dad2-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4dad2-107">說明</span><span class="sxs-lookup"><span data-stu-id="4dad2-107">DESCRIPTION</span></span>
<span data-ttu-id="4dad2-108">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="4dad2-108">Delete the specified offer.</span></span>

## <span data-ttu-id="4dad2-109">示例</span><span class="sxs-lookup"><span data-stu-id="4dad2-109">EXAMPLES</span></span>

### <span data-ttu-id="4dad2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4dad2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="4dad2-111">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="4dad2-111">Delete the specified offer.</span></span>

## <span data-ttu-id="4dad2-112">參數</span><span class="sxs-lookup"><span data-stu-id="4dad2-112">PARAMETERS</span></span>

### <span data-ttu-id="4dad2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dad2-113">-DefaultProfile</span></span>
<span data-ttu-id="4dad2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dad2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dad2-115">-InputObject</span></span>
<span data-ttu-id="4dad2-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4dad2-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4dad2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4dad2-117">-Name</span></span>
<span data-ttu-id="4dad2-118">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-118">Name of an offer.</span></span>

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

### <span data-ttu-id="4dad2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dad2-119">-PassThru</span></span>
<span data-ttu-id="4dad2-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="4dad2-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4dad2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dad2-121">-ResourceGroupName</span></span>
<span data-ttu-id="4dad2-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4dad2-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4dad2-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dad2-123">-SubscriptionId</span></span>
<span data-ttu-id="4dad2-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4dad2-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4dad2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4dad2-125">-Confirm</span></span>
<span data-ttu-id="4dad2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4dad2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dad2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dad2-127">-WhatIf</span></span>
<span data-ttu-id="4dad2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4dad2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dad2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4dad2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dad2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dad2-130">CommonParameters</span></span>
<span data-ttu-id="4dad2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4dad2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dad2-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4dad2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dad2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4dad2-133">INPUTS</span></span>

### <span data-ttu-id="4dad2-134">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="4dad2-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="4dad2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4dad2-135">OUTPUTS</span></span>

### <span data-ttu-id="4dad2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4dad2-136">System.Boolean</span></span>

<span data-ttu-id="4dad2-137">別名</span><span class="sxs-lookup"><span data-stu-id="4dad2-137">ALIASES</span></span>

## <span data-ttu-id="4dad2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4dad2-138">NOTES</span></span>

<span data-ttu-id="4dad2-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4dad2-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dad2-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4dad2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4dad2-141">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4dad2-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dad2-142">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4dad2-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="4dad2-143">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4dad2-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="4dad2-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4dad2-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dad2-145">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="4dad2-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="4dad2-146">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="4dad2-147">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="4dad2-148">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="4dad2-149">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="4dad2-150">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="4dad2-151">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="4dad2-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="4dad2-152">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4dad2-153">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4dad2-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="4dad2-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4dad2-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4dad2-155">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4dad2-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="4dad2-156">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4dad2-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="4dad2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dad2-157">RELATED LINKS</span></span>

