---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442411"
---
# <span data-ttu-id="c565c-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="c565c-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="c565c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c565c-102">SYNOPSIS</span></span>
<span data-ttu-id="c565c-103">傳回載入到平臺影像儲存庫的虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="c565c-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="c565c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c565c-104">SYNTAX</span></span>

### <span data-ttu-id="c565c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c565c-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c565c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c565c-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c565c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c565c-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c565c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c565c-108">DESCRIPTION</span></span>
<span data-ttu-id="c565c-109">傳回平臺影像。</span><span class="sxs-lookup"><span data-stu-id="c565c-109">Returns platform images.</span></span>

## <span data-ttu-id="c565c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c565c-110">EXAMPLES</span></span>

### <span data-ttu-id="c565c-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c565c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="c565c-112">傳回載入至位於當地位置的平臺影像存放庫中的虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="c565c-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="c565c-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c565c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="c565c-114">取得特定的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="c565c-114">Get a specific platform image.</span></span>

## <span data-ttu-id="c565c-115">參數</span><span class="sxs-lookup"><span data-stu-id="c565c-115">PARAMETERS</span></span>

### <span data-ttu-id="c565c-116">-位置</span><span class="sxs-lookup"><span data-stu-id="c565c-116">-Location</span></span>
<span data-ttu-id="c565c-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c565c-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565c-118">-優惠</span><span class="sxs-lookup"><span data-stu-id="c565c-118">-Offer</span></span>
<span data-ttu-id="c565c-119">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c565c-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565c-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c565c-120">-Publisher</span></span>
<span data-ttu-id="c565c-121">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c565c-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c565c-122">-ResourceId</span></span>
<span data-ttu-id="c565c-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c565c-123">The resource id.</span></span>

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

### <span data-ttu-id="c565c-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="c565c-124">-Sku</span></span>
<span data-ttu-id="c565c-125">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c565c-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565c-126">-版本</span><span class="sxs-lookup"><span data-stu-id="c565c-126">-Version</span></span>
<span data-ttu-id="c565c-127">平臺影像的版本。</span><span class="sxs-lookup"><span data-stu-id="c565c-127">The version of the platform image.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c565c-128">CommonParameters</span></span>
<span data-ttu-id="c565c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c565c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c565c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c565c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c565c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c565c-131">INPUTS</span></span>

## <span data-ttu-id="c565c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c565c-132">OUTPUTS</span></span>

### <span data-ttu-id="c565c-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="c565c-133">PlatformImageObject</span></span>

## <span data-ttu-id="c565c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c565c-134">NOTES</span></span>

## <span data-ttu-id="c565c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c565c-135">RELATED LINKS</span></span>

