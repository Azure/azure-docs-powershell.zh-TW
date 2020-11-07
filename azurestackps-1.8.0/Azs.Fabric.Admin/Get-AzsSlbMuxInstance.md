---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793494"
---
# <span data-ttu-id="1f9a7-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="1f9a7-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="1f9a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9a7-103">傳回位於某個位置的所有軟體負載平衡器實例清單。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="1f9a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f9a7-104">SYNTAX</span></span>

### <span data-ttu-id="1f9a7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1f9a7-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1f9a7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1f9a7-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f9a7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a7-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1f9a7-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f9a7-108">DESCRIPTION</span></span>
<span data-ttu-id="1f9a7-109">傳回位於某個位置的所有軟體負載平衡器實例清單。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="1f9a7-110">示例</span><span class="sxs-lookup"><span data-stu-id="1f9a7-110">EXAMPLES</span></span>

### <span data-ttu-id="1f9a7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1f9a7-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="1f9a7-112">在某個位置取得所有軟體負載平衡器複用器實例。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="1f9a7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1f9a7-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="1f9a7-114">在指定名稱的位置取得特定軟體負載平衡器多工器實例。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="1f9a7-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f9a7-115">PARAMETERS</span></span>

### <span data-ttu-id="1f9a7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f9a7-116">-Name</span></span>
<span data-ttu-id="1f9a7-117">SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="1f9a7-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1f9a7-118">-Location</span></span>
<span data-ttu-id="1f9a7-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1f9a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f9a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f9a7-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1f9a7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a7-122">-ResourceId</span></span>
<span data-ttu-id="1f9a7-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-123">The resource id.</span></span>

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

### <span data-ttu-id="1f9a7-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="1f9a7-124">-Filter</span></span>
<span data-ttu-id="1f9a7-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1f9a7-126">-略過</span><span class="sxs-lookup"><span data-stu-id="1f9a7-126">-Skip</span></span>
<span data-ttu-id="1f9a7-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1f9a7-128">-上方</span><span class="sxs-lookup"><span data-stu-id="1f9a7-128">-Top</span></span>
<span data-ttu-id="1f9a7-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1f9a7-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1f9a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9a7-131">CommonParameters</span></span>
<span data-ttu-id="1f9a7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9a7-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f9a7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9a7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1f9a7-134">INPUTS</span></span>

## <span data-ttu-id="1f9a7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1f9a7-135">OUTPUTS</span></span>

### <span data-ttu-id="1f9a7-136">SlbMuxInstance 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="1f9a7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="1f9a7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1f9a7-137">NOTES</span></span>

## <span data-ttu-id="1f9a7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f9a7-138">RELATED LINKS</span></span>