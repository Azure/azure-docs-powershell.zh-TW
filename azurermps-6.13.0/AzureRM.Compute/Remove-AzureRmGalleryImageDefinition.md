---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: e6e62fbe52aeb87868c688343ebbaed8f0046891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449242"
---
# <span data-ttu-id="cb1ae-101">Remove-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="cb1ae-101">Remove-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="cb1ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1ae-103">刪除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-103">Delete a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb1ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb1ae-104">SYNTAX</span></span>

### <span data-ttu-id="cb1ae-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="cb1ae-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb1ae-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="cb1ae-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb1ae-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="cb1ae-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb1ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="cb1ae-108">DESCRIPTION</span></span>
<span data-ttu-id="cb1ae-109">刪除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="cb1ae-110">示例</span><span class="sxs-lookup"><span data-stu-id="cb1ae-110">EXAMPLES</span></span>

### <span data-ttu-id="cb1ae-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cb1ae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="cb1ae-112">移除圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="cb1ae-113">參數</span><span class="sxs-lookup"><span data-stu-id="cb1ae-113">PARAMETERS</span></span>

### <span data-ttu-id="cb1ae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb1ae-114">-AsJob</span></span>
<span data-ttu-id="cb1ae-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb1ae-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb1ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1ae-116">-DefaultProfile</span></span>
<span data-ttu-id="cb1ae-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1ae-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cb1ae-118">-Force</span></span>
<span data-ttu-id="cb1ae-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb1ae-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="cb1ae-120">-GalleryName</span></span>
<span data-ttu-id="cb1ae-121">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="cb1ae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb1ae-122">-InputObject</span></span>
<span data-ttu-id="cb1ae-123">PS 圖庫影像定義物件</span><span class="sxs-lookup"><span data-stu-id="cb1ae-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="cb1ae-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb1ae-124">-Name</span></span>
<span data-ttu-id="cb1ae-125">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="cb1ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb1ae-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb1ae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb1ae-128">-ResourceId</span></span>
<span data-ttu-id="cb1ae-129">畫廊影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cb1ae-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="cb1ae-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cb1ae-130">-Confirm</span></span>
<span data-ttu-id="cb1ae-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb1ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb1ae-132">-WhatIf</span></span>
<span data-ttu-id="cb1ae-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb1ae-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb1ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1ae-135">CommonParameters</span></span>
<span data-ttu-id="cb1ae-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1ae-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1ae-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cb1ae-138">INPUTS</span></span>

### <span data-ttu-id="cb1ae-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cb1ae-139">System.String</span></span>

### <span data-ttu-id="cb1ae-140">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="cb1ae-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cb1ae-141">OUTPUTS</span></span>

### <span data-ttu-id="cb1ae-142">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="cb1ae-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cb1ae-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cb1ae-143">NOTES</span></span>

## <span data-ttu-id="cb1ae-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb1ae-144">RELATED LINKS</span></span>
