---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968162"
---
# <span data-ttu-id="8e71f-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="8e71f-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="8e71f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e71f-102">SYNOPSIS</span></span>


## <span data-ttu-id="8e71f-103">句法</span><span class="sxs-lookup"><span data-stu-id="8e71f-103">SYNTAX</span></span>

### <span data-ttu-id="8e71f-104">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="8e71f-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e71f-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="8e71f-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e71f-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="8e71f-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="8e71f-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e71f-107">DESCRIPTION</span></span>
<span data-ttu-id="8e71f-108">更新計算配額</span><span class="sxs-lookup"><span data-stu-id="8e71f-108">Update a Compute Quota</span></span>

## <span data-ttu-id="8e71f-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e71f-109">EXAMPLES</span></span>

### <span data-ttu-id="8e71f-110">範例1：在現有的計算配額上設定屬性</span><span class="sxs-lookup"><span data-stu-id="8e71f-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="8e71f-111">設定命令列上指定的參數。</span><span class="sxs-lookup"><span data-stu-id="8e71f-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="8e71f-112">未設定的任何參數都會預設為0</span><span class="sxs-lookup"><span data-stu-id="8e71f-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="8e71f-113">參數</span><span class="sxs-lookup"><span data-stu-id="8e71f-113">PARAMETERS</span></span>

### <span data-ttu-id="8e71f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e71f-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8e71f-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="8e71f-115">-NewQuota</span></span>
<span data-ttu-id="8e71f-116">若要建立，請參閱 NEWQUOTA 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8e71f-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8e71f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e71f-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="8e71f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="8e71f-118">-Confirm</span></span>
<span data-ttu-id="8e71f-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e71f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e71f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e71f-120">-WhatIf</span></span>
<span data-ttu-id="8e71f-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e71f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e71f-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e71f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e71f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e71f-123">CommonParameters</span></span>
<span data-ttu-id="8e71f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e71f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e71f-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e71f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e71f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8e71f-126">INPUTS</span></span>

### <span data-ttu-id="8e71f-127">IQuota （ComputeAdmin）。 Api20180209。</span><span class="sxs-lookup"><span data-stu-id="8e71f-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="8e71f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8e71f-128">OUTPUTS</span></span>

### <span data-ttu-id="8e71f-129">IQuota （ComputeAdmin）。 Api20180209。</span><span class="sxs-lookup"><span data-stu-id="8e71f-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="8e71f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8e71f-130">NOTES</span></span>

<span data-ttu-id="8e71f-131">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8e71f-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e71f-132">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8e71f-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e71f-133">NEWQUOTA <IQuota> ：</span><span class="sxs-lookup"><span data-stu-id="8e71f-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="8e71f-134">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8e71f-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8e71f-135">`[AvailabilitySetCount <Int32?>]`：允許的可用性集數目上限。</span><span class="sxs-lookup"><span data-stu-id="8e71f-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="8e71f-136">`[CoresLimit <Int32?>]`：允許的核心數上限。</span><span class="sxs-lookup"><span data-stu-id="8e71f-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="8e71f-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`：允許的最大受管理磁片數量及類型為 [特優] 的快照。</span><span class="sxs-lookup"><span data-stu-id="8e71f-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="8e71f-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`：允許的 [標準類型] 的受管理磁片和快照數目上限。</span><span class="sxs-lookup"><span data-stu-id="8e71f-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="8e71f-139">`[VMScaleSetCount <Int32?>]`：已允許的小數位集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="8e71f-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="8e71f-140">`[VirtualMachineCount <Int32?>]`：允許的虛擬機器數上限。</span><span class="sxs-lookup"><span data-stu-id="8e71f-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="8e71f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e71f-141">RELATED LINKS</span></span>

