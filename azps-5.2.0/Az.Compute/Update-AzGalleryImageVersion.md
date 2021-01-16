---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278471"
---
# <span data-ttu-id="9af3c-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="9af3c-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="9af3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9af3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9af3c-103">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="9af3c-103">Update a gallery image version.</span></span>

## <span data-ttu-id="9af3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9af3c-104">SYNTAX</span></span>

### <span data-ttu-id="9af3c-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="9af3c-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af3c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9af3c-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af3c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9af3c-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af3c-108">說明</span><span class="sxs-lookup"><span data-stu-id="9af3c-108">DESCRIPTION</span></span>
<span data-ttu-id="9af3c-109">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="9af3c-109">Update a gallery image version.</span></span>

## <span data-ttu-id="9af3c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9af3c-110">EXAMPLES</span></span>

### <span data-ttu-id="9af3c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9af3c-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="9af3c-112">更新圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="9af3c-112">Update a gallery image version.</span></span>

## <span data-ttu-id="9af3c-113">參數</span><span class="sxs-lookup"><span data-stu-id="9af3c-113">PARAMETERS</span></span>

### <span data-ttu-id="9af3c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9af3c-114">-AsJob</span></span>
<span data-ttu-id="9af3c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9af3c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9af3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af3c-116">-DefaultProfile</span></span>
<span data-ttu-id="9af3c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9af3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af3c-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9af3c-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="9af3c-119">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af3c-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="9af3c-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="9af3c-120">-GalleryName</span></span>
<span data-ttu-id="9af3c-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af3c-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="9af3c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9af3c-122">-InputObject</span></span>
<span data-ttu-id="9af3c-123">PS 圖庫影像版本物件。</span><span class="sxs-lookup"><span data-stu-id="9af3c-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="9af3c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9af3c-124">-Name</span></span>
<span data-ttu-id="9af3c-125">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af3c-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="9af3c-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="9af3c-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="9af3c-127">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="9af3c-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="9af3c-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="9af3c-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="9af3c-129">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="9af3c-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="9af3c-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="9af3c-130">-ReplicaCount</span></span>
<span data-ttu-id="9af3c-131">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="9af3c-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="9af3c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af3c-132">-ResourceGroupName</span></span>
<span data-ttu-id="9af3c-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9af3c-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="9af3c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9af3c-134">-ResourceId</span></span>
<span data-ttu-id="9af3c-135">畫廊影像版本的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9af3c-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="9af3c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="9af3c-136">-Tag</span></span>
<span data-ttu-id="9af3c-137">資源標記</span><span class="sxs-lookup"><span data-stu-id="9af3c-137">Resource tags</span></span>

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

### <span data-ttu-id="9af3c-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="9af3c-138">-TargetRegion</span></span>
<span data-ttu-id="9af3c-139">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="9af3c-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="9af3c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="9af3c-140">-Confirm</span></span>
<span data-ttu-id="9af3c-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9af3c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af3c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af3c-142">-WhatIf</span></span>
<span data-ttu-id="9af3c-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9af3c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af3c-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9af3c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af3c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af3c-145">CommonParameters</span></span>
<span data-ttu-id="9af3c-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9af3c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af3c-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9af3c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af3c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="9af3c-148">INPUTS</span></span>

### <span data-ttu-id="9af3c-149">System.object</span><span class="sxs-lookup"><span data-stu-id="9af3c-149">System.String</span></span>

### <span data-ttu-id="9af3c-150">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9af3c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="9af3c-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9af3c-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9af3c-152">System.object</span><span class="sxs-lookup"><span data-stu-id="9af3c-152">System.Int32</span></span>

### <span data-ttu-id="9af3c-153">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9af3c-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9af3c-154">System.object</span><span class="sxs-lookup"><span data-stu-id="9af3c-154">System.DateTime</span></span>

### <span data-ttu-id="9af3c-155">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="9af3c-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="9af3c-156">輸出</span><span class="sxs-lookup"><span data-stu-id="9af3c-156">OUTPUTS</span></span>

### <span data-ttu-id="9af3c-157">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9af3c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="9af3c-158">筆記</span><span class="sxs-lookup"><span data-stu-id="9af3c-158">NOTES</span></span>

## <span data-ttu-id="9af3c-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="9af3c-159">RELATED LINKS</span></span>
