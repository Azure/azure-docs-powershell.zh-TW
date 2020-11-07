---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796245"
---
# <span data-ttu-id="55e7d-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="55e7d-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="55e7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="55e7d-103">取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="55e7d-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="55e7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="55e7d-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55e7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="55e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="55e7d-106">**AzVMExtensionImage** Cmdlet 會取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="55e7d-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="55e7d-107">示例</span><span class="sxs-lookup"><span data-stu-id="55e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="55e7d-108">範例1：取得副檔名影像的版本</span><span class="sxs-lookup"><span data-stu-id="55e7d-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="55e7d-109">這個命令會取得指定位置、發行者及類型的所有副檔名影像版本。</span><span class="sxs-lookup"><span data-stu-id="55e7d-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="55e7d-110">參數</span><span class="sxs-lookup"><span data-stu-id="55e7d-110">PARAMETERS</span></span>

### <span data-ttu-id="55e7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e7d-111">-DefaultProfile</span></span>
<span data-ttu-id="55e7d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55e7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e7d-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="55e7d-113">-FilterExpression</span></span>
<span data-ttu-id="55e7d-114">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="55e7d-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="55e7d-115">-位置</span><span class="sxs-lookup"><span data-stu-id="55e7d-115">-Location</span></span>
<span data-ttu-id="55e7d-116">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="55e7d-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="55e7d-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="55e7d-117">-PublisherName</span></span>
<span data-ttu-id="55e7d-118">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e7d-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="55e7d-119">若要取得延伸發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e7d-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="55e7d-120">-類型</span><span class="sxs-lookup"><span data-stu-id="55e7d-120">-Type</span></span>
<span data-ttu-id="55e7d-121">指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="55e7d-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="55e7d-122">若要取得延伸類型，請使用 Get-AzVMExtensionImageType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e7d-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="55e7d-123">-版本</span><span class="sxs-lookup"><span data-stu-id="55e7d-123">-Version</span></span>
<span data-ttu-id="55e7d-124">指定此 Cmdlet 取得的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="55e7d-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55e7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e7d-125">CommonParameters</span></span>
<span data-ttu-id="55e7d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55e7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e7d-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55e7d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e7d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="55e7d-128">INPUTS</span></span>

### <span data-ttu-id="55e7d-129">所有</span><span class="sxs-lookup"><span data-stu-id="55e7d-129">None</span></span>
<span data-ttu-id="55e7d-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="55e7d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55e7d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="55e7d-131">OUTPUTS</span></span>

### <span data-ttu-id="55e7d-132">PSVirtualMachineExtensionImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="55e7d-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="55e7d-133">PSVirtualMachineExtensionImageDetails 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="55e7d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="55e7d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="55e7d-134">NOTES</span></span>

## <span data-ttu-id="55e7d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="55e7d-135">RELATED LINKS</span></span>

[<span data-ttu-id="55e7d-136">AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="55e7d-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="55e7d-137">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="55e7d-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="55e7d-138">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="55e7d-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


