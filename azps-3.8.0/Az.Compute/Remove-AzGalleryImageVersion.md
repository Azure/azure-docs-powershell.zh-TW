---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: addf292e2a73b27f6e1e40258c0d8c60e54cfaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799298"
---
# <span data-ttu-id="b8c19-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b8c19-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="b8c19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c19-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c19-103">刪除圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="b8c19-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="b8c19-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c19-104">SYNTAX</span></span>

### <span data-ttu-id="b8c19-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b8c19-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c19-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b8c19-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c19-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b8c19-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c19-108">說明</span><span class="sxs-lookup"><span data-stu-id="b8c19-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c19-109">刪除圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="b8c19-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="b8c19-110">示例</span><span class="sxs-lookup"><span data-stu-id="b8c19-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c19-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b8c19-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="b8c19-112">刪除指定的圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="b8c19-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="b8c19-113">參數</span><span class="sxs-lookup"><span data-stu-id="b8c19-113">PARAMETERS</span></span>

### <span data-ttu-id="b8c19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c19-114">-AsJob</span></span>
<span data-ttu-id="b8c19-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8c19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c19-116">-DefaultProfile</span></span>
<span data-ttu-id="b8c19-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8c19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c19-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c19-118">-Force</span></span>
<span data-ttu-id="b8c19-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b8c19-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8c19-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b8c19-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b8c19-121">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c19-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b8c19-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b8c19-122">-GalleryName</span></span>
<span data-ttu-id="b8c19-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c19-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="b8c19-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c19-124">-InputObject</span></span>
<span data-ttu-id="b8c19-125">PS 圖庫影像版本物件</span><span class="sxs-lookup"><span data-stu-id="b8c19-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="b8c19-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8c19-126">-Name</span></span>
<span data-ttu-id="b8c19-127">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c19-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="b8c19-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c19-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8c19-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c19-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8c19-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c19-130">-ResourceId</span></span>
<span data-ttu-id="b8c19-131">圖庫影像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b8c19-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="b8c19-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b8c19-132">-Confirm</span></span>
<span data-ttu-id="b8c19-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8c19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c19-134">-WhatIf</span></span>
<span data-ttu-id="b8c19-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8c19-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c19-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8c19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c19-137">CommonParameters</span></span>
<span data-ttu-id="b8c19-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c19-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8c19-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c19-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c19-140">INPUTS</span></span>

### <span data-ttu-id="b8c19-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b8c19-141">System.String</span></span>

### <span data-ttu-id="b8c19-142">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b8c19-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b8c19-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c19-143">OUTPUTS</span></span>

### <span data-ttu-id="b8c19-144">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b8c19-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b8c19-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c19-145">NOTES</span></span>

## <span data-ttu-id="b8c19-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c19-146">RELATED LINKS</span></span>
