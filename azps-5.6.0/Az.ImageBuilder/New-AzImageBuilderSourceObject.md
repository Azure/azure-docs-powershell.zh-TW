---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917182"
---
# <span data-ttu-id="302ea-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="302ea-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="302ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="302ea-102">SYNOPSIS</span></span>
<span data-ttu-id="302ea-103">說明建立、自訂及散發的虛擬機器映射來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="302ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="302ea-104">SYNTAX</span></span>

### <span data-ttu-id="302ea-105">ManagedImage (預設) </span><span class="sxs-lookup"><span data-stu-id="302ea-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="302ea-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="302ea-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="302ea-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="302ea-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="302ea-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="302ea-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="302ea-109">描述</span><span class="sxs-lookup"><span data-stu-id="302ea-109">DESCRIPTION</span></span>
<span data-ttu-id="302ea-110">說明建立、自訂及散發的虛擬機器映射來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="302ea-111">例子</span><span class="sxs-lookup"><span data-stu-id="302ea-111">EXAMPLES</span></span>

### <span data-ttu-id="302ea-112">範例 1：建立受管理的影像來源</span><span class="sxs-lookup"><span data-stu-id="302ea-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="302ea-113">此命令會建立受管理的影像來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="302ea-114">範例 2：建立共用圖像來源</span><span class="sxs-lookup"><span data-stu-id="302ea-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="302ea-115">此命令會建立共用圖像來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="302ea-116">範例 3：建立一個 platfrom 圖像來源</span><span class="sxs-lookup"><span data-stu-id="302ea-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="302ea-117">此命令會建立一個圖像來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="302ea-118">參數</span><span class="sxs-lookup"><span data-stu-id="302ea-118">PARAMETERS</span></span>

### <span data-ttu-id="302ea-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="302ea-119">-ImageId</span></span>
<span data-ttu-id="302ea-120">客戶訂閱中受管理圖像的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="302ea-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="302ea-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="302ea-121">-ImageVersionId</span></span>
<span data-ttu-id="302ea-122">共用圖像庫中影像版本的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="302ea-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="302ea-123">-優惠</span><span class="sxs-lookup"><span data-stu-id="302ea-123">-Offer</span></span>
<span data-ttu-id="302ea-124">Azure 圖庫 [圖像中的影像優惠](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)。</span><span class="sxs-lookup"><span data-stu-id="302ea-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="302ea-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="302ea-125">-PlanName</span></span>
<span data-ttu-id="302ea-126">購買方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="302ea-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="302ea-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="302ea-127">-PlanProduct</span></span>
<span data-ttu-id="302ea-128">購買方案的產品。</span><span class="sxs-lookup"><span data-stu-id="302ea-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="302ea-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="302ea-129">-PlanPublisher</span></span>
<span data-ttu-id="302ea-130">購買計畫的發行者。</span><span class="sxs-lookup"><span data-stu-id="302ea-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="302ea-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="302ea-131">-Publisher</span></span>
<span data-ttu-id="302ea-132">Azure 圖庫 [圖像中的圖像](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)Publisher。</span><span class="sxs-lookup"><span data-stu-id="302ea-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="302ea-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="302ea-133">-Sku</span></span>
<span data-ttu-id="302ea-134">Azure 圖庫圖像[中的影像 SKU。](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="302ea-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="302ea-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="302ea-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="302ea-136">說明客戶訂閱中受管理的影像來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="302ea-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="302ea-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="302ea-138">說明來自 Azure 圖庫 [圖像的圖像來源](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)。</span><span class="sxs-lookup"><span data-stu-id="302ea-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="302ea-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="302ea-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="302ea-140">說明共用圖像庫中的圖像版本圖像來源。</span><span class="sxs-lookup"><span data-stu-id="302ea-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="302ea-141">-版本</span><span class="sxs-lookup"><span data-stu-id="302ea-141">-Version</span></span>
<span data-ttu-id="302ea-142">Azure 圖庫 [圖像的圖像版本](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)。</span><span class="sxs-lookup"><span data-stu-id="302ea-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="302ea-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302ea-143">CommonParameters</span></span>
<span data-ttu-id="302ea-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="302ea-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302ea-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="302ea-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302ea-146">輸入</span><span class="sxs-lookup"><span data-stu-id="302ea-146">INPUTS</span></span>

## <span data-ttu-id="302ea-147">輸出</span><span class="sxs-lookup"><span data-stu-id="302ea-147">OUTPUTS</span></span>

### <span data-ttu-id="302ea-148">Microsoft.Azure.PowerShell.Cmdlets.ImageSourceer.models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="302ea-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="302ea-149">筆記</span><span class="sxs-lookup"><span data-stu-id="302ea-149">NOTES</span></span>

<span data-ttu-id="302ea-150">別名</span><span class="sxs-lookup"><span data-stu-id="302ea-150">ALIASES</span></span>

## <span data-ttu-id="302ea-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="302ea-151">RELATED LINKS</span></span>

