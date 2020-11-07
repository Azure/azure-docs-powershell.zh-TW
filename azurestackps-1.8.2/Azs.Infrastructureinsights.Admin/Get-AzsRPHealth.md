---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968560"
---
# <span data-ttu-id="c01d3-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="c01d3-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="c01d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c01d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c01d3-103">傳回每個服務健康情況的清單。</span><span class="sxs-lookup"><span data-stu-id="c01d3-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="c01d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c01d3-104">SYNTAX</span></span>

### <span data-ttu-id="c01d3-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c01d3-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c01d3-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c01d3-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c01d3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c01d3-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c01d3-108">說明</span><span class="sxs-lookup"><span data-stu-id="c01d3-108">DESCRIPTION</span></span>
<span data-ttu-id="c01d3-109">傳回每個服務健康情況的清單。</span><span class="sxs-lookup"><span data-stu-id="c01d3-109">Returns a list of each service's health.</span></span> <span data-ttu-id="c01d3-110">AlertSummary 屬性包含有關警告/錯誤計數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c01d3-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="c01d3-111">示例</span><span class="sxs-lookup"><span data-stu-id="c01d3-111">EXAMPLES</span></span>

### <span data-ttu-id="c01d3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c01d3-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="c01d3-113">傳回每個服務健康情況的清單。</span><span class="sxs-lookup"><span data-stu-id="c01d3-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="c01d3-114">範例2</span><span class="sxs-lookup"><span data-stu-id="c01d3-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="c01d3-115">傳回服務的健康情況。</span><span class="sxs-lookup"><span data-stu-id="c01d3-115">Returns a service's health.</span></span>

## <span data-ttu-id="c01d3-116">參數</span><span class="sxs-lookup"><span data-stu-id="c01d3-116">PARAMETERS</span></span>

### <span data-ttu-id="c01d3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c01d3-117">-Name</span></span>
<span data-ttu-id="c01d3-118">服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="c01d3-118">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01d3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="c01d3-119">-Location</span></span>
<span data-ttu-id="c01d3-120">地區名稱</span><span class="sxs-lookup"><span data-stu-id="c01d3-120">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c01d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="c01d3-122">資源群組的名稱，選用。</span><span class="sxs-lookup"><span data-stu-id="c01d3-122">Name of the resource group, optional.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01d3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c01d3-123">-ResourceId</span></span>
<span data-ttu-id="c01d3-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c01d3-124">The resource id.</span></span>

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

### <span data-ttu-id="c01d3-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="c01d3-125">-Filter</span></span>
<span data-ttu-id="c01d3-126">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c01d3-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01d3-127">-略過</span><span class="sxs-lookup"><span data-stu-id="c01d3-127">-Skip</span></span>
<span data-ttu-id="c01d3-128">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c01d3-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c01d3-129">-上方</span><span class="sxs-lookup"><span data-stu-id="c01d3-129">-Top</span></span>
<span data-ttu-id="c01d3-130">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c01d3-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c01d3-131">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="c01d3-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c01d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01d3-132">CommonParameters</span></span>
<span data-ttu-id="c01d3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c01d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01d3-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c01d3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01d3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c01d3-135">INPUTS</span></span>

## <span data-ttu-id="c01d3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c01d3-136">OUTPUTS</span></span>

### <span data-ttu-id="c01d3-137">AzureStack InfrastructureInsights. ServiceHealth （）</span><span class="sxs-lookup"><span data-stu-id="c01d3-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="c01d3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c01d3-138">NOTES</span></span>

## <span data-ttu-id="c01d3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c01d3-139">RELATED LINKS</span></span>
