---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275188"
---
# <span data-ttu-id="51cd8-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="51cd8-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="51cd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="51cd8-103">移除私人商店提供的促銷活動。</span><span class="sxs-lookup"><span data-stu-id="51cd8-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="51cd8-104">句法</span><span class="sxs-lookup"><span data-stu-id="51cd8-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51cd8-105">說明</span><span class="sxs-lookup"><span data-stu-id="51cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="51cd8-106">從已在租使用者範圍中建立的私人存儲移除優惠。</span><span class="sxs-lookup"><span data-stu-id="51cd8-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="51cd8-107">示例</span><span class="sxs-lookup"><span data-stu-id="51cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="51cd8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="51cd8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="51cd8-109">從已在租使用者範圍中建立的私人存儲移除優惠。</span><span class="sxs-lookup"><span data-stu-id="51cd8-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="51cd8-110">參數</span><span class="sxs-lookup"><span data-stu-id="51cd8-110">PARAMETERS</span></span>

### <span data-ttu-id="51cd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cd8-111">-DefaultProfile</span></span>
<span data-ttu-id="51cd8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51cd8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51cd8-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="51cd8-113">-OfferId</span></span>
<span data-ttu-id="51cd8-114">所需的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="51cd8-114">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cd8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51cd8-115">-PassThru</span></span>
<span data-ttu-id="51cd8-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="51cd8-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="51cd8-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="51cd8-117">-PrivateStoreId</span></span>
<span data-ttu-id="51cd8-118">所需的 Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="51cd8-118">Required Azure Marketplace privateStore</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cd8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="51cd8-119">-Confirm</span></span>
<span data-ttu-id="51cd8-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="51cd8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51cd8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cd8-121">-WhatIf</span></span>
<span data-ttu-id="51cd8-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51cd8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51cd8-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51cd8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51cd8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cd8-124">CommonParameters</span></span>
<span data-ttu-id="51cd8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51cd8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cd8-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="51cd8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cd8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="51cd8-127">INPUTS</span></span>

### <span data-ttu-id="51cd8-128">所有</span><span class="sxs-lookup"><span data-stu-id="51cd8-128">None</span></span>

## <span data-ttu-id="51cd8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="51cd8-129">OUTPUTS</span></span>

### <span data-ttu-id="51cd8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="51cd8-130">System.Boolean</span></span>

## <span data-ttu-id="51cd8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="51cd8-131">NOTES</span></span>

## <span data-ttu-id="51cd8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="51cd8-132">RELATED LINKS</span></span>
