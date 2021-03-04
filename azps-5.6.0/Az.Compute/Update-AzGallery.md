---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 4badbfc9973b20869c6db421bd1299e00337d7fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911742"
---
# <span data-ttu-id="ddae7-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="ddae7-101">Update-AzGallery</span></span>

## <span data-ttu-id="ddae7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddae7-102">SYNOPSIS</span></span>
<span data-ttu-id="ddae7-103">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="ddae7-103">Update a gallery.</span></span>

## <span data-ttu-id="ddae7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddae7-104">SYNTAX</span></span>

### <span data-ttu-id="ddae7-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ddae7-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddae7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ddae7-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddae7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ddae7-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddae7-108">描述</span><span class="sxs-lookup"><span data-stu-id="ddae7-108">DESCRIPTION</span></span>
<span data-ttu-id="ddae7-109">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="ddae7-109">Update a gallery.</span></span>

## <span data-ttu-id="ddae7-110">例子</span><span class="sxs-lookup"><span data-stu-id="ddae7-110">EXAMPLES</span></span>

### <span data-ttu-id="ddae7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ddae7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="ddae7-112">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="ddae7-112">Update a gallery.</span></span>

## <span data-ttu-id="ddae7-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddae7-113">PARAMETERS</span></span>

### <span data-ttu-id="ddae7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddae7-114">-AsJob</span></span>
<span data-ttu-id="ddae7-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddae7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddae7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddae7-116">-DefaultProfile</span></span>
<span data-ttu-id="ddae7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddae7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddae7-118">-描述</span><span class="sxs-lookup"><span data-stu-id="ddae7-118">-Description</span></span>
<span data-ttu-id="ddae7-119">圖庫資源的描述。</span><span class="sxs-lookup"><span data-stu-id="ddae7-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="ddae7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddae7-120">-InputObject</span></span>
<span data-ttu-id="ddae7-121">PS 圖庫物件。</span><span class="sxs-lookup"><span data-stu-id="ddae7-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="ddae7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddae7-122">-Name</span></span>
<span data-ttu-id="ddae7-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddae7-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="ddae7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddae7-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddae7-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddae7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddae7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddae7-126">-ResourceId</span></span>
<span data-ttu-id="ddae7-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ddae7-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="ddae7-128">-標記</span><span class="sxs-lookup"><span data-stu-id="ddae7-128">-Tag</span></span>
<span data-ttu-id="ddae7-129">資源標記</span><span class="sxs-lookup"><span data-stu-id="ddae7-129">Resource tags</span></span>

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

### <span data-ttu-id="ddae7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ddae7-130">-Confirm</span></span>
<span data-ttu-id="ddae7-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddae7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddae7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddae7-132">-WhatIf</span></span>
<span data-ttu-id="ddae7-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddae7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddae7-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddae7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddae7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddae7-135">CommonParameters</span></span>
<span data-ttu-id="ddae7-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddae7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddae7-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddae7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddae7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ddae7-138">INPUTS</span></span>

### <span data-ttu-id="ddae7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ddae7-139">System.String</span></span>

### <span data-ttu-id="ddae7-140">Microsoft.Azure.Commands.Compute.Automation.models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="ddae7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="ddae7-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddae7-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ddae7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ddae7-142">OUTPUTS</span></span>

### <span data-ttu-id="ddae7-143">Microsoft.Azure.Commands.Compute.Automation.models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="ddae7-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ddae7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ddae7-144">NOTES</span></span>

## <span data-ttu-id="ddae7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddae7-145">RELATED LINKS</span></span>
