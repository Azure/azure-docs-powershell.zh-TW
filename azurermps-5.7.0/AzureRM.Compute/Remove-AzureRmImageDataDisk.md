---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446351"
---
# <span data-ttu-id="7f8d2-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="7f8d2-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="7f8d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8d2-103">從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f8d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f8d2-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f8d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="7f8d2-106">**AzureRmImageDataDisk** Cmdlet 會從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="7f8d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="7f8d2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7f8d2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="7f8d2-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7f8d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f8d2-110">PARAMETERS</span></span>

### <span data-ttu-id="7f8d2-111">-影像</span><span class="sxs-lookup"><span data-stu-id="7f8d2-111">-Image</span></span>
<span data-ttu-id="7f8d2-112">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8d2-113">-Lun</span><span class="sxs-lookup"><span data-stu-id="7f8d2-113">-Lun</span></span>
<span data-ttu-id="7f8d2-114">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8d2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7f8d2-115">-Confirm</span></span>
<span data-ttu-id="7f8d2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8d2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8d2-117">-WhatIf</span></span>
<span data-ttu-id="7f8d2-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f8d2-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8d2-120">CommonParameters</span></span>
<span data-ttu-id="7f8d2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8d2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8d2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7f8d2-123">INPUTS</span></span>

### <span data-ttu-id="7f8d2-124">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="7f8d2-125">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7f8d2-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7f8d2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7f8d2-126">OUTPUTS</span></span>

### <span data-ttu-id="7f8d2-127">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="7f8d2-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="7f8d2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7f8d2-128">NOTES</span></span>

## <span data-ttu-id="7f8d2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f8d2-129">RELATED LINKS</span></span>

