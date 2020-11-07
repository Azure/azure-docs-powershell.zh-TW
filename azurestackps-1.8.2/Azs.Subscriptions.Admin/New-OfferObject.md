---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968140"
---
# <span data-ttu-id="8fc7f-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="8fc7f-101">New-OfferObject</span></span>

## <span data-ttu-id="8fc7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc7f-103">代表可建立訂閱的服務產品。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="8fc7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fc7f-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="8fc7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fc7f-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc7f-106">代表可建立訂閱的服務產品。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="8fc7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8fc7f-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc7f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8fc7f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8fc7f-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="8fc7f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8fc7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="8fc7f-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc7f-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="8fc7f-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="8fc7f-112">提供給附加元件方案的參考，租使用者也可以選擇作為優惠的一部分取得。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="8fc7f-113">-BasePlanIds</span></span>
<span data-ttu-id="8fc7f-114">當租使用者訂閱優惠時，會立即提供給租使用者的基本方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-115">-描述</span><span class="sxs-lookup"><span data-stu-id="8fc7f-115">-Description</span></span>
<span data-ttu-id="8fc7f-116">優惠說明。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-116">Description of offer.</span></span>

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

### <span data-ttu-id="8fc7f-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8fc7f-117">-DisplayName</span></span>
<span data-ttu-id="8fc7f-118">[優惠] 的 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-118">Display name of offer.</span></span>

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

### <span data-ttu-id="8fc7f-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8fc7f-119">-ExternalReferenceId</span></span>
<span data-ttu-id="8fc7f-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-120">External reference identifier.</span></span>

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

### <span data-ttu-id="8fc7f-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8fc7f-121">-Id</span></span>
<span data-ttu-id="8fc7f-122">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-123">-位置</span><span class="sxs-lookup"><span data-stu-id="8fc7f-123">-Location</span></span>
<span data-ttu-id="8fc7f-124">資源所在位置的位置。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="8fc7f-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="8fc7f-126">每個帳戶的最大訂閱數。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fc7f-127">-Name</span></span>
<span data-ttu-id="8fc7f-128">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-128">Name of the resource.</span></span>

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

### <span data-ttu-id="8fc7f-129">-State</span><span class="sxs-lookup"><span data-stu-id="8fc7f-129">-State</span></span>
<span data-ttu-id="8fc7f-130">提供協助工具狀態。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="8fc7f-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8fc7f-131">-SubscriptionCount</span></span>
<span data-ttu-id="8fc7f-132">目前的訂閱數。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-133">-標記</span><span class="sxs-lookup"><span data-stu-id="8fc7f-133">-Tags</span></span>
<span data-ttu-id="8fc7f-134">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc7f-135">-類型</span><span class="sxs-lookup"><span data-stu-id="8fc7f-135">-Type</span></span>
<span data-ttu-id="8fc7f-136">資源類型。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-136">Type of resource.</span></span>

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

### <span data-ttu-id="8fc7f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc7f-137">CommonParameters</span></span>
<span data-ttu-id="8fc7f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc7f-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fc7f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc7f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="8fc7f-140">INPUTS</span></span>

## <span data-ttu-id="8fc7f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8fc7f-141">OUTPUTS</span></span>

## <span data-ttu-id="8fc7f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8fc7f-142">NOTES</span></span>

## <span data-ttu-id="8fc7f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fc7f-143">RELATED LINKS</span></span>

