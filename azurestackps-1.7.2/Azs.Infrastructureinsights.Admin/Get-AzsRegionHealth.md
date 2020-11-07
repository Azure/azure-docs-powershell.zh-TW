---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793325"
---
# <span data-ttu-id="87fdb-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="87fdb-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="87fdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="87fdb-103">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="87fdb-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="87fdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="87fdb-104">SYNTAX</span></span>

### <span data-ttu-id="87fdb-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="87fdb-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="87fdb-106">獲取</span><span class="sxs-lookup"><span data-stu-id="87fdb-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="87fdb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87fdb-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="87fdb-108">說明</span><span class="sxs-lookup"><span data-stu-id="87fdb-108">DESCRIPTION</span></span>
<span data-ttu-id="87fdb-109">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="87fdb-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="87fdb-110">示例</span><span class="sxs-lookup"><span data-stu-id="87fdb-110">EXAMPLES</span></span>

### <span data-ttu-id="87fdb-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="87fdb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="87fdb-112">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="87fdb-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="87fdb-113">參數</span><span class="sxs-lookup"><span data-stu-id="87fdb-113">PARAMETERS</span></span>

### <span data-ttu-id="87fdb-114">-篩選</span><span class="sxs-lookup"><span data-stu-id="87fdb-114">-Filter</span></span>
<span data-ttu-id="87fdb-115">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="87fdb-115">OData filter parameter.</span></span>

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

### <span data-ttu-id="87fdb-116">-位置</span><span class="sxs-lookup"><span data-stu-id="87fdb-116">-Location</span></span>
<span data-ttu-id="87fdb-117">地區名稱</span><span class="sxs-lookup"><span data-stu-id="87fdb-117">Name of the region</span></span>

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

### <span data-ttu-id="87fdb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87fdb-118">-ResourceGroupName</span></span>
<span data-ttu-id="87fdb-119">資源所駐留的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="87fdb-119">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="87fdb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87fdb-120">-ResourceId</span></span>
<span data-ttu-id="87fdb-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="87fdb-121">The resource id.</span></span>

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

### <span data-ttu-id="87fdb-122">-略過</span><span class="sxs-lookup"><span data-stu-id="87fdb-122">-Skip</span></span>
<span data-ttu-id="87fdb-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="87fdb-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="87fdb-124">-上方</span><span class="sxs-lookup"><span data-stu-id="87fdb-124">-Top</span></span>
<span data-ttu-id="87fdb-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="87fdb-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="87fdb-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="87fdb-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="87fdb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fdb-127">CommonParameters</span></span>
<span data-ttu-id="87fdb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87fdb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fdb-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87fdb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fdb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="87fdb-130">INPUTS</span></span>

## <span data-ttu-id="87fdb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="87fdb-131">OUTPUTS</span></span>

### <span data-ttu-id="87fdb-132">AzureStack InfrastructureInsights. RegionHealth （）</span><span class="sxs-lookup"><span data-stu-id="87fdb-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="87fdb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="87fdb-133">NOTES</span></span>

## <span data-ttu-id="87fdb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="87fdb-134">RELATED LINKS</span></span>
