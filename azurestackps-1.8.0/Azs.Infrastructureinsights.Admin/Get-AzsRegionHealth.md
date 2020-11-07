---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793576"
---
# <span data-ttu-id="e2f5e-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="e2f5e-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="e2f5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f5e-103">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="e2f5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2f5e-104">SYNTAX</span></span>

### <span data-ttu-id="e2f5e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e2f5e-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f5e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e2f5e-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e2f5e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f5e-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e2f5e-108">說明</span><span class="sxs-lookup"><span data-stu-id="e2f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f5e-109">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="e2f5e-110">示例</span><span class="sxs-lookup"><span data-stu-id="e2f5e-110">EXAMPLES</span></span>

### <span data-ttu-id="e2f5e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e2f5e-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="e2f5e-112">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="e2f5e-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2f5e-113">PARAMETERS</span></span>

### <span data-ttu-id="e2f5e-114">-位置</span><span class="sxs-lookup"><span data-stu-id="e2f5e-114">-Location</span></span>
<span data-ttu-id="e2f5e-115">地區名稱</span><span class="sxs-lookup"><span data-stu-id="e2f5e-115">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f5e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f5e-116">-ResourceGroupName</span></span>
<span data-ttu-id="e2f5e-117">資源群組名稱，選用。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="e2f5e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f5e-118">-ResourceId</span></span>
<span data-ttu-id="e2f5e-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-119">The resource id.</span></span>

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

### <span data-ttu-id="e2f5e-120">-篩選</span><span class="sxs-lookup"><span data-stu-id="e2f5e-120">-Filter</span></span>
<span data-ttu-id="e2f5e-121">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="e2f5e-122">-上方</span><span class="sxs-lookup"><span data-stu-id="e2f5e-122">-Top</span></span>
<span data-ttu-id="e2f5e-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e2f5e-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e2f5e-125">-略過</span><span class="sxs-lookup"><span data-stu-id="e2f5e-125">-Skip</span></span>
<span data-ttu-id="e2f5e-126">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e2f5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f5e-127">CommonParameters</span></span>
<span data-ttu-id="e2f5e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f5e-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2f5e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f5e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e2f5e-130">INPUTS</span></span>

## <span data-ttu-id="e2f5e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e2f5e-131">OUTPUTS</span></span>

### <span data-ttu-id="e2f5e-132">AzureStack InfrastructureInsights. RegionHealth （）</span><span class="sxs-lookup"><span data-stu-id="e2f5e-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="e2f5e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e2f5e-133">NOTES</span></span>

## <span data-ttu-id="e2f5e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2f5e-134">RELATED LINKS</span></span>
