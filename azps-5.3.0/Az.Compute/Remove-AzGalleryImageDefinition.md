---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449782"
---
# <span data-ttu-id="bf5a6-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="bf5a6-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="bf5a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5a6-103">刪除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="bf5a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf5a6-104">SYNTAX</span></span>

### <span data-ttu-id="bf5a6-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="bf5a6-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5a6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bf5a6-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5a6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bf5a6-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5a6-108">說明</span><span class="sxs-lookup"><span data-stu-id="bf5a6-108">DESCRIPTION</span></span>
<span data-ttu-id="bf5a6-109">刪除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="bf5a6-110">示例</span><span class="sxs-lookup"><span data-stu-id="bf5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5a6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bf5a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="bf5a6-112">移除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="bf5a6-113">參數</span><span class="sxs-lookup"><span data-stu-id="bf5a6-113">PARAMETERS</span></span>

### <span data-ttu-id="bf5a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf5a6-114">-AsJob</span></span>
<span data-ttu-id="bf5a6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bf5a6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf5a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5a6-116">-DefaultProfile</span></span>
<span data-ttu-id="bf5a6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf5a6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bf5a6-118">-Force</span></span>
<span data-ttu-id="bf5a6-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf5a6-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="bf5a6-120">-GalleryName</span></span>
<span data-ttu-id="bf5a6-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="bf5a6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5a6-122">-InputObject</span></span>
<span data-ttu-id="bf5a6-123">PS 圖庫影像定義物件</span><span class="sxs-lookup"><span data-stu-id="bf5a6-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="bf5a6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf5a6-124">-Name</span></span>
<span data-ttu-id="bf5a6-125">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="bf5a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf5a6-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf5a6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5a6-128">-ResourceId</span></span>
<span data-ttu-id="bf5a6-129">畫廊影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bf5a6-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="bf5a6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="bf5a6-130">-Confirm</span></span>
<span data-ttu-id="bf5a6-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf5a6-132">-WhatIf</span></span>
<span data-ttu-id="bf5a6-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf5a6-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5a6-135">CommonParameters</span></span>
<span data-ttu-id="bf5a6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5a6-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5a6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bf5a6-138">INPUTS</span></span>

### <span data-ttu-id="bf5a6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bf5a6-139">System.String</span></span>

### <span data-ttu-id="bf5a6-140">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="bf5a6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bf5a6-141">OUTPUTS</span></span>

### <span data-ttu-id="bf5a6-142">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="bf5a6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bf5a6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bf5a6-143">NOTES</span></span>

## <span data-ttu-id="bf5a6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf5a6-144">RELATED LINKS</span></span>
