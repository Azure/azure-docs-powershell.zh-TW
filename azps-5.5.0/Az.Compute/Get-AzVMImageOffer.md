---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138666"
---
# <span data-ttu-id="cb003-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="cb003-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="cb003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb003-102">SYNOPSIS</span></span>
<span data-ttu-id="cb003-103">取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="cb003-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="cb003-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb003-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb003-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb003-105">DESCRIPTION</span></span>
<span data-ttu-id="cb003-106">**AzVMImageOffer** Cmdlet 會取得 VMImage 優惠類型。</span><span class="sxs-lookup"><span data-stu-id="cb003-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="cb003-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb003-107">EXAMPLES</span></span>

### <span data-ttu-id="cb003-108">範例1：取得發行商的優惠類型</span><span class="sxs-lookup"><span data-stu-id="cb003-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="cb003-109">這個命令會取得中央美區域中指定發行者的方案類型。</span><span class="sxs-lookup"><span data-stu-id="cb003-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="cb003-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb003-110">PARAMETERS</span></span>

### <span data-ttu-id="cb003-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb003-111">-DefaultProfile</span></span>
<span data-ttu-id="cb003-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb003-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb003-113">-位置</span><span class="sxs-lookup"><span data-stu-id="cb003-113">-Location</span></span>
<span data-ttu-id="cb003-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="cb003-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="cb003-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="cb003-115">-PublisherName</span></span>
<span data-ttu-id="cb003-116">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb003-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="cb003-117">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb003-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="cb003-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb003-118">CommonParameters</span></span>
<span data-ttu-id="cb003-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb003-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb003-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb003-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb003-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cb003-121">INPUTS</span></span>

### <span data-ttu-id="cb003-122">System.object</span><span class="sxs-lookup"><span data-stu-id="cb003-122">System.String</span></span>

## <span data-ttu-id="cb003-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cb003-123">OUTPUTS</span></span>

### <span data-ttu-id="cb003-124">PSVirtualMachineImageOffer 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="cb003-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="cb003-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cb003-125">NOTES</span></span>

## <span data-ttu-id="cb003-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb003-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb003-127">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cb003-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="cb003-128">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cb003-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="cb003-129">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cb003-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="cb003-130">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cb003-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


