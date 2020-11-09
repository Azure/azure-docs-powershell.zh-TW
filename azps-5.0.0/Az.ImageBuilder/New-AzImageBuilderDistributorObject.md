---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284412"
---
# <span data-ttu-id="aa9aa-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="aa9aa-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="aa9aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9aa-103">一般分佈物件</span><span class="sxs-lookup"><span data-stu-id="aa9aa-103">Generic distribution object</span></span>

## <span data-ttu-id="aa9aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa9aa-104">SYNTAX</span></span>

### <span data-ttu-id="aa9aa-105">ManagedImageDistributor (預設) </span><span class="sxs-lookup"><span data-stu-id="aa9aa-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="aa9aa-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="aa9aa-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="aa9aa-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="aa9aa-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="aa9aa-108">說明</span><span class="sxs-lookup"><span data-stu-id="aa9aa-108">DESCRIPTION</span></span>
<span data-ttu-id="aa9aa-109">一般分佈物件</span><span class="sxs-lookup"><span data-stu-id="aa9aa-109">Generic distribution object</span></span>

## <span data-ttu-id="aa9aa-110">示例</span><span class="sxs-lookup"><span data-stu-id="aa9aa-110">EXAMPLES</span></span>

### <span data-ttu-id="aa9aa-111">範例1：建立受管理的映射分發伺服器</span><span class="sxs-lookup"><span data-stu-id="aa9aa-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="aa9aa-112">這個命令會建立受管理的映射分發伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="aa9aa-113">範例2：建立 VHD 分發伺服器</span><span class="sxs-lookup"><span data-stu-id="aa9aa-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="aa9aa-114">這個命令會建立 VHD 發行商。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="aa9aa-115">範例3：建立共用的影像分發伺服器</span><span class="sxs-lookup"><span data-stu-id="aa9aa-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="aa9aa-116">這個命令會建立共用的影像分發伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="aa9aa-117">參數</span><span class="sxs-lookup"><span data-stu-id="aa9aa-117">PARAMETERS</span></span>

### <span data-ttu-id="aa9aa-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="aa9aa-118">-ArtifactTag</span></span>
<span data-ttu-id="aa9aa-119">在由分銷商建立/更新後，會套用到專案的標記。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="aa9aa-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="aa9aa-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="aa9aa-121">指示是否應將所建立的影像版本排除在最新的標記。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="aa9aa-122">[忽略] 使用預設 (false) 。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="aa9aa-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="aa9aa-123">-GalleryImageId</span></span>
<span data-ttu-id="aa9aa-124">共用影像庫影像的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="aa9aa-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="aa9aa-125">-ImageId</span></span>
<span data-ttu-id="aa9aa-126">受管理磁片映射的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="aa9aa-127">-位置</span><span class="sxs-lookup"><span data-stu-id="aa9aa-127">-Location</span></span>
<span data-ttu-id="aa9aa-128">影像的 Azure 位置應該與映射已存在相符。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="aa9aa-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="aa9aa-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="aa9aa-130">發佈成受管理的磁片影像。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="aa9aa-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="aa9aa-131">-ReplicationRegion</span></span>
<span data-ttu-id="aa9aa-132">要將影像複製到其中的地區清單。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="aa9aa-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="aa9aa-133">-RunOutputName</span></span>
<span data-ttu-id="aa9aa-134">要用於關聯 RunOutput 的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="aa9aa-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="aa9aa-135">-SharedImageDistributor</span></span>
<span data-ttu-id="aa9aa-136">透過共用圖像庫散佈。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="aa9aa-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aa9aa-137">-StorageAccountType</span></span>
<span data-ttu-id="aa9aa-138">儲存空間帳戶類型，用來儲存共用的影像。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="aa9aa-139">[忽略]，使用預設 (Standard_LRS) 。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="aa9aa-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="aa9aa-140">-VhdDistributor</span></span>
<span data-ttu-id="aa9aa-141">透過 VHD 在儲存帳戶中發佈。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="aa9aa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9aa-142">CommonParameters</span></span>
<span data-ttu-id="aa9aa-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9aa-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9aa-145">輸入</span><span class="sxs-lookup"><span data-stu-id="aa9aa-145">INPUTS</span></span>

## <span data-ttu-id="aa9aa-146">輸出</span><span class="sxs-lookup"><span data-stu-id="aa9aa-146">OUTPUTS</span></span>

### <span data-ttu-id="aa9aa-147">IImageTemplateDistributor （ImageBuilder）。 Api20200214。</span><span class="sxs-lookup"><span data-stu-id="aa9aa-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="aa9aa-148">筆記</span><span class="sxs-lookup"><span data-stu-id="aa9aa-148">NOTES</span></span>

<span data-ttu-id="aa9aa-149">別名</span><span class="sxs-lookup"><span data-stu-id="aa9aa-149">ALIASES</span></span>

## <span data-ttu-id="aa9aa-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa9aa-150">RELATED LINKS</span></span>

