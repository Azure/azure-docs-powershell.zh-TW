---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793159"
---
# <span data-ttu-id="bcd31-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="bcd31-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="bcd31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcd31-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd31-103">傳回所有邏輯子網的清單。</span><span class="sxs-lookup"><span data-stu-id="bcd31-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="bcd31-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcd31-104">SYNTAX</span></span>

### <span data-ttu-id="bcd31-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="bcd31-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bcd31-106">獲取</span><span class="sxs-lookup"><span data-stu-id="bcd31-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcd31-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd31-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bcd31-108">說明</span><span class="sxs-lookup"><span data-stu-id="bcd31-108">DESCRIPTION</span></span>
<span data-ttu-id="bcd31-109">傳回所有邏輯子網的清單。</span><span class="sxs-lookup"><span data-stu-id="bcd31-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="bcd31-110">示例</span><span class="sxs-lookup"><span data-stu-id="bcd31-110">EXAMPLES</span></span>

### <span data-ttu-id="bcd31-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bcd31-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="bcd31-112">取得指定邏輯網路和位置的所有邏輯子網清單。</span><span class="sxs-lookup"><span data-stu-id="bcd31-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="bcd31-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bcd31-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="bcd31-114">根據名稱取得指定之邏輯網路和位置的特定邏輯子網。</span><span class="sxs-lookup"><span data-stu-id="bcd31-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="bcd31-115">參數</span><span class="sxs-lookup"><span data-stu-id="bcd31-115">PARAMETERS</span></span>

### <span data-ttu-id="bcd31-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="bcd31-116">-Filter</span></span>
<span data-ttu-id="bcd31-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="bcd31-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="bcd31-118">-位置</span><span class="sxs-lookup"><span data-stu-id="bcd31-118">-Location</span></span>
<span data-ttu-id="bcd31-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="bcd31-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bcd31-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="bcd31-120">-LogicalNetwork</span></span>
<span data-ttu-id="bcd31-121">邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcd31-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="bcd31-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcd31-122">-Name</span></span>
<span data-ttu-id="bcd31-123">邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcd31-123">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="bcd31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd31-124">-ResourceGroupName</span></span>
<span data-ttu-id="bcd31-125">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bcd31-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bcd31-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd31-126">-ResourceId</span></span>
<span data-ttu-id="bcd31-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="bcd31-127">The resource id.</span></span>

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

### <span data-ttu-id="bcd31-128">-略過</span><span class="sxs-lookup"><span data-stu-id="bcd31-128">-Skip</span></span>
<span data-ttu-id="bcd31-129">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="bcd31-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bcd31-130">-上方</span><span class="sxs-lookup"><span data-stu-id="bcd31-130">-Top</span></span>
<span data-ttu-id="bcd31-131">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="bcd31-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bcd31-132">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="bcd31-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bcd31-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd31-133">CommonParameters</span></span>
<span data-ttu-id="bcd31-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcd31-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd31-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcd31-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd31-136">輸入</span><span class="sxs-lookup"><span data-stu-id="bcd31-136">INPUTS</span></span>

## <span data-ttu-id="bcd31-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bcd31-137">OUTPUTS</span></span>

### <span data-ttu-id="bcd31-138">LogicalSubnet 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="bcd31-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="bcd31-139">筆記</span><span class="sxs-lookup"><span data-stu-id="bcd31-139">NOTES</span></span>

## <span data-ttu-id="bcd31-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcd31-140">RELATED LINKS</span></span>

