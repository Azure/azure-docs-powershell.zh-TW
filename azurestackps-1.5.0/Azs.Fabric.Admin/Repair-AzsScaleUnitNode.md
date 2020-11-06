---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442548"
---
# <span data-ttu-id="13dc6-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="13dc6-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="13dc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="13dc6-103">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="13dc6-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="13dc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="13dc6-104">SYNTAX</span></span>

### <span data-ttu-id="13dc6-105">修復 (預設) </span><span class="sxs-lookup"><span data-stu-id="13dc6-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13dc6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13dc6-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13dc6-107">說明</span><span class="sxs-lookup"><span data-stu-id="13dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="13dc6-108">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="13dc6-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="13dc6-109">示例</span><span class="sxs-lookup"><span data-stu-id="13dc6-109">EXAMPLES</span></span>

### <span data-ttu-id="13dc6-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="13dc6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="13dc6-111">修復 [縮放單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="13dc6-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="13dc6-112">參數</span><span class="sxs-lookup"><span data-stu-id="13dc6-112">PARAMETERS</span></span>

### <span data-ttu-id="13dc6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13dc6-113">-AsJob</span></span>
<span data-ttu-id="13dc6-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="13dc6-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="13dc6-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="13dc6-115">-BMCIPv4Address</span></span>
<span data-ttu-id="13dc6-116">物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="13dc6-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="13dc6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13dc6-117">-Force</span></span>
<span data-ttu-id="13dc6-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="13dc6-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="13dc6-119">-位置</span><span class="sxs-lookup"><span data-stu-id="13dc6-119">-Location</span></span>
<span data-ttu-id="13dc6-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="13dc6-120">Location of the resource.</span></span>

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

### <span data-ttu-id="13dc6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="13dc6-121">-Name</span></span>
<span data-ttu-id="13dc6-122">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="13dc6-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="13dc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13dc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="13dc6-124">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="13dc6-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="13dc6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13dc6-125">-ResourceId</span></span>
<span data-ttu-id="13dc6-126">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="13dc6-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="13dc6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="13dc6-127">-Confirm</span></span>
<span data-ttu-id="13dc6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13dc6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13dc6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13dc6-129">-WhatIf</span></span>
<span data-ttu-id="13dc6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13dc6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13dc6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13dc6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13dc6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13dc6-132">CommonParameters</span></span>
<span data-ttu-id="13dc6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13dc6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13dc6-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13dc6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13dc6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="13dc6-135">INPUTS</span></span>

## <span data-ttu-id="13dc6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="13dc6-136">OUTPUTS</span></span>

## <span data-ttu-id="13dc6-137">筆記</span><span class="sxs-lookup"><span data-stu-id="13dc6-137">NOTES</span></span>

## <span data-ttu-id="13dc6-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="13dc6-138">RELATED LINKS</span></span>

