---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969580"
---
# <span data-ttu-id="e0bfe-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e0bfe-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="e0bfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bfe-103">取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="e0bfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0bfe-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0bfe-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bfe-106">**AzVMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="e0bfe-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="e0bfe-108">範例1：為區域取得 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="e0bfe-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="e0bfe-109">這個命令會在您的 Azure 設定檔中取得美國中部地區的 VMImage 實例發行者。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="e0bfe-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="e0bfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bfe-111">-DefaultProfile</span></span>
<span data-ttu-id="e0bfe-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0bfe-113">-位置</span><span class="sxs-lookup"><span data-stu-id="e0bfe-113">-Location</span></span>
<span data-ttu-id="e0bfe-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e0bfe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bfe-115">CommonParameters</span></span>
<span data-ttu-id="e0bfe-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bfe-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0bfe-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bfe-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e0bfe-118">INPUTS</span></span>

### <span data-ttu-id="e0bfe-119">System.object</span><span class="sxs-lookup"><span data-stu-id="e0bfe-119">System.String</span></span>

## <span data-ttu-id="e0bfe-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e0bfe-120">OUTPUTS</span></span>

### <span data-ttu-id="e0bfe-121">PSVirtualMachineImagePublisher 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="e0bfe-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="e0bfe-122">筆記</span><span class="sxs-lookup"><span data-stu-id="e0bfe-122">NOTES</span></span>

## <span data-ttu-id="e0bfe-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0bfe-123">RELATED LINKS</span></span>

[<span data-ttu-id="e0bfe-124">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e0bfe-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="e0bfe-125">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e0bfe-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="e0bfe-126">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e0bfe-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="e0bfe-127">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e0bfe-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

