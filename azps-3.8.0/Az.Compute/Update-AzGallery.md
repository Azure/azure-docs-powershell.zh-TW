---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797793"
---
# <span data-ttu-id="3d366-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="3d366-101">Update-AzGallery</span></span>

## <span data-ttu-id="3d366-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d366-102">SYNOPSIS</span></span>
<span data-ttu-id="3d366-103">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="3d366-103">Update a gallery.</span></span>

## <span data-ttu-id="3d366-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d366-104">SYNTAX</span></span>

### <span data-ttu-id="3d366-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="3d366-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d366-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3d366-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d366-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3d366-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d366-108">說明</span><span class="sxs-lookup"><span data-stu-id="3d366-108">DESCRIPTION</span></span>
<span data-ttu-id="3d366-109">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="3d366-109">Update a gallery.</span></span>

## <span data-ttu-id="3d366-110">示例</span><span class="sxs-lookup"><span data-stu-id="3d366-110">EXAMPLES</span></span>

### <span data-ttu-id="3d366-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3d366-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="3d366-112">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="3d366-112">Update a gallery.</span></span>

## <span data-ttu-id="3d366-113">參數</span><span class="sxs-lookup"><span data-stu-id="3d366-113">PARAMETERS</span></span>

### <span data-ttu-id="3d366-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d366-114">-AsJob</span></span>
<span data-ttu-id="3d366-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d366-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d366-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d366-116">-DefaultProfile</span></span>
<span data-ttu-id="3d366-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d366-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d366-118">-描述</span><span class="sxs-lookup"><span data-stu-id="3d366-118">-Description</span></span>
<span data-ttu-id="3d366-119">圖庫資源的描述。</span><span class="sxs-lookup"><span data-stu-id="3d366-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="3d366-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d366-120">-InputObject</span></span>
<span data-ttu-id="3d366-121">PS 圖庫物件。</span><span class="sxs-lookup"><span data-stu-id="3d366-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="3d366-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d366-122">-Name</span></span>
<span data-ttu-id="3d366-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d366-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="3d366-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d366-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d366-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d366-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d366-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d366-126">-ResourceId</span></span>
<span data-ttu-id="3d366-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3d366-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="3d366-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d366-128">-Tag</span></span>
<span data-ttu-id="3d366-129">資源標記</span><span class="sxs-lookup"><span data-stu-id="3d366-129">Resource tags</span></span>

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

### <span data-ttu-id="3d366-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3d366-130">-Confirm</span></span>
<span data-ttu-id="3d366-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d366-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d366-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d366-132">-WhatIf</span></span>
<span data-ttu-id="3d366-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d366-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d366-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d366-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d366-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d366-135">CommonParameters</span></span>
<span data-ttu-id="3d366-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d366-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d366-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d366-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d366-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3d366-138">INPUTS</span></span>

### <span data-ttu-id="3d366-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3d366-139">System.String</span></span>

### <span data-ttu-id="3d366-140">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3d366-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="3d366-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d366-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d366-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3d366-142">OUTPUTS</span></span>

### <span data-ttu-id="3d366-143">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3d366-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="3d366-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3d366-144">NOTES</span></span>

## <span data-ttu-id="3d366-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d366-145">RELATED LINKS</span></span>
