---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455864"
---
# <span data-ttu-id="e5996-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e5996-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="e5996-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5996-102">SYNOPSIS</span></span>
<span data-ttu-id="e5996-103">取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="e5996-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5996-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5996-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5996-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5996-105">DESCRIPTION</span></span>
<span data-ttu-id="e5996-106">**AzureRmVMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="e5996-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="e5996-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5996-107">EXAMPLES</span></span>

### <span data-ttu-id="e5996-108">範例1：為區域取得 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="e5996-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="e5996-109">這個命令會在您的 Azure 設定檔中取得美國中部地區的 VMImage 實例發行者。</span><span class="sxs-lookup"><span data-stu-id="e5996-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="e5996-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5996-110">PARAMETERS</span></span>

### <span data-ttu-id="e5996-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5996-111">-DefaultProfile</span></span>
<span data-ttu-id="e5996-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5996-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5996-113">-位置</span><span class="sxs-lookup"><span data-stu-id="e5996-113">-Location</span></span>
<span data-ttu-id="e5996-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="e5996-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e5996-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5996-115">CommonParameters</span></span>
<span data-ttu-id="e5996-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5996-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5996-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5996-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5996-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e5996-118">INPUTS</span></span>

## <span data-ttu-id="e5996-119">輸出</span><span class="sxs-lookup"><span data-stu-id="e5996-119">OUTPUTS</span></span>

## <span data-ttu-id="e5996-120">筆記</span><span class="sxs-lookup"><span data-stu-id="e5996-120">NOTES</span></span>

## <span data-ttu-id="e5996-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5996-121">RELATED LINKS</span></span>

[<span data-ttu-id="e5996-122">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e5996-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e5996-123">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e5996-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e5996-124">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e5996-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e5996-125">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e5996-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


