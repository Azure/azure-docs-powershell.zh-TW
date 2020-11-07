---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968619"
---
# <span data-ttu-id="1fc30-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1fc30-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1fc30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fc30-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc30-103">傳回位置中所有縮放單位節點的清單。</span><span class="sxs-lookup"><span data-stu-id="1fc30-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1fc30-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fc30-104">SYNTAX</span></span>

### <span data-ttu-id="1fc30-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1fc30-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1fc30-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1fc30-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1fc30-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc30-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1fc30-108">說明</span><span class="sxs-lookup"><span data-stu-id="1fc30-108">DESCRIPTION</span></span>
<span data-ttu-id="1fc30-109">傳回位置中所有縮放單位節點的清單。</span><span class="sxs-lookup"><span data-stu-id="1fc30-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="1fc30-110">示例</span><span class="sxs-lookup"><span data-stu-id="1fc30-110">EXAMPLES</span></span>

### <span data-ttu-id="1fc30-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1fc30-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="1fc30-112">取得某個位置的所有縮放單位節點。</span><span class="sxs-lookup"><span data-stu-id="1fc30-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="1fc30-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1fc30-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="1fc30-114">在指定名稱的位置取得特定的縮放單位節點。</span><span class="sxs-lookup"><span data-stu-id="1fc30-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="1fc30-115">參數</span><span class="sxs-lookup"><span data-stu-id="1fc30-115">PARAMETERS</span></span>

### <span data-ttu-id="1fc30-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fc30-116">-Name</span></span>
<span data-ttu-id="1fc30-117">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fc30-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1fc30-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1fc30-118">-Location</span></span>
<span data-ttu-id="1fc30-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1fc30-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1fc30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc30-120">-ResourceGroupName</span></span>
<span data-ttu-id="1fc30-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1fc30-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1fc30-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc30-122">-ResourceId</span></span>
<span data-ttu-id="1fc30-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1fc30-123">The resource id.</span></span>

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

### <span data-ttu-id="1fc30-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="1fc30-124">-Filter</span></span>
<span data-ttu-id="1fc30-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1fc30-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1fc30-126">-略過</span><span class="sxs-lookup"><span data-stu-id="1fc30-126">-Skip</span></span>
<span data-ttu-id="1fc30-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1fc30-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1fc30-128">-上方</span><span class="sxs-lookup"><span data-stu-id="1fc30-128">-Top</span></span>
<span data-ttu-id="1fc30-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1fc30-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1fc30-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1fc30-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1fc30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc30-131">CommonParameters</span></span>
<span data-ttu-id="1fc30-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fc30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc30-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fc30-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc30-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1fc30-134">INPUTS</span></span>

## <span data-ttu-id="1fc30-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1fc30-135">OUTPUTS</span></span>

### <span data-ttu-id="1fc30-136">ScaleUnitNode 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="1fc30-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="1fc30-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1fc30-137">NOTES</span></span>

## <span data-ttu-id="1fc30-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fc30-138">RELATED LINKS</span></span>
