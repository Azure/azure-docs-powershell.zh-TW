---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4caf955c25cd29c9cc9c09f1182454ee3a4d56df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793425"
---
# <span data-ttu-id="c7bf6-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c7bf6-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="c7bf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bf6-103">使用提供的參數更新現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="c7bf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7bf6-104">SYNTAX</span></span>

### <span data-ttu-id="c7bf6-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="c7bf6-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bf6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bf6-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7bf6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7bf6-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bf6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7bf6-108">DESCRIPTION</span></span>
<span data-ttu-id="c7bf6-109">更新現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="c7bf6-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7bf6-110">EXAMPLES</span></span>

### <span data-ttu-id="c7bf6-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c7bf6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="c7bf6-112">更新計算配額。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-112">Update a compute quota.</span></span>

## <span data-ttu-id="c7bf6-113">參數</span><span class="sxs-lookup"><span data-stu-id="c7bf6-113">PARAMETERS</span></span>

### <span data-ttu-id="c7bf6-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="c7bf6-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="c7bf6-115">允許的可用性集數目。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="c7bf6-116">-CoresCount</span></span>
<span data-ttu-id="c7bf6-117">允許的核心數。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7bf6-118">-InputObject</span></span>
<span data-ttu-id="c7bf6-119">可能已修改的計算配額傳回了表單 AzsComputeQuota。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-120">-位置</span><span class="sxs-lookup"><span data-stu-id="c7bf6-120">-Location</span></span>
<span data-ttu-id="c7bf6-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7bf6-122">-Name</span></span>
<span data-ttu-id="c7bf6-123">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="c7bf6-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="c7bf6-125">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bf6-126">-ResourceId</span></span>
<span data-ttu-id="c7bf6-127">ARM 會計算配額 id。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="c7bf6-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="c7bf6-129">標準管理磁片與允許快照的大小。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="c7bf6-130">-VirtualMachineCount</span></span>
<span data-ttu-id="c7bf6-131">允許的虛擬機器數。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="c7bf6-132">-VmScaleSetCount</span></span>
<span data-ttu-id="c7bf6-133">允許的縮放集數目。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c7bf6-134">-Confirm</span></span>
<span data-ttu-id="c7bf6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bf6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bf6-136">-WhatIf</span></span>
<span data-ttu-id="c7bf6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7bf6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bf6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bf6-139">CommonParameters</span></span>
<span data-ttu-id="c7bf6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bf6-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7bf6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bf6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c7bf6-142">INPUTS</span></span>

## <span data-ttu-id="c7bf6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c7bf6-143">OUTPUTS</span></span>

### <span data-ttu-id="c7bf6-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="c7bf6-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="c7bf6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c7bf6-145">NOTES</span></span>

## <span data-ttu-id="c7bf6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7bf6-146">RELATED LINKS</span></span>

