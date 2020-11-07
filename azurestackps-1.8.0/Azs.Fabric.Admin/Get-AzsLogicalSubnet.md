---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793507"
---
# <span data-ttu-id="0bedf-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="0bedf-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="0bedf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bedf-102">SYNOPSIS</span></span>
<span data-ttu-id="0bedf-103">傳回所有邏輯子網的清單。</span><span class="sxs-lookup"><span data-stu-id="0bedf-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="0bedf-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bedf-104">SYNTAX</span></span>

### <span data-ttu-id="0bedf-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0bedf-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0bedf-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0bedf-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bedf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bedf-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0bedf-108">說明</span><span class="sxs-lookup"><span data-stu-id="0bedf-108">DESCRIPTION</span></span>
<span data-ttu-id="0bedf-109">傳回所有邏輯子網的清單。</span><span class="sxs-lookup"><span data-stu-id="0bedf-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="0bedf-110">示例</span><span class="sxs-lookup"><span data-stu-id="0bedf-110">EXAMPLES</span></span>

### <span data-ttu-id="0bedf-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0bedf-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="0bedf-112">取得指定邏輯網路和位置的所有邏輯子網清單。</span><span class="sxs-lookup"><span data-stu-id="0bedf-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="0bedf-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0bedf-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="0bedf-114">根據名稱取得指定之邏輯網路和位置的特定邏輯子網。</span><span class="sxs-lookup"><span data-stu-id="0bedf-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="0bedf-115">參數</span><span class="sxs-lookup"><span data-stu-id="0bedf-115">PARAMETERS</span></span>

### <span data-ttu-id="0bedf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bedf-116">-Name</span></span>
<span data-ttu-id="0bedf-117">邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bedf-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="0bedf-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="0bedf-118">-LogicalNetwork</span></span>
<span data-ttu-id="0bedf-119">邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bedf-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="0bedf-120">-位置</span><span class="sxs-lookup"><span data-stu-id="0bedf-120">-Location</span></span>
<span data-ttu-id="0bedf-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0bedf-121">Location of the resource.</span></span>

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

### <span data-ttu-id="0bedf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bedf-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bedf-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0bedf-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0bedf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bedf-124">-ResourceId</span></span>
<span data-ttu-id="0bedf-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0bedf-125">The resource id.</span></span>

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

### <span data-ttu-id="0bedf-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="0bedf-126">-Filter</span></span>
<span data-ttu-id="0bedf-127">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="0bedf-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="0bedf-128">-略過</span><span class="sxs-lookup"><span data-stu-id="0bedf-128">-Skip</span></span>
<span data-ttu-id="0bedf-129">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0bedf-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0bedf-130">-上方</span><span class="sxs-lookup"><span data-stu-id="0bedf-130">-Top</span></span>
<span data-ttu-id="0bedf-131">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0bedf-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0bedf-132">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="0bedf-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0bedf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bedf-133">CommonParameters</span></span>
<span data-ttu-id="0bedf-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bedf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bedf-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bedf-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bedf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0bedf-136">INPUTS</span></span>

## <span data-ttu-id="0bedf-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0bedf-137">OUTPUTS</span></span>

### <span data-ttu-id="0bedf-138">LogicalSubnet 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="0bedf-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="0bedf-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0bedf-139">NOTES</span></span>

## <span data-ttu-id="0bedf-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bedf-140">RELATED LINKS</span></span>
