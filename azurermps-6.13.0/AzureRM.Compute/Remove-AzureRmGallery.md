---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
ms.openlocfilehash: 2711b5398f3d10f894214473f6ff68045748af22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449246"
---
# <span data-ttu-id="b149f-101">Remove-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="b149f-101">Remove-AzureRmGallery</span></span>

## <span data-ttu-id="b149f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b149f-102">SYNOPSIS</span></span>
<span data-ttu-id="b149f-103">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="b149f-103">Delete a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b149f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b149f-104">SYNTAX</span></span>

### <span data-ttu-id="b149f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b149f-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b149f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b149f-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b149f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b149f-107">ObjectParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b149f-108">說明</span><span class="sxs-lookup"><span data-stu-id="b149f-108">DESCRIPTION</span></span>
<span data-ttu-id="b149f-109">刪除圖庫。</span><span class="sxs-lookup"><span data-stu-id="b149f-109">Delete a gallery.</span></span>

## <span data-ttu-id="b149f-110">示例</span><span class="sxs-lookup"><span data-stu-id="b149f-110">EXAMPLES</span></span>

### <span data-ttu-id="b149f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b149f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="b149f-112">刪除指定的圖庫。</span><span class="sxs-lookup"><span data-stu-id="b149f-112">Delete the given gallery.</span></span>

## <span data-ttu-id="b149f-113">參數</span><span class="sxs-lookup"><span data-stu-id="b149f-113">PARAMETERS</span></span>

### <span data-ttu-id="b149f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b149f-114">-AsJob</span></span>
<span data-ttu-id="b149f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b149f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b149f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b149f-116">-DefaultProfile</span></span>
<span data-ttu-id="b149f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b149f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b149f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b149f-118">-Force</span></span>
<span data-ttu-id="b149f-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b149f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b149f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b149f-120">-InputObject</span></span>
<span data-ttu-id="b149f-121">PS 圖庫物件</span><span class="sxs-lookup"><span data-stu-id="b149f-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="b149f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b149f-122">-Name</span></span>
<span data-ttu-id="b149f-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b149f-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="b149f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b149f-124">-ResourceGroupName</span></span>
<span data-ttu-id="b149f-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b149f-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b149f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b149f-126">-ResourceId</span></span>
<span data-ttu-id="b149f-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b149f-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="b149f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b149f-128">-Confirm</span></span>
<span data-ttu-id="b149f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b149f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b149f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b149f-130">-WhatIf</span></span>
<span data-ttu-id="b149f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b149f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b149f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b149f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b149f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b149f-133">CommonParameters</span></span>
<span data-ttu-id="b149f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b149f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b149f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b149f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b149f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b149f-136">INPUTS</span></span>

### <span data-ttu-id="b149f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="b149f-137">System.String</span></span>

### <span data-ttu-id="b149f-138">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b149f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b149f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b149f-139">OUTPUTS</span></span>

### <span data-ttu-id="b149f-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b149f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b149f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b149f-141">NOTES</span></span>

## <span data-ttu-id="b149f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b149f-142">RELATED LINKS</span></span>
