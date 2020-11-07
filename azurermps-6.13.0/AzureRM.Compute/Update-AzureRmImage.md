---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624433"
---
# <span data-ttu-id="10bb8-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="10bb8-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="10bb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="10bb8-103">更新影像。</span><span class="sxs-lookup"><span data-stu-id="10bb8-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10bb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="10bb8-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10bb8-105">說明</span><span class="sxs-lookup"><span data-stu-id="10bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="10bb8-106">**更新-AzureRmImage** Cmdlet 會更新影像。</span><span class="sxs-lookup"><span data-stu-id="10bb8-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="10bb8-107">示例</span><span class="sxs-lookup"><span data-stu-id="10bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="10bb8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="10bb8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="10bb8-109">這個命令會從資源群組 "ResourceGroup01" 中現有的 [Image01] 移除邏輯單元編號1的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="10bb8-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="10bb8-110">參數</span><span class="sxs-lookup"><span data-stu-id="10bb8-110">PARAMETERS</span></span>

### <span data-ttu-id="10bb8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10bb8-111">-AsJob</span></span>
<span data-ttu-id="10bb8-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="10bb8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10bb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bb8-113">-DefaultProfile</span></span>
<span data-ttu-id="10bb8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10bb8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10bb8-115">-影像</span><span class="sxs-lookup"><span data-stu-id="10bb8-115">-Image</span></span>
<span data-ttu-id="10bb8-116">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="10bb8-116">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10bb8-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="10bb8-117">-ImageName</span></span>
<span data-ttu-id="10bb8-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="10bb8-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bb8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bb8-119">-ResourceGroupName</span></span>
<span data-ttu-id="10bb8-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10bb8-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bb8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="10bb8-121">-Confirm</span></span>
<span data-ttu-id="10bb8-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10bb8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bb8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bb8-123">-WhatIf</span></span>
<span data-ttu-id="10bb8-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10bb8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10bb8-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10bb8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bb8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bb8-126">CommonParameters</span></span>
<span data-ttu-id="10bb8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10bb8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bb8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10bb8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bb8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="10bb8-129">INPUTS</span></span>

### <span data-ttu-id="10bb8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="10bb8-130">System.String</span></span>

### <span data-ttu-id="10bb8-131">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="10bb8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="10bb8-132">參數：影像 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="10bb8-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="10bb8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="10bb8-133">OUTPUTS</span></span>

### <span data-ttu-id="10bb8-134">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="10bb8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="10bb8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="10bb8-135">NOTES</span></span>

## <span data-ttu-id="10bb8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="10bb8-136">RELATED LINKS</span></span>