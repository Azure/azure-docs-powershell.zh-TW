---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: abc9fd93545f229c39dd696a856781ceed748a77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911154"
---
# <span data-ttu-id="2bf4c-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="2bf4c-101">Remove-AzGallery</span></span>

## <span data-ttu-id="2bf4c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2bf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf4c-103">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-103">Delete a gallery.</span></span>

## <span data-ttu-id="2bf4c-104">語法</span><span class="sxs-lookup"><span data-stu-id="2bf4c-104">SYNTAX</span></span>

### <span data-ttu-id="2bf4c-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2bf4c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf4c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2bf4c-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf4c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2bf4c-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf4c-108">描述</span><span class="sxs-lookup"><span data-stu-id="2bf4c-108">DESCRIPTION</span></span>
<span data-ttu-id="2bf4c-109">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-109">Delete a gallery.</span></span>

## <span data-ttu-id="2bf4c-110">例子</span><span class="sxs-lookup"><span data-stu-id="2bf4c-110">EXAMPLES</span></span>

### <span data-ttu-id="2bf4c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2bf4c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="2bf4c-112">刪除所給予的圖庫。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-112">Delete the given gallery.</span></span>

## <span data-ttu-id="2bf4c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2bf4c-113">PARAMETERS</span></span>

### <span data-ttu-id="2bf4c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bf4c-114">-AsJob</span></span>
<span data-ttu-id="2bf4c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2bf4c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bf4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf4c-116">-DefaultProfile</span></span>
<span data-ttu-id="2bf4c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf4c-118">-強制</span><span class="sxs-lookup"><span data-stu-id="2bf4c-118">-Force</span></span>
<span data-ttu-id="2bf4c-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2bf4c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bf4c-120">-InputObject</span></span>
<span data-ttu-id="2bf4c-121">PS 圖庫物件</span><span class="sxs-lookup"><span data-stu-id="2bf4c-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf4c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bf4c-122">-Name</span></span>
<span data-ttu-id="2bf4c-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2bf4c-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2bf4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bf4c-126">-ResourceId</span></span>
<span data-ttu-id="2bf4c-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2bf4c-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="2bf4c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2bf4c-128">-Confirm</span></span>
<span data-ttu-id="2bf4c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf4c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf4c-130">-WhatIf</span></span>
<span data-ttu-id="2bf4c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf4c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf4c-133">CommonParameters</span></span>
<span data-ttu-id="2bf4c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2bf4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf4c-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bf4c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf4c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2bf4c-136">INPUTS</span></span>

### <span data-ttu-id="2bf4c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2bf4c-137">System.String</span></span>

### <span data-ttu-id="2bf4c-138">Microsoft.Azure.Commands.Compute.Automation.models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="2bf4c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="2bf4c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2bf4c-139">OUTPUTS</span></span>

### <span data-ttu-id="2bf4c-140">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2bf4c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2bf4c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2bf4c-141">NOTES</span></span>

## <span data-ttu-id="2bf4c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bf4c-142">RELATED LINKS</span></span>
