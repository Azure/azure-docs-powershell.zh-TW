---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286060"
---
# <span data-ttu-id="151e7-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="151e7-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="151e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="151e7-102">SYNOPSIS</span></span>
<span data-ttu-id="151e7-103">從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="151e7-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="151e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="151e7-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="151e7-105">DESCRIPTION</span></span>
<span data-ttu-id="151e7-106">**AzImageDataDisk** Cmdlet 會從 image 物件中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="151e7-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="151e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="151e7-107">EXAMPLES</span></span>

### <span data-ttu-id="151e7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="151e7-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="151e7-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="151e7-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="151e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="151e7-110">PARAMETERS</span></span>

### <span data-ttu-id="151e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151e7-111">-DefaultProfile</span></span>
<span data-ttu-id="151e7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="151e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="151e7-113">-影像</span><span class="sxs-lookup"><span data-stu-id="151e7-113">-Image</span></span>
<span data-ttu-id="151e7-114">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="151e7-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="151e7-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="151e7-115">-Lun</span></span>
<span data-ttu-id="151e7-116">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="151e7-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="151e7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="151e7-117">-Confirm</span></span>
<span data-ttu-id="151e7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="151e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151e7-119">-WhatIf</span></span>
<span data-ttu-id="151e7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="151e7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="151e7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="151e7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151e7-122">CommonParameters</span></span>
<span data-ttu-id="151e7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="151e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151e7-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="151e7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151e7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="151e7-125">INPUTS</span></span>

### <span data-ttu-id="151e7-126">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="151e7-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="151e7-127">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="151e7-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="151e7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="151e7-128">OUTPUTS</span></span>

### <span data-ttu-id="151e7-129">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="151e7-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="151e7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="151e7-130">NOTES</span></span>

## <span data-ttu-id="151e7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="151e7-131">RELATED LINKS</span></span>
