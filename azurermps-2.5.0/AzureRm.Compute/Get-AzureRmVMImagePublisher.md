---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801813"
---
# <span data-ttu-id="9b18f-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b18f-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="9b18f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b18f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b18f-103">取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="9b18f-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b18f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b18f-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b18f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b18f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b18f-106">**AzureRmVMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="9b18f-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="9b18f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b18f-107">EXAMPLES</span></span>

### <span data-ttu-id="9b18f-108">範例1：為區域取得 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="9b18f-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="9b18f-109">這個命令會在您的 Azure 設定檔中取得美國中部地區的 VMImage 實例發行者。</span><span class="sxs-lookup"><span data-stu-id="9b18f-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="9b18f-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b18f-110">PARAMETERS</span></span>

### <span data-ttu-id="9b18f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b18f-111">-DefaultProfile</span></span>
<span data-ttu-id="9b18f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b18f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b18f-113">-位置</span><span class="sxs-lookup"><span data-stu-id="9b18f-113">-Location</span></span>
<span data-ttu-id="9b18f-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="9b18f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9b18f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b18f-115">CommonParameters</span></span>
<span data-ttu-id="9b18f-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b18f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b18f-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b18f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b18f-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9b18f-118">INPUTS</span></span>

### <span data-ttu-id="9b18f-119">所有</span><span class="sxs-lookup"><span data-stu-id="9b18f-119">None</span></span>
<span data-ttu-id="9b18f-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9b18f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b18f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9b18f-121">OUTPUTS</span></span>

### <span data-ttu-id="9b18f-122">PSVirtualMachineImagePublisher 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9b18f-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="9b18f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9b18f-123">NOTES</span></span>

## <span data-ttu-id="9b18f-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b18f-124">RELATED LINKS</span></span>

[<span data-ttu-id="9b18f-125">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b18f-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9b18f-126">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b18f-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="9b18f-127">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b18f-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9b18f-128">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9b18f-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


