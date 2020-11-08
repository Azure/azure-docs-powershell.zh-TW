---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127137"
---
# <span data-ttu-id="a1955-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a1955-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="a1955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1955-102">SYNOPSIS</span></span>
<span data-ttu-id="a1955-103">取得 VMImage Sku。</span><span class="sxs-lookup"><span data-stu-id="a1955-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="a1955-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1955-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1955-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1955-105">DESCRIPTION</span></span>
<span data-ttu-id="a1955-106">**AzVMImageSku** Cmdlet 會取得 VMImage sku。</span><span class="sxs-lookup"><span data-stu-id="a1955-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="a1955-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1955-107">EXAMPLES</span></span>

### <span data-ttu-id="a1955-108">範例1：取得 VMImage Sku</span><span class="sxs-lookup"><span data-stu-id="a1955-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="a1955-109">這個命令會取得指定發行商和優惠的 Sku。</span><span class="sxs-lookup"><span data-stu-id="a1955-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="a1955-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1955-110">PARAMETERS</span></span>

### <span data-ttu-id="a1955-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1955-111">-DefaultProfile</span></span>
<span data-ttu-id="a1955-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1955-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1955-113">-位置</span><span class="sxs-lookup"><span data-stu-id="a1955-113">-Location</span></span>
<span data-ttu-id="a1955-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="a1955-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a1955-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="a1955-115">-Offer</span></span>
<span data-ttu-id="a1955-116">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="a1955-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="a1955-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a1955-117">-PublisherName</span></span>
<span data-ttu-id="a1955-118">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="a1955-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="a1955-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1955-119">CommonParameters</span></span>
<span data-ttu-id="a1955-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1955-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1955-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1955-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1955-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a1955-122">INPUTS</span></span>

### <span data-ttu-id="a1955-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a1955-123">System.String</span></span>

## <span data-ttu-id="a1955-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a1955-124">OUTPUTS</span></span>

### <span data-ttu-id="a1955-125">PSVirtualMachineImageSku 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a1955-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="a1955-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a1955-126">NOTES</span></span>

## <span data-ttu-id="a1955-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1955-127">RELATED LINKS</span></span>

[<span data-ttu-id="a1955-128">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a1955-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a1955-129">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a1955-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a1955-130">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a1955-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a1955-131">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a1955-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


