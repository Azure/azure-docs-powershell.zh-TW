---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442519"
---
# <span data-ttu-id="7d900-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="7d900-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="7d900-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d900-102">SYNOPSIS</span></span>
<span data-ttu-id="7d900-103">建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d900-103">Create a new subscription.</span></span>

## <span data-ttu-id="7d900-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d900-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d900-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d900-105">DESCRIPTION</span></span>
<span data-ttu-id="7d900-106">建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d900-106">Create a new subscription.</span></span>

## <span data-ttu-id="7d900-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d900-107">EXAMPLES</span></span>

### <span data-ttu-id="7d900-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d900-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="7d900-109">建立新的使用者訂閱</span><span class="sxs-lookup"><span data-stu-id="7d900-109">Creates a new user subscription</span></span>

## <span data-ttu-id="7d900-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d900-110">PARAMETERS</span></span>

### <span data-ttu-id="7d900-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d900-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="7d900-112">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d900-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d900-113">-DisplayName</span></span>
<span data-ttu-id="7d900-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="7d900-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="7d900-115">-ExternalReferenceId</span></span>
<span data-ttu-id="7d900-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d900-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="7d900-117">-OfferId</span></span>
<span data-ttu-id="7d900-118">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d900-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-119">-擁有者</span><span class="sxs-lookup"><span data-stu-id="7d900-119">-Owner</span></span>
<span data-ttu-id="7d900-120">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="7d900-120">Subscription owner.</span></span>

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

### <span data-ttu-id="7d900-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="7d900-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="7d900-122">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="7d900-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-123">-State</span><span class="sxs-lookup"><span data-stu-id="7d900-123">-State</span></span>
<span data-ttu-id="7d900-124">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="7d900-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d900-125">-SubscriptionId</span></span>
<span data-ttu-id="7d900-126">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7d900-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d900-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7d900-127">-TenantId</span></span>
<span data-ttu-id="7d900-128">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d900-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="7d900-129">-確認</span><span class="sxs-lookup"><span data-stu-id="7d900-129">-Confirm</span></span>
<span data-ttu-id="7d900-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d900-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d900-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d900-131">-WhatIf</span></span>
<span data-ttu-id="7d900-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d900-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d900-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d900-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d900-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d900-134">CommonParameters</span></span>
<span data-ttu-id="7d900-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d900-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d900-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d900-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d900-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7d900-137">INPUTS</span></span>

## <span data-ttu-id="7d900-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7d900-138">OUTPUTS</span></span>

### <span data-ttu-id="7d900-139">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="7d900-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="7d900-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7d900-140">NOTES</span></span>

## <span data-ttu-id="7d900-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d900-141">RELATED LINKS</span></span>

