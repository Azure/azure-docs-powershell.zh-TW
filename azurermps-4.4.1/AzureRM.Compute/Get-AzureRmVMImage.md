---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445115"
---
# <span data-ttu-id="a93f6-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a93f6-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="a93f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a93f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a93f6-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="a93f6-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a93f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a93f6-104">SYNTAX</span></span>

### <span data-ttu-id="a93f6-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="a93f6-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a93f6-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="a93f6-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93f6-107">說明</span><span class="sxs-lookup"><span data-stu-id="a93f6-107">DESCRIPTION</span></span>
<span data-ttu-id="a93f6-108">**AzureRmVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="a93f6-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="a93f6-109">示例</span><span class="sxs-lookup"><span data-stu-id="a93f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a93f6-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="a93f6-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="a93f6-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="a93f6-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="a93f6-112">參數</span><span class="sxs-lookup"><span data-stu-id="a93f6-112">PARAMETERS</span></span>

### <span data-ttu-id="a93f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93f6-113">-DefaultProfile</span></span>
<span data-ttu-id="a93f6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a93f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="a93f6-115">-FilterExpression</span></span>
<span data-ttu-id="a93f6-116">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="a93f6-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-117">-位置</span><span class="sxs-lookup"><span data-stu-id="a93f6-117">-Location</span></span>
<span data-ttu-id="a93f6-118">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="a93f6-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-119">-優惠</span><span class="sxs-lookup"><span data-stu-id="a93f6-119">-Offer</span></span>
<span data-ttu-id="a93f6-120">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="a93f6-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="a93f6-121">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a93f6-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a93f6-122">-PublisherName</span></span>
<span data-ttu-id="a93f6-123">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="a93f6-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="a93f6-124">若要取得影像發行商，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a93f6-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="a93f6-125">-Skus</span></span>
<span data-ttu-id="a93f6-126">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="a93f6-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="a93f6-127">若要取得 SKU，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a93f6-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-128">-版本</span><span class="sxs-lookup"><span data-stu-id="a93f6-128">-Version</span></span>
<span data-ttu-id="a93f6-129">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="a93f6-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93f6-130">CommonParameters</span></span>
<span data-ttu-id="a93f6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a93f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93f6-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a93f6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93f6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a93f6-133">INPUTS</span></span>

## <span data-ttu-id="a93f6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a93f6-134">OUTPUTS</span></span>

## <span data-ttu-id="a93f6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a93f6-135">NOTES</span></span>

## <span data-ttu-id="a93f6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a93f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="a93f6-137">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a93f6-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="a93f6-138">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a93f6-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="a93f6-139">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a93f6-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="a93f6-140">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a93f6-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)

