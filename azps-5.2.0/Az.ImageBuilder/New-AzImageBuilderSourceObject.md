---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278252"
---
# <span data-ttu-id="ec46a-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="ec46a-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="ec46a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec46a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec46a-103">描述建立、自訂及發佈的虛擬機器影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="ec46a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec46a-104">SYNTAX</span></span>

### <span data-ttu-id="ec46a-105">ManagedImage (預設) </span><span class="sxs-lookup"><span data-stu-id="ec46a-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec46a-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="ec46a-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec46a-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="ec46a-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec46a-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="ec46a-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec46a-109">說明</span><span class="sxs-lookup"><span data-stu-id="ec46a-109">DESCRIPTION</span></span>
<span data-ttu-id="ec46a-110">描述建立、自訂及發佈的虛擬機器影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="ec46a-111">示例</span><span class="sxs-lookup"><span data-stu-id="ec46a-111">EXAMPLES</span></span>

### <span data-ttu-id="ec46a-112">範例1：建立受管理的影像來源</span><span class="sxs-lookup"><span data-stu-id="ec46a-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="ec46a-113">這個命令會建立受管理的影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="ec46a-114">範例2：建立共用的影像來源</span><span class="sxs-lookup"><span data-stu-id="ec46a-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="ec46a-115">這個命令會建立共用的影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="ec46a-116">範例3：建立 platfrom 影像來源</span><span class="sxs-lookup"><span data-stu-id="ec46a-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="ec46a-117">這個命令會建立 platfrom 影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="ec46a-118">參數</span><span class="sxs-lookup"><span data-stu-id="ec46a-118">PARAMETERS</span></span>

### <span data-ttu-id="ec46a-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="ec46a-119">-ImageId</span></span>
<span data-ttu-id="ec46a-120">客戶訂閱中受管理之影像的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec46a-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="ec46a-121">-ImageVersionId</span></span>
<span data-ttu-id="ec46a-122">共用影像圖庫中影像版本的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec46a-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-123">-優惠</span><span class="sxs-lookup"><span data-stu-id="ec46a-123">-Offer</span></span>
<span data-ttu-id="ec46a-124">從 [Azure 圖庫影像](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)提供的影像。</span><span class="sxs-lookup"><span data-stu-id="ec46a-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ec46a-125">-PlanName</span></span>
<span data-ttu-id="ec46a-126">採購方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46a-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ec46a-127">-PlanProduct</span></span>
<span data-ttu-id="ec46a-128">購買方案的產品。</span><span class="sxs-lookup"><span data-stu-id="ec46a-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ec46a-129">-PlanPublisher</span></span>
<span data-ttu-id="ec46a-130">購買方案的發行者。</span><span class="sxs-lookup"><span data-stu-id="ec46a-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ec46a-131">-Publisher</span></span>
<span data-ttu-id="ec46a-132">[Azure 圖庫影像](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)中的圖像發行者。</span><span class="sxs-lookup"><span data-stu-id="ec46a-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="ec46a-133">-Sku</span></span>
<span data-ttu-id="ec46a-134">來自 [Azure 圖庫影像](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)的影像 sku。</span><span class="sxs-lookup"><span data-stu-id="ec46a-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="ec46a-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="ec46a-136">描述在客戶訂閱中受管理的影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="ec46a-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="ec46a-138">描述來自 [Azure 圖庫影像](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)的影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="ec46a-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="ec46a-140">描述共用影像圖庫中影像版本的影像來源。</span><span class="sxs-lookup"><span data-stu-id="ec46a-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-141">-版本</span><span class="sxs-lookup"><span data-stu-id="ec46a-141">-Version</span></span>
<span data-ttu-id="ec46a-142">來自 [Azure 圖庫影像](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)的影像版本。</span><span class="sxs-lookup"><span data-stu-id="ec46a-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec46a-143">CommonParameters</span></span>
<span data-ttu-id="ec46a-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec46a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec46a-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec46a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec46a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ec46a-146">INPUTS</span></span>

## <span data-ttu-id="ec46a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ec46a-147">OUTPUTS</span></span>

### <span data-ttu-id="ec46a-148">IImageTemplateSource （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="ec46a-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="ec46a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="ec46a-149">NOTES</span></span>

<span data-ttu-id="ec46a-150">別名</span><span class="sxs-lookup"><span data-stu-id="ec46a-150">ALIASES</span></span>

## <span data-ttu-id="ec46a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec46a-151">RELATED LINKS</span></span>

