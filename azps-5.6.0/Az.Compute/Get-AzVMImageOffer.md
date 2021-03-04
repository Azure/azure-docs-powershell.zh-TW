---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 94556ce0b78b90ae9c418aee175f090e9209adb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917374"
---
# <span data-ttu-id="f7bce-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f7bce-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="f7bce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7bce-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bce-103">獲得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="f7bce-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="f7bce-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7bce-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7bce-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7bce-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bce-106">**Get-Az VMImageOffer** Cmdlet 會取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="f7bce-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="f7bce-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7bce-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bce-108">範例 1：取得發行者優惠類型</span><span class="sxs-lookup"><span data-stu-id="f7bce-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="f7bce-109">此命令會針對美國中地區的指定發行者獲得優惠類型。</span><span class="sxs-lookup"><span data-stu-id="f7bce-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="f7bce-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7bce-110">PARAMETERS</span></span>

### <span data-ttu-id="f7bce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bce-111">-DefaultProfile</span></span>
<span data-ttu-id="f7bce-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7bce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7bce-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f7bce-113">-Location</span></span>
<span data-ttu-id="f7bce-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="f7bce-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f7bce-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f7bce-115">-PublisherName</span></span>
<span data-ttu-id="f7bce-116">指定 VMImage 的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="f7bce-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f7bce-117">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7bce-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f7bce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bce-118">CommonParameters</span></span>
<span data-ttu-id="f7bce-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7bce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bce-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7bce-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bce-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f7bce-121">INPUTS</span></span>

### <span data-ttu-id="f7bce-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f7bce-122">System.String</span></span>

## <span data-ttu-id="f7bce-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f7bce-123">OUTPUTS</span></span>

### <span data-ttu-id="f7bce-124">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="f7bce-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="f7bce-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f7bce-125">NOTES</span></span>

## <span data-ttu-id="f7bce-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7bce-126">RELATED LINKS</span></span>

[<span data-ttu-id="f7bce-127">Get-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="f7bce-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f7bce-128">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="f7bce-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f7bce-129">Get-AzKUImageSku</span><span class="sxs-lookup"><span data-stu-id="f7bce-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f7bce-130">Save-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="f7bce-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


