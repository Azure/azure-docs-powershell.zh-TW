---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793613"
---
# <span data-ttu-id="24301-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="24301-101">Get-AzsOffer</span></span>

## <span data-ttu-id="24301-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24301-102">SYNOPSIS</span></span>
<span data-ttu-id="24301-103">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="24301-103">Get the list of public offers.</span></span>

## <span data-ttu-id="24301-104">句法</span><span class="sxs-lookup"><span data-stu-id="24301-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="24301-105">說明</span><span class="sxs-lookup"><span data-stu-id="24301-105">DESCRIPTION</span></span>
<span data-ttu-id="24301-106">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="24301-106">Get the list of public offers.</span></span>

## <span data-ttu-id="24301-107">示例</span><span class="sxs-lookup"><span data-stu-id="24301-107">EXAMPLES</span></span>

### <span data-ttu-id="24301-108">範例1</span><span class="sxs-lookup"><span data-stu-id="24301-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="24301-109">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="24301-109">Get the list of public offers.</span></span>

## <span data-ttu-id="24301-110">參數</span><span class="sxs-lookup"><span data-stu-id="24301-110">PARAMETERS</span></span>

### <span data-ttu-id="24301-111">-略過</span><span class="sxs-lookup"><span data-stu-id="24301-111">-Skip</span></span>
<span data-ttu-id="24301-112">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="24301-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24301-113">-上方</span><span class="sxs-lookup"><span data-stu-id="24301-113">-Top</span></span>
<span data-ttu-id="24301-114">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="24301-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="24301-115">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="24301-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24301-116">-提供者</span><span class="sxs-lookup"><span data-stu-id="24301-116">-Provider</span></span>
<span data-ttu-id="24301-117">選用來指定委派的提供者名稱的參數。</span><span class="sxs-lookup"><span data-stu-id="24301-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="24301-118">此參數不在使用中，未來將會被否決。</span><span class="sxs-lookup"><span data-stu-id="24301-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24301-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24301-119">CommonParameters</span></span>
<span data-ttu-id="24301-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24301-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24301-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24301-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24301-122">輸入</span><span class="sxs-lookup"><span data-stu-id="24301-122">INPUTS</span></span>

## <span data-ttu-id="24301-123">輸出</span><span class="sxs-lookup"><span data-stu-id="24301-123">OUTPUTS</span></span>

### <span data-ttu-id="24301-124">AzureStack 的訂閱. 方案</span><span class="sxs-lookup"><span data-stu-id="24301-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="24301-125">筆記</span><span class="sxs-lookup"><span data-stu-id="24301-125">NOTES</span></span>

## <span data-ttu-id="24301-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="24301-126">RELATED LINKS</span></span>
