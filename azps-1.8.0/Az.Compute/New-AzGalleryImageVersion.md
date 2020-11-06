---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622759"
---
# <span data-ttu-id="24554-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="24554-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="24554-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24554-102">SYNOPSIS</span></span>
<span data-ttu-id="24554-103">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="24554-103">Create a gallery image version.</span></span>

## <span data-ttu-id="24554-104">句法</span><span class="sxs-lookup"><span data-stu-id="24554-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24554-105">說明</span><span class="sxs-lookup"><span data-stu-id="24554-105">DESCRIPTION</span></span>
<span data-ttu-id="24554-106">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="24554-106">Create a gallery image version.</span></span>

## <span data-ttu-id="24554-107">示例</span><span class="sxs-lookup"><span data-stu-id="24554-107">EXAMPLES</span></span>

### <span data-ttu-id="24554-108">範例1</span><span class="sxs-lookup"><span data-stu-id="24554-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="24554-109">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="24554-109">Create a gallery image version.</span></span>

## <span data-ttu-id="24554-110">參數</span><span class="sxs-lookup"><span data-stu-id="24554-110">PARAMETERS</span></span>

### <span data-ttu-id="24554-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24554-111">-AsJob</span></span>
<span data-ttu-id="24554-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24554-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24554-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24554-113">-DefaultProfile</span></span>
<span data-ttu-id="24554-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24554-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24554-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="24554-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="24554-116">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="24554-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="24554-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="24554-117">-GalleryName</span></span>
<span data-ttu-id="24554-118">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="24554-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="24554-119">-位置</span><span class="sxs-lookup"><span data-stu-id="24554-119">-Location</span></span>
<span data-ttu-id="24554-120">資源位置</span><span class="sxs-lookup"><span data-stu-id="24554-120">Resource location</span></span>

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

### <span data-ttu-id="24554-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="24554-121">-Name</span></span>
<span data-ttu-id="24554-122">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="24554-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="24554-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="24554-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="24554-124">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="24554-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="24554-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="24554-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="24554-126">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="24554-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="24554-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="24554-127">-ReplicaCount</span></span>
<span data-ttu-id="24554-128">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="24554-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="24554-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24554-129">-ResourceGroupName</span></span>
<span data-ttu-id="24554-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24554-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="24554-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="24554-131">-SourceImageId</span></span>
<span data-ttu-id="24554-132">要建立影像版本之來源影像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="24554-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="24554-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="24554-133">-Tag</span></span>
<span data-ttu-id="24554-134">資源標記</span><span class="sxs-lookup"><span data-stu-id="24554-134">Resource tags</span></span>

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

### <span data-ttu-id="24554-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="24554-135">-TargetRegion</span></span>
<span data-ttu-id="24554-136">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="24554-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="24554-137">-確認</span><span class="sxs-lookup"><span data-stu-id="24554-137">-Confirm</span></span>
<span data-ttu-id="24554-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24554-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24554-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24554-139">-WhatIf</span></span>
<span data-ttu-id="24554-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24554-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24554-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24554-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24554-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24554-142">CommonParameters</span></span>
<span data-ttu-id="24554-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24554-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24554-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24554-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24554-145">輸入</span><span class="sxs-lookup"><span data-stu-id="24554-145">INPUTS</span></span>

### <span data-ttu-id="24554-146">System.object</span><span class="sxs-lookup"><span data-stu-id="24554-146">System.String</span></span>

### <span data-ttu-id="24554-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24554-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="24554-148">System.object</span><span class="sxs-lookup"><span data-stu-id="24554-148">System.Int32</span></span>

### <span data-ttu-id="24554-149">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="24554-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="24554-150">System.object</span><span class="sxs-lookup"><span data-stu-id="24554-150">System.DateTime</span></span>

### <span data-ttu-id="24554-151">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="24554-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="24554-152">輸出</span><span class="sxs-lookup"><span data-stu-id="24554-152">OUTPUTS</span></span>

### <span data-ttu-id="24554-153">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="24554-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="24554-154">筆記</span><span class="sxs-lookup"><span data-stu-id="24554-154">NOTES</span></span>

## <span data-ttu-id="24554-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="24554-155">RELATED LINKS</span></span>
