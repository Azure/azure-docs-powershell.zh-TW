---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 551774d61e7887dfe115f37f67ce66fe95147406
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903669"
---
# <span data-ttu-id="2d174-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="2d174-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="2d174-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d174-102">SYNOPSIS</span></span>
<span data-ttu-id="2d174-103">獲得 Azure 擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="2d174-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="2d174-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d174-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d174-105">描述</span><span class="sxs-lookup"><span data-stu-id="2d174-105">DESCRIPTION</span></span>
<span data-ttu-id="2d174-106">**Get-AzCMExtensionImageType** Cmdlet 會取得 Azure 擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="2d174-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="2d174-107">例子</span><span class="sxs-lookup"><span data-stu-id="2d174-107">EXAMPLES</span></span>

### <span data-ttu-id="2d174-108">範例 1：取得擴充功能影像類型</span><span class="sxs-lookup"><span data-stu-id="2d174-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="2d174-109">此命令會獲得指定發行者與位置的擴充影像類型。</span><span class="sxs-lookup"><span data-stu-id="2d174-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="2d174-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d174-110">PARAMETERS</span></span>

### <span data-ttu-id="2d174-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d174-111">-DefaultProfile</span></span>
<span data-ttu-id="2d174-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d174-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d174-113">-位置</span><span class="sxs-lookup"><span data-stu-id="2d174-113">-Location</span></span>
<span data-ttu-id="2d174-114">指定擴充功能的位置。</span><span class="sxs-lookup"><span data-stu-id="2d174-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="2d174-115">此 Cmdlet 會在此參數指定的位置輸入擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2d174-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d174-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2d174-116">-PublisherName</span></span>
<span data-ttu-id="2d174-117">指定擴充功能發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d174-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="2d174-118">若要取得擴充功能發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d174-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="2d174-119">此 Cmdlet 會從此參數指定的發行者獲得副檔名類型。</span><span class="sxs-lookup"><span data-stu-id="2d174-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d174-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d174-120">CommonParameters</span></span>
<span data-ttu-id="2d174-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d174-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d174-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d174-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d174-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2d174-123">INPUTS</span></span>

### <span data-ttu-id="2d174-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2d174-124">System.String</span></span>

## <span data-ttu-id="2d174-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2d174-125">OUTPUTS</span></span>

### <span data-ttu-id="2d174-126">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="2d174-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="2d174-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2d174-127">NOTES</span></span>

## <span data-ttu-id="2d174-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d174-128">RELATED LINKS</span></span>

[<span data-ttu-id="2d174-129">Get-Az解說ExtensionImage</span><span class="sxs-lookup"><span data-stu-id="2d174-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="2d174-130">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="2d174-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


