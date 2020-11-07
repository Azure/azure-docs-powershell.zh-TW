---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793884"
---
# <span data-ttu-id="a0bec-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="a0bec-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="a0bec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0bec-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bec-103">建立用來限制計算資源的新計算配額。</span><span class="sxs-lookup"><span data-stu-id="a0bec-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="a0bec-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0bec-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0bec-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0bec-105">DESCRIPTION</span></span>
<span data-ttu-id="a0bec-106">建立新的計算配額。</span><span class="sxs-lookup"><span data-stu-id="a0bec-106">Create a new compute quota.</span></span>

## <span data-ttu-id="a0bec-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0bec-107">EXAMPLES</span></span>

### <span data-ttu-id="a0bec-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a0bec-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="a0bec-109">建立新的計算配額。</span><span class="sxs-lookup"><span data-stu-id="a0bec-109">Create a new compute quota.</span></span>

## <span data-ttu-id="a0bec-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0bec-110">PARAMETERS</span></span>

### <span data-ttu-id="a0bec-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="a0bec-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="a0bec-112">允許的可用性集數目。</span><span class="sxs-lookup"><span data-stu-id="a0bec-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="a0bec-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="a0bec-113">-CoresCount</span></span>
<span data-ttu-id="a0bec-114">允許的核心數。</span><span class="sxs-lookup"><span data-stu-id="a0bec-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="a0bec-115">-位置</span><span class="sxs-lookup"><span data-stu-id="a0bec-115">-Location</span></span>
<span data-ttu-id="a0bec-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a0bec-116">Location of the resource.</span></span>

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

### <span data-ttu-id="a0bec-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0bec-117">-Name</span></span>
<span data-ttu-id="a0bec-118">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0bec-118">Name of the quota.</span></span>

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

### <span data-ttu-id="a0bec-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a0bec-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a0bec-120">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="a0bec-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="a0bec-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a0bec-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a0bec-122">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="a0bec-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="a0bec-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="a0bec-123">-VirtualMachineCount</span></span>
<span data-ttu-id="a0bec-124">允許的虛擬機器數。</span><span class="sxs-lookup"><span data-stu-id="a0bec-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="a0bec-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="a0bec-125">-VmScaleSetCount</span></span>
<span data-ttu-id="a0bec-126">允許的縮放集數目。</span><span class="sxs-lookup"><span data-stu-id="a0bec-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="a0bec-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a0bec-127">-Confirm</span></span>
<span data-ttu-id="a0bec-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0bec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bec-129">-WhatIf</span></span>
<span data-ttu-id="a0bec-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0bec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bec-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0bec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bec-132">CommonParameters</span></span>
<span data-ttu-id="a0bec-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0bec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bec-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0bec-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bec-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a0bec-135">INPUTS</span></span>

## <span data-ttu-id="a0bec-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a0bec-136">OUTPUTS</span></span>

### <span data-ttu-id="a0bec-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="a0bec-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="a0bec-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a0bec-138">NOTES</span></span>

## <span data-ttu-id="a0bec-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0bec-139">RELATED LINKS</span></span>

