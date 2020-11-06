---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449841"
---
# <span data-ttu-id="ec866-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ec866-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="ec866-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec866-102">SYNOPSIS</span></span>
<span data-ttu-id="ec866-103">取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="ec866-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec866-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec866-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec866-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec866-105">DESCRIPTION</span></span>
<span data-ttu-id="ec866-106">**AzureRmVMExtensionImageType** Cmdlet 會取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="ec866-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="ec866-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec866-107">EXAMPLES</span></span>

### <span data-ttu-id="ec866-108">範例1：取得延伸圖像類型</span><span class="sxs-lookup"><span data-stu-id="ec866-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="ec866-109">這個命令會取得指定發行者和位置的副檔名影像類型。</span><span class="sxs-lookup"><span data-stu-id="ec866-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="ec866-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec866-110">PARAMETERS</span></span>

### <span data-ttu-id="ec866-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec866-111">-DefaultProfile</span></span>
<span data-ttu-id="ec866-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec866-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec866-113">-位置</span><span class="sxs-lookup"><span data-stu-id="ec866-113">-Location</span></span>
<span data-ttu-id="ec866-114">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="ec866-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="ec866-115">這個 Cmdlet 會取得此參數指定位置的延伸類型。</span><span class="sxs-lookup"><span data-stu-id="ec866-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec866-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="ec866-116">-PublisherName</span></span>
<span data-ttu-id="ec866-117">指定副檔名發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec866-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="ec866-118">若要取得延伸發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec866-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="ec866-119">這個 Cmdlet 會從發行者取得此參數指定之延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="ec866-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec866-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec866-120">CommonParameters</span></span>
<span data-ttu-id="ec866-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec866-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec866-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec866-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec866-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ec866-123">INPUTS</span></span>

### <span data-ttu-id="ec866-124">System.object</span><span class="sxs-lookup"><span data-stu-id="ec866-124">System.String</span></span>

## <span data-ttu-id="ec866-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ec866-125">OUTPUTS</span></span>

### <span data-ttu-id="ec866-126">PSVirtualMachineExtensionImageType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ec866-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="ec866-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ec866-127">NOTES</span></span>

## <span data-ttu-id="ec866-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec866-128">RELATED LINKS</span></span>

[<span data-ttu-id="ec866-129">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ec866-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="ec866-130">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ec866-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


