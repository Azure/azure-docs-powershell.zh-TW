---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968192"
---
# <span data-ttu-id="1e43d-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1e43d-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="1e43d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e43d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e43d-103">移除 [提供委派]</span><span class="sxs-lookup"><span data-stu-id="1e43d-103">Removes the offer delegation</span></span>

## <span data-ttu-id="1e43d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e43d-104">SYNTAX</span></span>

### <span data-ttu-id="1e43d-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="1e43d-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e43d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e43d-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e43d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e43d-107">DESCRIPTION</span></span>
<span data-ttu-id="1e43d-108">移除 [提供委派]</span><span class="sxs-lookup"><span data-stu-id="1e43d-108">Removes the offer delegation</span></span>

## <span data-ttu-id="1e43d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e43d-109">EXAMPLES</span></span>

### <span data-ttu-id="1e43d-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e43d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="1e43d-111">移除 [提供委派]</span><span class="sxs-lookup"><span data-stu-id="1e43d-111">Removes the offer delegation</span></span>

## <span data-ttu-id="1e43d-112">參數</span><span class="sxs-lookup"><span data-stu-id="1e43d-112">PARAMETERS</span></span>

### <span data-ttu-id="1e43d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e43d-113">-Force</span></span>
<span data-ttu-id="1e43d-114">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="1e43d-114">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e43d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e43d-115">-Name</span></span>
<span data-ttu-id="1e43d-116">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e43d-116">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e43d-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="1e43d-117">-OfferName</span></span>
<span data-ttu-id="1e43d-118">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e43d-118">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e43d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e43d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e43d-120">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1e43d-120">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e43d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e43d-121">-ResourceId</span></span>
<span data-ttu-id="1e43d-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1e43d-122">The resource id.</span></span>

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

### <span data-ttu-id="1e43d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1e43d-123">-Confirm</span></span>
<span data-ttu-id="1e43d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e43d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e43d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e43d-125">-WhatIf</span></span>
<span data-ttu-id="1e43d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e43d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e43d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e43d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e43d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e43d-128">CommonParameters</span></span>
<span data-ttu-id="1e43d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e43d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e43d-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e43d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e43d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1e43d-131">INPUTS</span></span>

## <span data-ttu-id="1e43d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1e43d-132">OUTPUTS</span></span>

## <span data-ttu-id="1e43d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1e43d-133">NOTES</span></span>

## <span data-ttu-id="1e43d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e43d-134">RELATED LINKS</span></span>

