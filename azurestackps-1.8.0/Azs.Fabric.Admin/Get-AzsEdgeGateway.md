---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793525"
---
# <span data-ttu-id="1b7ec-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="1b7ec-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="1b7ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7ec-103">傳回特定位置上所有 edge 閘道的清單。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="1b7ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b7ec-104">SYNTAX</span></span>

### <span data-ttu-id="1b7ec-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1b7ec-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1b7ec-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1b7ec-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1b7ec-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b7ec-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1b7ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="1b7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1b7ec-109">傳回特定位置上所有 edge 閘道的清單。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="1b7ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="1b7ec-110">EXAMPLES</span></span>

### <span data-ttu-id="1b7ec-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1b7ec-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="1b7ec-112">取得所有 edge 閘道的清單。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="1b7ec-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1b7ec-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="1b7ec-114">取得特定的邊緣閘道。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="1b7ec-115">參數</span><span class="sxs-lookup"><span data-stu-id="1b7ec-115">PARAMETERS</span></span>

### <span data-ttu-id="1b7ec-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b7ec-116">-Name</span></span>
<span data-ttu-id="1b7ec-117">Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="1b7ec-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1b7ec-118">-Location</span></span>
<span data-ttu-id="1b7ec-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1b7ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b7ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b7ec-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1b7ec-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b7ec-122">-ResourceId</span></span>
<span data-ttu-id="1b7ec-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-123">The resource id.</span></span>

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

### <span data-ttu-id="1b7ec-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="1b7ec-124">-Filter</span></span>
<span data-ttu-id="1b7ec-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1b7ec-126">-略過</span><span class="sxs-lookup"><span data-stu-id="1b7ec-126">-Skip</span></span>
<span data-ttu-id="1b7ec-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1b7ec-128">-上方</span><span class="sxs-lookup"><span data-stu-id="1b7ec-128">-Top</span></span>
<span data-ttu-id="1b7ec-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1b7ec-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1b7ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7ec-131">CommonParameters</span></span>
<span data-ttu-id="1b7ec-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7ec-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b7ec-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7ec-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1b7ec-134">INPUTS</span></span>

## <span data-ttu-id="1b7ec-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1b7ec-135">OUTPUTS</span></span>

### <span data-ttu-id="1b7ec-136">EdgeGateway 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="1b7ec-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="1b7ec-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1b7ec-137">NOTES</span></span>

## <span data-ttu-id="1b7ec-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b7ec-138">RELATED LINKS</span></span>
