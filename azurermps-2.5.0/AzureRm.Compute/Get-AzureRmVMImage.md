---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801030"
---
# <span data-ttu-id="9b80f-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b80f-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="9b80f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b80f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b80f-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9b80f-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b80f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b80f-104">SYNTAX</span></span>

### <span data-ttu-id="9b80f-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9b80f-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b80f-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9b80f-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b80f-107">說明</span><span class="sxs-lookup"><span data-stu-id="9b80f-107">DESCRIPTION</span></span>
<span data-ttu-id="9b80f-108">**AzureRmVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9b80f-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9b80f-109">示例</span><span class="sxs-lookup"><span data-stu-id="9b80f-109">EXAMPLES</span></span>

### <span data-ttu-id="9b80f-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="9b80f-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="9b80f-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="9b80f-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="9b80f-112">參數</span><span class="sxs-lookup"><span data-stu-id="9b80f-112">PARAMETERS</span></span>

### <span data-ttu-id="9b80f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b80f-113">-DefaultProfile</span></span>
<span data-ttu-id="9b80f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b80f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b80f-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9b80f-115">-FilterExpression</span></span>
<span data-ttu-id="9b80f-116">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="9b80f-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="9b80f-117">-位置</span><span class="sxs-lookup"><span data-stu-id="9b80f-117">-Location</span></span>
<span data-ttu-id="9b80f-118">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="9b80f-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9b80f-119">-優惠</span><span class="sxs-lookup"><span data-stu-id="9b80f-119">-Offer</span></span>
<span data-ttu-id="9b80f-120">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="9b80f-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9b80f-121">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b80f-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9b80f-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9b80f-122">-PublisherName</span></span>
<span data-ttu-id="9b80f-123">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="9b80f-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9b80f-124">若要取得影像發行商，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b80f-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9b80f-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="9b80f-125">-Skus</span></span>
<span data-ttu-id="9b80f-126">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="9b80f-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9b80f-127">若要取得 SKU，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b80f-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9b80f-128">-版本</span><span class="sxs-lookup"><span data-stu-id="9b80f-128">-Version</span></span>
<span data-ttu-id="9b80f-129">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="9b80f-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="9b80f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b80f-130">CommonParameters</span></span>
<span data-ttu-id="9b80f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b80f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b80f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b80f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b80f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9b80f-133">INPUTS</span></span>

### <span data-ttu-id="9b80f-134">所有</span><span class="sxs-lookup"><span data-stu-id="9b80f-134">None</span></span>
<span data-ttu-id="9b80f-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9b80f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b80f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="9b80f-136">OUTPUTS</span></span>

### <span data-ttu-id="9b80f-137">PSVirtualMachineImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9b80f-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9b80f-138">PSVirtualMachineImageDetail 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9b80f-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9b80f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9b80f-139">NOTES</span></span>

## <span data-ttu-id="9b80f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b80f-140">RELATED LINKS</span></span>

[<span data-ttu-id="9b80f-141">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b80f-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="9b80f-142">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b80f-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9b80f-143">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b80f-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9b80f-144">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b80f-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


