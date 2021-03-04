---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: d632f3f9717c706adf2881aa177d9cb7ff2425dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911150"
---
# <span data-ttu-id="6378f-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6378f-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6378f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6378f-102">SYNOPSIS</span></span>
<span data-ttu-id="6378f-103">刪除圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="6378f-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6378f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6378f-104">SYNTAX</span></span>

### <span data-ttu-id="6378f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="6378f-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6378f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6378f-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6378f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6378f-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6378f-108">描述</span><span class="sxs-lookup"><span data-stu-id="6378f-108">DESCRIPTION</span></span>
<span data-ttu-id="6378f-109">刪除圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="6378f-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6378f-110">例子</span><span class="sxs-lookup"><span data-stu-id="6378f-110">EXAMPLES</span></span>

### <span data-ttu-id="6378f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6378f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="6378f-112">移除圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="6378f-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="6378f-113">參數</span><span class="sxs-lookup"><span data-stu-id="6378f-113">PARAMETERS</span></span>

### <span data-ttu-id="6378f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6378f-114">-AsJob</span></span>
<span data-ttu-id="6378f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6378f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6378f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6378f-116">-DefaultProfile</span></span>
<span data-ttu-id="6378f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6378f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6378f-118">-強制</span><span class="sxs-lookup"><span data-stu-id="6378f-118">-Force</span></span>
<span data-ttu-id="6378f-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6378f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6378f-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6378f-120">-GalleryName</span></span>
<span data-ttu-id="6378f-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6378f-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="6378f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6378f-122">-InputObject</span></span>
<span data-ttu-id="6378f-123">PS 圖庫圖像定義物件</span><span class="sxs-lookup"><span data-stu-id="6378f-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6378f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6378f-124">-Name</span></span>
<span data-ttu-id="6378f-125">圖庫圖像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="6378f-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6378f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6378f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6378f-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6378f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6378f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6378f-128">-ResourceId</span></span>
<span data-ttu-id="6378f-129">圖庫圖像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6378f-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="6378f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="6378f-130">-Confirm</span></span>
<span data-ttu-id="6378f-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6378f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6378f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6378f-132">-WhatIf</span></span>
<span data-ttu-id="6378f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6378f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6378f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6378f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6378f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6378f-135">CommonParameters</span></span>
<span data-ttu-id="6378f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6378f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6378f-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6378f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6378f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6378f-138">INPUTS</span></span>

### <span data-ttu-id="6378f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6378f-139">System.String</span></span>

### <span data-ttu-id="6378f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6378f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6378f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="6378f-141">OUTPUTS</span></span>

### <span data-ttu-id="6378f-142">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6378f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6378f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6378f-143">NOTES</span></span>

## <span data-ttu-id="6378f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6378f-144">RELATED LINKS</span></span>
