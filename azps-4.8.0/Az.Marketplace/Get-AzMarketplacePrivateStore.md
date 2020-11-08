---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970987"
---
# <span data-ttu-id="dbd61-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="dbd61-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="dbd61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbd61-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd61-103">取得私人商店清單</span><span class="sxs-lookup"><span data-stu-id="dbd61-103">Get private store list</span></span>

## <span data-ttu-id="dbd61-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbd61-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd61-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbd61-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd61-106">取得在租使用者範圍下建立的私人商店清單</span><span class="sxs-lookup"><span data-stu-id="dbd61-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="dbd61-107">示例</span><span class="sxs-lookup"><span data-stu-id="dbd61-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd61-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dbd61-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="dbd61-109">在租使用者範圍中建立的私人商店清單</span><span class="sxs-lookup"><span data-stu-id="dbd61-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="dbd61-110">參數</span><span class="sxs-lookup"><span data-stu-id="dbd61-110">PARAMETERS</span></span>

### <span data-ttu-id="dbd61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd61-111">-DefaultProfile</span></span>
<span data-ttu-id="dbd61-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbd61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd61-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd61-113">CommonParameters</span></span>
<span data-ttu-id="dbd61-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbd61-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd61-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbd61-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd61-116">輸入</span><span class="sxs-lookup"><span data-stu-id="dbd61-116">INPUTS</span></span>

### <span data-ttu-id="dbd61-117">所有</span><span class="sxs-lookup"><span data-stu-id="dbd61-117">None</span></span>

## <span data-ttu-id="dbd61-118">輸出</span><span class="sxs-lookup"><span data-stu-id="dbd61-118">OUTPUTS</span></span>

### <span data-ttu-id="dbd61-119">[PrivateStore]. [PSPrivateStore]</span><span class="sxs-lookup"><span data-stu-id="dbd61-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="dbd61-120">筆記</span><span class="sxs-lookup"><span data-stu-id="dbd61-120">NOTES</span></span>

## <span data-ttu-id="dbd61-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbd61-121">RELATED LINKS</span></span>
