---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626019"
---
# <span data-ttu-id="e4fc0-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e4fc0-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="e4fc0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fc0-103">取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4fc0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4fc0-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4fc0-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fc0-106">**AzureRmVMImageOffer** Cmdlet 會取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="e4fc0-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fc0-108">範例1：取得發行商的優惠類型</span><span class="sxs-lookup"><span data-stu-id="e4fc0-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="e4fc0-109">這個命令會取得中央美區域中指定發行者的方案類型。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="e4fc0-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4fc0-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fc0-111">-DefaultProfile</span></span>
<span data-ttu-id="e4fc0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4fc0-113">-位置</span><span class="sxs-lookup"><span data-stu-id="e4fc0-113">-Location</span></span>
<span data-ttu-id="e4fc0-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e4fc0-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e4fc0-115">-PublisherName</span></span>
<span data-ttu-id="e4fc0-116">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e4fc0-117">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e4fc0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fc0-118">CommonParameters</span></span>
<span data-ttu-id="e4fc0-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fc0-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4fc0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fc0-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e4fc0-121">INPUTS</span></span>

## <span data-ttu-id="e4fc0-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e4fc0-122">OUTPUTS</span></span>

## <span data-ttu-id="e4fc0-123">筆記</span><span class="sxs-lookup"><span data-stu-id="e4fc0-123">NOTES</span></span>

## <span data-ttu-id="e4fc0-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4fc0-124">RELATED LINKS</span></span>

[<span data-ttu-id="e4fc0-125">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e4fc0-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e4fc0-126">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e4fc0-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e4fc0-127">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e4fc0-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e4fc0-128">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e4fc0-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


