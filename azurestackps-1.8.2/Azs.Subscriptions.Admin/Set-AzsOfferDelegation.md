---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968516"
---
# <span data-ttu-id="74cea-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="74cea-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="74cea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74cea-102">SYNOPSIS</span></span>
<span data-ttu-id="74cea-103">更新 [提供委派]。</span><span class="sxs-lookup"><span data-stu-id="74cea-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="74cea-104">句法</span><span class="sxs-lookup"><span data-stu-id="74cea-104">SYNTAX</span></span>

### <span data-ttu-id="74cea-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="74cea-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74cea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="74cea-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74cea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="74cea-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74cea-108">說明</span><span class="sxs-lookup"><span data-stu-id="74cea-108">DESCRIPTION</span></span>
<span data-ttu-id="74cea-109">更新 [提供委派]。</span><span class="sxs-lookup"><span data-stu-id="74cea-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="74cea-110">示例</span><span class="sxs-lookup"><span data-stu-id="74cea-110">EXAMPLES</span></span>

### <span data-ttu-id="74cea-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="74cea-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="74cea-112">更新 [提供委派]。</span><span class="sxs-lookup"><span data-stu-id="74cea-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="74cea-113">參數</span><span class="sxs-lookup"><span data-stu-id="74cea-113">PARAMETERS</span></span>

### <span data-ttu-id="74cea-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74cea-114">-InputObject</span></span>
<span data-ttu-id="74cea-115">OfferDelegation 的輸入物件。 AzureStack 類型的 []。</span><span class="sxs-lookup"><span data-stu-id="74cea-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-116">-位置</span><span class="sxs-lookup"><span data-stu-id="74cea-116">-Location</span></span>
<span data-ttu-id="74cea-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="74cea-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="74cea-118">-Name</span></span>
<span data-ttu-id="74cea-119">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="74cea-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="74cea-120">-OfferName</span></span>
<span data-ttu-id="74cea-121">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="74cea-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cea-122">-ResourceGroupName</span></span>
<span data-ttu-id="74cea-123">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="74cea-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74cea-124">-ResourceId</span></span>
<span data-ttu-id="74cea-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="74cea-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74cea-126">-SubscriptionId</span></span>
<span data-ttu-id="74cea-127">接收委派優惠之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="74cea-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74cea-128">-確認</span><span class="sxs-lookup"><span data-stu-id="74cea-128">-Confirm</span></span>
<span data-ttu-id="74cea-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74cea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74cea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74cea-130">-WhatIf</span></span>
<span data-ttu-id="74cea-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74cea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74cea-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74cea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74cea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cea-133">CommonParameters</span></span>
<span data-ttu-id="74cea-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74cea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cea-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74cea-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cea-136">輸入</span><span class="sxs-lookup"><span data-stu-id="74cea-136">INPUTS</span></span>

## <span data-ttu-id="74cea-137">輸出</span><span class="sxs-lookup"><span data-stu-id="74cea-137">OUTPUTS</span></span>

### <span data-ttu-id="74cea-138">AzureStack OfferDelegation 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="74cea-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="74cea-139">筆記</span><span class="sxs-lookup"><span data-stu-id="74cea-139">NOTES</span></span>

## <span data-ttu-id="74cea-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="74cea-140">RELATED LINKS</span></span>

