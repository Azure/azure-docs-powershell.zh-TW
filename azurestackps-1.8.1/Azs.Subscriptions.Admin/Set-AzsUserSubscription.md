---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793770"
---
# <span data-ttu-id="7d1e2-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="7d1e2-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="7d1e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1e2-103">更新指定的使用者訂閱</span><span class="sxs-lookup"><span data-stu-id="7d1e2-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="7d1e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d1e2-104">SYNTAX</span></span>

### <span data-ttu-id="7d1e2-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="7d1e2-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1e2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d1e2-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d1e2-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1e2-109">更新指定的使用者訂閱</span><span class="sxs-lookup"><span data-stu-id="7d1e2-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="7d1e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d1e2-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1e2-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d1e2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="7d1e2-112">更新訂閱</span><span class="sxs-lookup"><span data-stu-id="7d1e2-112">Updates a subscription</span></span>

## <span data-ttu-id="7d1e2-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d1e2-113">PARAMETERS</span></span>

### <span data-ttu-id="7d1e2-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="7d1e2-115">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d1e2-116">-DisplayName</span></span>
<span data-ttu-id="7d1e2-117">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-118">-ExternalReferenceId</span></span>
<span data-ttu-id="7d1e2-119">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d1e2-120">-InputObject</span></span>
<span data-ttu-id="7d1e2-121">AzureStack 類型的輸入物件，其為 [系統管理]。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-122">-位置</span><span class="sxs-lookup"><span data-stu-id="7d1e2-122">-Location</span></span>
<span data-ttu-id="7d1e2-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-124">-OfferId</span></span>
<span data-ttu-id="7d1e2-125">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-126">-擁有者</span><span class="sxs-lookup"><span data-stu-id="7d1e2-126">-Owner</span></span>
<span data-ttu-id="7d1e2-127">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-128">-ResourceId</span></span>
<span data-ttu-id="7d1e2-129">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-129">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="7d1e2-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="7d1e2-131">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-132">-State</span><span class="sxs-lookup"><span data-stu-id="7d1e2-132">-State</span></span>
<span data-ttu-id="7d1e2-133">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-134">-SubscriptionId</span></span>
<span data-ttu-id="7d1e2-135">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7d1e2-136">-TenantId</span></span>
<span data-ttu-id="7d1e2-137">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-138">-確認</span><span class="sxs-lookup"><span data-stu-id="7d1e2-138">-Confirm</span></span>
<span data-ttu-id="7d1e2-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1e2-140">-WhatIf</span></span>
<span data-ttu-id="7d1e2-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1e2-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1e2-143">CommonParameters</span></span>
<span data-ttu-id="7d1e2-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1e2-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d1e2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1e2-146">輸入</span><span class="sxs-lookup"><span data-stu-id="7d1e2-146">INPUTS</span></span>

## <span data-ttu-id="7d1e2-147">輸出</span><span class="sxs-lookup"><span data-stu-id="7d1e2-147">OUTPUTS</span></span>

### <span data-ttu-id="7d1e2-148">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="7d1e2-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="7d1e2-149">筆記</span><span class="sxs-lookup"><span data-stu-id="7d1e2-149">NOTES</span></span>

## <span data-ttu-id="7d1e2-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d1e2-150">RELATED LINKS</span></span>

