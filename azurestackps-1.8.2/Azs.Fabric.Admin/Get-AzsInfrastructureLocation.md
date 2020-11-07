---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968092"
---
# <span data-ttu-id="f3f90-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="f3f90-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="f3f90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3f90-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f90-103">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="f3f90-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="f3f90-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3f90-104">SYNTAX</span></span>

### <span data-ttu-id="f3f90-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f3f90-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3f90-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f3f90-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3f90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f90-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3f90-108">說明</span><span class="sxs-lookup"><span data-stu-id="f3f90-108">DESCRIPTION</span></span>
<span data-ttu-id="f3f90-109">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="f3f90-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="f3f90-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3f90-110">EXAMPLES</span></span>

### <span data-ttu-id="f3f90-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f3f90-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="f3f90-112">傳回所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="f3f90-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="f3f90-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f3f90-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="f3f90-114">根據名稱返回位置。</span><span class="sxs-lookup"><span data-stu-id="f3f90-114">Return a location based on the name.</span></span>

## <span data-ttu-id="f3f90-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3f90-115">PARAMETERS</span></span>

### <span data-ttu-id="f3f90-116">-位置</span><span class="sxs-lookup"><span data-stu-id="f3f90-116">-Location</span></span>
<span data-ttu-id="f3f90-117">Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="f3f90-117">Fabric location.</span></span>

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

### <span data-ttu-id="f3f90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f90-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3f90-119">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f3f90-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f3f90-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f90-120">-ResourceId</span></span>
<span data-ttu-id="f3f90-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f3f90-121">The resource id.</span></span>

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

### <span data-ttu-id="f3f90-122">-篩選</span><span class="sxs-lookup"><span data-stu-id="f3f90-122">-Filter</span></span>
<span data-ttu-id="f3f90-123">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f3f90-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="f3f90-124">-略過</span><span class="sxs-lookup"><span data-stu-id="f3f90-124">-Skip</span></span>
<span data-ttu-id="f3f90-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f3f90-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f3f90-126">-上方</span><span class="sxs-lookup"><span data-stu-id="f3f90-126">-Top</span></span>
<span data-ttu-id="f3f90-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f3f90-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f3f90-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="f3f90-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f3f90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f90-129">CommonParameters</span></span>
<span data-ttu-id="f3f90-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3f90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f90-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3f90-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f90-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f3f90-132">INPUTS</span></span>

## <span data-ttu-id="f3f90-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f3f90-133">OUTPUTS</span></span>

### <span data-ttu-id="f3f90-134">FabricLocation 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="f3f90-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="f3f90-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f3f90-135">NOTES</span></span>

## <span data-ttu-id="f3f90-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3f90-136">RELATED LINKS</span></span>
