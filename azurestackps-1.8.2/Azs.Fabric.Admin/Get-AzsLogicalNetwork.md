---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968051"
---
# <span data-ttu-id="469ef-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="469ef-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="469ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="469ef-102">SYNOPSIS</span></span>
<span data-ttu-id="469ef-103">傳回位於某個位置的所有邏輯網路清單。</span><span class="sxs-lookup"><span data-stu-id="469ef-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="469ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="469ef-104">SYNTAX</span></span>

### <span data-ttu-id="469ef-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="469ef-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="469ef-106">獲取</span><span class="sxs-lookup"><span data-stu-id="469ef-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="469ef-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="469ef-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="469ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="469ef-108">DESCRIPTION</span></span>
<span data-ttu-id="469ef-109">傳回位於某個位置的所有邏輯網路清單。</span><span class="sxs-lookup"><span data-stu-id="469ef-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="469ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="469ef-110">EXAMPLES</span></span>

### <span data-ttu-id="469ef-111">範例1</span><span class="sxs-lookup"><span data-stu-id="469ef-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="469ef-112">取得某個位置的所有邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="469ef-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="469ef-113">範例2</span><span class="sxs-lookup"><span data-stu-id="469ef-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="469ef-114">根據名稱在某個位置取得特定的邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="469ef-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="469ef-115">參數</span><span class="sxs-lookup"><span data-stu-id="469ef-115">PARAMETERS</span></span>

### <span data-ttu-id="469ef-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="469ef-116">-Name</span></span>
<span data-ttu-id="469ef-117">邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="469ef-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="469ef-118">-位置</span><span class="sxs-lookup"><span data-stu-id="469ef-118">-Location</span></span>
<span data-ttu-id="469ef-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="469ef-119">Location of the resource.</span></span>

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

### <span data-ttu-id="469ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="469ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="469ef-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="469ef-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="469ef-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="469ef-122">-ResourceId</span></span>
<span data-ttu-id="469ef-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="469ef-123">The resource id.</span></span>

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

### <span data-ttu-id="469ef-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="469ef-124">-Filter</span></span>
<span data-ttu-id="469ef-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="469ef-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="469ef-126">-略過</span><span class="sxs-lookup"><span data-stu-id="469ef-126">-Skip</span></span>
<span data-ttu-id="469ef-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="469ef-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="469ef-128">-上方</span><span class="sxs-lookup"><span data-stu-id="469ef-128">-Top</span></span>
<span data-ttu-id="469ef-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="469ef-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="469ef-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="469ef-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="469ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469ef-131">CommonParameters</span></span>
<span data-ttu-id="469ef-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="469ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469ef-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="469ef-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469ef-134">輸入</span><span class="sxs-lookup"><span data-stu-id="469ef-134">INPUTS</span></span>

## <span data-ttu-id="469ef-135">輸出</span><span class="sxs-lookup"><span data-stu-id="469ef-135">OUTPUTS</span></span>

### <span data-ttu-id="469ef-136">LogicalNetwork 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="469ef-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="469ef-137">筆記</span><span class="sxs-lookup"><span data-stu-id="469ef-137">NOTES</span></span>

## <span data-ttu-id="469ef-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="469ef-138">RELATED LINKS</span></span>
