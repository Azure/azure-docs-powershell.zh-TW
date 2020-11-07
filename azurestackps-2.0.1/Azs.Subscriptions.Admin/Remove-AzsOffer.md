---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966623"
---
# <span data-ttu-id="5b9a4-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="5b9a4-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="5b9a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9a4-103">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-103">Delete the specified offer.</span></span>

## <span data-ttu-id="5b9a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b9a4-104">SYNTAX</span></span>

### <span data-ttu-id="5b9a4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5b9a4-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b9a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b9a4-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b9a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b9a4-107">DESCRIPTION</span></span>
<span data-ttu-id="5b9a4-108">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-108">Delete the specified offer.</span></span>

## <span data-ttu-id="5b9a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="5b9a4-109">EXAMPLES</span></span>

### <span data-ttu-id="5b9a4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5b9a4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="5b9a4-111">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-111">Delete the specified offer.</span></span>

## <span data-ttu-id="5b9a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b9a4-112">PARAMETERS</span></span>

### <span data-ttu-id="5b9a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9a4-113">-DefaultProfile</span></span>
<span data-ttu-id="5b9a4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b9a4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b9a4-115">-InputObject</span></span>
<span data-ttu-id="5b9a4-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5b9a4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b9a4-117">-Name</span></span>
<span data-ttu-id="5b9a4-118">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-118">Name of an offer.</span></span>

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

### <span data-ttu-id="5b9a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b9a4-119">-PassThru</span></span>
<span data-ttu-id="5b9a4-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5b9a4-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5b9a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="5b9a4-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5b9a4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b9a4-123">-SubscriptionId</span></span>
<span data-ttu-id="5b9a4-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b9a4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5b9a4-125">-Confirm</span></span>
<span data-ttu-id="5b9a4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b9a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b9a4-127">-WhatIf</span></span>
<span data-ttu-id="5b9a4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b9a4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b9a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9a4-130">CommonParameters</span></span>
<span data-ttu-id="5b9a4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9a4-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9a4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5b9a4-133">INPUTS</span></span>

### <span data-ttu-id="5b9a4-134">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="5b9a4-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="5b9a4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5b9a4-135">OUTPUTS</span></span>

### <span data-ttu-id="5b9a4-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5b9a4-136">System.Boolean</span></span>

<span data-ttu-id="5b9a4-137">別名</span><span class="sxs-lookup"><span data-stu-id="5b9a4-137">ALIASES</span></span>

## <span data-ttu-id="5b9a4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5b9a4-138">NOTES</span></span>

<span data-ttu-id="5b9a4-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b9a4-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5b9a4-141">INPUTOBJECT <ISubscriptionsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5b9a4-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b9a4-142">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="5b9a4-143">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="5b9a4-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5b9a4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b9a4-145">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="5b9a4-146">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="5b9a4-147">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="5b9a4-148">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="5b9a4-149">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="5b9a4-150">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="5b9a4-151">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="5b9a4-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="5b9a4-152">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5b9a4-153">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="5b9a4-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5b9a4-155">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="5b9a4-156">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5b9a4-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="5b9a4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b9a4-157">RELATED LINKS</span></span>

