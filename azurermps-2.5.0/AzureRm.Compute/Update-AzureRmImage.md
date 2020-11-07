---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802517"
---
# <span data-ttu-id="7dd4e-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="7dd4e-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="7dd4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd4e-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dd4e-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7dd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd4e-106">**更新-AzureRmImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="7dd4e-107">示例</span><span class="sxs-lookup"><span data-stu-id="7dd4e-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd4e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7dd4e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="7dd4e-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7dd4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7dd4e-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd4e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dd4e-111">-AsJob</span></span>
<span data-ttu-id="7dd4e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7dd4e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dd4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd4e-113">-DefaultProfile</span></span>
<span data-ttu-id="7dd4e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd4e-115">-影像</span><span class="sxs-lookup"><span data-stu-id="7dd4e-115">-Image</span></span>
<span data-ttu-id="7dd4e-116">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd4e-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7dd4e-117">-ImageName</span></span>
<span data-ttu-id="7dd4e-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7dd4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7dd4e-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7dd4e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7dd4e-121">-Confirm</span></span>
<span data-ttu-id="7dd4e-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd4e-123">-WhatIf</span></span>
<span data-ttu-id="7dd4e-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd4e-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd4e-126">CommonParameters</span></span>
<span data-ttu-id="7dd4e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd4e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd4e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7dd4e-129">INPUTS</span></span>

### <span data-ttu-id="7dd4e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7dd4e-130">System.String</span></span>
<span data-ttu-id="7dd4e-131">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7dd4e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7dd4e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7dd4e-132">OUTPUTS</span></span>

### <span data-ttu-id="7dd4e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7dd4e-133">System.Object</span></span>

## <span data-ttu-id="7dd4e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7dd4e-134">NOTES</span></span>

## <span data-ttu-id="7dd4e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dd4e-135">RELATED LINKS</span></span>

