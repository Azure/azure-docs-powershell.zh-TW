---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966696"
---
# <span data-ttu-id="738bb-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="738bb-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="738bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="738bb-102">SYNOPSIS</span></span>
<span data-ttu-id="738bb-103">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="738bb-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="738bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="738bb-104">SYNTAX</span></span>

### <span data-ttu-id="738bb-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="738bb-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="738bb-106">時更新</span><span class="sxs-lookup"><span data-stu-id="738bb-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="738bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="738bb-107">DESCRIPTION</span></span>
<span data-ttu-id="738bb-108">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="738bb-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="738bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="738bb-109">EXAMPLES</span></span>

### <span data-ttu-id="738bb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="738bb-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="738bb-111">更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="738bb-111">Updates a subscription.</span></span>

## <span data-ttu-id="738bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="738bb-112">PARAMETERS</span></span>

### <span data-ttu-id="738bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738bb-113">-DefaultProfile</span></span>
<span data-ttu-id="738bb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="738bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="738bb-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="738bb-115">-DisplayName</span></span>
<span data-ttu-id="738bb-116">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="738bb-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="738bb-117">-Id</span></span>
<span data-ttu-id="738bb-118">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="738bb-119">-OfferId</span></span>
<span data-ttu-id="738bb-120">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-121">-State</span><span class="sxs-lookup"><span data-stu-id="738bb-121">-State</span></span>
<span data-ttu-id="738bb-122">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="738bb-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="738bb-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="738bb-124">支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="738bb-124">List of supported operations.</span></span>
<span data-ttu-id="738bb-125">若要建立，請參閱 SUBSCRIPTIONDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="738bb-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="738bb-126">-SubscriptionId</span></span>
<span data-ttu-id="738bb-127">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="738bb-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="738bb-128">-TenantId</span></span>
<span data-ttu-id="738bb-129">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="738bb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="738bb-130">-Confirm</span></span>
<span data-ttu-id="738bb-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="738bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="738bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="738bb-132">-WhatIf</span></span>
<span data-ttu-id="738bb-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="738bb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="738bb-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="738bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738bb-135">CommonParameters</span></span>
<span data-ttu-id="738bb-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="738bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738bb-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="738bb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738bb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="738bb-138">INPUTS</span></span>

### <span data-ttu-id="738bb-139">ISubscription 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="738bb-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="738bb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="738bb-140">OUTPUTS</span></span>

### <span data-ttu-id="738bb-141">ISubscription 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="738bb-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="738bb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="738bb-142">NOTES</span></span>

<span data-ttu-id="738bb-143">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="738bb-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="738bb-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="738bb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="738bb-145">SUBSCRIPTIONDEFINITION <ISubscription> ：支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="738bb-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="738bb-146">`[DisplayName <String>]`：訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="738bb-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="738bb-147">`[Id <String>]`：完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="738bb-148">`[OfferId <String>]`：受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="738bb-149">`[State <SubscriptionState?>]`：訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="738bb-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="738bb-150">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="738bb-151">`[TenantId <String>]`：目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="738bb-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="738bb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="738bb-152">RELATED LINKS</span></span>

