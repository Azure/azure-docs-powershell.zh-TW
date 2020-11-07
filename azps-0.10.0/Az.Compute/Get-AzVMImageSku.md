---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: fad6c42c53e475343ad518c89dbb1a918a0f1e68
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796230"
---
# <span data-ttu-id="82e49-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="82e49-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="82e49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82e49-102">SYNOPSIS</span></span>
<span data-ttu-id="82e49-103">取得 VMImage Sku。</span><span class="sxs-lookup"><span data-stu-id="82e49-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="82e49-104">句法</span><span class="sxs-lookup"><span data-stu-id="82e49-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e49-105">說明</span><span class="sxs-lookup"><span data-stu-id="82e49-105">DESCRIPTION</span></span>
<span data-ttu-id="82e49-106">**AzVMImageSku** Cmdlet 會取得 VMImage sku。</span><span class="sxs-lookup"><span data-stu-id="82e49-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="82e49-107">示例</span><span class="sxs-lookup"><span data-stu-id="82e49-107">EXAMPLES</span></span>

### <span data-ttu-id="82e49-108">範例1：取得 VMImage Sku</span><span class="sxs-lookup"><span data-stu-id="82e49-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="82e49-109">這個命令會取得指定發行商和優惠的 Sku。</span><span class="sxs-lookup"><span data-stu-id="82e49-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="82e49-110">參數</span><span class="sxs-lookup"><span data-stu-id="82e49-110">PARAMETERS</span></span>

### <span data-ttu-id="82e49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e49-111">-DefaultProfile</span></span>
<span data-ttu-id="82e49-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82e49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82e49-113">-位置</span><span class="sxs-lookup"><span data-stu-id="82e49-113">-Location</span></span>
<span data-ttu-id="82e49-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="82e49-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="82e49-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="82e49-115">-Offer</span></span>
<span data-ttu-id="82e49-116">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="82e49-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="82e49-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="82e49-117">-PublisherName</span></span>
<span data-ttu-id="82e49-118">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="82e49-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="82e49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e49-119">CommonParameters</span></span>
<span data-ttu-id="82e49-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82e49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e49-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82e49-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e49-122">輸入</span><span class="sxs-lookup"><span data-stu-id="82e49-122">INPUTS</span></span>

### <span data-ttu-id="82e49-123">所有</span><span class="sxs-lookup"><span data-stu-id="82e49-123">None</span></span>
<span data-ttu-id="82e49-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="82e49-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82e49-125">輸出</span><span class="sxs-lookup"><span data-stu-id="82e49-125">OUTPUTS</span></span>

### <span data-ttu-id="82e49-126">PSVirtualMachineImageSku 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="82e49-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="82e49-127">筆記</span><span class="sxs-lookup"><span data-stu-id="82e49-127">NOTES</span></span>

## <span data-ttu-id="82e49-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="82e49-128">RELATED LINKS</span></span>

[<span data-ttu-id="82e49-129">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="82e49-129">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="82e49-130">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="82e49-130">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="82e49-131">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="82e49-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="82e49-132">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="82e49-132">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


