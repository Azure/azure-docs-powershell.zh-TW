---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443576"
---
# <span data-ttu-id="02dd4-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="02dd4-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="02dd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="02dd4-103">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="02dd4-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="02dd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="02dd4-104">SYNTAX</span></span>

### <span data-ttu-id="02dd4-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="02dd4-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02dd4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="02dd4-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02dd4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="02dd4-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02dd4-108">說明</span><span class="sxs-lookup"><span data-stu-id="02dd4-108">DESCRIPTION</span></span>
<span data-ttu-id="02dd4-109">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="02dd4-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="02dd4-110">示例</span><span class="sxs-lookup"><span data-stu-id="02dd4-110">EXAMPLES</span></span>

### <span data-ttu-id="02dd4-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="02dd4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="02dd4-112">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="02dd4-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="02dd4-113">參數</span><span class="sxs-lookup"><span data-stu-id="02dd4-113">PARAMETERS</span></span>

### <span data-ttu-id="02dd4-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02dd4-114">-DisplayName</span></span>
<span data-ttu-id="02dd4-115">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="02dd4-115">Subscription name.</span></span>

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

### <span data-ttu-id="02dd4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02dd4-116">-InputObject</span></span>
<span data-ttu-id="02dd4-117">Posbbily 由 AzsNetworkQuota 傳回的已修改網路配額。</span><span class="sxs-lookup"><span data-stu-id="02dd4-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="02dd4-118">-位置</span><span class="sxs-lookup"><span data-stu-id="02dd4-118">-Location</span></span>
<span data-ttu-id="02dd4-119">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="02dd4-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="02dd4-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="02dd4-120">-OfferId</span></span>
<span data-ttu-id="02dd4-121">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="02dd4-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="02dd4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02dd4-122">-ResourceId</span></span>
<span data-ttu-id="02dd4-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="02dd4-123">The resource ID.</span></span>

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

### <span data-ttu-id="02dd4-124">-State</span><span class="sxs-lookup"><span data-stu-id="02dd4-124">-State</span></span>
<span data-ttu-id="02dd4-125">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="02dd4-125">Subscription state.</span></span>

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

### <span data-ttu-id="02dd4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02dd4-126">-SubscriptionId</span></span>
<span data-ttu-id="02dd4-127">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="02dd4-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="02dd4-128">-標記</span><span class="sxs-lookup"><span data-stu-id="02dd4-128">-Tags</span></span>
<span data-ttu-id="02dd4-129">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="02dd4-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="02dd4-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="02dd4-130">-TenantId</span></span>
<span data-ttu-id="02dd4-131">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="02dd4-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="02dd4-132">-類型</span><span class="sxs-lookup"><span data-stu-id="02dd4-132">-Type</span></span>
<span data-ttu-id="02dd4-133">資源類型。</span><span class="sxs-lookup"><span data-stu-id="02dd4-133">Type of resource.</span></span>

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

### <span data-ttu-id="02dd4-134">-確認</span><span class="sxs-lookup"><span data-stu-id="02dd4-134">-Confirm</span></span>
<span data-ttu-id="02dd4-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02dd4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02dd4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02dd4-136">-WhatIf</span></span>
<span data-ttu-id="02dd4-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02dd4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dd4-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02dd4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02dd4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dd4-139">CommonParameters</span></span>
<span data-ttu-id="02dd4-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02dd4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dd4-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02dd4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dd4-142">輸入</span><span class="sxs-lookup"><span data-stu-id="02dd4-142">INPUTS</span></span>

## <span data-ttu-id="02dd4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="02dd4-143">OUTPUTS</span></span>

### <span data-ttu-id="02dd4-144">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="02dd4-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="02dd4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="02dd4-145">NOTES</span></span>

## <span data-ttu-id="02dd4-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="02dd4-146">RELATED LINKS</span></span>
