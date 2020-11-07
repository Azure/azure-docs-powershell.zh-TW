---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimage
schema: 2.0.0
ms.openlocfilehash: 5e52e75ea1af799eb2640e38cfa0e053b6b3cc7d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801733"
---
# <span data-ttu-id="f4bea-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="f4bea-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="f4bea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4bea-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bea-103">移除影像。</span><span class="sxs-lookup"><span data-stu-id="f4bea-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4bea-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4bea-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4bea-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4bea-105">DESCRIPTION</span></span>
<span data-ttu-id="f4bea-106">**AzureRmImage** Cmdlet 會移除影像。</span><span class="sxs-lookup"><span data-stu-id="f4bea-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="f4bea-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4bea-107">EXAMPLES</span></span>

### <span data-ttu-id="f4bea-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f4bea-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="f4bea-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為 "Image01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="f4bea-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f4bea-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4bea-110">PARAMETERS</span></span>

### <span data-ttu-id="f4bea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4bea-111">-AsJob</span></span>
<span data-ttu-id="f4bea-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="f4bea-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bea-113">-DefaultProfile</span></span>
<span data-ttu-id="f4bea-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4bea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f4bea-115">-Force</span></span>
<span data-ttu-id="f4bea-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f4bea-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bea-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f4bea-117">-ImageName</span></span>
<span data-ttu-id="f4bea-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4bea-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f4bea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4bea-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4bea-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4bea-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4bea-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f4bea-121">-Confirm</span></span>
<span data-ttu-id="f4bea-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4bea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4bea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4bea-123">-WhatIf</span></span>
<span data-ttu-id="f4bea-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4bea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4bea-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4bea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4bea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bea-126">CommonParameters</span></span>
<span data-ttu-id="f4bea-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4bea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bea-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4bea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bea-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f4bea-129">INPUTS</span></span>

### <span data-ttu-id="f4bea-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f4bea-130">System.String</span></span>

## <span data-ttu-id="f4bea-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f4bea-131">OUTPUTS</span></span>

### <span data-ttu-id="f4bea-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f4bea-132">System.Object</span></span>

## <span data-ttu-id="f4bea-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f4bea-133">NOTES</span></span>

## <span data-ttu-id="f4bea-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4bea-134">RELATED LINKS</span></span>

