---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 3421eec7fa723767db0dc896d0c3c40e7c5cbebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917185"
---
# <span data-ttu-id="ad895-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="ad895-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="ad895-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad895-102">SYNOPSIS</span></span>
<span data-ttu-id="ad895-103">一般發佈物件</span><span class="sxs-lookup"><span data-stu-id="ad895-103">Generic distribution object</span></span>

## <span data-ttu-id="ad895-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad895-104">SYNTAX</span></span>

### <span data-ttu-id="ad895-105">ManagedImageDistributor (預設) </span><span class="sxs-lookup"><span data-stu-id="ad895-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="ad895-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="ad895-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="ad895-108">描述</span><span class="sxs-lookup"><span data-stu-id="ad895-108">DESCRIPTION</span></span>
<span data-ttu-id="ad895-109">一般發佈物件</span><span class="sxs-lookup"><span data-stu-id="ad895-109">Generic distribution object</span></span>

## <span data-ttu-id="ad895-110">例子</span><span class="sxs-lookup"><span data-stu-id="ad895-110">EXAMPLES</span></span>

### <span data-ttu-id="ad895-111">範例 1：建立受管理的圖像發行者</span><span class="sxs-lookup"><span data-stu-id="ad895-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="ad895-112">此命令會建立受管理的映射發行者。</span><span class="sxs-lookup"><span data-stu-id="ad895-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="ad895-113">範例 2：建立 VHD 分配器</span><span class="sxs-lookup"><span data-stu-id="ad895-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="ad895-114">此命令會建立 VHD 分配器。</span><span class="sxs-lookup"><span data-stu-id="ad895-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="ad895-115">範例 3：建立共用圖像發行者</span><span class="sxs-lookup"><span data-stu-id="ad895-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="ad895-116">此命令會建立共用圖像發行者。</span><span class="sxs-lookup"><span data-stu-id="ad895-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="ad895-117">參數</span><span class="sxs-lookup"><span data-stu-id="ad895-117">PARAMETERS</span></span>

### <span data-ttu-id="ad895-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="ad895-118">-ArtifactTag</span></span>
<span data-ttu-id="ad895-119">發行者建立/更新之後，就會將之用於產品上的標記。</span><span class="sxs-lookup"><span data-stu-id="ad895-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="ad895-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="ad895-121">指出建立的圖像版本是否應該排除在最新版本中的標標。</span><span class="sxs-lookup"><span data-stu-id="ad895-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="ad895-122">省略以使用預設 (false) 。</span><span class="sxs-lookup"><span data-stu-id="ad895-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="ad895-123">-GalleryImageId</span></span>
<span data-ttu-id="ad895-124">共用圖像庫圖像的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad895-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="ad895-125">-ImageId</span></span>
<span data-ttu-id="ad895-126">受管理磁片映射的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad895-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-127">-位置</span><span class="sxs-lookup"><span data-stu-id="ad895-127">-Location</span></span>
<span data-ttu-id="ad895-128">如果圖像已存在，則影像的 Azure 位置應該相符。</span><span class="sxs-lookup"><span data-stu-id="ad895-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="ad895-130">以受管理的磁片映射發佈。</span><span class="sxs-lookup"><span data-stu-id="ad895-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="ad895-131">-ReplicationRegion</span></span>
<span data-ttu-id="ad895-132">影像要複製到的區域清單。</span><span class="sxs-lookup"><span data-stu-id="ad895-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="ad895-133">-RunOutputName</span></span>
<span data-ttu-id="ad895-134">用於關聯 RunOutput 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad895-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-135">-SharedImageDistributor</span></span>
<span data-ttu-id="ad895-136">透過共用圖像庫發佈。</span><span class="sxs-lookup"><span data-stu-id="ad895-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ad895-137">-StorageAccountType</span></span>
<span data-ttu-id="ad895-138">用來儲存共用圖像的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="ad895-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="ad895-139">省略以使用預設 (Standard_LRS) 。</span><span class="sxs-lookup"><span data-stu-id="ad895-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-140">-VhdDistributor</span></span>
<span data-ttu-id="ad895-141">透過儲存帳戶中的 VHD 發佈。</span><span class="sxs-lookup"><span data-stu-id="ad895-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad895-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad895-142">CommonParameters</span></span>
<span data-ttu-id="ad895-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad895-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad895-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad895-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad895-145">輸入</span><span class="sxs-lookup"><span data-stu-id="ad895-145">INPUTS</span></span>

## <span data-ttu-id="ad895-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ad895-146">OUTPUTS</span></span>

### <span data-ttu-id="ad895-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="ad895-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="ad895-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ad895-148">NOTES</span></span>

<span data-ttu-id="ad895-149">別名</span><span class="sxs-lookup"><span data-stu-id="ad895-149">ALIASES</span></span>

## <span data-ttu-id="ad895-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad895-150">RELATED LINKS</span></span>

