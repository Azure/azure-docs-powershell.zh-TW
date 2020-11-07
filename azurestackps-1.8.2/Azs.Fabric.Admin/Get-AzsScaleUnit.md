---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968506"
---
# <span data-ttu-id="e5b33-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e5b33-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="e5b33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5b33-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b33-103">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="e5b33-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="e5b33-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5b33-104">SYNTAX</span></span>

### <span data-ttu-id="e5b33-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e5b33-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e5b33-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e5b33-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e5b33-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b33-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e5b33-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5b33-108">DESCRIPTION</span></span>
<span data-ttu-id="e5b33-109">傳回位於某個位置的所有縮放單位清單。</span><span class="sxs-lookup"><span data-stu-id="e5b33-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="e5b33-110">示例</span><span class="sxs-lookup"><span data-stu-id="e5b33-110">EXAMPLES</span></span>

### <span data-ttu-id="e5b33-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e5b33-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="e5b33-112">傳回比例單位的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e5b33-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="e5b33-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e5b33-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="e5b33-114">傳回特定縮放單位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b33-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="e5b33-115">參數</span><span class="sxs-lookup"><span data-stu-id="e5b33-115">PARAMETERS</span></span>

### <span data-ttu-id="e5b33-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5b33-116">-Name</span></span>
<span data-ttu-id="e5b33-117">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b33-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="e5b33-118">-位置</span><span class="sxs-lookup"><span data-stu-id="e5b33-118">-Location</span></span>
<span data-ttu-id="e5b33-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e5b33-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e5b33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b33-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5b33-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e5b33-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e5b33-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b33-122">-ResourceId</span></span>
<span data-ttu-id="e5b33-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e5b33-123">The resource id.</span></span>

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

### <span data-ttu-id="e5b33-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="e5b33-124">-Filter</span></span>
<span data-ttu-id="e5b33-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="e5b33-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="e5b33-126">-略過</span><span class="sxs-lookup"><span data-stu-id="e5b33-126">-Skip</span></span>
<span data-ttu-id="e5b33-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e5b33-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e5b33-128">-上方</span><span class="sxs-lookup"><span data-stu-id="e5b33-128">-Top</span></span>
<span data-ttu-id="e5b33-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e5b33-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e5b33-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="e5b33-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e5b33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b33-131">CommonParameters</span></span>
<span data-ttu-id="e5b33-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5b33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b33-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5b33-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b33-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e5b33-134">INPUTS</span></span>

## <span data-ttu-id="e5b33-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e5b33-135">OUTPUTS</span></span>

### <span data-ttu-id="e5b33-136">ScaleUnit 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="e5b33-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="e5b33-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e5b33-137">NOTES</span></span>

## <span data-ttu-id="e5b33-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5b33-138">RELATED LINKS</span></span>
