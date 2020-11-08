---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968582"
---
# <span data-ttu-id="087e5-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="087e5-101">New-AzsPlan</span></span>

## <span data-ttu-id="087e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="087e5-102">SYNOPSIS</span></span>
<span data-ttu-id="087e5-103">建立新方案</span><span class="sxs-lookup"><span data-stu-id="087e5-103">Creates a new plan</span></span>

## <span data-ttu-id="087e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="087e5-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="087e5-105">DESCRIPTION</span></span>
<span data-ttu-id="087e5-106">建立新方案</span><span class="sxs-lookup"><span data-stu-id="087e5-106">Creates a new plan</span></span>

## <span data-ttu-id="087e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="087e5-107">EXAMPLES</span></span>

### <span data-ttu-id="087e5-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="087e5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="087e5-109">建立新方案</span><span class="sxs-lookup"><span data-stu-id="087e5-109">Creates a new plan</span></span>

## <span data-ttu-id="087e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="087e5-110">PARAMETERS</span></span>

### <span data-ttu-id="087e5-111">-描述</span><span class="sxs-lookup"><span data-stu-id="087e5-111">-Description</span></span>
<span data-ttu-id="087e5-112">方案的描述。</span><span class="sxs-lookup"><span data-stu-id="087e5-112">Description of the plan.</span></span>

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

### <span data-ttu-id="087e5-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="087e5-113">-DisplayName</span></span>
<span data-ttu-id="087e5-114">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="087e5-114">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087e5-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="087e5-115">-ExternalReferenceId</span></span>
<span data-ttu-id="087e5-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="087e5-116">External reference identifier.</span></span>

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

### <span data-ttu-id="087e5-117">-位置</span><span class="sxs-lookup"><span data-stu-id="087e5-117">-Location</span></span>
<span data-ttu-id="087e5-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="087e5-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087e5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="087e5-119">-Name</span></span>
<span data-ttu-id="087e5-120">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="087e5-120">Name of the plan.</span></span>

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

### <span data-ttu-id="087e5-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="087e5-121">-QuotaIds</span></span>
<span data-ttu-id="087e5-122">方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="087e5-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="087e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="087e5-124">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="087e5-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="087e5-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="087e5-125">-SkuIds</span></span>
<span data-ttu-id="087e5-126">SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="087e5-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087e5-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="087e5-127">-SubscriptionCount</span></span>
<span data-ttu-id="087e5-128">[訂閱計數]。</span><span class="sxs-lookup"><span data-stu-id="087e5-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087e5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="087e5-129">-Confirm</span></span>
<span data-ttu-id="087e5-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="087e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="087e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087e5-131">-WhatIf</span></span>
<span data-ttu-id="087e5-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="087e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="087e5-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="087e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="087e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087e5-134">CommonParameters</span></span>
<span data-ttu-id="087e5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="087e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087e5-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="087e5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087e5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="087e5-137">INPUTS</span></span>

## <span data-ttu-id="087e5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="087e5-138">OUTPUTS</span></span>

### <span data-ttu-id="087e5-139">AzureStack. 管理模型. 規劃</span><span class="sxs-lookup"><span data-stu-id="087e5-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="087e5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="087e5-140">NOTES</span></span>

## <span data-ttu-id="087e5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="087e5-141">RELATED LINKS</span></span>
