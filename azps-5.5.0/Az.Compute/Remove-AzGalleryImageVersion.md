---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127826"
---
# <span data-ttu-id="982ea-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="982ea-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="982ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="982ea-102">SYNOPSIS</span></span>
<span data-ttu-id="982ea-103">刪除圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="982ea-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="982ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="982ea-104">SYNTAX</span></span>

### <span data-ttu-id="982ea-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="982ea-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982ea-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="982ea-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982ea-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="982ea-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982ea-108">說明</span><span class="sxs-lookup"><span data-stu-id="982ea-108">DESCRIPTION</span></span>
<span data-ttu-id="982ea-109">刪除圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="982ea-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="982ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="982ea-110">EXAMPLES</span></span>

### <span data-ttu-id="982ea-111">範例1</span><span class="sxs-lookup"><span data-stu-id="982ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="982ea-112">刪除指定的圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="982ea-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="982ea-113">參數</span><span class="sxs-lookup"><span data-stu-id="982ea-113">PARAMETERS</span></span>

### <span data-ttu-id="982ea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="982ea-114">-AsJob</span></span>
<span data-ttu-id="982ea-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="982ea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="982ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982ea-116">-DefaultProfile</span></span>
<span data-ttu-id="982ea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="982ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="982ea-118">-Force</span><span class="sxs-lookup"><span data-stu-id="982ea-118">-Force</span></span>
<span data-ttu-id="982ea-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="982ea-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="982ea-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="982ea-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="982ea-121">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="982ea-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="982ea-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="982ea-122">-GalleryName</span></span>
<span data-ttu-id="982ea-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="982ea-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="982ea-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="982ea-124">-InputObject</span></span>
<span data-ttu-id="982ea-125">PS 圖庫影像版本物件</span><span class="sxs-lookup"><span data-stu-id="982ea-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="982ea-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="982ea-126">-Name</span></span>
<span data-ttu-id="982ea-127">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="982ea-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="982ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="982ea-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="982ea-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="982ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="982ea-130">-ResourceId</span></span>
<span data-ttu-id="982ea-131">圖庫影像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="982ea-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="982ea-132">-確認</span><span class="sxs-lookup"><span data-stu-id="982ea-132">-Confirm</span></span>
<span data-ttu-id="982ea-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="982ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982ea-134">-WhatIf</span></span>
<span data-ttu-id="982ea-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="982ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982ea-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="982ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982ea-137">CommonParameters</span></span>
<span data-ttu-id="982ea-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="982ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982ea-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="982ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982ea-140">輸入</span><span class="sxs-lookup"><span data-stu-id="982ea-140">INPUTS</span></span>

### <span data-ttu-id="982ea-141">System.object</span><span class="sxs-lookup"><span data-stu-id="982ea-141">System.String</span></span>

### <span data-ttu-id="982ea-142">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="982ea-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="982ea-143">輸出</span><span class="sxs-lookup"><span data-stu-id="982ea-143">OUTPUTS</span></span>

### <span data-ttu-id="982ea-144">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="982ea-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="982ea-145">筆記</span><span class="sxs-lookup"><span data-stu-id="982ea-145">NOTES</span></span>

## <span data-ttu-id="982ea-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="982ea-146">RELATED LINKS</span></span>
