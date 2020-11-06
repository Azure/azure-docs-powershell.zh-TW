---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623140"
---
# <span data-ttu-id="8082a-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="8082a-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="8082a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8082a-102">SYNOPSIS</span></span>
<span data-ttu-id="8082a-103">傳回位於某個位置的所有軟體負載平衡器實例清單。</span><span class="sxs-lookup"><span data-stu-id="8082a-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="8082a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8082a-104">SYNTAX</span></span>

### <span data-ttu-id="8082a-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8082a-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8082a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8082a-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8082a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8082a-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8082a-108">說明</span><span class="sxs-lookup"><span data-stu-id="8082a-108">DESCRIPTION</span></span>
<span data-ttu-id="8082a-109">傳回位於某個位置的所有軟體負載平衡器實例清單。</span><span class="sxs-lookup"><span data-stu-id="8082a-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="8082a-110">示例</span><span class="sxs-lookup"><span data-stu-id="8082a-110">EXAMPLES</span></span>

### <span data-ttu-id="8082a-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8082a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="8082a-112">在某個位置取得所有軟體負載平衡器複用器實例。</span><span class="sxs-lookup"><span data-stu-id="8082a-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="8082a-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8082a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="8082a-114">在指定名稱的位置取得特定軟體負載平衡器多工器實例。</span><span class="sxs-lookup"><span data-stu-id="8082a-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="8082a-115">參數</span><span class="sxs-lookup"><span data-stu-id="8082a-115">PARAMETERS</span></span>

### <span data-ttu-id="8082a-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="8082a-116">-Filter</span></span>
<span data-ttu-id="8082a-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="8082a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="8082a-118">-位置</span><span class="sxs-lookup"><span data-stu-id="8082a-118">-Location</span></span>
<span data-ttu-id="8082a-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8082a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8082a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8082a-120">-Name</span></span>
<span data-ttu-id="8082a-121">SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="8082a-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="8082a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8082a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8082a-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8082a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8082a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8082a-124">-ResourceId</span></span>
<span data-ttu-id="8082a-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8082a-125">The resource id.</span></span>

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

### <span data-ttu-id="8082a-126">-略過</span><span class="sxs-lookup"><span data-stu-id="8082a-126">-Skip</span></span>
<span data-ttu-id="8082a-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8082a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8082a-128">-上方</span><span class="sxs-lookup"><span data-stu-id="8082a-128">-Top</span></span>
<span data-ttu-id="8082a-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8082a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8082a-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="8082a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8082a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8082a-131">CommonParameters</span></span>
<span data-ttu-id="8082a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8082a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8082a-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8082a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8082a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8082a-134">INPUTS</span></span>

## <span data-ttu-id="8082a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8082a-135">OUTPUTS</span></span>

### <span data-ttu-id="8082a-136">SlbMuxInstance 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="8082a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="8082a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8082a-137">NOTES</span></span>

## <span data-ttu-id="8082a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8082a-138">RELATED LINKS</span></span>

