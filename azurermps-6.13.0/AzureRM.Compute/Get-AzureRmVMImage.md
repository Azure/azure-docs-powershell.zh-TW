---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 881f4ba2d9750c9edbcb988ce3d438e062934a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449835"
---
# <span data-ttu-id="0a11c-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a11c-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="0a11c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a11c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a11c-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="0a11c-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a11c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a11c-104">SYNTAX</span></span>

### <span data-ttu-id="0a11c-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="0a11c-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a11c-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="0a11c-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a11c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0a11c-107">DESCRIPTION</span></span>
<span data-ttu-id="0a11c-108">**AzureRmVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="0a11c-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="0a11c-109">示例</span><span class="sxs-lookup"><span data-stu-id="0a11c-109">EXAMPLES</span></span>

### <span data-ttu-id="0a11c-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="0a11c-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"
```

<span data-ttu-id="0a11c-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="0a11c-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="0a11c-112">參數</span><span class="sxs-lookup"><span data-stu-id="0a11c-112">PARAMETERS</span></span>

### <span data-ttu-id="0a11c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a11c-113">-DefaultProfile</span></span>
<span data-ttu-id="0a11c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a11c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a11c-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="0a11c-115">-FilterExpression</span></span>
<span data-ttu-id="0a11c-116">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="0a11c-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="0a11c-117">-位置</span><span class="sxs-lookup"><span data-stu-id="0a11c-117">-Location</span></span>
<span data-ttu-id="0a11c-118">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="0a11c-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="0a11c-119">-優惠</span><span class="sxs-lookup"><span data-stu-id="0a11c-119">-Offer</span></span>
<span data-ttu-id="0a11c-120">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="0a11c-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="0a11c-121">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a11c-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="0a11c-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0a11c-122">-PublisherName</span></span>
<span data-ttu-id="0a11c-123">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="0a11c-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="0a11c-124">若要取得影像發行商，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a11c-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0a11c-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="0a11c-125">-Skus</span></span>
<span data-ttu-id="0a11c-126">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="0a11c-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="0a11c-127">若要取得 SKU，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a11c-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="0a11c-128">-版本</span><span class="sxs-lookup"><span data-stu-id="0a11c-128">-Version</span></span>
<span data-ttu-id="0a11c-129">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="0a11c-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="0a11c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a11c-130">CommonParameters</span></span>
<span data-ttu-id="0a11c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a11c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a11c-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a11c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a11c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0a11c-133">INPUTS</span></span>

### <span data-ttu-id="0a11c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="0a11c-134">System.String</span></span>

## <span data-ttu-id="0a11c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0a11c-135">OUTPUTS</span></span>

### <span data-ttu-id="0a11c-136">PSVirtualMachineImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0a11c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="0a11c-137">PSVirtualMachineImageDetail 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0a11c-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="0a11c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0a11c-138">NOTES</span></span>

## <span data-ttu-id="0a11c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a11c-139">RELATED LINKS</span></span>

[<span data-ttu-id="0a11c-140">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0a11c-140">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="0a11c-141">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0a11c-141">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0a11c-142">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0a11c-142">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="0a11c-143">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a11c-143">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


