---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971262"
---
# <span data-ttu-id="daa53-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="daa53-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="daa53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daa53-102">SYNOPSIS</span></span>
<span data-ttu-id="daa53-103">取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="daa53-104">句法</span><span class="sxs-lookup"><span data-stu-id="daa53-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa53-105">說明</span><span class="sxs-lookup"><span data-stu-id="daa53-105">DESCRIPTION</span></span>
<span data-ttu-id="daa53-106">**AzVMExtensionImage** Cmdlet 會取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="daa53-107">示例</span><span class="sxs-lookup"><span data-stu-id="daa53-107">EXAMPLES</span></span>

### <span data-ttu-id="daa53-108">範例1：取得副檔名影像的版本</span><span class="sxs-lookup"><span data-stu-id="daa53-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="daa53-109">這個命令會取得指定位置、發行者及類型的所有副檔名影像版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="daa53-110">範例2：取得含篩選器版本的擴充影像版本</span><span class="sxs-lookup"><span data-stu-id="daa53-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="daa53-111">這個命令會從12開始，取得指定位置、發行者、類型及版本的擴充影像所有版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="daa53-112">範例3：取得含篩選器版本的擴充影像版本</span><span class="sxs-lookup"><span data-stu-id="daa53-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="daa53-113">這個命令會取得指定位置、發行者、類型及版本的擴充影像的所有版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="daa53-114">參數</span><span class="sxs-lookup"><span data-stu-id="daa53-114">PARAMETERS</span></span>

### <span data-ttu-id="daa53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa53-115">-DefaultProfile</span></span>
<span data-ttu-id="daa53-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="daa53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa53-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="daa53-117">-FilterExpression</span></span>
<span data-ttu-id="daa53-118">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="daa53-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="daa53-119">-位置</span><span class="sxs-lookup"><span data-stu-id="daa53-119">-Location</span></span>
<span data-ttu-id="daa53-120">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="daa53-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="daa53-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="daa53-121">-PublisherName</span></span>
<span data-ttu-id="daa53-122">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="daa53-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="daa53-123">若要取得延伸發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daa53-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="daa53-124">-類型</span><span class="sxs-lookup"><span data-stu-id="daa53-124">-Type</span></span>
<span data-ttu-id="daa53-125">指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="daa53-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="daa53-126">若要取得延伸類型，請使用 Get-AzVMExtensionImageType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daa53-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="daa53-127">-版本</span><span class="sxs-lookup"><span data-stu-id="daa53-127">-Version</span></span>
<span data-ttu-id="daa53-128">指定此 Cmdlet 取得的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="daa53-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="daa53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa53-129">CommonParameters</span></span>
<span data-ttu-id="daa53-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daa53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa53-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="daa53-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa53-132">輸入</span><span class="sxs-lookup"><span data-stu-id="daa53-132">INPUTS</span></span>

### <span data-ttu-id="daa53-133">System.object</span><span class="sxs-lookup"><span data-stu-id="daa53-133">System.String</span></span>

## <span data-ttu-id="daa53-134">輸出</span><span class="sxs-lookup"><span data-stu-id="daa53-134">OUTPUTS</span></span>

### <span data-ttu-id="daa53-135">PSVirtualMachineExtensionImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="daa53-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="daa53-136">PSVirtualMachineExtensionImageDetails 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="daa53-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="daa53-137">筆記</span><span class="sxs-lookup"><span data-stu-id="daa53-137">NOTES</span></span>

## <span data-ttu-id="daa53-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="daa53-138">RELATED LINKS</span></span>

[<span data-ttu-id="daa53-139">AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="daa53-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="daa53-140">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="daa53-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="daa53-141">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="daa53-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


