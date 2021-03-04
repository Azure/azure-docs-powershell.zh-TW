---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 983eba222959fb11a50ce94704ebdf39a9bc9fbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917373"
---
# <span data-ttu-id="93451-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="93451-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="93451-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93451-102">SYNOPSIS</span></span>
<span data-ttu-id="93451-103">獲得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="93451-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="93451-104">語法</span><span class="sxs-lookup"><span data-stu-id="93451-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93451-105">描述</span><span class="sxs-lookup"><span data-stu-id="93451-105">DESCRIPTION</span></span>
<span data-ttu-id="93451-106">**Get-Az VMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="93451-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="93451-107">例子</span><span class="sxs-lookup"><span data-stu-id="93451-107">EXAMPLES</span></span>

### <span data-ttu-id="93451-108">範例 1：取得地區的 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="93451-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="93451-109">此命令會獲得 Azure 設定檔中美國中地區 VMImage 實例的發行者。</span><span class="sxs-lookup"><span data-stu-id="93451-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="93451-110">參數</span><span class="sxs-lookup"><span data-stu-id="93451-110">PARAMETERS</span></span>

### <span data-ttu-id="93451-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93451-111">-DefaultProfile</span></span>
<span data-ttu-id="93451-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93451-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93451-113">-位置</span><span class="sxs-lookup"><span data-stu-id="93451-113">-Location</span></span>
<span data-ttu-id="93451-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="93451-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="93451-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93451-115">CommonParameters</span></span>
<span data-ttu-id="93451-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93451-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93451-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93451-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93451-118">輸入</span><span class="sxs-lookup"><span data-stu-id="93451-118">INPUTS</span></span>

### <span data-ttu-id="93451-119">System.String</span><span class="sxs-lookup"><span data-stu-id="93451-119">System.String</span></span>

## <span data-ttu-id="93451-120">輸出</span><span class="sxs-lookup"><span data-stu-id="93451-120">OUTPUTS</span></span>

### <span data-ttu-id="93451-121">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="93451-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="93451-122">筆記</span><span class="sxs-lookup"><span data-stu-id="93451-122">NOTES</span></span>

## <span data-ttu-id="93451-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="93451-123">RELATED LINKS</span></span>

[<span data-ttu-id="93451-124">Get-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="93451-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="93451-125">Get-AzEVImageOffer</span><span class="sxs-lookup"><span data-stu-id="93451-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="93451-126">Get-AzKUImageSku</span><span class="sxs-lookup"><span data-stu-id="93451-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="93451-127">Save-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="93451-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


