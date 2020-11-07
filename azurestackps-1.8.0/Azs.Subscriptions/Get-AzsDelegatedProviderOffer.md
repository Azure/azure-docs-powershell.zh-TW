---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793614"
---
# <span data-ttu-id="89655-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="89655-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="89655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89655-102">SYNOPSIS</span></span>
<span data-ttu-id="89655-103">取得指定委派提供者的優惠清單。</span><span class="sxs-lookup"><span data-stu-id="89655-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="89655-104">句法</span><span class="sxs-lookup"><span data-stu-id="89655-104">SYNTAX</span></span>

### <span data-ttu-id="89655-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="89655-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="89655-106">獲取</span><span class="sxs-lookup"><span data-stu-id="89655-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="89655-107">說明</span><span class="sxs-lookup"><span data-stu-id="89655-107">DESCRIPTION</span></span>
<span data-ttu-id="89655-108">取得指定委派提供者的優惠清單。</span><span class="sxs-lookup"><span data-stu-id="89655-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="89655-109">示例</span><span class="sxs-lookup"><span data-stu-id="89655-109">EXAMPLES</span></span>

### <span data-ttu-id="89655-110">範例1</span><span class="sxs-lookup"><span data-stu-id="89655-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="89655-111">取得指定委派提供者的優惠清單。</span><span class="sxs-lookup"><span data-stu-id="89655-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="89655-112">參數</span><span class="sxs-lookup"><span data-stu-id="89655-112">PARAMETERS</span></span>

### <span data-ttu-id="89655-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="89655-113">-OfferName</span></span>
<span data-ttu-id="89655-114">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="89655-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89655-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="89655-115">-DelegatedProviderId</span></span>
<span data-ttu-id="89655-116">委派提供者的 Id。</span><span class="sxs-lookup"><span data-stu-id="89655-116">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89655-117">-略過</span><span class="sxs-lookup"><span data-stu-id="89655-117">-Skip</span></span>
<span data-ttu-id="89655-118">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="89655-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89655-119">-上方</span><span class="sxs-lookup"><span data-stu-id="89655-119">-Top</span></span>
<span data-ttu-id="89655-120">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="89655-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="89655-121">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="89655-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89655-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89655-122">CommonParameters</span></span>
<span data-ttu-id="89655-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89655-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89655-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89655-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89655-125">輸入</span><span class="sxs-lookup"><span data-stu-id="89655-125">INPUTS</span></span>

## <span data-ttu-id="89655-126">輸出</span><span class="sxs-lookup"><span data-stu-id="89655-126">OUTPUTS</span></span>

### <span data-ttu-id="89655-127">AzureStack 的訂閱. 方案</span><span class="sxs-lookup"><span data-stu-id="89655-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="89655-128">筆記</span><span class="sxs-lookup"><span data-stu-id="89655-128">NOTES</span></span>

## <span data-ttu-id="89655-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="89655-129">RELATED LINKS</span></span>
