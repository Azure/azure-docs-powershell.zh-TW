---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793549"
---
# <span data-ttu-id="1905c-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="1905c-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="1905c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1905c-102">SYNOPSIS</span></span>
<span data-ttu-id="1905c-103">建立用來限制計算資源的新計算配額。</span><span class="sxs-lookup"><span data-stu-id="1905c-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="1905c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1905c-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1905c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1905c-105">DESCRIPTION</span></span>
<span data-ttu-id="1905c-106">建立新的計算配額。</span><span class="sxs-lookup"><span data-stu-id="1905c-106">Create a new compute quota.</span></span>

## <span data-ttu-id="1905c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1905c-107">EXAMPLES</span></span>

### <span data-ttu-id="1905c-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1905c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="1905c-109">建立新的計算配額。</span><span class="sxs-lookup"><span data-stu-id="1905c-109">Create a new compute quota.</span></span>

## <span data-ttu-id="1905c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1905c-110">PARAMETERS</span></span>

### <span data-ttu-id="1905c-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="1905c-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="1905c-112">允許的可用性集數目。</span><span class="sxs-lookup"><span data-stu-id="1905c-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="1905c-113">-CoresCount</span></span>
<span data-ttu-id="1905c-114">允許的核心數。</span><span class="sxs-lookup"><span data-stu-id="1905c-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-115">-位置</span><span class="sxs-lookup"><span data-stu-id="1905c-115">-Location</span></span>
<span data-ttu-id="1905c-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1905c-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1905c-117">-Name</span></span>
<span data-ttu-id="1905c-118">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="1905c-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="1905c-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="1905c-120">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="1905c-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="1905c-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="1905c-122">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="1905c-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="1905c-123">-VirtualMachineCount</span></span>
<span data-ttu-id="1905c-124">允許的虛擬機器數。</span><span class="sxs-lookup"><span data-stu-id="1905c-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="1905c-125">-VmScaleSetCount</span></span>
<span data-ttu-id="1905c-126">允許的縮放集數目。</span><span class="sxs-lookup"><span data-stu-id="1905c-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1905c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1905c-127">-Confirm</span></span>
<span data-ttu-id="1905c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1905c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1905c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1905c-129">-WhatIf</span></span>
<span data-ttu-id="1905c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1905c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1905c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1905c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1905c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1905c-132">CommonParameters</span></span>
<span data-ttu-id="1905c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1905c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1905c-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1905c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1905c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1905c-135">INPUTS</span></span>

## <span data-ttu-id="1905c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1905c-136">OUTPUTS</span></span>

### <span data-ttu-id="1905c-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="1905c-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="1905c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1905c-138">NOTES</span></span>

## <span data-ttu-id="1905c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1905c-139">RELATED LINKS</span></span>

