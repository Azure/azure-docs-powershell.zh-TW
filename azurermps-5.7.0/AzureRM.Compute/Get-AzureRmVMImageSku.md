---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625926"
---
# <span data-ttu-id="502d0-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="502d0-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="502d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="502d0-102">SYNOPSIS</span></span>
<span data-ttu-id="502d0-103">取得 VMImage Sku。</span><span class="sxs-lookup"><span data-stu-id="502d0-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="502d0-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="502d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="502d0-105">DESCRIPTION</span></span>
<span data-ttu-id="502d0-106">**AzureRmVMImageSku** Cmdlet 會取得 VMImage sku。</span><span class="sxs-lookup"><span data-stu-id="502d0-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="502d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="502d0-107">EXAMPLES</span></span>

### <span data-ttu-id="502d0-108">範例1：取得 VMImage Sku</span><span class="sxs-lookup"><span data-stu-id="502d0-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="502d0-109">這個命令會取得指定發行商和優惠的 Sku。</span><span class="sxs-lookup"><span data-stu-id="502d0-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="502d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="502d0-110">PARAMETERS</span></span>

### <span data-ttu-id="502d0-111">-位置</span><span class="sxs-lookup"><span data-stu-id="502d0-111">-Location</span></span>
<span data-ttu-id="502d0-112">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="502d0-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="502d0-113">-優惠</span><span class="sxs-lookup"><span data-stu-id="502d0-113">-Offer</span></span>
<span data-ttu-id="502d0-114">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="502d0-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="502d0-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="502d0-115">-PublisherName</span></span>
<span data-ttu-id="502d0-116">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="502d0-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="502d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502d0-117">CommonParameters</span></span>
<span data-ttu-id="502d0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="502d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502d0-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="502d0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502d0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="502d0-120">INPUTS</span></span>

### <span data-ttu-id="502d0-121">所有</span><span class="sxs-lookup"><span data-stu-id="502d0-121">None</span></span>
<span data-ttu-id="502d0-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="502d0-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="502d0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="502d0-123">OUTPUTS</span></span>

## <span data-ttu-id="502d0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="502d0-124">NOTES</span></span>

## <span data-ttu-id="502d0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="502d0-125">RELATED LINKS</span></span>

[<span data-ttu-id="502d0-126">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="502d0-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="502d0-127">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="502d0-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="502d0-128">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="502d0-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="502d0-129">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="502d0-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


