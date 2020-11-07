---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793333"
---
# <span data-ttu-id="2cf21-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2cf21-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="2cf21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cf21-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf21-103">列出圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="2cf21-103">Lists gallery items.</span></span>

## <span data-ttu-id="2cf21-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cf21-104">SYNTAX</span></span>

### <span data-ttu-id="2cf21-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2cf21-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="2cf21-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2cf21-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="2cf21-107">說明</span><span class="sxs-lookup"><span data-stu-id="2cf21-107">DESCRIPTION</span></span>
<span data-ttu-id="2cf21-108">取得 Azure 堆疊 Marketplace 中可用的圖庫專案清單</span><span class="sxs-lookup"><span data-stu-id="2cf21-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="2cf21-109">示例</span><span class="sxs-lookup"><span data-stu-id="2cf21-109">EXAMPLES</span></span>

### <span data-ttu-id="2cf21-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2cf21-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="2cf21-111">清單庫專案。</span><span class="sxs-lookup"><span data-stu-id="2cf21-111">List gallery items.</span></span>

### <span data-ttu-id="2cf21-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2cf21-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="2cf21-113">依名稱取得圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="2cf21-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="2cf21-114">參數</span><span class="sxs-lookup"><span data-stu-id="2cf21-114">PARAMETERS</span></span>

### <span data-ttu-id="2cf21-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cf21-115">-Name</span></span>
<span data-ttu-id="2cf21-116">圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="2cf21-116">Identity of the gallery item.</span></span>
<span data-ttu-id="2cf21-117">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="2cf21-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf21-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf21-118">CommonParameters</span></span>
<span data-ttu-id="2cf21-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cf21-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf21-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cf21-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf21-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2cf21-121">INPUTS</span></span>

## <span data-ttu-id="2cf21-122">輸出</span><span class="sxs-lookup"><span data-stu-id="2cf21-122">OUTPUTS</span></span>

### <span data-ttu-id="2cf21-123">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="2cf21-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="2cf21-124">筆記</span><span class="sxs-lookup"><span data-stu-id="2cf21-124">NOTES</span></span>

## <span data-ttu-id="2cf21-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cf21-125">RELATED LINKS</span></span>

