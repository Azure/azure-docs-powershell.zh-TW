---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ce726675946b2b8dc40feb82a529ccf27ccef443
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917378"
---
# <span data-ttu-id="9b6ad-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9b6ad-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="9b6ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6ad-103">獲得 Azure 擴充功能的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="9b6ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b6ad-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="9b6ad-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6ad-106">**Get-AzCMExtensionImdlet** 會取得 Azure 擴充功能的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="9b6ad-107">例子</span><span class="sxs-lookup"><span data-stu-id="9b6ad-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6ad-108">範例 1：取得擴充功能圖像的版本</span><span class="sxs-lookup"><span data-stu-id="9b6ad-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="9b6ad-109">此命令會針對指定的位置、發行者及類型，獲得擴充影像的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="9b6ad-110">範例 2：取得具有版本篩選的擴充功能圖像版本</span><span class="sxs-lookup"><span data-stu-id="9b6ad-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="9b6ad-111">此命令會從 12 開始，獲得指定位置、發行者、類型和版本的所有副檔名影像版本。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="9b6ad-112">範例 3：取得具有版本篩選的擴充功能圖像版本</span><span class="sxs-lookup"><span data-stu-id="9b6ad-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="9b6ad-113">此命令會針對指定的位置、發行者、類型和版本，獲得所有版本的擴充功能影像。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="9b6ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="9b6ad-114">PARAMETERS</span></span>

### <span data-ttu-id="9b6ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6ad-115">-DefaultProfile</span></span>
<span data-ttu-id="9b6ad-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6ad-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9b6ad-117">-FilterExpression</span></span>
<span data-ttu-id="9b6ad-118">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6ad-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9b6ad-119">-Location</span></span>
<span data-ttu-id="9b6ad-120">指定擴充功能的位置。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="9b6ad-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9b6ad-121">-PublisherName</span></span>
<span data-ttu-id="9b6ad-122">指定擴充功能發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="9b6ad-123">若要取得擴充功能發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9b6ad-124">-類型</span><span class="sxs-lookup"><span data-stu-id="9b6ad-124">-Type</span></span>
<span data-ttu-id="9b6ad-125">指定擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="9b6ad-126">若要取得擴充功能類型，請使用 Get-AzVMExtensionImageType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="9b6ad-127">-版本</span><span class="sxs-lookup"><span data-stu-id="9b6ad-127">-Version</span></span>
<span data-ttu-id="9b6ad-128">指定此 Cmdlet 的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9b6ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6ad-129">CommonParameters</span></span>
<span data-ttu-id="9b6ad-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6ad-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b6ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6ad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9b6ad-132">INPUTS</span></span>

### <span data-ttu-id="9b6ad-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9b6ad-133">System.String</span></span>

## <span data-ttu-id="9b6ad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9b6ad-134">OUTPUTS</span></span>

### <span data-ttu-id="9b6ad-135">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9b6ad-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="9b6ad-136">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="9b6ad-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="9b6ad-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9b6ad-137">NOTES</span></span>

## <span data-ttu-id="9b6ad-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b6ad-138">RELATED LINKS</span></span>

[<span data-ttu-id="9b6ad-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9b6ad-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="9b6ad-140">Get-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="9b6ad-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9b6ad-141">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b6ad-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


