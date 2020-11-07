---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626643"
---
# <span data-ttu-id="75b85-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="75b85-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="75b85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75b85-102">SYNOPSIS</span></span>
<span data-ttu-id="75b85-103">取得 VMImage Sku。</span><span class="sxs-lookup"><span data-stu-id="75b85-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b85-104">句法</span><span class="sxs-lookup"><span data-stu-id="75b85-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75b85-105">說明</span><span class="sxs-lookup"><span data-stu-id="75b85-105">DESCRIPTION</span></span>
<span data-ttu-id="75b85-106">**AzureRmVMImageSku** Cmdlet 會取得 VMImage sku。</span><span class="sxs-lookup"><span data-stu-id="75b85-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="75b85-107">示例</span><span class="sxs-lookup"><span data-stu-id="75b85-107">EXAMPLES</span></span>

### <span data-ttu-id="75b85-108">範例1：取得 VMImage Sku</span><span class="sxs-lookup"><span data-stu-id="75b85-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="75b85-109">這個命令會取得指定發行商和優惠的 Sku。</span><span class="sxs-lookup"><span data-stu-id="75b85-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="75b85-110">參數</span><span class="sxs-lookup"><span data-stu-id="75b85-110">PARAMETERS</span></span>

### <span data-ttu-id="75b85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b85-111">-DefaultProfile</span></span>
<span data-ttu-id="75b85-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75b85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75b85-113">-位置</span><span class="sxs-lookup"><span data-stu-id="75b85-113">-Location</span></span>
<span data-ttu-id="75b85-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="75b85-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="75b85-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="75b85-115">-Offer</span></span>
<span data-ttu-id="75b85-116">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="75b85-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="75b85-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="75b85-117">-PublisherName</span></span>
<span data-ttu-id="75b85-118">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="75b85-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="75b85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b85-119">CommonParameters</span></span>
<span data-ttu-id="75b85-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75b85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b85-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75b85-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b85-122">輸入</span><span class="sxs-lookup"><span data-stu-id="75b85-122">INPUTS</span></span>

## <span data-ttu-id="75b85-123">輸出</span><span class="sxs-lookup"><span data-stu-id="75b85-123">OUTPUTS</span></span>

## <span data-ttu-id="75b85-124">筆記</span><span class="sxs-lookup"><span data-stu-id="75b85-124">NOTES</span></span>

## <span data-ttu-id="75b85-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="75b85-125">RELATED LINKS</span></span>

[<span data-ttu-id="75b85-126">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="75b85-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="75b85-127">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="75b85-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="75b85-128">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="75b85-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="75b85-129">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="75b85-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


