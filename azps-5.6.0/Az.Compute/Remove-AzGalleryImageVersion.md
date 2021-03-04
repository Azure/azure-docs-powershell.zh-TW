---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: cb1f9ca5354810f6459a8d0a0e3ea1a53ad6cf78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903650"
---
# <span data-ttu-id="7f15a-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7f15a-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="7f15a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f15a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f15a-103">刪除圖庫圖像版本。</span><span class="sxs-lookup"><span data-stu-id="7f15a-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="7f15a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f15a-104">SYNTAX</span></span>

### <span data-ttu-id="7f15a-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="7f15a-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f15a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7f15a-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f15a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7f15a-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f15a-108">描述</span><span class="sxs-lookup"><span data-stu-id="7f15a-108">DESCRIPTION</span></span>
<span data-ttu-id="7f15a-109">刪除圖庫圖像版本。</span><span class="sxs-lookup"><span data-stu-id="7f15a-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="7f15a-110">例子</span><span class="sxs-lookup"><span data-stu-id="7f15a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f15a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7f15a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="7f15a-112">刪除所給予的圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="7f15a-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="7f15a-113">參數</span><span class="sxs-lookup"><span data-stu-id="7f15a-113">PARAMETERS</span></span>

### <span data-ttu-id="7f15a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f15a-114">-AsJob</span></span>
<span data-ttu-id="7f15a-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7f15a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f15a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f15a-116">-DefaultProfile</span></span>
<span data-ttu-id="7f15a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f15a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f15a-118">-強制</span><span class="sxs-lookup"><span data-stu-id="7f15a-118">-Force</span></span>
<span data-ttu-id="7f15a-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7f15a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f15a-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7f15a-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="7f15a-121">圖庫圖像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f15a-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="7f15a-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="7f15a-122">-GalleryName</span></span>
<span data-ttu-id="7f15a-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f15a-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="7f15a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f15a-124">-InputObject</span></span>
<span data-ttu-id="7f15a-125">PS 圖庫圖像版本物件</span><span class="sxs-lookup"><span data-stu-id="7f15a-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="7f15a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f15a-126">-Name</span></span>
<span data-ttu-id="7f15a-127">圖庫圖像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f15a-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="7f15a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f15a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f15a-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f15a-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f15a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f15a-130">-ResourceId</span></span>
<span data-ttu-id="7f15a-131">圖庫圖像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7f15a-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="7f15a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7f15a-132">-Confirm</span></span>
<span data-ttu-id="7f15a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7f15a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f15a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f15a-134">-WhatIf</span></span>
<span data-ttu-id="7f15a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f15a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f15a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f15a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f15a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f15a-137">CommonParameters</span></span>
<span data-ttu-id="7f15a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f15a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f15a-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f15a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f15a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7f15a-140">INPUTS</span></span>

### <span data-ttu-id="7f15a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7f15a-141">System.String</span></span>

### <span data-ttu-id="7f15a-142">Microsoft.Azure.Commands.Compute.Automation.models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7f15a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="7f15a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7f15a-143">OUTPUTS</span></span>

### <span data-ttu-id="7f15a-144">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7f15a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7f15a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7f15a-145">NOTES</span></span>

## <span data-ttu-id="7f15a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f15a-146">RELATED LINKS</span></span>
