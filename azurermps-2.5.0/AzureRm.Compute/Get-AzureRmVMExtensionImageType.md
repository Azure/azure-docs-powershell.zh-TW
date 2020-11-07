---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801049"
---
# <span data-ttu-id="645cc-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="645cc-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="645cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="645cc-102">SYNOPSIS</span></span>
<span data-ttu-id="645cc-103">取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="645cc-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="645cc-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="645cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="645cc-105">DESCRIPTION</span></span>
<span data-ttu-id="645cc-106">**AzureRmVMExtensionImageType** Cmdlet 會取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="645cc-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="645cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="645cc-107">EXAMPLES</span></span>

### <span data-ttu-id="645cc-108">範例1：取得延伸圖像類型</span><span class="sxs-lookup"><span data-stu-id="645cc-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="645cc-109">這個命令會取得指定發行者和位置的副檔名影像類型。</span><span class="sxs-lookup"><span data-stu-id="645cc-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="645cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="645cc-110">PARAMETERS</span></span>

### <span data-ttu-id="645cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645cc-111">-DefaultProfile</span></span>
<span data-ttu-id="645cc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="645cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="645cc-113">-位置</span><span class="sxs-lookup"><span data-stu-id="645cc-113">-Location</span></span>
<span data-ttu-id="645cc-114">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="645cc-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="645cc-115">這個 Cmdlet 會取得此參數指定位置的延伸類型。</span><span class="sxs-lookup"><span data-stu-id="645cc-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="645cc-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="645cc-116">-PublisherName</span></span>
<span data-ttu-id="645cc-117">指定副檔名發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="645cc-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="645cc-118">若要取得延伸發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="645cc-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="645cc-119">這個 Cmdlet 會從發行者取得此參數指定之延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="645cc-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="645cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645cc-120">CommonParameters</span></span>
<span data-ttu-id="645cc-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="645cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645cc-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="645cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645cc-123">輸入</span><span class="sxs-lookup"><span data-stu-id="645cc-123">INPUTS</span></span>

### <span data-ttu-id="645cc-124">所有</span><span class="sxs-lookup"><span data-stu-id="645cc-124">None</span></span>
<span data-ttu-id="645cc-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="645cc-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="645cc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="645cc-126">OUTPUTS</span></span>

### <span data-ttu-id="645cc-127">PSVirtualMachineExtensionImageType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="645cc-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="645cc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="645cc-128">NOTES</span></span>

## <span data-ttu-id="645cc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="645cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="645cc-130">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="645cc-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="645cc-131">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="645cc-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


