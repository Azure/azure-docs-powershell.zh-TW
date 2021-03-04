---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 47ba904378ed8f58da29876d5835ca43bb8a7a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903845"
---
# <span data-ttu-id="50986-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="50986-101">New-AzGallery</span></span>

## <span data-ttu-id="50986-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50986-102">SYNOPSIS</span></span>
<span data-ttu-id="50986-103">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="50986-103">Create a gallery.</span></span>

## <span data-ttu-id="50986-104">語法</span><span class="sxs-lookup"><span data-stu-id="50986-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50986-105">描述</span><span class="sxs-lookup"><span data-stu-id="50986-105">DESCRIPTION</span></span>
<span data-ttu-id="50986-106">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="50986-106">Create a gallery.</span></span>

## <span data-ttu-id="50986-107">例子</span><span class="sxs-lookup"><span data-stu-id="50986-107">EXAMPLES</span></span>

### <span data-ttu-id="50986-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="50986-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="50986-109">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="50986-109">Create a gallery.</span></span>

## <span data-ttu-id="50986-110">參數</span><span class="sxs-lookup"><span data-stu-id="50986-110">PARAMETERS</span></span>

### <span data-ttu-id="50986-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50986-111">-AsJob</span></span>
<span data-ttu-id="50986-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="50986-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50986-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50986-113">-DefaultProfile</span></span>
<span data-ttu-id="50986-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50986-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50986-115">-描述</span><span class="sxs-lookup"><span data-stu-id="50986-115">-Description</span></span>
<span data-ttu-id="50986-116">圖庫資源的描述。</span><span class="sxs-lookup"><span data-stu-id="50986-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="50986-117">-位置</span><span class="sxs-lookup"><span data-stu-id="50986-117">-Location</span></span>
<span data-ttu-id="50986-118">資源位置</span><span class="sxs-lookup"><span data-stu-id="50986-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50986-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="50986-119">-Name</span></span>
<span data-ttu-id="50986-120">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="50986-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50986-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50986-121">-ResourceGroupName</span></span>
<span data-ttu-id="50986-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50986-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50986-123">-標記</span><span class="sxs-lookup"><span data-stu-id="50986-123">-Tag</span></span>
<span data-ttu-id="50986-124">資源標記</span><span class="sxs-lookup"><span data-stu-id="50986-124">Resource tags</span></span>

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

### <span data-ttu-id="50986-125">-確認</span><span class="sxs-lookup"><span data-stu-id="50986-125">-Confirm</span></span>
<span data-ttu-id="50986-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50986-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50986-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50986-127">-WhatIf</span></span>
<span data-ttu-id="50986-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50986-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50986-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50986-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50986-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50986-130">CommonParameters</span></span>
<span data-ttu-id="50986-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50986-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50986-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50986-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50986-133">輸入</span><span class="sxs-lookup"><span data-stu-id="50986-133">INPUTS</span></span>

### <span data-ttu-id="50986-134">System.String</span><span class="sxs-lookup"><span data-stu-id="50986-134">System.String</span></span>

### <span data-ttu-id="50986-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="50986-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="50986-136">輸出</span><span class="sxs-lookup"><span data-stu-id="50986-136">OUTPUTS</span></span>

### <span data-ttu-id="50986-137">Microsoft.Azure.Commands.Compute.Automation.models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="50986-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="50986-138">筆記</span><span class="sxs-lookup"><span data-stu-id="50986-138">NOTES</span></span>

## <span data-ttu-id="50986-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="50986-139">RELATED LINKS</span></span>
