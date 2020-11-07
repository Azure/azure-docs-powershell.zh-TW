---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793459"
---
# <span data-ttu-id="0cc2e-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="0cc2e-101">New-PlanObject</span></span>

## <span data-ttu-id="0cc2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc2e-103">方案代表提供承租人的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="0cc2e-104">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="0cc2e-105">句法</span><span class="sxs-lookup"><span data-stu-id="0cc2e-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="0cc2e-106">說明</span><span class="sxs-lookup"><span data-stu-id="0cc2e-106">DESCRIPTION</span></span>
<span data-ttu-id="0cc2e-107">方案代表提供承租人的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="0cc2e-108">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="0cc2e-109">示例</span><span class="sxs-lookup"><span data-stu-id="0cc2e-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc2e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0cc2e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0cc2e-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="0cc2e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="0cc2e-112">參數</span><span class="sxs-lookup"><span data-stu-id="0cc2e-112">PARAMETERS</span></span>

### <span data-ttu-id="0cc2e-113">-描述</span><span class="sxs-lookup"><span data-stu-id="0cc2e-113">-Description</span></span>
<span data-ttu-id="0cc2e-114">方案的描述。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0cc2e-115">-DisplayName</span></span>
<span data-ttu-id="0cc2e-116">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0cc2e-117">-ExternalReferenceId</span></span>
<span data-ttu-id="0cc2e-118">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-118">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0cc2e-119">-Id</span></span>
<span data-ttu-id="0cc2e-120">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-120">URI of the resource.</span></span>

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

### <span data-ttu-id="0cc2e-121">-位置</span><span class="sxs-lookup"><span data-stu-id="0cc2e-121">-Location</span></span>
<span data-ttu-id="0cc2e-122">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0cc2e-123">-Name</span></span>
<span data-ttu-id="0cc2e-124">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-124">Name of the resource.</span></span>

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

### <span data-ttu-id="0cc2e-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="0cc2e-125">-QuotaIds</span></span>
<span data-ttu-id="0cc2e-126">方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="0cc2e-127">-SkuIds</span></span>
<span data-ttu-id="0cc2e-128">SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="0cc2e-129">-SubscriptionCount</span></span>
<span data-ttu-id="0cc2e-130">[訂閱計數]。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-131">-標記</span><span class="sxs-lookup"><span data-stu-id="0cc2e-131">-Tags</span></span>
<span data-ttu-id="0cc2e-132">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc2e-133">-類型</span><span class="sxs-lookup"><span data-stu-id="0cc2e-133">-Type</span></span>
<span data-ttu-id="0cc2e-134">資源類型。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-134">Type of resource.</span></span>

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

### <span data-ttu-id="0cc2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc2e-135">CommonParameters</span></span>
<span data-ttu-id="0cc2e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc2e-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0cc2e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc2e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0cc2e-138">INPUTS</span></span>

## <span data-ttu-id="0cc2e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0cc2e-139">OUTPUTS</span></span>

## <span data-ttu-id="0cc2e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="0cc2e-140">NOTES</span></span>

## <span data-ttu-id="0cc2e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cc2e-141">RELATED LINKS</span></span>

