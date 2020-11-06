---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623144"
---
# <span data-ttu-id="aa1dd-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="aa1dd-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="aa1dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1dd-103">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="aa1dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa1dd-104">SYNTAX</span></span>

### <span data-ttu-id="aa1dd-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="aa1dd-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="aa1dd-106">獲取</span><span class="sxs-lookup"><span data-stu-id="aa1dd-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa1dd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa1dd-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aa1dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="aa1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="aa1dd-109">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="aa1dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="aa1dd-110">EXAMPLES</span></span>

### <span data-ttu-id="aa1dd-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa1dd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="aa1dd-112">傳回比例單位的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="aa1dd-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa1dd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="aa1dd-114">傳回特定縮放單位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="aa1dd-115">參數</span><span class="sxs-lookup"><span data-stu-id="aa1dd-115">PARAMETERS</span></span>

### <span data-ttu-id="aa1dd-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="aa1dd-116">-Filter</span></span>
<span data-ttu-id="aa1dd-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="aa1dd-118">-位置</span><span class="sxs-lookup"><span data-stu-id="aa1dd-118">-Location</span></span>
<span data-ttu-id="aa1dd-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-119">Location of the resource.</span></span>

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

### <span data-ttu-id="aa1dd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa1dd-120">-Name</span></span>
<span data-ttu-id="aa1dd-121">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="aa1dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa1dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa1dd-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="aa1dd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa1dd-124">-ResourceId</span></span>
<span data-ttu-id="aa1dd-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-125">The resource id.</span></span>

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

### <span data-ttu-id="aa1dd-126">-略過</span><span class="sxs-lookup"><span data-stu-id="aa1dd-126">-Skip</span></span>
<span data-ttu-id="aa1dd-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="aa1dd-128">-上方</span><span class="sxs-lookup"><span data-stu-id="aa1dd-128">-Top</span></span>
<span data-ttu-id="aa1dd-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="aa1dd-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="aa1dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1dd-131">CommonParameters</span></span>
<span data-ttu-id="aa1dd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1dd-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1dd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="aa1dd-134">INPUTS</span></span>

## <span data-ttu-id="aa1dd-135">輸出</span><span class="sxs-lookup"><span data-stu-id="aa1dd-135">OUTPUTS</span></span>

### <span data-ttu-id="aa1dd-136">ScaleUnit 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="aa1dd-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="aa1dd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="aa1dd-137">NOTES</span></span>

## <span data-ttu-id="aa1dd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa1dd-138">RELATED LINKS</span></span>

