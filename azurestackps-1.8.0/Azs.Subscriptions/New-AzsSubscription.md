---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793444"
---
# <span data-ttu-id="9a6d3-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9a6d3-101">New-AzsSubscription</span></span>

## <span data-ttu-id="9a6d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6d3-103">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-103">Create a subscription.</span></span>

## <span data-ttu-id="9a6d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a6d3-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a6d3-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a6d3-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6d3-106">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-106">Create a subscription.</span></span>

## <span data-ttu-id="9a6d3-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a6d3-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6d3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9a6d3-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="9a6d3-109">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-109">Create a subscription.</span></span>

## <span data-ttu-id="9a6d3-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a6d3-110">PARAMETERS</span></span>

### <span data-ttu-id="9a6d3-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9a6d3-111">-OfferId</span></span>
<span data-ttu-id="9a6d3-112">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="9a6d3-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a6d3-113">-DisplayName</span></span>
<span data-ttu-id="9a6d3-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-114">Subscription name.</span></span>

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

### <span data-ttu-id="9a6d3-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9a6d3-115">-TenantId</span></span>
<span data-ttu-id="9a6d3-116">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="9a6d3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a6d3-117">-SubscriptionId</span></span>
<span data-ttu-id="9a6d3-118">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="9a6d3-119">-State</span><span class="sxs-lookup"><span data-stu-id="9a6d3-119">-State</span></span>
<span data-ttu-id="9a6d3-120">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-120">Subscription state.</span></span>

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

### <span data-ttu-id="9a6d3-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9a6d3-121">-Location</span></span>
<span data-ttu-id="9a6d3-122">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="9a6d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6d3-123">-WhatIf</span></span>
<span data-ttu-id="9a6d3-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6d3-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a6d3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9a6d3-126">-Confirm</span></span>
<span data-ttu-id="9a6d3-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a6d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6d3-128">CommonParameters</span></span>
<span data-ttu-id="9a6d3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6d3-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6d3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9a6d3-131">INPUTS</span></span>

## <span data-ttu-id="9a6d3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9a6d3-132">OUTPUTS</span></span>

### <span data-ttu-id="9a6d3-133">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="9a6d3-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="9a6d3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9a6d3-134">NOTES</span></span>

## <span data-ttu-id="9a6d3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a6d3-135">RELATED LINKS</span></span>
