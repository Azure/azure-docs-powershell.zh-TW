---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625324"
---
# <span data-ttu-id="54fe2-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="54fe2-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="54fe2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="54fe2-103">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="54fe2-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fe2-104">句法</span><span class="sxs-lookup"><span data-stu-id="54fe2-104">SYNTAX</span></span>

### <span data-ttu-id="54fe2-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="54fe2-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fe2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="54fe2-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fe2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="54fe2-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fe2-108">說明</span><span class="sxs-lookup"><span data-stu-id="54fe2-108">DESCRIPTION</span></span>
<span data-ttu-id="54fe2-109">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="54fe2-109">Update a gallery.</span></span>

## <span data-ttu-id="54fe2-110">示例</span><span class="sxs-lookup"><span data-stu-id="54fe2-110">EXAMPLES</span></span>

### <span data-ttu-id="54fe2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="54fe2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="54fe2-112">更新圖庫。</span><span class="sxs-lookup"><span data-stu-id="54fe2-112">Update a gallery.</span></span>

## <span data-ttu-id="54fe2-113">參數</span><span class="sxs-lookup"><span data-stu-id="54fe2-113">PARAMETERS</span></span>

### <span data-ttu-id="54fe2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fe2-114">-AsJob</span></span>
<span data-ttu-id="54fe2-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54fe2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54fe2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fe2-116">-DefaultProfile</span></span>
<span data-ttu-id="54fe2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54fe2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54fe2-118">-描述</span><span class="sxs-lookup"><span data-stu-id="54fe2-118">-Description</span></span>
<span data-ttu-id="54fe2-119">圖庫資源的描述。</span><span class="sxs-lookup"><span data-stu-id="54fe2-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="54fe2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fe2-120">-InputObject</span></span>
<span data-ttu-id="54fe2-121">PS 圖庫物件。</span><span class="sxs-lookup"><span data-stu-id="54fe2-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="54fe2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="54fe2-122">-Name</span></span>
<span data-ttu-id="54fe2-123">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe2-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="54fe2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fe2-124">-ResourceGroupName</span></span>
<span data-ttu-id="54fe2-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="54fe2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fe2-126">-ResourceId</span></span>
<span data-ttu-id="54fe2-127">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="54fe2-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="54fe2-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="54fe2-128">-Tag</span></span>
<span data-ttu-id="54fe2-129">資源標記</span><span class="sxs-lookup"><span data-stu-id="54fe2-129">Resource tags</span></span>

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

### <span data-ttu-id="54fe2-130">-確認</span><span class="sxs-lookup"><span data-stu-id="54fe2-130">-Confirm</span></span>
<span data-ttu-id="54fe2-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54fe2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fe2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fe2-132">-WhatIf</span></span>
<span data-ttu-id="54fe2-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54fe2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fe2-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54fe2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fe2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fe2-135">CommonParameters</span></span>
<span data-ttu-id="54fe2-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54fe2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fe2-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54fe2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fe2-138">輸入</span><span class="sxs-lookup"><span data-stu-id="54fe2-138">INPUTS</span></span>

### <span data-ttu-id="54fe2-139">System.object</span><span class="sxs-lookup"><span data-stu-id="54fe2-139">System.String</span></span>

### <span data-ttu-id="54fe2-140">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="54fe2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="54fe2-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54fe2-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="54fe2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="54fe2-142">OUTPUTS</span></span>

### <span data-ttu-id="54fe2-143">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="54fe2-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="54fe2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="54fe2-144">NOTES</span></span>

## <span data-ttu-id="54fe2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="54fe2-145">RELATED LINKS</span></span>
