---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958605"
---
# <span data-ttu-id="a0e69-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a0e69-101">Update-AzImage</span></span>

## <span data-ttu-id="a0e69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0e69-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e69-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="a0e69-103">Updates an image.</span></span>

## <span data-ttu-id="a0e69-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0e69-104">SYNTAX</span></span>

### <span data-ttu-id="a0e69-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="a0e69-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e69-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a0e69-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e69-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a0e69-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e69-108">說明</span><span class="sxs-lookup"><span data-stu-id="a0e69-108">DESCRIPTION</span></span>
<span data-ttu-id="a0e69-109">**更新-AzImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="a0e69-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="a0e69-110">目前，只有標記可以更新。</span><span class="sxs-lookup"><span data-stu-id="a0e69-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="a0e69-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0e69-111">EXAMPLES</span></span>

### <span data-ttu-id="a0e69-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a0e69-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="a0e69-113">這個命令會更新資源群組 ' ResourceGroup01 ' 中現有影像 ' Image01 ' 的 Tag 值。</span><span class="sxs-lookup"><span data-stu-id="a0e69-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a0e69-114">參數</span><span class="sxs-lookup"><span data-stu-id="a0e69-114">PARAMETERS</span></span>

### <span data-ttu-id="a0e69-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0e69-115">-AsJob</span></span>
<span data-ttu-id="a0e69-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0e69-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0e69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e69-117">-DefaultProfile</span></span>
<span data-ttu-id="a0e69-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0e69-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e69-119">-影像</span><span class="sxs-lookup"><span data-stu-id="a0e69-119">-Image</span></span>
<span data-ttu-id="a0e69-120">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="a0e69-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="a0e69-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a0e69-121">-ImageName</span></span>
<span data-ttu-id="a0e69-122">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0e69-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="a0e69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e69-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0e69-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0e69-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a0e69-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0e69-125">-ResourceId</span></span>
<span data-ttu-id="a0e69-126">影像的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a0e69-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="a0e69-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0e69-127">-Tag</span></span>
<span data-ttu-id="a0e69-128">資源標記</span><span class="sxs-lookup"><span data-stu-id="a0e69-128">Resource tags</span></span>

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

### <span data-ttu-id="a0e69-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a0e69-129">-Confirm</span></span>
<span data-ttu-id="a0e69-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0e69-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e69-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e69-131">-WhatIf</span></span>
<span data-ttu-id="a0e69-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0e69-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e69-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0e69-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e69-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e69-134">CommonParameters</span></span>
<span data-ttu-id="a0e69-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0e69-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e69-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0e69-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e69-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a0e69-137">INPUTS</span></span>

### <span data-ttu-id="a0e69-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a0e69-138">System.String</span></span>

### <span data-ttu-id="a0e69-139">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a0e69-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a0e69-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a0e69-140">OUTPUTS</span></span>

### <span data-ttu-id="a0e69-141">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a0e69-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a0e69-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a0e69-142">NOTES</span></span>

## <span data-ttu-id="a0e69-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0e69-143">RELATED LINKS</span></span>
