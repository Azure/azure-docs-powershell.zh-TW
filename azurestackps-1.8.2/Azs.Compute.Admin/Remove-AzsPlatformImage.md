---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968229"
---
# <span data-ttu-id="cc30d-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="cc30d-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="cc30d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc30d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc30d-103">從平臺影像儲存庫刪除虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="cc30d-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="cc30d-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc30d-104">SYNTAX</span></span>

### <span data-ttu-id="cc30d-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="cc30d-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc30d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc30d-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc30d-107">說明</span><span class="sxs-lookup"><span data-stu-id="cc30d-107">DESCRIPTION</span></span>
<span data-ttu-id="cc30d-108">刪除平臺影像</span><span class="sxs-lookup"><span data-stu-id="cc30d-108">Delete a platform image</span></span>

## <span data-ttu-id="cc30d-109">示例</span><span class="sxs-lookup"><span data-stu-id="cc30d-109">EXAMPLES</span></span>

### <span data-ttu-id="cc30d-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cc30d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="cc30d-111">刪除現有的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="cc30d-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="cc30d-112">參數</span><span class="sxs-lookup"><span data-stu-id="cc30d-112">PARAMETERS</span></span>

### <span data-ttu-id="cc30d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cc30d-113">-Force</span></span>
<span data-ttu-id="cc30d-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cc30d-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cc30d-115">-位置</span><span class="sxs-lookup"><span data-stu-id="cc30d-115">-Location</span></span>
<span data-ttu-id="cc30d-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cc30d-116">Location of the resource.</span></span>

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

### <span data-ttu-id="cc30d-117">-優惠</span><span class="sxs-lookup"><span data-stu-id="cc30d-117">-Offer</span></span>
<span data-ttu-id="cc30d-118">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc30d-118">Name of the offer.</span></span>

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

### <span data-ttu-id="cc30d-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cc30d-119">-Publisher</span></span>
<span data-ttu-id="cc30d-120">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc30d-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="cc30d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc30d-121">-ResourceId</span></span>
<span data-ttu-id="cc30d-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cc30d-122">The resource id.</span></span>

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

### <span data-ttu-id="cc30d-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="cc30d-123">-Sku</span></span>
<span data-ttu-id="cc30d-124">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc30d-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="cc30d-125">-版本</span><span class="sxs-lookup"><span data-stu-id="cc30d-125">-Version</span></span>
<span data-ttu-id="cc30d-126">虛擬機器影像的版本。</span><span class="sxs-lookup"><span data-stu-id="cc30d-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="cc30d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="cc30d-127">-Confirm</span></span>
<span data-ttu-id="cc30d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc30d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc30d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc30d-129">-WhatIf</span></span>
<span data-ttu-id="cc30d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc30d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc30d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc30d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc30d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc30d-132">CommonParameters</span></span>
<span data-ttu-id="cc30d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc30d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc30d-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc30d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc30d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cc30d-135">INPUTS</span></span>

## <span data-ttu-id="cc30d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cc30d-136">OUTPUTS</span></span>

## <span data-ttu-id="cc30d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="cc30d-137">NOTES</span></span>

## <span data-ttu-id="cc30d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc30d-138">RELATED LINKS</span></span>

