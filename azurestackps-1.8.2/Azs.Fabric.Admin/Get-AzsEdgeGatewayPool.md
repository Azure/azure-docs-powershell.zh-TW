---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968091"
---
# <span data-ttu-id="2a60f-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="2a60f-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="2a60f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a60f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a60f-103">傳回位置上的閘道池物件。</span><span class="sxs-lookup"><span data-stu-id="2a60f-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="2a60f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a60f-104">SYNTAX</span></span>

### <span data-ttu-id="2a60f-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2a60f-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2a60f-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2a60f-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a60f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a60f-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2a60f-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a60f-108">DESCRIPTION</span></span>
<span data-ttu-id="2a60f-109">在某個位置傳回 edge 閘道池物件。</span><span class="sxs-lookup"><span data-stu-id="2a60f-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="2a60f-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a60f-110">EXAMPLES</span></span>

### <span data-ttu-id="2a60f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2a60f-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="2a60f-112">取得所有 Edge 閘道池的清單。</span><span class="sxs-lookup"><span data-stu-id="2a60f-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="2a60f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="2a60f-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="2a60f-114">取得特定的 edge 閘道池。</span><span class="sxs-lookup"><span data-stu-id="2a60f-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="2a60f-115">參數</span><span class="sxs-lookup"><span data-stu-id="2a60f-115">PARAMETERS</span></span>

### <span data-ttu-id="2a60f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a60f-116">-Name</span></span>
<span data-ttu-id="2a60f-117">Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a60f-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="2a60f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="2a60f-118">-Location</span></span>
<span data-ttu-id="2a60f-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="2a60f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2a60f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a60f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a60f-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2a60f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2a60f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a60f-122">-ResourceId</span></span>
<span data-ttu-id="2a60f-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2a60f-123">The resource id.</span></span>

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

### <span data-ttu-id="2a60f-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="2a60f-124">-Filter</span></span>
<span data-ttu-id="2a60f-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="2a60f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="2a60f-126">-略過</span><span class="sxs-lookup"><span data-stu-id="2a60f-126">-Skip</span></span>
<span data-ttu-id="2a60f-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2a60f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2a60f-128">-上方</span><span class="sxs-lookup"><span data-stu-id="2a60f-128">-Top</span></span>
<span data-ttu-id="2a60f-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2a60f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2a60f-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="2a60f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2a60f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a60f-131">CommonParameters</span></span>
<span data-ttu-id="2a60f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a60f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a60f-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a60f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a60f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2a60f-134">INPUTS</span></span>

## <span data-ttu-id="2a60f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2a60f-135">OUTPUTS</span></span>

### <span data-ttu-id="2a60f-136">EdgeGatewayPool 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="2a60f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="2a60f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2a60f-137">NOTES</span></span>

## <span data-ttu-id="2a60f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a60f-138">RELATED LINKS</span></span>
