---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 57520697c0107cdf81bf55e562e78bd991a73fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957404"
---
# <span data-ttu-id="6fe53-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6fe53-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="6fe53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fe53-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe53-103">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="6fe53-103">Create a gallery image version.</span></span>

## <span data-ttu-id="6fe53-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fe53-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe53-105">說明</span><span class="sxs-lookup"><span data-stu-id="6fe53-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe53-106">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="6fe53-106">Create a gallery image version.</span></span>

## <span data-ttu-id="6fe53-107">示例</span><span class="sxs-lookup"><span data-stu-id="6fe53-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe53-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6fe53-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="6fe53-109">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="6fe53-109">Create a gallery image version.</span></span>

### <span data-ttu-id="6fe53-110">範例2</span><span class="sxs-lookup"><span data-stu-id="6fe53-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="6fe53-111">使用磁片影像加密建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="6fe53-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="6fe53-112">參數</span><span class="sxs-lookup"><span data-stu-id="6fe53-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe53-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fe53-113">-AsJob</span></span>
<span data-ttu-id="6fe53-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6fe53-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="6fe53-115">-DataDiskImage</span></span>
<span data-ttu-id="6fe53-116">資料磁片影像。</span><span class="sxs-lookup"><span data-stu-id="6fe53-116">Data disk images.</span></span>   <span data-ttu-id="6fe53-117">例如，@ {Source = @ {Id =<source_id>};Lun = 1;SizeInGB = 100;HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="6fe53-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe53-118">-DefaultProfile</span></span>
<span data-ttu-id="6fe53-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fe53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe53-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6fe53-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="6fe53-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fe53-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6fe53-122">-GalleryName</span></span>
<span data-ttu-id="6fe53-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fe53-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-124">-位置</span><span class="sxs-lookup"><span data-stu-id="6fe53-124">-Location</span></span>
<span data-ttu-id="6fe53-125">資源位置</span><span class="sxs-lookup"><span data-stu-id="6fe53-125">Resource location</span></span>

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

### <span data-ttu-id="6fe53-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fe53-126">-Name</span></span>
<span data-ttu-id="6fe53-127">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fe53-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="6fe53-128">-OSDiskImage</span></span>
<span data-ttu-id="6fe53-129">OS 磁片圖像（例如 @ {Source = @ {Id =<source_id>};SizeInGB = 100;HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="6fe53-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6fe53-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="6fe53-131">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="6fe53-131">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="6fe53-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="6fe53-133">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="6fe53-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6fe53-134">-ReplicaCount</span></span>
<span data-ttu-id="6fe53-135">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="6fe53-135">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe53-136">-ResourceGroupName</span></span>
<span data-ttu-id="6fe53-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fe53-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="6fe53-138">-SourceImageId</span></span>
<span data-ttu-id="6fe53-139">要建立影像版本之來源影像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fe53-139">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6fe53-140">-StorageAccountType</span></span>
<span data-ttu-id="6fe53-141">指定要用來儲存影像的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="6fe53-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="6fe53-142">這個屬性無法更新。</span><span class="sxs-lookup"><span data-stu-id="6fe53-142">This property is not updatable.</span></span> <span data-ttu-id="6fe53-143">可用的值 Standard_LRS 和 Standard_ZRS。</span><span class="sxs-lookup"><span data-stu-id="6fe53-143">Available values are Standard_LRS and Standard_ZRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fe53-144">-Tag</span></span>
<span data-ttu-id="6fe53-145">資源標記</span><span class="sxs-lookup"><span data-stu-id="6fe53-145">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="6fe53-146">-TargetRegion</span></span>
<span data-ttu-id="6fe53-147">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="6fe53-147">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-148">-確認</span><span class="sxs-lookup"><span data-stu-id="6fe53-148">-Confirm</span></span>
<span data-ttu-id="6fe53-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fe53-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe53-150">-WhatIf</span></span>
<span data-ttu-id="6fe53-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fe53-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe53-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fe53-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe53-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe53-153">CommonParameters</span></span>
<span data-ttu-id="6fe53-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fe53-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe53-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6fe53-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe53-156">輸入</span><span class="sxs-lookup"><span data-stu-id="6fe53-156">INPUTS</span></span>

### <span data-ttu-id="6fe53-157">System.object</span><span class="sxs-lookup"><span data-stu-id="6fe53-157">System.String</span></span>

### <span data-ttu-id="6fe53-158">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6fe53-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6fe53-159">System.object</span><span class="sxs-lookup"><span data-stu-id="6fe53-159">System.Int32</span></span>

### <span data-ttu-id="6fe53-160">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="6fe53-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6fe53-161">System.object</span><span class="sxs-lookup"><span data-stu-id="6fe53-161">System.DateTime</span></span>

### <span data-ttu-id="6fe53-162">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="6fe53-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="6fe53-163">輸出</span><span class="sxs-lookup"><span data-stu-id="6fe53-163">OUTPUTS</span></span>

### <span data-ttu-id="6fe53-164">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6fe53-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="6fe53-165">筆記</span><span class="sxs-lookup"><span data-stu-id="6fe53-165">NOTES</span></span>

## <span data-ttu-id="6fe53-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fe53-166">RELATED LINKS</span></span>
