---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457708"
---
# <span data-ttu-id="8da93-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8da93-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="8da93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8da93-102">SYNOPSIS</span></span>
<span data-ttu-id="8da93-103">取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="8da93-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da93-104">句法</span><span class="sxs-lookup"><span data-stu-id="8da93-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da93-105">說明</span><span class="sxs-lookup"><span data-stu-id="8da93-105">DESCRIPTION</span></span>
<span data-ttu-id="8da93-106">**AzureRmVMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="8da93-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="8da93-107">示例</span><span class="sxs-lookup"><span data-stu-id="8da93-107">EXAMPLES</span></span>

### <span data-ttu-id="8da93-108">範例1：為區域取得 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="8da93-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="8da93-109">這個命令會在您的 Azure 設定檔中取得美國中部地區的 VMImage 實例發行者。</span><span class="sxs-lookup"><span data-stu-id="8da93-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="8da93-110">參數</span><span class="sxs-lookup"><span data-stu-id="8da93-110">PARAMETERS</span></span>

### <span data-ttu-id="8da93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da93-111">-DefaultProfile</span></span>
<span data-ttu-id="8da93-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8da93-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da93-113">-位置</span><span class="sxs-lookup"><span data-stu-id="8da93-113">-Location</span></span>
<span data-ttu-id="8da93-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="8da93-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="8da93-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da93-115">CommonParameters</span></span>
<span data-ttu-id="8da93-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8da93-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da93-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8da93-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da93-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8da93-118">INPUTS</span></span>

### <span data-ttu-id="8da93-119">System.object</span><span class="sxs-lookup"><span data-stu-id="8da93-119">System.String</span></span>

## <span data-ttu-id="8da93-120">輸出</span><span class="sxs-lookup"><span data-stu-id="8da93-120">OUTPUTS</span></span>

### <span data-ttu-id="8da93-121">PSVirtualMachineImagePublisher 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8da93-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="8da93-122">筆記</span><span class="sxs-lookup"><span data-stu-id="8da93-122">NOTES</span></span>

## <span data-ttu-id="8da93-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="8da93-123">RELATED LINKS</span></span>

[<span data-ttu-id="8da93-124">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8da93-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8da93-125">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8da93-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8da93-126">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8da93-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8da93-127">儲存-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8da93-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


