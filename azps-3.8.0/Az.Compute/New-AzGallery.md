---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957407"
---
# <span data-ttu-id="22f73-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="22f73-101">New-AzGallery</span></span>

## <span data-ttu-id="22f73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22f73-102">SYNOPSIS</span></span>
<span data-ttu-id="22f73-103">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="22f73-103">Create a gallery.</span></span>

## <span data-ttu-id="22f73-104">句法</span><span class="sxs-lookup"><span data-stu-id="22f73-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22f73-105">說明</span><span class="sxs-lookup"><span data-stu-id="22f73-105">DESCRIPTION</span></span>
<span data-ttu-id="22f73-106">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="22f73-106">Create a gallery.</span></span>

## <span data-ttu-id="22f73-107">示例</span><span class="sxs-lookup"><span data-stu-id="22f73-107">EXAMPLES</span></span>

### <span data-ttu-id="22f73-108">範例1</span><span class="sxs-lookup"><span data-stu-id="22f73-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="22f73-109">建立圖庫。</span><span class="sxs-lookup"><span data-stu-id="22f73-109">Create a gallery.</span></span>

## <span data-ttu-id="22f73-110">參數</span><span class="sxs-lookup"><span data-stu-id="22f73-110">PARAMETERS</span></span>

### <span data-ttu-id="22f73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22f73-111">-AsJob</span></span>
<span data-ttu-id="22f73-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="22f73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22f73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f73-113">-DefaultProfile</span></span>
<span data-ttu-id="22f73-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22f73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22f73-115">-描述</span><span class="sxs-lookup"><span data-stu-id="22f73-115">-Description</span></span>
<span data-ttu-id="22f73-116">圖庫資源的描述。</span><span class="sxs-lookup"><span data-stu-id="22f73-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="22f73-117">-位置</span><span class="sxs-lookup"><span data-stu-id="22f73-117">-Location</span></span>
<span data-ttu-id="22f73-118">資源位置</span><span class="sxs-lookup"><span data-stu-id="22f73-118">Resource location</span></span>

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

### <span data-ttu-id="22f73-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="22f73-119">-Name</span></span>
<span data-ttu-id="22f73-120">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="22f73-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="22f73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f73-121">-ResourceGroupName</span></span>
<span data-ttu-id="22f73-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22f73-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="22f73-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="22f73-123">-Tag</span></span>
<span data-ttu-id="22f73-124">資源標記</span><span class="sxs-lookup"><span data-stu-id="22f73-124">Resource tags</span></span>

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

### <span data-ttu-id="22f73-125">-確認</span><span class="sxs-lookup"><span data-stu-id="22f73-125">-Confirm</span></span>
<span data-ttu-id="22f73-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22f73-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f73-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f73-127">-WhatIf</span></span>
<span data-ttu-id="22f73-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22f73-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f73-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22f73-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f73-130">CommonParameters</span></span>
<span data-ttu-id="22f73-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22f73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f73-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22f73-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f73-133">輸入</span><span class="sxs-lookup"><span data-stu-id="22f73-133">INPUTS</span></span>

### <span data-ttu-id="22f73-134">System.object</span><span class="sxs-lookup"><span data-stu-id="22f73-134">System.String</span></span>

### <span data-ttu-id="22f73-135">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22f73-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22f73-136">輸出</span><span class="sxs-lookup"><span data-stu-id="22f73-136">OUTPUTS</span></span>

### <span data-ttu-id="22f73-137">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="22f73-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="22f73-138">筆記</span><span class="sxs-lookup"><span data-stu-id="22f73-138">NOTES</span></span>

## <span data-ttu-id="22f73-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="22f73-139">RELATED LINKS</span></span>