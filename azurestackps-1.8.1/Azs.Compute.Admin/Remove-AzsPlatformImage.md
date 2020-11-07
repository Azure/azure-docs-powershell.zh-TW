---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793879"
---
# <span data-ttu-id="ece91-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ece91-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="ece91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ece91-102">SYNOPSIS</span></span>
<span data-ttu-id="ece91-103">從平臺影像儲存庫刪除虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="ece91-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="ece91-104">句法</span><span class="sxs-lookup"><span data-stu-id="ece91-104">SYNTAX</span></span>

### <span data-ttu-id="ece91-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ece91-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece91-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece91-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece91-107">說明</span><span class="sxs-lookup"><span data-stu-id="ece91-107">DESCRIPTION</span></span>
<span data-ttu-id="ece91-108">刪除平臺影像</span><span class="sxs-lookup"><span data-stu-id="ece91-108">Delete a platform image</span></span>

## <span data-ttu-id="ece91-109">示例</span><span class="sxs-lookup"><span data-stu-id="ece91-109">EXAMPLES</span></span>

### <span data-ttu-id="ece91-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ece91-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="ece91-111">刪除現有的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="ece91-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="ece91-112">參數</span><span class="sxs-lookup"><span data-stu-id="ece91-112">PARAMETERS</span></span>

### <span data-ttu-id="ece91-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ece91-113">-Force</span></span>
<span data-ttu-id="ece91-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ece91-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ece91-115">-位置</span><span class="sxs-lookup"><span data-stu-id="ece91-115">-Location</span></span>
<span data-ttu-id="ece91-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ece91-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ece91-117">-優惠</span><span class="sxs-lookup"><span data-stu-id="ece91-117">-Offer</span></span>
<span data-ttu-id="ece91-118">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="ece91-118">Name of the offer.</span></span>

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

### <span data-ttu-id="ece91-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ece91-119">-Publisher</span></span>
<span data-ttu-id="ece91-120">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="ece91-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="ece91-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece91-121">-ResourceId</span></span>
<span data-ttu-id="ece91-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ece91-122">The resource id.</span></span>

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

### <span data-ttu-id="ece91-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="ece91-123">-Sku</span></span>
<span data-ttu-id="ece91-124">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ece91-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="ece91-125">-版本</span><span class="sxs-lookup"><span data-stu-id="ece91-125">-Version</span></span>
<span data-ttu-id="ece91-126">虛擬機器影像的版本。</span><span class="sxs-lookup"><span data-stu-id="ece91-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="ece91-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ece91-127">-Confirm</span></span>
<span data-ttu-id="ece91-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ece91-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece91-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece91-129">-WhatIf</span></span>
<span data-ttu-id="ece91-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ece91-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece91-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece91-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece91-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece91-132">CommonParameters</span></span>
<span data-ttu-id="ece91-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ece91-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece91-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ece91-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece91-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ece91-135">INPUTS</span></span>

## <span data-ttu-id="ece91-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ece91-136">OUTPUTS</span></span>

## <span data-ttu-id="ece91-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ece91-137">NOTES</span></span>

## <span data-ttu-id="ece91-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ece91-138">RELATED LINKS</span></span>

