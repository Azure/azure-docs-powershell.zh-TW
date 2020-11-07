---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
ms.openlocfilehash: ccb48064bb2d6b91801a58ecfa9d229a748889a8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801053"
---
# <span data-ttu-id="3f855-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3f855-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="3f855-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f855-102">SYNOPSIS</span></span>
<span data-ttu-id="3f855-103">取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="3f855-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f855-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f855-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f855-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f855-105">DESCRIPTION</span></span>
<span data-ttu-id="3f855-106">**AzureRmVMExtensionImage** Cmdlet 會取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="3f855-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3f855-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f855-107">EXAMPLES</span></span>

### <span data-ttu-id="3f855-108">範例1：取得副檔名影像的版本</span><span class="sxs-lookup"><span data-stu-id="3f855-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="3f855-109">這個命令會取得指定位置、發行者及類型的所有副檔名影像版本。</span><span class="sxs-lookup"><span data-stu-id="3f855-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="3f855-110">參數</span><span class="sxs-lookup"><span data-stu-id="3f855-110">PARAMETERS</span></span>

### <span data-ttu-id="3f855-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f855-111">-DefaultProfile</span></span>
<span data-ttu-id="3f855-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f855-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f855-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3f855-113">-FilterExpression</span></span>
<span data-ttu-id="3f855-114">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="3f855-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f855-115">-位置</span><span class="sxs-lookup"><span data-stu-id="3f855-115">-Location</span></span>
<span data-ttu-id="3f855-116">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="3f855-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="3f855-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3f855-117">-PublisherName</span></span>
<span data-ttu-id="3f855-118">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f855-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="3f855-119">若要取得延伸發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f855-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="3f855-120">-類型</span><span class="sxs-lookup"><span data-stu-id="3f855-120">-Type</span></span>
<span data-ttu-id="3f855-121">指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="3f855-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="3f855-122">若要取得延伸類型，請使用 Get-AzureRmVMExtensionImageType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f855-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="3f855-123">-版本</span><span class="sxs-lookup"><span data-stu-id="3f855-123">-Version</span></span>
<span data-ttu-id="3f855-124">指定此 Cmdlet 取得的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="3f855-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f855-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f855-125">CommonParameters</span></span>
<span data-ttu-id="3f855-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f855-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f855-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f855-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f855-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3f855-128">INPUTS</span></span>

### <span data-ttu-id="3f855-129">所有</span><span class="sxs-lookup"><span data-stu-id="3f855-129">None</span></span>
<span data-ttu-id="3f855-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3f855-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f855-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3f855-131">OUTPUTS</span></span>

### <span data-ttu-id="3f855-132">PSVirtualMachineExtensionImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3f855-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="3f855-133">PSVirtualMachineExtensionImageDetails 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3f855-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="3f855-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3f855-134">NOTES</span></span>

## <span data-ttu-id="3f855-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f855-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f855-136">AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3f855-136">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="3f855-137">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3f855-137">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="3f855-138">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3f855-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


