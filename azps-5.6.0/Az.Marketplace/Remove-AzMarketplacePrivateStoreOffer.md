---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 829f6b4e95e1d45d68f12ed6dbd8ad7c7987eba3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915394"
---
# <span data-ttu-id="b23e6-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b23e6-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="b23e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b23e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b23e6-103">從私人市商店移除優惠。</span><span class="sxs-lookup"><span data-stu-id="b23e6-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="b23e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="b23e6-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b23e6-105">描述</span><span class="sxs-lookup"><span data-stu-id="b23e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b23e6-106">從租使用者範圍中建立的私人市場移除優惠。</span><span class="sxs-lookup"><span data-stu-id="b23e6-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b23e6-107">例子</span><span class="sxs-lookup"><span data-stu-id="b23e6-107">EXAMPLES</span></span>

### <span data-ttu-id="b23e6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b23e6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="b23e6-109">從租使用者範圍中建立的私人市場移除優惠。</span><span class="sxs-lookup"><span data-stu-id="b23e6-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b23e6-110">參數</span><span class="sxs-lookup"><span data-stu-id="b23e6-110">PARAMETERS</span></span>

### <span data-ttu-id="b23e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23e6-111">-DefaultProfile</span></span>
<span data-ttu-id="b23e6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b23e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b23e6-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b23e6-113">-OfferId</span></span>
<span data-ttu-id="b23e6-114">必要的 Azure Marketplace privateStore 優惠</span><span class="sxs-lookup"><span data-stu-id="b23e6-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="b23e6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b23e6-115">-PassThru</span></span>
<span data-ttu-id="b23e6-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b23e6-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b23e6-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="b23e6-117">-PrivateStoreId</span></span>
<span data-ttu-id="b23e6-118">必要的 Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="b23e6-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="b23e6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b23e6-119">-Confirm</span></span>
<span data-ttu-id="b23e6-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b23e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b23e6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b23e6-121">-WhatIf</span></span>
<span data-ttu-id="b23e6-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b23e6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b23e6-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b23e6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b23e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23e6-124">CommonParameters</span></span>
<span data-ttu-id="b23e6-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b23e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23e6-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b23e6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23e6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b23e6-127">INPUTS</span></span>

### <span data-ttu-id="b23e6-128">沒有</span><span class="sxs-lookup"><span data-stu-id="b23e6-128">None</span></span>

## <span data-ttu-id="b23e6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b23e6-129">OUTPUTS</span></span>

### <span data-ttu-id="b23e6-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b23e6-130">System.Boolean</span></span>

## <span data-ttu-id="b23e6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b23e6-131">NOTES</span></span>

## <span data-ttu-id="b23e6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b23e6-132">RELATED LINKS</span></span>
