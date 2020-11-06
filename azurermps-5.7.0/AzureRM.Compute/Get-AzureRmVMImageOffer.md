---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455507"
---
# <span data-ttu-id="6c476-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6c476-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="6c476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c476-102">SYNOPSIS</span></span>
<span data-ttu-id="6c476-103">取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="6c476-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c476-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c476-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="6c476-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c476-105">DESCRIPTION</span></span>
<span data-ttu-id="6c476-106">**AzureRmVMImageOffer** Cmdlet 會取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="6c476-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="6c476-107">示例</span><span class="sxs-lookup"><span data-stu-id="6c476-107">EXAMPLES</span></span>

### <span data-ttu-id="6c476-108">範例1：取得發行商的優惠類型</span><span class="sxs-lookup"><span data-stu-id="6c476-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="6c476-109">這個命令會取得中央美區域中指定發行者的方案類型。</span><span class="sxs-lookup"><span data-stu-id="6c476-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="6c476-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c476-110">PARAMETERS</span></span>

### <span data-ttu-id="6c476-111">-位置</span><span class="sxs-lookup"><span data-stu-id="6c476-111">-Location</span></span>
<span data-ttu-id="6c476-112">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="6c476-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="6c476-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6c476-113">-PublisherName</span></span>
<span data-ttu-id="6c476-114">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c476-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6c476-115">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c476-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6c476-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c476-116">CommonParameters</span></span>
<span data-ttu-id="6c476-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c476-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c476-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c476-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c476-119">輸入</span><span class="sxs-lookup"><span data-stu-id="6c476-119">INPUTS</span></span>

### <span data-ttu-id="6c476-120">所有</span><span class="sxs-lookup"><span data-stu-id="6c476-120">None</span></span>
<span data-ttu-id="6c476-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6c476-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c476-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6c476-122">OUTPUTS</span></span>

## <span data-ttu-id="6c476-123">筆記</span><span class="sxs-lookup"><span data-stu-id="6c476-123">NOTES</span></span>

## <span data-ttu-id="6c476-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c476-124">RELATED LINKS</span></span>

[<span data-ttu-id="6c476-125">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6c476-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="6c476-126">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6c476-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6c476-127">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6c476-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="6c476-128">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6c476-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


