---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: a6046dc58e010905094f1f0db47f49f7840cc913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788406"
---
# <span data-ttu-id="8f936-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="8f936-101">Remove-AzGallery</span></span>

## <span data-ttu-id="8f936-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f936-102">SYNOPSIS</span></span>
<span data-ttu-id="8f936-103">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="8f936-103">Delete a gallery.</span></span>

## <span data-ttu-id="8f936-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f936-104">SYNTAX</span></span>

### <span data-ttu-id="8f936-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="8f936-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f936-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8f936-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f936-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8f936-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f936-108">說明</span><span class="sxs-lookup"><span data-stu-id="8f936-108">DESCRIPTION</span></span>
<span data-ttu-id="8f936-109">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="8f936-109">Delete a gallery.</span></span>

## <span data-ttu-id="8f936-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f936-110">EXAMPLES</span></span>

### <span data-ttu-id="8f936-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8f936-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="8f936-112">刪除指定的圖庫。</span><span class="sxs-lookup"><span data-stu-id="8f936-112">Delete the given gallery.</span></span>

## <span data-ttu-id="8f936-113">參數</span><span class="sxs-lookup"><span data-stu-id="8f936-113">PARAMETERS</span></span>

### <span data-ttu-id="8f936-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f936-114">-AsJob</span></span>
<span data-ttu-id="8f936-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f936-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f936-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f936-116">-DefaultProfile</span></span>
<span data-ttu-id="8f936-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f936-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f936-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8f936-118">-Force</span></span>
<span data-ttu-id="8f936-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8f936-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f936-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f936-120">-InputObject</span></span>
<span data-ttu-id="8f936-121">PS 圖庫物件</span><span class="sxs-lookup"><span data-stu-id="8f936-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="8f936-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f936-122">-Name</span></span>
<span data-ttu-id="8f936-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f936-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="8f936-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f936-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f936-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f936-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f936-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f936-126">-ResourceId</span></span>
<span data-ttu-id="8f936-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8f936-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="8f936-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8f936-128">-Confirm</span></span>
<span data-ttu-id="8f936-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f936-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f936-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f936-130">-WhatIf</span></span>
<span data-ttu-id="8f936-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f936-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f936-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f936-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f936-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f936-133">CommonParameters</span></span>
<span data-ttu-id="8f936-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f936-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f936-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f936-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f936-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8f936-136">INPUTS</span></span>

### <span data-ttu-id="8f936-137">System.object</span><span class="sxs-lookup"><span data-stu-id="8f936-137">System.String</span></span>

### <span data-ttu-id="8f936-138">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="8f936-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="8f936-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8f936-139">OUTPUTS</span></span>

### <span data-ttu-id="8f936-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="8f936-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8f936-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8f936-141">NOTES</span></span>

## <span data-ttu-id="8f936-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f936-142">RELATED LINKS</span></span>
