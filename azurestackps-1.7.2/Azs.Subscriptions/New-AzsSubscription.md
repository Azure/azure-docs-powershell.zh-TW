---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793411"
---
# <span data-ttu-id="81449-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="81449-101">New-AzsSubscription</span></span>

## <span data-ttu-id="81449-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81449-102">SYNOPSIS</span></span>
<span data-ttu-id="81449-103">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="81449-103">Create a subscription.</span></span>

## <span data-ttu-id="81449-104">句法</span><span class="sxs-lookup"><span data-stu-id="81449-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81449-105">說明</span><span class="sxs-lookup"><span data-stu-id="81449-105">DESCRIPTION</span></span>
<span data-ttu-id="81449-106">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="81449-106">Create a subscription.</span></span>

## <span data-ttu-id="81449-107">示例</span><span class="sxs-lookup"><span data-stu-id="81449-107">EXAMPLES</span></span>

### <span data-ttu-id="81449-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81449-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="81449-109">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="81449-109">Create a subscription.</span></span>

## <span data-ttu-id="81449-110">參數</span><span class="sxs-lookup"><span data-stu-id="81449-110">PARAMETERS</span></span>

### <span data-ttu-id="81449-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81449-111">-DisplayName</span></span>
<span data-ttu-id="81449-112">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="81449-112">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-113">-位置</span><span class="sxs-lookup"><span data-stu-id="81449-113">-Location</span></span>
<span data-ttu-id="81449-114">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="81449-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="81449-115">-OfferId</span></span>
<span data-ttu-id="81449-116">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="81449-116">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-117">-State</span><span class="sxs-lookup"><span data-stu-id="81449-117">-State</span></span>
<span data-ttu-id="81449-118">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="81449-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81449-119">-SubscriptionId</span></span>
<span data-ttu-id="81449-120">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="81449-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="81449-121">-TenantId</span></span>
<span data-ttu-id="81449-122">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="81449-122">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81449-123">-確認</span><span class="sxs-lookup"><span data-stu-id="81449-123">-Confirm</span></span>
<span data-ttu-id="81449-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81449-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81449-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81449-125">-WhatIf</span></span>
<span data-ttu-id="81449-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81449-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81449-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81449-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81449-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81449-128">CommonParameters</span></span>
<span data-ttu-id="81449-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81449-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81449-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81449-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81449-131">輸入</span><span class="sxs-lookup"><span data-stu-id="81449-131">INPUTS</span></span>

## <span data-ttu-id="81449-132">輸出</span><span class="sxs-lookup"><span data-stu-id="81449-132">OUTPUTS</span></span>

### <span data-ttu-id="81449-133">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="81449-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="81449-134">筆記</span><span class="sxs-lookup"><span data-stu-id="81449-134">NOTES</span></span>

## <span data-ttu-id="81449-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="81449-135">RELATED LINKS</span></span>

