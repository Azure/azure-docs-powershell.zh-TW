---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443179"
---
# <span data-ttu-id="2075c-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="2075c-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="2075c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2075c-102">SYNOPSIS</span></span>
<span data-ttu-id="2075c-103">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="2075c-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="2075c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2075c-104">SYNTAX</span></span>

### <span data-ttu-id="2075c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2075c-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2075c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2075c-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="2075c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2075c-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2075c-108">說明</span><span class="sxs-lookup"><span data-stu-id="2075c-108">DESCRIPTION</span></span>
<span data-ttu-id="2075c-109">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="2075c-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="2075c-110">示例</span><span class="sxs-lookup"><span data-stu-id="2075c-110">EXAMPLES</span></span>

### <span data-ttu-id="2075c-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2075c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="2075c-112">取得委派優惠清單。</span><span class="sxs-lookup"><span data-stu-id="2075c-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="2075c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2075c-113">PARAMETERS</span></span>

### <span data-ttu-id="2075c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="2075c-114">-Name</span></span>
<span data-ttu-id="2075c-115">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="2075c-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="2075c-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="2075c-116">-OfferName</span></span>
<span data-ttu-id="2075c-117">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2075c-117">Name of an offer.</span></span>

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

### <span data-ttu-id="2075c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2075c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2075c-119">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2075c-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2075c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2075c-120">-ResourceId</span></span>
<span data-ttu-id="2075c-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2075c-121">The resource id.</span></span>

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

### <span data-ttu-id="2075c-122">-略過</span><span class="sxs-lookup"><span data-stu-id="2075c-122">-Skip</span></span>
<span data-ttu-id="2075c-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2075c-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2075c-124">-上方</span><span class="sxs-lookup"><span data-stu-id="2075c-124">-Top</span></span>
<span data-ttu-id="2075c-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2075c-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2075c-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="2075c-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2075c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2075c-127">CommonParameters</span></span>
<span data-ttu-id="2075c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2075c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2075c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2075c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2075c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2075c-130">INPUTS</span></span>

## <span data-ttu-id="2075c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2075c-131">OUTPUTS</span></span>

### <span data-ttu-id="2075c-132">AzureStack OfferDelegation 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2075c-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="2075c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2075c-133">NOTES</span></span>

## <span data-ttu-id="2075c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2075c-134">RELATED LINKS</span></span>
