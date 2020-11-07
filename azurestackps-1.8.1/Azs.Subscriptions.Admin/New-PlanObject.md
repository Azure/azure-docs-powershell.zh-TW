---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793784"
---
# <span data-ttu-id="82fb4-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="82fb4-101">New-PlanObject</span></span>

## <span data-ttu-id="82fb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="82fb4-103">方案代表提供承租人的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="82fb4-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="82fb4-104">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="82fb4-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="82fb4-105">句法</span><span class="sxs-lookup"><span data-stu-id="82fb4-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="82fb4-106">說明</span><span class="sxs-lookup"><span data-stu-id="82fb4-106">DESCRIPTION</span></span>
<span data-ttu-id="82fb4-107">方案代表提供承租人的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="82fb4-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="82fb4-108">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="82fb4-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="82fb4-109">示例</span><span class="sxs-lookup"><span data-stu-id="82fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="82fb4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="82fb4-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="82fb4-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="82fb4-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="82fb4-112">參數</span><span class="sxs-lookup"><span data-stu-id="82fb4-112">PARAMETERS</span></span>

### <span data-ttu-id="82fb4-113">-描述</span><span class="sxs-lookup"><span data-stu-id="82fb4-113">-Description</span></span>
<span data-ttu-id="82fb4-114">方案的描述。</span><span class="sxs-lookup"><span data-stu-id="82fb4-114">Description of the plan.</span></span>

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

### <span data-ttu-id="82fb4-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="82fb4-115">-DisplayName</span></span>
<span data-ttu-id="82fb4-116">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="82fb4-116">Display name.</span></span>

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

### <span data-ttu-id="82fb4-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="82fb4-117">-ExternalReferenceId</span></span>
<span data-ttu-id="82fb4-118">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="82fb4-118">External reference identifier.</span></span>

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

### <span data-ttu-id="82fb4-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="82fb4-119">-Id</span></span>
<span data-ttu-id="82fb4-120">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="82fb4-120">URI of the resource.</span></span>

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

### <span data-ttu-id="82fb4-121">-位置</span><span class="sxs-lookup"><span data-stu-id="82fb4-121">-Location</span></span>
<span data-ttu-id="82fb4-122">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="82fb4-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="82fb4-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="82fb4-123">-Name</span></span>
<span data-ttu-id="82fb4-124">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="82fb4-124">Name of the resource.</span></span>

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

### <span data-ttu-id="82fb4-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="82fb4-125">-QuotaIds</span></span>
<span data-ttu-id="82fb4-126">方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="82fb4-126">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="82fb4-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="82fb4-127">-SkuIds</span></span>
<span data-ttu-id="82fb4-128">SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="82fb4-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="82fb4-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="82fb4-129">-SubscriptionCount</span></span>
<span data-ttu-id="82fb4-130">[訂閱計數]。</span><span class="sxs-lookup"><span data-stu-id="82fb4-130">Subscription count.</span></span>

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

### <span data-ttu-id="82fb4-131">-標記</span><span class="sxs-lookup"><span data-stu-id="82fb4-131">-Tags</span></span>
<span data-ttu-id="82fb4-132">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="82fb4-132">List of key-value pairs.</span></span>

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

### <span data-ttu-id="82fb4-133">-類型</span><span class="sxs-lookup"><span data-stu-id="82fb4-133">-Type</span></span>
<span data-ttu-id="82fb4-134">資源類型。</span><span class="sxs-lookup"><span data-stu-id="82fb4-134">Type of resource.</span></span>

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

### <span data-ttu-id="82fb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fb4-135">CommonParameters</span></span>
<span data-ttu-id="82fb4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82fb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fb4-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82fb4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fb4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="82fb4-138">INPUTS</span></span>

## <span data-ttu-id="82fb4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="82fb4-139">OUTPUTS</span></span>

## <span data-ttu-id="82fb4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="82fb4-140">NOTES</span></span>

## <span data-ttu-id="82fb4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="82fb4-141">RELATED LINKS</span></span>

