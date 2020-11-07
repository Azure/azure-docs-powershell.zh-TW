---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793899"
---
# <span data-ttu-id="791c5-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="791c5-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="791c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="791c5-102">SYNOPSIS</span></span>
<span data-ttu-id="791c5-103">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="791c5-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="791c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="791c5-104">SYNTAX</span></span>

### <span data-ttu-id="791c5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="791c5-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="791c5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="791c5-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="791c5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="791c5-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="791c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="791c5-108">DESCRIPTION</span></span>
<span data-ttu-id="791c5-109">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="791c5-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="791c5-110">示例</span><span class="sxs-lookup"><span data-stu-id="791c5-110">EXAMPLES</span></span>

### <span data-ttu-id="791c5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="791c5-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="791c5-112">傳回比例單位的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="791c5-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="791c5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="791c5-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="791c5-114">傳回特定縮放單位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="791c5-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="791c5-115">參數</span><span class="sxs-lookup"><span data-stu-id="791c5-115">PARAMETERS</span></span>

### <span data-ttu-id="791c5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="791c5-116">-Name</span></span>
<span data-ttu-id="791c5-117">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="791c5-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="791c5-118">-位置</span><span class="sxs-lookup"><span data-stu-id="791c5-118">-Location</span></span>
<span data-ttu-id="791c5-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="791c5-119">Location of the resource.</span></span>

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

### <span data-ttu-id="791c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="791c5-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="791c5-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="791c5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="791c5-122">-ResourceId</span></span>
<span data-ttu-id="791c5-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="791c5-123">The resource id.</span></span>

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

### <span data-ttu-id="791c5-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="791c5-124">-Filter</span></span>
<span data-ttu-id="791c5-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="791c5-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="791c5-126">-略過</span><span class="sxs-lookup"><span data-stu-id="791c5-126">-Skip</span></span>
<span data-ttu-id="791c5-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="791c5-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="791c5-128">-上方</span><span class="sxs-lookup"><span data-stu-id="791c5-128">-Top</span></span>
<span data-ttu-id="791c5-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="791c5-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="791c5-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="791c5-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="791c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791c5-131">CommonParameters</span></span>
<span data-ttu-id="791c5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="791c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791c5-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="791c5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791c5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="791c5-134">INPUTS</span></span>

## <span data-ttu-id="791c5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="791c5-135">OUTPUTS</span></span>

### <span data-ttu-id="791c5-136">ScaleUnit 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="791c5-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="791c5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="791c5-137">NOTES</span></span>

## <span data-ttu-id="791c5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="791c5-138">RELATED LINKS</span></span>