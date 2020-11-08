---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137688"
---
# <span data-ttu-id="fffcc-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="fffcc-101">Remove-AzImage</span></span>

## <span data-ttu-id="fffcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fffcc-102">SYNOPSIS</span></span>
<span data-ttu-id="fffcc-103">移除影像。</span><span class="sxs-lookup"><span data-stu-id="fffcc-103">Removes an image.</span></span>

## <span data-ttu-id="fffcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="fffcc-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fffcc-105">說明</span><span class="sxs-lookup"><span data-stu-id="fffcc-105">DESCRIPTION</span></span>
<span data-ttu-id="fffcc-106">**AzImage** Cmdlet 會移除影像。</span><span class="sxs-lookup"><span data-stu-id="fffcc-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="fffcc-107">示例</span><span class="sxs-lookup"><span data-stu-id="fffcc-107">EXAMPLES</span></span>

### <span data-ttu-id="fffcc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fffcc-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="fffcc-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為 "Image01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="fffcc-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fffcc-110">參數</span><span class="sxs-lookup"><span data-stu-id="fffcc-110">PARAMETERS</span></span>

### <span data-ttu-id="fffcc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fffcc-111">-AsJob</span></span>
<span data-ttu-id="fffcc-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="fffcc-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fffcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffcc-113">-DefaultProfile</span></span>
<span data-ttu-id="fffcc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fffcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fffcc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fffcc-115">-Force</span></span>
<span data-ttu-id="fffcc-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fffcc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fffcc-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fffcc-117">-ImageName</span></span>
<span data-ttu-id="fffcc-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffcc-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="fffcc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffcc-119">-ResourceGroupName</span></span>
<span data-ttu-id="fffcc-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffcc-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fffcc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fffcc-121">-Confirm</span></span>
<span data-ttu-id="fffcc-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fffcc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffcc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffcc-123">-WhatIf</span></span>
<span data-ttu-id="fffcc-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fffcc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffcc-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fffcc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffcc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffcc-126">CommonParameters</span></span>
<span data-ttu-id="fffcc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fffcc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffcc-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fffcc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffcc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fffcc-129">INPUTS</span></span>

### <span data-ttu-id="fffcc-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fffcc-130">System.String</span></span>

## <span data-ttu-id="fffcc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fffcc-131">OUTPUTS</span></span>

### <span data-ttu-id="fffcc-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fffcc-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fffcc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fffcc-133">NOTES</span></span>

## <span data-ttu-id="fffcc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fffcc-134">RELATED LINKS</span></span>
