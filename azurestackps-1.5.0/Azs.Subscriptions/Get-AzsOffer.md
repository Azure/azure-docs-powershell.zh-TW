---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442947"
---
# <span data-ttu-id="1207a-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="1207a-101">Get-AzsOffer</span></span>

## <span data-ttu-id="1207a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1207a-102">SYNOPSIS</span></span>
<span data-ttu-id="1207a-103">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="1207a-103">Get the list of public offers.</span></span>

## <span data-ttu-id="1207a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1207a-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1207a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1207a-105">DESCRIPTION</span></span>
<span data-ttu-id="1207a-106">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="1207a-106">Get the list of public offers.</span></span>

## <span data-ttu-id="1207a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1207a-107">EXAMPLES</span></span>

### <span data-ttu-id="1207a-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1207a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="1207a-109">取得公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="1207a-109">Get the list of public offers.</span></span>

## <span data-ttu-id="1207a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1207a-110">PARAMETERS</span></span>

### <span data-ttu-id="1207a-111">-略過</span><span class="sxs-lookup"><span data-stu-id="1207a-111">-Skip</span></span>
<span data-ttu-id="1207a-112">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1207a-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1207a-113">-上方</span><span class="sxs-lookup"><span data-stu-id="1207a-113">-Top</span></span>
<span data-ttu-id="1207a-114">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1207a-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1207a-115">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1207a-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1207a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1207a-116">CommonParameters</span></span>
<span data-ttu-id="1207a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1207a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1207a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1207a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1207a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1207a-119">INPUTS</span></span>

## <span data-ttu-id="1207a-120">輸出</span><span class="sxs-lookup"><span data-stu-id="1207a-120">OUTPUTS</span></span>

### <span data-ttu-id="1207a-121">AzureStack 的訂閱. 方案</span><span class="sxs-lookup"><span data-stu-id="1207a-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="1207a-122">筆記</span><span class="sxs-lookup"><span data-stu-id="1207a-122">NOTES</span></span>

## <span data-ttu-id="1207a-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="1207a-123">RELATED LINKS</span></span>

