---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 1d37af16fcb84db8247ac5db495abb1f41319c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455843"
---
# <span data-ttu-id="22f7e-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="22f7e-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="22f7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="22f7e-103">從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="22f7e-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22f7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="22f7e-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f7e-105">說明</span><span class="sxs-lookup"><span data-stu-id="22f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="22f7e-106">**AzureRmImageDataDisk** Cmdlet 會從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="22f7e-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="22f7e-107">示例</span><span class="sxs-lookup"><span data-stu-id="22f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="22f7e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="22f7e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="22f7e-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="22f7e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="22f7e-110">參數</span><span class="sxs-lookup"><span data-stu-id="22f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="22f7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f7e-111">-DefaultProfile</span></span>
<span data-ttu-id="22f7e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22f7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22f7e-113">-影像</span><span class="sxs-lookup"><span data-stu-id="22f7e-113">-Image</span></span>
<span data-ttu-id="22f7e-114">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="22f7e-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22f7e-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="22f7e-115">-Lun</span></span>
<span data-ttu-id="22f7e-116">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="22f7e-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22f7e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="22f7e-117">-Confirm</span></span>
<span data-ttu-id="22f7e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22f7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f7e-119">-WhatIf</span></span>
<span data-ttu-id="22f7e-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22f7e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22f7e-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22f7e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f7e-122">CommonParameters</span></span>
<span data-ttu-id="22f7e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22f7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f7e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22f7e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f7e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="22f7e-125">INPUTS</span></span>

### <span data-ttu-id="22f7e-126">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="22f7e-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="22f7e-127">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22f7e-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="22f7e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="22f7e-128">OUTPUTS</span></span>

### <span data-ttu-id="22f7e-129">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="22f7e-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="22f7e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="22f7e-130">NOTES</span></span>

## <span data-ttu-id="22f7e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="22f7e-131">RELATED LINKS</span></span>

