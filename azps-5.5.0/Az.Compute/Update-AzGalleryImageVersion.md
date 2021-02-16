---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129782"
---
# <span data-ttu-id="2a87b-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2a87b-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="2a87b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a87b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a87b-103">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="2a87b-103">Update a gallery image version.</span></span>

## <span data-ttu-id="2a87b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a87b-104">SYNTAX</span></span>

### <span data-ttu-id="2a87b-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2a87b-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a87b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2a87b-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a87b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2a87b-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a87b-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a87b-108">DESCRIPTION</span></span>
<span data-ttu-id="2a87b-109">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="2a87b-109">Update a gallery image version.</span></span>

## <span data-ttu-id="2a87b-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a87b-110">EXAMPLES</span></span>

### <span data-ttu-id="2a87b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2a87b-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="2a87b-112">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="2a87b-112">Update a gallery image version.</span></span>

## <span data-ttu-id="2a87b-113">參數</span><span class="sxs-lookup"><span data-stu-id="2a87b-113">PARAMETERS</span></span>

### <span data-ttu-id="2a87b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a87b-114">-AsJob</span></span>
<span data-ttu-id="2a87b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2a87b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a87b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a87b-116">-DefaultProfile</span></span>
<span data-ttu-id="2a87b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a87b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a87b-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2a87b-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="2a87b-119">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a87b-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="2a87b-120">-GalleryName</span></span>
<span data-ttu-id="2a87b-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a87b-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a87b-122">-InputObject</span></span>
<span data-ttu-id="2a87b-123">PS 圖庫影像版本物件。</span><span class="sxs-lookup"><span data-stu-id="2a87b-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a87b-124">-Name</span></span>
<span data-ttu-id="2a87b-125">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a87b-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="2a87b-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="2a87b-127">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="2a87b-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="2a87b-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="2a87b-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="2a87b-129">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="2a87b-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="2a87b-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2a87b-130">-ReplicaCount</span></span>
<span data-ttu-id="2a87b-131">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="2a87b-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="2a87b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a87b-132">-ResourceGroupName</span></span>
<span data-ttu-id="2a87b-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a87b-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a87b-134">-ResourceId</span></span>
<span data-ttu-id="2a87b-135">畫廊影像版本的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a87b-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a87b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a87b-136">-Tag</span></span>
<span data-ttu-id="2a87b-137">資源標記</span><span class="sxs-lookup"><span data-stu-id="2a87b-137">Resource tags</span></span>

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

### <span data-ttu-id="2a87b-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="2a87b-138">-TargetRegion</span></span>
<span data-ttu-id="2a87b-139">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="2a87b-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="2a87b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="2a87b-140">-Confirm</span></span>
<span data-ttu-id="2a87b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a87b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a87b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a87b-142">-WhatIf</span></span>
<span data-ttu-id="2a87b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a87b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a87b-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a87b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a87b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a87b-145">CommonParameters</span></span>
<span data-ttu-id="2a87b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a87b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a87b-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a87b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a87b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="2a87b-148">INPUTS</span></span>

### <span data-ttu-id="2a87b-149">System.object</span><span class="sxs-lookup"><span data-stu-id="2a87b-149">System.String</span></span>

### <span data-ttu-id="2a87b-150">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2a87b-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="2a87b-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a87b-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2a87b-152">System.object</span><span class="sxs-lookup"><span data-stu-id="2a87b-152">System.Int32</span></span>

### <span data-ttu-id="2a87b-153">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2a87b-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2a87b-154">System.object</span><span class="sxs-lookup"><span data-stu-id="2a87b-154">System.DateTime</span></span>

### <span data-ttu-id="2a87b-155">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="2a87b-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="2a87b-156">輸出</span><span class="sxs-lookup"><span data-stu-id="2a87b-156">OUTPUTS</span></span>

### <span data-ttu-id="2a87b-157">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2a87b-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="2a87b-158">筆記</span><span class="sxs-lookup"><span data-stu-id="2a87b-158">NOTES</span></span>

## <span data-ttu-id="2a87b-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a87b-159">RELATED LINKS</span></span>
