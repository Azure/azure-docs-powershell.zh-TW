---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: 2dd2ec778a64403b9f13cd923e7b7312e72a6c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915406"
---
# <span data-ttu-id="2b3da-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="2b3da-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="2b3da-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b3da-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3da-103">取得私人市面清單</span><span class="sxs-lookup"><span data-stu-id="2b3da-103">Get private store list</span></span>

## <span data-ttu-id="2b3da-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b3da-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b3da-105">描述</span><span class="sxs-lookup"><span data-stu-id="2b3da-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3da-106">取得在租使用者範圍下建立的私人市場清單</span><span class="sxs-lookup"><span data-stu-id="2b3da-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="2b3da-107">例子</span><span class="sxs-lookup"><span data-stu-id="2b3da-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3da-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2b3da-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="2b3da-109">在租使用者範圍下建立的私人市/市清單</span><span class="sxs-lookup"><span data-stu-id="2b3da-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="2b3da-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b3da-110">PARAMETERS</span></span>

### <span data-ttu-id="2b3da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3da-111">-DefaultProfile</span></span>
<span data-ttu-id="2b3da-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b3da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b3da-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3da-113">CommonParameters</span></span>
<span data-ttu-id="2b3da-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b3da-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3da-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b3da-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3da-116">輸入</span><span class="sxs-lookup"><span data-stu-id="2b3da-116">INPUTS</span></span>

### <span data-ttu-id="2b3da-117">沒有</span><span class="sxs-lookup"><span data-stu-id="2b3da-117">None</span></span>

## <span data-ttu-id="2b3da-118">輸出</span><span class="sxs-lookup"><span data-stu-id="2b3da-118">OUTPUTS</span></span>

### <span data-ttu-id="2b3da-119">Microsoft.Azure.Commands.Marketplace.models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="2b3da-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="2b3da-120">筆記</span><span class="sxs-lookup"><span data-stu-id="2b3da-120">NOTES</span></span>

## <span data-ttu-id="2b3da-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b3da-121">RELATED LINKS</span></span>
