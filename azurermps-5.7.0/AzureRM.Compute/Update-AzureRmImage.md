---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444667"
---
# <span data-ttu-id="2d2f1-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="2d2f1-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="2d2f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2f1-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d2f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d2f1-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d2f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d2f1-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2f1-106">**更新-AzureRmImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="2d2f1-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d2f1-107">EXAMPLES</span></span>

### <span data-ttu-id="2d2f1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2d2f1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="2d2f1-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2d2f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d2f1-110">PARAMETERS</span></span>

### <span data-ttu-id="2d2f1-111">-影像</span><span class="sxs-lookup"><span data-stu-id="2d2f1-111">-Image</span></span>
<span data-ttu-id="2d2f1-112">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2f1-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="2d2f1-113">-ImageName</span></span>
<span data-ttu-id="2d2f1-114">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d2f1-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2f1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2d2f1-117">-Confirm</span></span>
<span data-ttu-id="2d2f1-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2f1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2f1-119">-WhatIf</span></span>
<span data-ttu-id="2d2f1-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d2f1-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2f1-122">CommonParameters</span></span>
<span data-ttu-id="2d2f1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2f1-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2f1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2d2f1-125">INPUTS</span></span>

### <span data-ttu-id="2d2f1-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2d2f1-126">System.String</span></span>
<span data-ttu-id="2d2f1-127">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="2d2f1-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="2d2f1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2d2f1-128">OUTPUTS</span></span>

### <span data-ttu-id="2d2f1-129">System.object</span><span class="sxs-lookup"><span data-stu-id="2d2f1-129">System.Object</span></span>

## <span data-ttu-id="2d2f1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2d2f1-130">NOTES</span></span>

## <span data-ttu-id="2d2f1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d2f1-131">RELATED LINKS</span></span>

