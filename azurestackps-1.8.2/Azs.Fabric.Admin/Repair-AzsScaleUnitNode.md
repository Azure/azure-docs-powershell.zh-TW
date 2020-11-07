---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968209"
---
# <span data-ttu-id="7128f-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="7128f-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="7128f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7128f-102">SYNOPSIS</span></span>
<span data-ttu-id="7128f-103">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="7128f-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="7128f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7128f-104">SYNTAX</span></span>

### <span data-ttu-id="7128f-105">修復 (預設) </span><span class="sxs-lookup"><span data-stu-id="7128f-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7128f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7128f-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7128f-107">說明</span><span class="sxs-lookup"><span data-stu-id="7128f-107">DESCRIPTION</span></span>
<span data-ttu-id="7128f-108">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="7128f-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="7128f-109">示例</span><span class="sxs-lookup"><span data-stu-id="7128f-109">EXAMPLES</span></span>

### <span data-ttu-id="7128f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7128f-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="7128f-111">修復 [縮放單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="7128f-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="7128f-112">參數</span><span class="sxs-lookup"><span data-stu-id="7128f-112">PARAMETERS</span></span>

### <span data-ttu-id="7128f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7128f-113">-Name</span></span>
<span data-ttu-id="7128f-114">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="7128f-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="7128f-115">-BMCIPv4Address</span></span>
<span data-ttu-id="7128f-116">物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="7128f-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7128f-117">-Location</span></span>
<span data-ttu-id="7128f-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="7128f-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7128f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7128f-120">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7128f-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7128f-121">-ResourceId</span></span>
<span data-ttu-id="7128f-122">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7128f-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="7128f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7128f-123">-AsJob</span></span>
<span data-ttu-id="7128f-124">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="7128f-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7128f-125">-Force</span></span>
<span data-ttu-id="7128f-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="7128f-126">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7128f-127">-WhatIf</span></span>
<span data-ttu-id="7128f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7128f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7128f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7128f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="7128f-130">-Confirm</span></span>
<span data-ttu-id="7128f-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7128f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7128f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7128f-132">CommonParameters</span></span>
<span data-ttu-id="7128f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7128f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7128f-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7128f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7128f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7128f-135">INPUTS</span></span>

## <span data-ttu-id="7128f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7128f-136">OUTPUTS</span></span>

## <span data-ttu-id="7128f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7128f-137">NOTES</span></span>

## <span data-ttu-id="7128f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7128f-138">RELATED LINKS</span></span>
