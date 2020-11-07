---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793882"
---
# <span data-ttu-id="c94bc-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c94bc-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="c94bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c94bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c94bc-103">刪除指定的計算配額。</span><span class="sxs-lookup"><span data-stu-id="c94bc-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="c94bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c94bc-104">SYNTAX</span></span>

### <span data-ttu-id="c94bc-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c94bc-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c94bc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c94bc-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c94bc-107">說明</span><span class="sxs-lookup"><span data-stu-id="c94bc-107">DESCRIPTION</span></span>
<span data-ttu-id="c94bc-108">刪除現有的配額。</span><span class="sxs-lookup"><span data-stu-id="c94bc-108">Delete an existing quota.</span></span>

## <span data-ttu-id="c94bc-109">示例</span><span class="sxs-lookup"><span data-stu-id="c94bc-109">EXAMPLES</span></span>

### <span data-ttu-id="c94bc-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c94bc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="c94bc-111">移除指定所有參數的計算配額。</span><span class="sxs-lookup"><span data-stu-id="c94bc-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="c94bc-112">參數</span><span class="sxs-lookup"><span data-stu-id="c94bc-112">PARAMETERS</span></span>

### <span data-ttu-id="c94bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c94bc-113">-Force</span></span>
<span data-ttu-id="c94bc-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="c94bc-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c94bc-115">-位置</span><span class="sxs-lookup"><span data-stu-id="c94bc-115">-Location</span></span>
<span data-ttu-id="c94bc-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c94bc-116">Location of the resource.</span></span> <span data-ttu-id="c94bc-117">如果未指定，我們會預設為系結至 tenat 訂閱的位置。</span><span class="sxs-lookup"><span data-stu-id="c94bc-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94bc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c94bc-118">-Name</span></span>
<span data-ttu-id="c94bc-119">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94bc-119">Name of the quota.</span></span>

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

### <span data-ttu-id="c94bc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c94bc-120">-ResourceId</span></span>
<span data-ttu-id="c94bc-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c94bc-121">The resource id.</span></span>

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

### <span data-ttu-id="c94bc-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c94bc-122">-Confirm</span></span>
<span data-ttu-id="c94bc-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c94bc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c94bc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c94bc-124">-WhatIf</span></span>
<span data-ttu-id="c94bc-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c94bc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c94bc-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c94bc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c94bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94bc-127">CommonParameters</span></span>
<span data-ttu-id="c94bc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c94bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94bc-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c94bc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94bc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c94bc-130">INPUTS</span></span>

## <span data-ttu-id="c94bc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c94bc-131">OUTPUTS</span></span>

## <span data-ttu-id="c94bc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c94bc-132">NOTES</span></span>

## <span data-ttu-id="c94bc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c94bc-133">RELATED LINKS</span></span>

