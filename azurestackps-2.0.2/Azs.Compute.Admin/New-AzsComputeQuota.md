---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968175"
---
# <span data-ttu-id="17cdd-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="17cdd-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="17cdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="17cdd-103">使用提供的配額參數建立或更新計算配額。</span><span class="sxs-lookup"><span data-stu-id="17cdd-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="17cdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="17cdd-104">SYNTAX</span></span>

### <span data-ttu-id="17cdd-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="17cdd-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="17cdd-106">建立</span><span class="sxs-lookup"><span data-stu-id="17cdd-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17cdd-107">說明</span><span class="sxs-lookup"><span data-stu-id="17cdd-107">DESCRIPTION</span></span>
<span data-ttu-id="17cdd-108">使用提供的配額參數建立或更新計算配額。</span><span class="sxs-lookup"><span data-stu-id="17cdd-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="17cdd-109">示例</span><span class="sxs-lookup"><span data-stu-id="17cdd-109">EXAMPLES</span></span>

### <span data-ttu-id="17cdd-110">範例1：使用預設參數建立計算配額</span><span class="sxs-lookup"><span data-stu-id="17cdd-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="17cdd-111">任何未指定的參數，都將會設定為其預設參數（如上所示）。</span><span class="sxs-lookup"><span data-stu-id="17cdd-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="17cdd-112">範例2：使用自訂參數建立計算配額</span><span class="sxs-lookup"><span data-stu-id="17cdd-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="17cdd-113">使用參數自訂配額。</span><span class="sxs-lookup"><span data-stu-id="17cdd-113">Customize Quota with parameters.</span></span> <span data-ttu-id="17cdd-114">未指定的任何參數都將會有預設值。</span><span class="sxs-lookup"><span data-stu-id="17cdd-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="17cdd-115">參數</span><span class="sxs-lookup"><span data-stu-id="17cdd-115">PARAMETERS</span></span>

### <span data-ttu-id="17cdd-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="17cdd-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="17cdd-117">允許的可用性集數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="17cdd-118">-CoresCount</span></span>
<span data-ttu-id="17cdd-119">允許的核心數上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17cdd-120">-DefaultProfile</span></span>
<span data-ttu-id="17cdd-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17cdd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-122">-位置</span><span class="sxs-lookup"><span data-stu-id="17cdd-122">-Location</span></span>
<span data-ttu-id="17cdd-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="17cdd-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="17cdd-124">-Location1</span></span>
<span data-ttu-id="17cdd-125">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="17cdd-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="17cdd-126">-Name</span></span>
<span data-ttu-id="17cdd-127">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="17cdd-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="17cdd-128">-NewQuota</span></span>
<span data-ttu-id="17cdd-129">保留用來控制資源配置的計算配額資訊。</span><span class="sxs-lookup"><span data-stu-id="17cdd-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="17cdd-130">若要建立，請參閱 NEWQUOTA 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="17cdd-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="17cdd-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="17cdd-132">支援的最大受管理磁片和 [特優] 類型的快照數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="17cdd-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="17cdd-134">支援之標準類型的受管理磁片和快照數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17cdd-135">-SubscriptionId</span></span>
<span data-ttu-id="17cdd-136">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="17cdd-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="17cdd-137">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="17cdd-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="17cdd-138">-VirtualMachineCount</span></span>
<span data-ttu-id="17cdd-139">允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="17cdd-140">-VMScaleSetCount</span></span>
<span data-ttu-id="17cdd-141">允許的小數位集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="17cdd-142">-Confirm</span></span>
<span data-ttu-id="17cdd-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17cdd-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17cdd-144">-WhatIf</span></span>
<span data-ttu-id="17cdd-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17cdd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17cdd-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17cdd-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17cdd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17cdd-147">CommonParameters</span></span>
<span data-ttu-id="17cdd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17cdd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17cdd-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17cdd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17cdd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="17cdd-150">INPUTS</span></span>

### <span data-ttu-id="17cdd-151">IQuota （ComputeAdmin）。 Api20180209。</span><span class="sxs-lookup"><span data-stu-id="17cdd-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="17cdd-152">輸出</span><span class="sxs-lookup"><span data-stu-id="17cdd-152">OUTPUTS</span></span>

### <span data-ttu-id="17cdd-153">IQuota （ComputeAdmin）。 Api20180209。</span><span class="sxs-lookup"><span data-stu-id="17cdd-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="17cdd-154">筆記</span><span class="sxs-lookup"><span data-stu-id="17cdd-154">NOTES</span></span>

<span data-ttu-id="17cdd-155">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="17cdd-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17cdd-156">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="17cdd-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="17cdd-157">NEWQUOTA <IQuota> ：保留用來控制資源配置的計算配額資訊。</span><span class="sxs-lookup"><span data-stu-id="17cdd-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="17cdd-158">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="17cdd-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="17cdd-159">`[AvailabilitySetCount <Int32?>]`：允許的可用性集數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="17cdd-160">`[CoresLimit <Int32?>]`：允許的核心數上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="17cdd-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`：允許的最大受管理磁片數量及類型為 [特優] 的快照。</span><span class="sxs-lookup"><span data-stu-id="17cdd-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="17cdd-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`：允許的 [標準類型] 的受管理磁片和快照數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="17cdd-163">`[VMScaleSetCount <Int32?>]`：已允許的小數位集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="17cdd-164">`[VirtualMachineCount <Int32?>]`：允許的虛擬機器數上限。</span><span class="sxs-lookup"><span data-stu-id="17cdd-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="17cdd-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="17cdd-165">RELATED LINKS</span></span>

