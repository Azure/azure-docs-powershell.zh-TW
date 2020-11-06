---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623203"
---
# <span data-ttu-id="b843c-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b843c-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="b843c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b843c-102">SYNOPSIS</span></span>
<span data-ttu-id="b843c-103">刪除特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="b843c-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b843c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b843c-104">SYNTAX</span></span>

### <span data-ttu-id="b843c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b843c-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b843c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b843c-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b843c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b843c-107">DESCRIPTION</span></span>
<span data-ttu-id="b843c-108">刪除特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="b843c-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b843c-109">示例</span><span class="sxs-lookup"><span data-stu-id="b843c-109">EXAMPLES</span></span>

### <span data-ttu-id="b843c-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b843c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="b843c-111">刪除圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="b843c-111">Delete a gallery item.</span></span>

## <span data-ttu-id="b843c-112">參數</span><span class="sxs-lookup"><span data-stu-id="b843c-112">PARAMETERS</span></span>

### <span data-ttu-id="b843c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b843c-113">-Force</span></span>
<span data-ttu-id="b843c-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b843c-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b843c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b843c-115">-Name</span></span>
<span data-ttu-id="b843c-116">圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b843c-116">Identity of the gallery item.</span></span>
<span data-ttu-id="b843c-117">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="b843c-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b843c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b843c-118">-ResourceId</span></span>
<span data-ttu-id="b843c-119">完全合格的 Azure 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="b843c-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="b843c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b843c-120">-Confirm</span></span>
<span data-ttu-id="b843c-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b843c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b843c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b843c-122">-WhatIf</span></span>
<span data-ttu-id="b843c-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b843c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b843c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b843c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b843c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b843c-125">CommonParameters</span></span>
<span data-ttu-id="b843c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b843c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b843c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b843c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b843c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b843c-128">INPUTS</span></span>

## <span data-ttu-id="b843c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b843c-129">OUTPUTS</span></span>

## <span data-ttu-id="b843c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b843c-130">NOTES</span></span>

## <span data-ttu-id="b843c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b843c-131">RELATED LINKS</span></span>

