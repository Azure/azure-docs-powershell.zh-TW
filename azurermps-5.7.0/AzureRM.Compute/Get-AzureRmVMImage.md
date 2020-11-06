---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446383"
---
# <span data-ttu-id="d285d-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d285d-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="d285d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d285d-102">SYNOPSIS</span></span>
<span data-ttu-id="d285d-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="d285d-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d285d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d285d-104">SYNTAX</span></span>

### <span data-ttu-id="d285d-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="d285d-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="d285d-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="d285d-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d285d-107">說明</span><span class="sxs-lookup"><span data-stu-id="d285d-107">DESCRIPTION</span></span>
<span data-ttu-id="d285d-108">**AzureRmVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="d285d-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="d285d-109">示例</span><span class="sxs-lookup"><span data-stu-id="d285d-109">EXAMPLES</span></span>

### <span data-ttu-id="d285d-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="d285d-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="d285d-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="d285d-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="d285d-112">參數</span><span class="sxs-lookup"><span data-stu-id="d285d-112">PARAMETERS</span></span>

### <span data-ttu-id="d285d-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="d285d-113">-FilterExpression</span></span>
<span data-ttu-id="d285d-114">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="d285d-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-115">-位置</span><span class="sxs-lookup"><span data-stu-id="d285d-115">-Location</span></span>
<span data-ttu-id="d285d-116">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="d285d-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-117">-優惠</span><span class="sxs-lookup"><span data-stu-id="d285d-117">-Offer</span></span>
<span data-ttu-id="d285d-118">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="d285d-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="d285d-119">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d285d-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d285d-120">-PublisherName</span></span>
<span data-ttu-id="d285d-121">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="d285d-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="d285d-122">若要取得影像發行商，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d285d-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="d285d-123">-Skus</span></span>
<span data-ttu-id="d285d-124">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="d285d-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="d285d-125">若要取得 SKU，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d285d-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-126">-版本</span><span class="sxs-lookup"><span data-stu-id="d285d-126">-Version</span></span>
<span data-ttu-id="d285d-127">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="d285d-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d285d-128">CommonParameters</span></span>
<span data-ttu-id="d285d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d285d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d285d-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d285d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d285d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d285d-131">INPUTS</span></span>

### <span data-ttu-id="d285d-132">所有</span><span class="sxs-lookup"><span data-stu-id="d285d-132">None</span></span>
<span data-ttu-id="d285d-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d285d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d285d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d285d-134">OUTPUTS</span></span>

## <span data-ttu-id="d285d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d285d-135">NOTES</span></span>

## <span data-ttu-id="d285d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d285d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d285d-137">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d285d-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d285d-138">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d285d-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d285d-139">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d285d-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="d285d-140">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d285d-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


