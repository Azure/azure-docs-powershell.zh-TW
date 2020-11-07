---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966555"
---
# <span data-ttu-id="17e62-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="17e62-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="17e62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17e62-102">SYNOPSIS</span></span>


## <span data-ttu-id="17e62-103">句法</span><span class="sxs-lookup"><span data-stu-id="17e62-103">SYNTAX</span></span>

### <span data-ttu-id="17e62-104">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="17e62-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17e62-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17e62-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17e62-106">說明</span><span class="sxs-lookup"><span data-stu-id="17e62-106">DESCRIPTION</span></span>


## <span data-ttu-id="17e62-107">示例</span><span class="sxs-lookup"><span data-stu-id="17e62-107">EXAMPLES</span></span>

### <span data-ttu-id="17e62-108">範例1</span><span class="sxs-lookup"><span data-stu-id="17e62-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="17e62-109">刪除指定的租使用者訂閱。</span><span class="sxs-lookup"><span data-stu-id="17e62-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="17e62-110">參數</span><span class="sxs-lookup"><span data-stu-id="17e62-110">PARAMETERS</span></span>

### <span data-ttu-id="17e62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e62-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="17e62-112">-Force</span><span class="sxs-lookup"><span data-stu-id="17e62-112">-Force</span></span>


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

### <span data-ttu-id="17e62-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e62-113">-InputObject</span></span>
<span data-ttu-id="17e62-114">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="17e62-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17e62-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17e62-115">-PassThru</span></span>


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

### <span data-ttu-id="17e62-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17e62-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="17e62-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17e62-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="17e62-118">-確認</span><span class="sxs-lookup"><span data-stu-id="17e62-118">-Confirm</span></span>
<span data-ttu-id="17e62-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17e62-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e62-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e62-120">-WhatIf</span></span>
<span data-ttu-id="17e62-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17e62-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e62-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17e62-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e62-123">CommonParameters</span></span>
<span data-ttu-id="17e62-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17e62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e62-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17e62-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e62-126">輸入</span><span class="sxs-lookup"><span data-stu-id="17e62-126">INPUTS</span></span>

### <span data-ttu-id="17e62-127">ISubscriptionsAdminIdentity （SubscriptionsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="17e62-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="17e62-128">輸出</span><span class="sxs-lookup"><span data-stu-id="17e62-128">OUTPUTS</span></span>

### <span data-ttu-id="17e62-129">System.object</span><span class="sxs-lookup"><span data-stu-id="17e62-129">System.Boolean</span></span>

<span data-ttu-id="17e62-130">別名</span><span class="sxs-lookup"><span data-stu-id="17e62-130">ALIASES</span></span>

## <span data-ttu-id="17e62-131">筆記</span><span class="sxs-lookup"><span data-stu-id="17e62-131">NOTES</span></span>

<span data-ttu-id="17e62-132">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="17e62-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17e62-133">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="17e62-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="17e62-134">INPUTOBJECT <ISubscriptionsAdminIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="17e62-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="17e62-135">`[DelegatedProvider <String>]`： DelegatedProvider 識別碼。</span><span class="sxs-lookup"><span data-stu-id="17e62-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="17e62-136">`[DelegatedProviderSubscriptionId <String>]`：已委派提供者訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="17e62-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="17e62-137">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="17e62-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17e62-138">`[Location <String>]`： AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="17e62-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="17e62-139">`[ManifestName <String>]`：資訊清單名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="17e62-140">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="17e62-141">`[OfferDelegationName <String>]`：優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="17e62-142">`[OperationsStatusName <String>]`：作業狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="17e62-143">`[Plan <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="17e62-144">`[PlanAcquisitionId <String>]`：方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="17e62-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="17e62-145">`[Quota <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="17e62-146">`[ResourceGroupName <String>]`：資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="17e62-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="17e62-147">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="17e62-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="17e62-148">`[TargetSubscriptionId <String>]`：目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="17e62-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="17e62-149">`[Tenant <String>]`：目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="17e62-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="17e62-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="17e62-150">RELATED LINKS</span></span>

