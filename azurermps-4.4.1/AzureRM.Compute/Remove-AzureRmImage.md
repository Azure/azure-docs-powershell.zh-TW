---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455844"
---
# <span data-ttu-id="753bd-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="753bd-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="753bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="753bd-102">SYNOPSIS</span></span>
<span data-ttu-id="753bd-103">移除影像。</span><span class="sxs-lookup"><span data-stu-id="753bd-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="753bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="753bd-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="753bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="753bd-105">DESCRIPTION</span></span>
<span data-ttu-id="753bd-106">**AzureRmImage** Cmdlet 會移除影像。</span><span class="sxs-lookup"><span data-stu-id="753bd-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="753bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="753bd-107">EXAMPLES</span></span>

### <span data-ttu-id="753bd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="753bd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="753bd-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為 "Image01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="753bd-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="753bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="753bd-110">PARAMETERS</span></span>

### <span data-ttu-id="753bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753bd-111">-DefaultProfile</span></span>
<span data-ttu-id="753bd-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="753bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="753bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="753bd-113">-Force</span></span>
<span data-ttu-id="753bd-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="753bd-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="753bd-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="753bd-115">-ImageName</span></span>
<span data-ttu-id="753bd-116">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="753bd-116">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="753bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="753bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="753bd-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="753bd-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="753bd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="753bd-119">-Confirm</span></span>
<span data-ttu-id="753bd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="753bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="753bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="753bd-121">-WhatIf</span></span>
<span data-ttu-id="753bd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="753bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="753bd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="753bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="753bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753bd-124">CommonParameters</span></span>
<span data-ttu-id="753bd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="753bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753bd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="753bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753bd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="753bd-127">INPUTS</span></span>

### <span data-ttu-id="753bd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="753bd-128">System.String</span></span>

## <span data-ttu-id="753bd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="753bd-129">OUTPUTS</span></span>

### <span data-ttu-id="753bd-130">System.object</span><span class="sxs-lookup"><span data-stu-id="753bd-130">System.Object</span></span>

## <span data-ttu-id="753bd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="753bd-131">NOTES</span></span>

## <span data-ttu-id="753bd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="753bd-132">RELATED LINKS</span></span>

