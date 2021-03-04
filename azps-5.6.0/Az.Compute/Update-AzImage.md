---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: edf0ce1b67c25b8f5e48282dba45e845820c7b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906774"
---
# <span data-ttu-id="e7670-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e7670-101">Update-AzImage</span></span>

## <span data-ttu-id="e7670-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7670-102">SYNOPSIS</span></span>
<span data-ttu-id="e7670-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="e7670-103">Updates an image.</span></span>

## <span data-ttu-id="e7670-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7670-104">SYNTAX</span></span>

### <span data-ttu-id="e7670-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="e7670-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7670-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e7670-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7670-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e7670-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7670-108">描述</span><span class="sxs-lookup"><span data-stu-id="e7670-108">DESCRIPTION</span></span>
<span data-ttu-id="e7670-109">**Update-AzImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="e7670-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="e7670-110">目前，只有標記可以更新。</span><span class="sxs-lookup"><span data-stu-id="e7670-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="e7670-111">例子</span><span class="sxs-lookup"><span data-stu-id="e7670-111">EXAMPLES</span></span>

### <span data-ttu-id="e7670-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="e7670-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="e7670-113">此命令會更新資源群組 "ResourceGroup01" 中現有圖像 "Image01" 的標記值。</span><span class="sxs-lookup"><span data-stu-id="e7670-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e7670-114">參數</span><span class="sxs-lookup"><span data-stu-id="e7670-114">PARAMETERS</span></span>

### <span data-ttu-id="e7670-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7670-115">-AsJob</span></span>
<span data-ttu-id="e7670-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7670-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e7670-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7670-117">-DefaultProfile</span></span>
<span data-ttu-id="e7670-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7670-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7670-119">-影像</span><span class="sxs-lookup"><span data-stu-id="e7670-119">-Image</span></span>
<span data-ttu-id="e7670-120">指定一個本地影像物件。</span><span class="sxs-lookup"><span data-stu-id="e7670-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7670-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e7670-121">-ImageName</span></span>
<span data-ttu-id="e7670-122">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7670-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7670-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7670-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7670-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7670-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e7670-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7670-125">-ResourceId</span></span>
<span data-ttu-id="e7670-126">影像的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e7670-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="e7670-127">-標記</span><span class="sxs-lookup"><span data-stu-id="e7670-127">-Tag</span></span>
<span data-ttu-id="e7670-128">資源標記</span><span class="sxs-lookup"><span data-stu-id="e7670-128">Resource tags</span></span>

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

### <span data-ttu-id="e7670-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e7670-129">-Confirm</span></span>
<span data-ttu-id="e7670-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e7670-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7670-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7670-131">-WhatIf</span></span>
<span data-ttu-id="e7670-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7670-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7670-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7670-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7670-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7670-134">CommonParameters</span></span>
<span data-ttu-id="e7670-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7670-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7670-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7670-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7670-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e7670-137">INPUTS</span></span>

### <span data-ttu-id="e7670-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e7670-138">System.String</span></span>

### <span data-ttu-id="e7670-139">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e7670-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e7670-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e7670-140">OUTPUTS</span></span>

### <span data-ttu-id="e7670-141">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e7670-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e7670-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e7670-142">NOTES</span></span>

## <span data-ttu-id="e7670-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7670-143">RELATED LINKS</span></span>
