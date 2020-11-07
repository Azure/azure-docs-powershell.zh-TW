---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801809"
---
# <span data-ttu-id="269e2-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="269e2-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="269e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="269e2-102">SYNOPSIS</span></span>
<span data-ttu-id="269e2-103">取得 VMImage Sku。</span><span class="sxs-lookup"><span data-stu-id="269e2-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="269e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="269e2-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="269e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="269e2-105">DESCRIPTION</span></span>
<span data-ttu-id="269e2-106">**AzureRmVMImageSku** Cmdlet 會取得 VMImage sku。</span><span class="sxs-lookup"><span data-stu-id="269e2-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="269e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="269e2-107">EXAMPLES</span></span>

### <span data-ttu-id="269e2-108">範例1：取得 VMImage Sku</span><span class="sxs-lookup"><span data-stu-id="269e2-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="269e2-109">這個命令會取得指定發行商和優惠的 Sku。</span><span class="sxs-lookup"><span data-stu-id="269e2-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="269e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="269e2-110">PARAMETERS</span></span>

### <span data-ttu-id="269e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269e2-111">-DefaultProfile</span></span>
<span data-ttu-id="269e2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="269e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="269e2-113">-位置</span><span class="sxs-lookup"><span data-stu-id="269e2-113">-Location</span></span>
<span data-ttu-id="269e2-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="269e2-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="269e2-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="269e2-115">-Offer</span></span>
<span data-ttu-id="269e2-116">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="269e2-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="269e2-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="269e2-117">-PublisherName</span></span>
<span data-ttu-id="269e2-118">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="269e2-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="269e2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269e2-119">CommonParameters</span></span>
<span data-ttu-id="269e2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="269e2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269e2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="269e2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269e2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="269e2-122">INPUTS</span></span>

### <span data-ttu-id="269e2-123">所有</span><span class="sxs-lookup"><span data-stu-id="269e2-123">None</span></span>
<span data-ttu-id="269e2-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="269e2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="269e2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="269e2-125">OUTPUTS</span></span>

### <span data-ttu-id="269e2-126">PSVirtualMachineImageSku 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="269e2-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="269e2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="269e2-127">NOTES</span></span>

## <span data-ttu-id="269e2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="269e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="269e2-129">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="269e2-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="269e2-130">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="269e2-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="269e2-131">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="269e2-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="269e2-132">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="269e2-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


