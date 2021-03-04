---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: bcbfaefcc94415acdd1100025e1eefc2977f107a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902634"
---
# <span data-ttu-id="298d2-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="298d2-101">Remove-AzImage</span></span>

## <span data-ttu-id="298d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="298d2-102">SYNOPSIS</span></span>
<span data-ttu-id="298d2-103">移除影像。</span><span class="sxs-lookup"><span data-stu-id="298d2-103">Removes an image.</span></span>

## <span data-ttu-id="298d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="298d2-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="298d2-105">描述</span><span class="sxs-lookup"><span data-stu-id="298d2-105">DESCRIPTION</span></span>
<span data-ttu-id="298d2-106">**Remove-AzImage** Cmdlet 會移除影像。</span><span class="sxs-lookup"><span data-stu-id="298d2-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="298d2-107">例子</span><span class="sxs-lookup"><span data-stu-id="298d2-107">EXAMPLES</span></span>

### <span data-ttu-id="298d2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="298d2-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="298d2-109">此命令會移除資源群組 "ResourceGroup01" 中名為 "Image01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="298d2-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="298d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="298d2-110">PARAMETERS</span></span>

### <span data-ttu-id="298d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="298d2-111">-AsJob</span></span>
<span data-ttu-id="298d2-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="298d2-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="298d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298d2-113">-DefaultProfile</span></span>
<span data-ttu-id="298d2-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="298d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="298d2-115">-強制</span><span class="sxs-lookup"><span data-stu-id="298d2-115">-Force</span></span>
<span data-ttu-id="298d2-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="298d2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="298d2-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="298d2-117">-ImageName</span></span>
<span data-ttu-id="298d2-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="298d2-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="298d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="298d2-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="298d2-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="298d2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="298d2-121">-Confirm</span></span>
<span data-ttu-id="298d2-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="298d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298d2-123">-WhatIf</span></span>
<span data-ttu-id="298d2-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="298d2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298d2-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="298d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298d2-126">CommonParameters</span></span>
<span data-ttu-id="298d2-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="298d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298d2-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="298d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298d2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="298d2-129">INPUTS</span></span>

### <span data-ttu-id="298d2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="298d2-130">System.String</span></span>

## <span data-ttu-id="298d2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="298d2-131">OUTPUTS</span></span>

### <span data-ttu-id="298d2-132">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="298d2-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="298d2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="298d2-133">NOTES</span></span>

## <span data-ttu-id="298d2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="298d2-134">RELATED LINKS</span></span>
