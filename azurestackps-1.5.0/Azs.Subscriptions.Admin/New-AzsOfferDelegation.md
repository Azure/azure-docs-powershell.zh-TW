---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442680"
---
# <span data-ttu-id="6e8a6-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="6e8a6-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="6e8a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8a6-103">建立新的 [優惠委派]。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="6e8a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e8a6-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="6e8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8a6-106">建立新的 [優惠委派]。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="6e8a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="6e8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6e8a6-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6e8a6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="6e8a6-109">建立新的 [優惠委派]。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="6e8a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6e8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="6e8a6-111">-位置</span><span class="sxs-lookup"><span data-stu-id="6e8a6-111">-Location</span></span>
<span data-ttu-id="6e8a6-112">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-112">Location of the resource.</span></span>

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

### <span data-ttu-id="6e8a6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e8a6-113">-Name</span></span>
<span data-ttu-id="6e8a6-114">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="6e8a6-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6e8a6-115">-OfferName</span></span>
<span data-ttu-id="6e8a6-116">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-116">Name of an offer.</span></span>

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

### <span data-ttu-id="6e8a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e8a6-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8a6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e8a6-119">-SubscriptionId</span></span>
<span data-ttu-id="6e8a6-120">接收委派優惠之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="6e8a6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="6e8a6-121">-Confirm</span></span>
<span data-ttu-id="6e8a6-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8a6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8a6-123">-WhatIf</span></span>
<span data-ttu-id="6e8a6-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8a6-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8a6-126">CommonParameters</span></span>
<span data-ttu-id="6e8a6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8a6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8a6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6e8a6-129">INPUTS</span></span>

## <span data-ttu-id="6e8a6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6e8a6-130">OUTPUTS</span></span>

### <span data-ttu-id="6e8a6-131">AzureStack OfferDelegation 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e8a6-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="6e8a6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6e8a6-132">NOTES</span></span>

## <span data-ttu-id="6e8a6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e8a6-133">RELATED LINKS</span></span>

