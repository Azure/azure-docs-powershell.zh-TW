---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793376"
---
# <span data-ttu-id="a0ea2-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="a0ea2-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="a0ea2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ea2-103">取得提供者清單做為運算子。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="a0ea2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0ea2-104">SYNTAX</span></span>

### <span data-ttu-id="a0ea2-105">ListAll (預設) </span><span class="sxs-lookup"><span data-stu-id="a0ea2-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a0ea2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a0ea2-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="a0ea2-107">清單</span><span class="sxs-lookup"><span data-stu-id="a0ea2-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a0ea2-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ea2-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a0ea2-109">說明</span><span class="sxs-lookup"><span data-stu-id="a0ea2-109">DESCRIPTION</span></span>
<span data-ttu-id="a0ea2-110">取得優惠清單。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-110">Get the list of offers.</span></span>

## <span data-ttu-id="a0ea2-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0ea2-111">EXAMPLES</span></span>

### <span data-ttu-id="a0ea2-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a0ea2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="a0ea2-113">取得提供者清單做為運算子。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="a0ea2-114">參數</span><span class="sxs-lookup"><span data-stu-id="a0ea2-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ea2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0ea2-115">-Name</span></span>
<span data-ttu-id="a0ea2-116">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-116">Name of an offer.</span></span>

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

### <span data-ttu-id="a0ea2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ea2-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0ea2-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ea2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ea2-119">-ResourceId</span></span>
<span data-ttu-id="a0ea2-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-120">The resource id.</span></span>

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

### <span data-ttu-id="a0ea2-121">-略過</span><span class="sxs-lookup"><span data-stu-id="a0ea2-121">-Skip</span></span>
<span data-ttu-id="a0ea2-122">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ea2-123">-上方</span><span class="sxs-lookup"><span data-stu-id="a0ea2-123">-Top</span></span>
<span data-ttu-id="a0ea2-124">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a0ea2-125">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ea2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ea2-126">CommonParameters</span></span>
<span data-ttu-id="a0ea2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ea2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ea2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a0ea2-129">INPUTS</span></span>

## <span data-ttu-id="a0ea2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a0ea2-130">OUTPUTS</span></span>

### <span data-ttu-id="a0ea2-131">AzureStack 的訂閱. 管理模型。</span><span class="sxs-lookup"><span data-stu-id="a0ea2-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="a0ea2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a0ea2-132">NOTES</span></span>

## <span data-ttu-id="a0ea2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0ea2-133">RELATED LINKS</span></span>

