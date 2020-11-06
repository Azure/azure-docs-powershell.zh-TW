---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611569"
---
# <span data-ttu-id="ce512-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="ce512-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="ce512-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce512-102">SYNOPSIS</span></span>
<span data-ttu-id="ce512-103">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="ce512-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ce512-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce512-104">SYNTAX</span></span>

### <span data-ttu-id="ce512-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ce512-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce512-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ce512-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ce512-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce512-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ce512-108">說明</span><span class="sxs-lookup"><span data-stu-id="ce512-108">DESCRIPTION</span></span>
<span data-ttu-id="ce512-109">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="ce512-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ce512-110">示例</span><span class="sxs-lookup"><span data-stu-id="ce512-110">EXAMPLES</span></span>

### <span data-ttu-id="ce512-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ce512-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="ce512-112">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="ce512-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="ce512-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ce512-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="ce512-114">根據名稱返回位置。</span><span class="sxs-lookup"><span data-stu-id="ce512-114">Return a location based on the name.</span></span>

## <span data-ttu-id="ce512-115">參數</span><span class="sxs-lookup"><span data-stu-id="ce512-115">PARAMETERS</span></span>

### <span data-ttu-id="ce512-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="ce512-116">-Filter</span></span>
<span data-ttu-id="ce512-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ce512-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ce512-118">-位置</span><span class="sxs-lookup"><span data-stu-id="ce512-118">-Location</span></span>
<span data-ttu-id="ce512-119">Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="ce512-119">Fabric location.</span></span>

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

### <span data-ttu-id="ce512-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce512-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce512-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ce512-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ce512-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce512-122">-ResourceId</span></span>
<span data-ttu-id="ce512-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ce512-123">The resource id.</span></span>

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

### <span data-ttu-id="ce512-124">-略過</span><span class="sxs-lookup"><span data-stu-id="ce512-124">-Skip</span></span>
<span data-ttu-id="ce512-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ce512-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ce512-126">-上方</span><span class="sxs-lookup"><span data-stu-id="ce512-126">-Top</span></span>
<span data-ttu-id="ce512-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ce512-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ce512-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="ce512-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ce512-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce512-129">CommonParameters</span></span>
<span data-ttu-id="ce512-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce512-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce512-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce512-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce512-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ce512-132">INPUTS</span></span>

## <span data-ttu-id="ce512-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ce512-133">OUTPUTS</span></span>

### <span data-ttu-id="ce512-134">FabricLocation 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="ce512-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="ce512-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ce512-135">NOTES</span></span>

## <span data-ttu-id="ce512-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce512-136">RELATED LINKS</span></span>
