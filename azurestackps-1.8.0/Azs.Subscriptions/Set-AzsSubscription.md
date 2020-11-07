---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793443"
---
# <span data-ttu-id="00787-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="00787-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="00787-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00787-102">SYNOPSIS</span></span>
<span data-ttu-id="00787-103">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="00787-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="00787-104">句法</span><span class="sxs-lookup"><span data-stu-id="00787-104">SYNTAX</span></span>

### <span data-ttu-id="00787-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="00787-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00787-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="00787-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00787-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="00787-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00787-108">說明</span><span class="sxs-lookup"><span data-stu-id="00787-108">DESCRIPTION</span></span>
<span data-ttu-id="00787-109">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="00787-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="00787-110">示例</span><span class="sxs-lookup"><span data-stu-id="00787-110">EXAMPLES</span></span>

### <span data-ttu-id="00787-111">範例1</span><span class="sxs-lookup"><span data-stu-id="00787-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="00787-112">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="00787-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="00787-113">參數</span><span class="sxs-lookup"><span data-stu-id="00787-113">PARAMETERS</span></span>

### <span data-ttu-id="00787-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="00787-114">-OfferId</span></span>
<span data-ttu-id="00787-115">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="00787-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="00787-116">-類型</span><span class="sxs-lookup"><span data-stu-id="00787-116">-Type</span></span>
<span data-ttu-id="00787-117">資源類型。</span><span class="sxs-lookup"><span data-stu-id="00787-117">Type of resource.</span></span>

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

### <span data-ttu-id="00787-118">-標記</span><span class="sxs-lookup"><span data-stu-id="00787-118">-Tags</span></span>
<span data-ttu-id="00787-119">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="00787-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00787-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00787-120">-SubscriptionId</span></span>
<span data-ttu-id="00787-121">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="00787-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00787-122">-State</span><span class="sxs-lookup"><span data-stu-id="00787-122">-State</span></span>
<span data-ttu-id="00787-123">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="00787-123">Subscription state.</span></span>

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

### <span data-ttu-id="00787-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="00787-124">-TenantId</span></span>
<span data-ttu-id="00787-125">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="00787-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="00787-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00787-126">-DisplayName</span></span>
<span data-ttu-id="00787-127">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="00787-127">Subscription name.</span></span>

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

### <span data-ttu-id="00787-128">-位置</span><span class="sxs-lookup"><span data-stu-id="00787-128">-Location</span></span>
<span data-ttu-id="00787-129">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="00787-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="00787-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00787-130">-ResourceId</span></span>
<span data-ttu-id="00787-131">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="00787-131">The resource ID.</span></span>

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

### <span data-ttu-id="00787-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00787-132">-InputObject</span></span>
<span data-ttu-id="00787-133">Posbbily 由 AzsNetworkQuota 傳回的已修改網路配額。</span><span class="sxs-lookup"><span data-stu-id="00787-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00787-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00787-134">-WhatIf</span></span>
<span data-ttu-id="00787-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00787-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00787-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00787-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00787-137">-確認</span><span class="sxs-lookup"><span data-stu-id="00787-137">-Confirm</span></span>
<span data-ttu-id="00787-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00787-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00787-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00787-139">CommonParameters</span></span>
<span data-ttu-id="00787-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00787-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00787-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00787-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00787-142">輸入</span><span class="sxs-lookup"><span data-stu-id="00787-142">INPUTS</span></span>

## <span data-ttu-id="00787-143">輸出</span><span class="sxs-lookup"><span data-stu-id="00787-143">OUTPUTS</span></span>

### <span data-ttu-id="00787-144">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="00787-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="00787-145">筆記</span><span class="sxs-lookup"><span data-stu-id="00787-145">NOTES</span></span>

## <span data-ttu-id="00787-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="00787-146">RELATED LINKS</span></span>
