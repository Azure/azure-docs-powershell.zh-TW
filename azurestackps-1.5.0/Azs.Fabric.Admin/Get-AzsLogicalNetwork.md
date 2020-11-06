---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443595"
---
# <span data-ttu-id="aa9e1-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="aa9e1-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="aa9e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9e1-103">傳回位於某個位置的所有邏輯網路清單。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="aa9e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa9e1-104">SYNTAX</span></span>

### <span data-ttu-id="aa9e1-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="aa9e1-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="aa9e1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="aa9e1-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa9e1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa9e1-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aa9e1-108">說明</span><span class="sxs-lookup"><span data-stu-id="aa9e1-108">DESCRIPTION</span></span>
<span data-ttu-id="aa9e1-109">傳回位於某個位置的所有邏輯網路清單。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="aa9e1-110">示例</span><span class="sxs-lookup"><span data-stu-id="aa9e1-110">EXAMPLES</span></span>

### <span data-ttu-id="aa9e1-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa9e1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="aa9e1-112">取得某個位置的所有邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="aa9e1-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa9e1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="aa9e1-114">根據名稱在某個位置取得特定的邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="aa9e1-115">參數</span><span class="sxs-lookup"><span data-stu-id="aa9e1-115">PARAMETERS</span></span>

### <span data-ttu-id="aa9e1-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="aa9e1-116">-Filter</span></span>
<span data-ttu-id="aa9e1-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="aa9e1-118">-位置</span><span class="sxs-lookup"><span data-stu-id="aa9e1-118">-Location</span></span>
<span data-ttu-id="aa9e1-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="aa9e1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa9e1-120">-Name</span></span>
<span data-ttu-id="aa9e1-121">邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="aa9e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa9e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa9e1-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="aa9e1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa9e1-124">-ResourceId</span></span>
<span data-ttu-id="aa9e1-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-125">The resource id.</span></span>

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

### <span data-ttu-id="aa9e1-126">-略過</span><span class="sxs-lookup"><span data-stu-id="aa9e1-126">-Skip</span></span>
<span data-ttu-id="aa9e1-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="aa9e1-128">-上方</span><span class="sxs-lookup"><span data-stu-id="aa9e1-128">-Top</span></span>
<span data-ttu-id="aa9e1-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="aa9e1-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="aa9e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9e1-131">CommonParameters</span></span>
<span data-ttu-id="aa9e1-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9e1-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa9e1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9e1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="aa9e1-134">INPUTS</span></span>

## <span data-ttu-id="aa9e1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="aa9e1-135">OUTPUTS</span></span>

### <span data-ttu-id="aa9e1-136">LogicalNetwork 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="aa9e1-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="aa9e1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="aa9e1-137">NOTES</span></span>

## <span data-ttu-id="aa9e1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa9e1-138">RELATED LINKS</span></span>

