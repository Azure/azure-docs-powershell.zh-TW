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
ms.locfileid: "93442796"
---
# <span data-ttu-id="4aae1-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="4aae1-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="4aae1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4aae1-102">SYNOPSIS</span></span>
<span data-ttu-id="4aae1-103">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="4aae1-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="4aae1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4aae1-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aae1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4aae1-105">DESCRIPTION</span></span>
<span data-ttu-id="4aae1-106">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="4aae1-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="4aae1-107">示例</span><span class="sxs-lookup"><span data-stu-id="4aae1-107">EXAMPLES</span></span>

### <span data-ttu-id="4aae1-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4aae1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="4aae1-109">建立新的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="4aae1-109">Create a new gallery item.</span></span>

## <span data-ttu-id="4aae1-110">參數</span><span class="sxs-lookup"><span data-stu-id="4aae1-110">PARAMETERS</span></span>

### <span data-ttu-id="4aae1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4aae1-111">-Force</span></span>
<span data-ttu-id="4aae1-112">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="4aae1-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4aae1-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="4aae1-113">-GalleryItemUri</span></span>
<span data-ttu-id="4aae1-114">畫廊專案 JSON 檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="4aae1-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="4aae1-115">-確認</span><span class="sxs-lookup"><span data-stu-id="4aae1-115">-Confirm</span></span>
<span data-ttu-id="4aae1-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4aae1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aae1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aae1-117">-WhatIf</span></span>
<span data-ttu-id="4aae1-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4aae1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aae1-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4aae1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aae1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aae1-120">CommonParameters</span></span>
<span data-ttu-id="4aae1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4aae1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aae1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4aae1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aae1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4aae1-123">INPUTS</span></span>

## <span data-ttu-id="4aae1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4aae1-124">OUTPUTS</span></span>

### <span data-ttu-id="4aae1-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="4aae1-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="4aae1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4aae1-126">NOTES</span></span>

## <span data-ttu-id="4aae1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4aae1-127">RELATED LINKS</span></span>
