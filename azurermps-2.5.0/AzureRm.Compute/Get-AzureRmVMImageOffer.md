---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801026"
---
# <span data-ttu-id="9e41d-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9e41d-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="9e41d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e41d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e41d-103">取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="9e41d-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e41d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e41d-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e41d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e41d-105">DESCRIPTION</span></span>
<span data-ttu-id="9e41d-106">**AzureRmVMImageOffer** Cmdlet 會取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="9e41d-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="9e41d-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e41d-107">EXAMPLES</span></span>

### <span data-ttu-id="9e41d-108">範例1：取得發行商的優惠類型</span><span class="sxs-lookup"><span data-stu-id="9e41d-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9e41d-109">這個命令會取得中央美區域中指定發行者的方案類型。</span><span class="sxs-lookup"><span data-stu-id="9e41d-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="9e41d-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e41d-110">PARAMETERS</span></span>

### <span data-ttu-id="9e41d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e41d-111">-DefaultProfile</span></span>
<span data-ttu-id="9e41d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e41d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e41d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="9e41d-113">-Location</span></span>
<span data-ttu-id="9e41d-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="9e41d-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9e41d-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9e41d-115">-PublisherName</span></span>
<span data-ttu-id="9e41d-116">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e41d-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9e41d-117">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e41d-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9e41d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e41d-118">CommonParameters</span></span>
<span data-ttu-id="9e41d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e41d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e41d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e41d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e41d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9e41d-121">INPUTS</span></span>

### <span data-ttu-id="9e41d-122">所有</span><span class="sxs-lookup"><span data-stu-id="9e41d-122">None</span></span>
<span data-ttu-id="9e41d-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9e41d-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e41d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9e41d-124">OUTPUTS</span></span>

### <span data-ttu-id="9e41d-125">PSVirtualMachineImageOffer 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9e41d-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="9e41d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9e41d-126">NOTES</span></span>

## <span data-ttu-id="9e41d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e41d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e41d-128">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9e41d-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9e41d-129">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9e41d-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9e41d-130">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9e41d-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9e41d-131">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9e41d-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


