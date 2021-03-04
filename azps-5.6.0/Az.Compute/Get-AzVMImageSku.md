---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917358"
---
# <span data-ttu-id="12397-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="12397-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="12397-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12397-102">SYNOPSIS</span></span>
<span data-ttu-id="12397-103">獲得 VMImage SKUS。</span><span class="sxs-lookup"><span data-stu-id="12397-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="12397-104">語法</span><span class="sxs-lookup"><span data-stu-id="12397-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12397-105">描述</span><span class="sxs-lookup"><span data-stu-id="12397-105">DESCRIPTION</span></span>
<span data-ttu-id="12397-106">**Get-Az VMImageSku** Cmdlet 會取得 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="12397-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="12397-107">例子</span><span class="sxs-lookup"><span data-stu-id="12397-107">EXAMPLES</span></span>

### <span data-ttu-id="12397-108">範例 1：取得 VMImage SKUs</span><span class="sxs-lookup"><span data-stu-id="12397-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="12397-109">此命令會獲得指定發行者及優惠的 SKUS。</span><span class="sxs-lookup"><span data-stu-id="12397-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="12397-110">參數</span><span class="sxs-lookup"><span data-stu-id="12397-110">PARAMETERS</span></span>

### <span data-ttu-id="12397-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12397-111">-DefaultProfile</span></span>
<span data-ttu-id="12397-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12397-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12397-113">-位置</span><span class="sxs-lookup"><span data-stu-id="12397-113">-Location</span></span>
<span data-ttu-id="12397-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="12397-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="12397-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="12397-115">-Offer</span></span>
<span data-ttu-id="12397-116">指定 VMImage 優惠的類型。</span><span class="sxs-lookup"><span data-stu-id="12397-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="12397-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="12397-117">-PublisherName</span></span>
<span data-ttu-id="12397-118">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="12397-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="12397-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12397-119">CommonParameters</span></span>
<span data-ttu-id="12397-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12397-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12397-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12397-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12397-122">輸入</span><span class="sxs-lookup"><span data-stu-id="12397-122">INPUTS</span></span>

### <span data-ttu-id="12397-123">System.String</span><span class="sxs-lookup"><span data-stu-id="12397-123">System.String</span></span>

## <span data-ttu-id="12397-124">輸出</span><span class="sxs-lookup"><span data-stu-id="12397-124">OUTPUTS</span></span>

### <span data-ttu-id="12397-125">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="12397-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="12397-126">筆記</span><span class="sxs-lookup"><span data-stu-id="12397-126">NOTES</span></span>

## <span data-ttu-id="12397-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="12397-127">RELATED LINKS</span></span>

[<span data-ttu-id="12397-128">Get-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="12397-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="12397-129">Get-AzEVImageOffer</span><span class="sxs-lookup"><span data-stu-id="12397-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="12397-130">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="12397-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="12397-131">Save-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="12397-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


