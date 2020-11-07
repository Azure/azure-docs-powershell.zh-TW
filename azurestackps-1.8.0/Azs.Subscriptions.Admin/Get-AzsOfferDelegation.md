---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793655"
---
# <span data-ttu-id="c3bb2-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c3bb2-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="c3bb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bb2-103">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c3bb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3bb2-104">SYNTAX</span></span>

### <span data-ttu-id="c3bb2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c3bb2-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3bb2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c3bb2-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c3bb2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3bb2-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c3bb2-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3bb2-108">DESCRIPTION</span></span>
<span data-ttu-id="c3bb2-109">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c3bb2-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="c3bb2-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3bb2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="c3bb2-112">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c3bb2-113">參數</span><span class="sxs-lookup"><span data-stu-id="c3bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="c3bb2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3bb2-114">-Name</span></span>
<span data-ttu-id="c3bb2-115">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c3bb2-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c3bb2-116">-OfferName</span></span>
<span data-ttu-id="c3bb2-117">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bb2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3bb2-118">-ResourceGroupName</span></span>
<span data-ttu-id="c3bb2-119">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bb2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3bb2-120">-ResourceId</span></span>
<span data-ttu-id="c3bb2-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bb2-122">-略過</span><span class="sxs-lookup"><span data-stu-id="c3bb2-122">-Skip</span></span>
<span data-ttu-id="c3bb2-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bb2-124">-上方</span><span class="sxs-lookup"><span data-stu-id="c3bb2-124">-Top</span></span>
<span data-ttu-id="c3bb2-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c3bb2-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bb2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bb2-127">CommonParameters</span></span>
<span data-ttu-id="c3bb2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bb2-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bb2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c3bb2-130">INPUTS</span></span>

## <span data-ttu-id="c3bb2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c3bb2-131">OUTPUTS</span></span>

### <span data-ttu-id="c3bb2-132">AzureStack OfferDelegation 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3bb2-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="c3bb2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c3bb2-133">NOTES</span></span>

## <span data-ttu-id="c3bb2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3bb2-134">RELATED LINKS</span></span>

