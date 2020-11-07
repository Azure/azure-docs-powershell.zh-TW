---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626132"
---
# <span data-ttu-id="47648-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="47648-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="47648-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47648-102">SYNOPSIS</span></span>
<span data-ttu-id="47648-103">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="47648-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47648-104">句法</span><span class="sxs-lookup"><span data-stu-id="47648-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47648-105">說明</span><span class="sxs-lookup"><span data-stu-id="47648-105">DESCRIPTION</span></span>
<span data-ttu-id="47648-106">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="47648-106">Create a gallery image version.</span></span>

## <span data-ttu-id="47648-107">示例</span><span class="sxs-lookup"><span data-stu-id="47648-107">EXAMPLES</span></span>

### <span data-ttu-id="47648-108">範例1</span><span class="sxs-lookup"><span data-stu-id="47648-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="47648-109">建立圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="47648-109">Create a gallery image version.</span></span>

## <span data-ttu-id="47648-110">參數</span><span class="sxs-lookup"><span data-stu-id="47648-110">PARAMETERS</span></span>

### <span data-ttu-id="47648-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47648-111">-AsJob</span></span>
<span data-ttu-id="47648-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47648-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47648-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47648-113">-DefaultProfile</span></span>
<span data-ttu-id="47648-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47648-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47648-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="47648-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="47648-116">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="47648-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="47648-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="47648-117">-GalleryName</span></span>
<span data-ttu-id="47648-118">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="47648-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="47648-119">-位置</span><span class="sxs-lookup"><span data-stu-id="47648-119">-Location</span></span>
<span data-ttu-id="47648-120">資源位置</span><span class="sxs-lookup"><span data-stu-id="47648-120">Resource location</span></span>

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

### <span data-ttu-id="47648-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="47648-121">-Name</span></span>
<span data-ttu-id="47648-122">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="47648-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="47648-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="47648-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="47648-124">圖庫影像版本的生命循環結束日期。</span><span class="sxs-lookup"><span data-stu-id="47648-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="47648-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="47648-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="47648-126">如果已設定，則從最新版本的影像定義部署的虛擬機器將不會使用此影像版本。</span><span class="sxs-lookup"><span data-stu-id="47648-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="47648-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="47648-127">-ReplicaCount</span></span>
<span data-ttu-id="47648-128">要為每個區域建立之影像版本的複製副本數目。</span><span class="sxs-lookup"><span data-stu-id="47648-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="47648-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47648-129">-ResourceGroupName</span></span>
<span data-ttu-id="47648-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47648-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="47648-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="47648-131">-SourceImageId</span></span>
<span data-ttu-id="47648-132">要建立影像版本之來源影像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47648-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="47648-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="47648-133">-Tag</span></span>
<span data-ttu-id="47648-134">資源標記</span><span class="sxs-lookup"><span data-stu-id="47648-134">Resource tags</span></span>

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

### <span data-ttu-id="47648-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="47648-135">-TargetRegion</span></span>
<span data-ttu-id="47648-136">要將影像版本複製到其中的目的地區域。</span><span class="sxs-lookup"><span data-stu-id="47648-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="47648-137">-確認</span><span class="sxs-lookup"><span data-stu-id="47648-137">-Confirm</span></span>
<span data-ttu-id="47648-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47648-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47648-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47648-139">-WhatIf</span></span>
<span data-ttu-id="47648-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47648-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47648-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47648-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47648-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47648-142">CommonParameters</span></span>
<span data-ttu-id="47648-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47648-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47648-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47648-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47648-145">輸入</span><span class="sxs-lookup"><span data-stu-id="47648-145">INPUTS</span></span>

### <span data-ttu-id="47648-146">System.object</span><span class="sxs-lookup"><span data-stu-id="47648-146">System.String</span></span>

### <span data-ttu-id="47648-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47648-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47648-148">System.object</span><span class="sxs-lookup"><span data-stu-id="47648-148">System.Int32</span></span>

### <span data-ttu-id="47648-149">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="47648-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="47648-150">System.object</span><span class="sxs-lookup"><span data-stu-id="47648-150">System.DateTime</span></span>

### <span data-ttu-id="47648-151">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="47648-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="47648-152">輸出</span><span class="sxs-lookup"><span data-stu-id="47648-152">OUTPUTS</span></span>

### <span data-ttu-id="47648-153">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="47648-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="47648-154">筆記</span><span class="sxs-lookup"><span data-stu-id="47648-154">NOTES</span></span>

## <span data-ttu-id="47648-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="47648-155">RELATED LINKS</span></span>
