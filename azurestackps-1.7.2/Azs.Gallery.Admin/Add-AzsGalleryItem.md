---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793334"
---
# <span data-ttu-id="a0f1a-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="a0f1a-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="a0f1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f1a-103">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="a0f1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0f1a-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f1a-106">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="a0f1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f1a-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a0f1a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="a0f1a-109">建立新的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-109">Create a new gallery item.</span></span>

## <span data-ttu-id="a0f1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f1a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a0f1a-111">-Force</span></span>
<span data-ttu-id="a0f1a-112">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a0f1a-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="a0f1a-113">-GalleryItemUri</span></span>
<span data-ttu-id="a0f1a-114">畫廊專案 JSON 檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="a0f1a-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a0f1a-115">-Confirm</span></span>
<span data-ttu-id="a0f1a-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f1a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f1a-117">-WhatIf</span></span>
<span data-ttu-id="a0f1a-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f1a-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f1a-120">CommonParameters</span></span>
<span data-ttu-id="a0f1a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f1a-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f1a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a0f1a-123">INPUTS</span></span>

## <span data-ttu-id="a0f1a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a0f1a-124">OUTPUTS</span></span>

### <span data-ttu-id="a0f1a-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="a0f1a-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="a0f1a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a0f1a-126">NOTES</span></span>

## <span data-ttu-id="a0f1a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0f1a-127">RELATED LINKS</span></span>

