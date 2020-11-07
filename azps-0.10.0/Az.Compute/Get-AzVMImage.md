---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796242"
---
# <span data-ttu-id="85713-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="85713-101">Get-AzVMImage</span></span>

## <span data-ttu-id="85713-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85713-102">SYNOPSIS</span></span>
<span data-ttu-id="85713-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="85713-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="85713-104">句法</span><span class="sxs-lookup"><span data-stu-id="85713-104">SYNTAX</span></span>

### <span data-ttu-id="85713-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="85713-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85713-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="85713-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85713-107">說明</span><span class="sxs-lookup"><span data-stu-id="85713-107">DESCRIPTION</span></span>
<span data-ttu-id="85713-108">**AzVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="85713-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="85713-109">示例</span><span class="sxs-lookup"><span data-stu-id="85713-109">EXAMPLES</span></span>

### <span data-ttu-id="85713-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="85713-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="85713-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="85713-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="85713-112">參數</span><span class="sxs-lookup"><span data-stu-id="85713-112">PARAMETERS</span></span>

### <span data-ttu-id="85713-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85713-113">-DefaultProfile</span></span>
<span data-ttu-id="85713-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85713-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85713-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="85713-115">-FilterExpression</span></span>
<span data-ttu-id="85713-116">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="85713-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="85713-117">-位置</span><span class="sxs-lookup"><span data-stu-id="85713-117">-Location</span></span>
<span data-ttu-id="85713-118">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="85713-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="85713-119">-優惠</span><span class="sxs-lookup"><span data-stu-id="85713-119">-Offer</span></span>
<span data-ttu-id="85713-120">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="85713-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="85713-121">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85713-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="85713-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="85713-122">-PublisherName</span></span>
<span data-ttu-id="85713-123">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="85713-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="85713-124">若要取得影像發行商，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85713-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="85713-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="85713-125">-Skus</span></span>
<span data-ttu-id="85713-126">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="85713-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="85713-127">若要取得 SKU，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85713-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="85713-128">-版本</span><span class="sxs-lookup"><span data-stu-id="85713-128">-Version</span></span>
<span data-ttu-id="85713-129">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="85713-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="85713-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85713-130">CommonParameters</span></span>
<span data-ttu-id="85713-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85713-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85713-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85713-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85713-133">輸入</span><span class="sxs-lookup"><span data-stu-id="85713-133">INPUTS</span></span>

### <span data-ttu-id="85713-134">所有</span><span class="sxs-lookup"><span data-stu-id="85713-134">None</span></span>
<span data-ttu-id="85713-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="85713-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85713-136">輸出</span><span class="sxs-lookup"><span data-stu-id="85713-136">OUTPUTS</span></span>

### <span data-ttu-id="85713-137">PSVirtualMachineImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="85713-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="85713-138">PSVirtualMachineImageDetail 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="85713-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="85713-139">筆記</span><span class="sxs-lookup"><span data-stu-id="85713-139">NOTES</span></span>

## <span data-ttu-id="85713-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="85713-140">RELATED LINKS</span></span>

[<span data-ttu-id="85713-141">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="85713-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="85713-142">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="85713-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="85713-143">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="85713-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="85713-144">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="85713-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


