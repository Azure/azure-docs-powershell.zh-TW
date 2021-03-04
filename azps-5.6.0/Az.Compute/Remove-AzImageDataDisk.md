---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909746"
---
# <span data-ttu-id="f5793-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5793-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="f5793-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5793-102">SYNOPSIS</span></span>
<span data-ttu-id="f5793-103">從影像物件移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f5793-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="f5793-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5793-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5793-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5793-105">DESCRIPTION</span></span>
<span data-ttu-id="f5793-106">**Remove-AzImageDataLet** Cmdlet 會從影像物件移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f5793-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="f5793-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5793-107">EXAMPLES</span></span>

### <span data-ttu-id="f5793-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5793-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="f5793-109">此命令會從資源群組 "ResourceGroup01" 中現有圖像 "Image01" 移除邏輯單元編號 1 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="f5793-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f5793-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5793-110">PARAMETERS</span></span>

### <span data-ttu-id="f5793-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5793-111">-DefaultProfile</span></span>
<span data-ttu-id="f5793-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5793-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5793-113">-影像</span><span class="sxs-lookup"><span data-stu-id="f5793-113">-Image</span></span>
<span data-ttu-id="f5793-114">指定一個本地影像物件。</span><span class="sxs-lookup"><span data-stu-id="f5793-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="f5793-115">-四分位</span><span class="sxs-lookup"><span data-stu-id="f5793-115">-Lun</span></span>
<span data-ttu-id="f5793-116">指定在中 (單位) 。</span><span class="sxs-lookup"><span data-stu-id="f5793-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="f5793-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f5793-117">-Confirm</span></span>
<span data-ttu-id="f5793-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5793-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5793-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5793-119">-WhatIf</span></span>
<span data-ttu-id="f5793-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5793-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5793-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5793-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5793-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5793-122">CommonParameters</span></span>
<span data-ttu-id="f5793-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5793-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5793-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5793-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5793-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f5793-125">INPUTS</span></span>

### <span data-ttu-id="f5793-126">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f5793-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="f5793-127">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f5793-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f5793-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f5793-128">OUTPUTS</span></span>

### <span data-ttu-id="f5793-129">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f5793-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f5793-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f5793-130">NOTES</span></span>

## <span data-ttu-id="f5793-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5793-131">RELATED LINKS</span></span>
