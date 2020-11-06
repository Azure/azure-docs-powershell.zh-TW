---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613319"
---
# <span data-ttu-id="4da56-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4da56-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="4da56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4da56-102">SYNOPSIS</span></span>
<span data-ttu-id="4da56-103">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="4da56-103">Create a gallery image version.</span></span>

## <span data-ttu-id="4da56-104">句法</span><span class="sxs-lookup"><span data-stu-id="4da56-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da56-105">說明</span><span class="sxs-lookup"><span data-stu-id="4da56-105">DESCRIPTION</span></span>
<span data-ttu-id="4da56-106">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="4da56-106">Create a gallery image version.</span></span>

## <span data-ttu-id="4da56-107">示例</span><span class="sxs-lookup"><span data-stu-id="4da56-107">EXAMPLES</span></span>

### <span data-ttu-id="4da56-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4da56-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="4da56-109">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="4da56-109">Create a gallery image version.</span></span>

## <span data-ttu-id="4da56-110">參數</span><span class="sxs-lookup"><span data-stu-id="4da56-110">PARAMETERS</span></span>

### <span data-ttu-id="4da56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4da56-111">-AsJob</span></span>
<span data-ttu-id="4da56-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4da56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4da56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da56-113">-DefaultProfile</span></span>
<span data-ttu-id="4da56-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4da56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da56-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4da56-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="4da56-116">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da56-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="4da56-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4da56-117">-GalleryName</span></span>
<span data-ttu-id="4da56-118">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da56-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="4da56-119">-位置</span><span class="sxs-lookup"><span data-stu-id="4da56-119">-Location</span></span>
<span data-ttu-id="4da56-120">資源位置</span><span class="sxs-lookup"><span data-stu-id="4da56-120">Resource location</span></span>

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

### <span data-ttu-id="4da56-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4da56-121">-Name</span></span>
<span data-ttu-id="4da56-122">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da56-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="4da56-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="4da56-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="4da56-124">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="4da56-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="4da56-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="4da56-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="4da56-126">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="4da56-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="4da56-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4da56-127">-ReplicaCount</span></span>
<span data-ttu-id="4da56-128">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="4da56-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="4da56-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da56-129">-ResourceGroupName</span></span>
<span data-ttu-id="4da56-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da56-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="4da56-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="4da56-131">-SourceImageId</span></span>
<span data-ttu-id="4da56-132">要建立影像版本之來源影像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4da56-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="4da56-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4da56-133">-StorageAccountType</span></span>
<span data-ttu-id="4da56-134">指定要用來儲存影像的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="4da56-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="4da56-135">這個屬性無法更新。</span><span class="sxs-lookup"><span data-stu-id="4da56-135">This property is not updatable.</span></span> <span data-ttu-id="4da56-136">可用的值 Standard_LRS 和 Standard_ZRS。</span><span class="sxs-lookup"><span data-stu-id="4da56-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="4da56-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="4da56-137">-Tag</span></span>
<span data-ttu-id="4da56-138">資源標記</span><span class="sxs-lookup"><span data-stu-id="4da56-138">Resource tags</span></span>

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

### <span data-ttu-id="4da56-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="4da56-139">-TargetRegion</span></span>
<span data-ttu-id="4da56-140">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="4da56-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="4da56-141">-確認</span><span class="sxs-lookup"><span data-stu-id="4da56-141">-Confirm</span></span>
<span data-ttu-id="4da56-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4da56-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da56-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da56-143">-WhatIf</span></span>
<span data-ttu-id="4da56-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4da56-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da56-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4da56-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da56-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da56-146">CommonParameters</span></span>
<span data-ttu-id="4da56-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4da56-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da56-148">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4da56-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da56-149">輸入</span><span class="sxs-lookup"><span data-stu-id="4da56-149">INPUTS</span></span>

### <span data-ttu-id="4da56-150">System.object</span><span class="sxs-lookup"><span data-stu-id="4da56-150">System.String</span></span>

### <span data-ttu-id="4da56-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4da56-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4da56-152">System.object</span><span class="sxs-lookup"><span data-stu-id="4da56-152">System.Int32</span></span>

### <span data-ttu-id="4da56-153">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4da56-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4da56-154">System.object</span><span class="sxs-lookup"><span data-stu-id="4da56-154">System.DateTime</span></span>

### <span data-ttu-id="4da56-155">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="4da56-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="4da56-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4da56-156">OUTPUTS</span></span>

### <span data-ttu-id="4da56-157">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4da56-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="4da56-158">筆記</span><span class="sxs-lookup"><span data-stu-id="4da56-158">NOTES</span></span>

## <span data-ttu-id="4da56-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="4da56-159">RELATED LINKS</span></span>
