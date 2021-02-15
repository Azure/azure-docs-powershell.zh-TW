---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127715"
---
# <span data-ttu-id="343fd-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="343fd-101">Update-AzImage</span></span>

## <span data-ttu-id="343fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="343fd-102">SYNOPSIS</span></span>
<span data-ttu-id="343fd-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="343fd-103">Updates an image.</span></span>

## <span data-ttu-id="343fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="343fd-104">SYNTAX</span></span>

### <span data-ttu-id="343fd-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="343fd-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="343fd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="343fd-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="343fd-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="343fd-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343fd-108">說明</span><span class="sxs-lookup"><span data-stu-id="343fd-108">DESCRIPTION</span></span>
<span data-ttu-id="343fd-109">**更新-AzImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="343fd-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="343fd-110">目前，只有標記可以更新。</span><span class="sxs-lookup"><span data-stu-id="343fd-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="343fd-111">示例</span><span class="sxs-lookup"><span data-stu-id="343fd-111">EXAMPLES</span></span>

### <span data-ttu-id="343fd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="343fd-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="343fd-113">這個命令會更新資源群組 ' ResourceGroup01 ' 中現有影像 ' Image01 ' 的 Tag 值。</span><span class="sxs-lookup"><span data-stu-id="343fd-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="343fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="343fd-114">PARAMETERS</span></span>

### <span data-ttu-id="343fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="343fd-115">-AsJob</span></span>
<span data-ttu-id="343fd-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="343fd-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="343fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343fd-117">-DefaultProfile</span></span>
<span data-ttu-id="343fd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="343fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343fd-119">-影像</span><span class="sxs-lookup"><span data-stu-id="343fd-119">-Image</span></span>
<span data-ttu-id="343fd-120">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="343fd-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="343fd-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="343fd-121">-ImageName</span></span>
<span data-ttu-id="343fd-122">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="343fd-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="343fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="343fd-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="343fd-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="343fd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="343fd-125">-ResourceId</span></span>
<span data-ttu-id="343fd-126">影像的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="343fd-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="343fd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="343fd-127">-Tag</span></span>
<span data-ttu-id="343fd-128">資源標記</span><span class="sxs-lookup"><span data-stu-id="343fd-128">Resource tags</span></span>

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

### <span data-ttu-id="343fd-129">-確認</span><span class="sxs-lookup"><span data-stu-id="343fd-129">-Confirm</span></span>
<span data-ttu-id="343fd-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="343fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343fd-131">-WhatIf</span></span>
<span data-ttu-id="343fd-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="343fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343fd-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="343fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343fd-134">CommonParameters</span></span>
<span data-ttu-id="343fd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="343fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343fd-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="343fd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343fd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="343fd-137">INPUTS</span></span>

### <span data-ttu-id="343fd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="343fd-138">System.String</span></span>

### <span data-ttu-id="343fd-139">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="343fd-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="343fd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="343fd-140">OUTPUTS</span></span>

### <span data-ttu-id="343fd-141">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="343fd-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="343fd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="343fd-142">NOTES</span></span>

## <span data-ttu-id="343fd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="343fd-143">RELATED LINKS</span></span>
