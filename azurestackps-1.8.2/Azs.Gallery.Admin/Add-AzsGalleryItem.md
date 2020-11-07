---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968323"
---
# <span data-ttu-id="58a9c-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="58a9c-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="58a9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="58a9c-103">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="58a9c-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="58a9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="58a9c-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a9c-105">說明</span><span class="sxs-lookup"><span data-stu-id="58a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="58a9c-106">將提供者圖庫專案上傳至儲存空間。</span><span class="sxs-lookup"><span data-stu-id="58a9c-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="58a9c-107">示例</span><span class="sxs-lookup"><span data-stu-id="58a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="58a9c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="58a9c-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="58a9c-109">建立新的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="58a9c-109">Create a new gallery item.</span></span>

## <span data-ttu-id="58a9c-110">參數</span><span class="sxs-lookup"><span data-stu-id="58a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="58a9c-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="58a9c-111">-GalleryItemUri</span></span>
<span data-ttu-id="58a9c-112">畫廊專案 JSON 檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="58a9c-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="58a9c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="58a9c-113">-Force</span></span>
<span data-ttu-id="58a9c-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="58a9c-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="58a9c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a9c-115">-WhatIf</span></span>
<span data-ttu-id="58a9c-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58a9c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a9c-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58a9c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a9c-118">-確認</span><span class="sxs-lookup"><span data-stu-id="58a9c-118">-Confirm</span></span>
<span data-ttu-id="58a9c-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58a9c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a9c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a9c-120">CommonParameters</span></span>
<span data-ttu-id="58a9c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58a9c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a9c-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58a9c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a9c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="58a9c-123">INPUTS</span></span>

## <span data-ttu-id="58a9c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="58a9c-124">OUTPUTS</span></span>

### <span data-ttu-id="58a9c-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="58a9c-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="58a9c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="58a9c-126">NOTES</span></span>

## <span data-ttu-id="58a9c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="58a9c-127">RELATED LINKS</span></span>
