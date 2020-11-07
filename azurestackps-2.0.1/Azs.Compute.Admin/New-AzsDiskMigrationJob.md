---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966816"
---
# <span data-ttu-id="ea579-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ea579-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ea579-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea579-102">SYNOPSIS</span></span>


## <span data-ttu-id="ea579-103">句法</span><span class="sxs-lookup"><span data-stu-id="ea579-103">SYNTAX</span></span>

### <span data-ttu-id="ea579-104">音量 (預設) </span><span class="sxs-lookup"><span data-stu-id="ea579-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ea579-105">共用</span><span class="sxs-lookup"><span data-stu-id="ea579-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea579-106">說明</span><span class="sxs-lookup"><span data-stu-id="ea579-106">DESCRIPTION</span></span>


## <span data-ttu-id="ea579-107">示例</span><span class="sxs-lookup"><span data-stu-id="ea579-107">EXAMPLES</span></span>

### <span data-ttu-id="ea579-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="ea579-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="ea579-109">建立磁片遷移作業，以將磁片遷移至目標縮放比例單位和標籤。</span><span class="sxs-lookup"><span data-stu-id="ea579-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="ea579-110">範例2：</span><span class="sxs-lookup"><span data-stu-id="ea579-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="ea579-111">建立磁片遷移作業，以將磁片遷移至目標共用。</span><span class="sxs-lookup"><span data-stu-id="ea579-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="ea579-112">參數</span><span class="sxs-lookup"><span data-stu-id="ea579-112">PARAMETERS</span></span>

### <span data-ttu-id="ea579-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea579-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="ea579-114">-磁片</span><span class="sxs-lookup"><span data-stu-id="ea579-114">-Disks</span></span>
<span data-ttu-id="ea579-115">若要建立，請參閱磁片摘要資訊的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ea579-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ea579-116">-位置</span><span class="sxs-lookup"><span data-stu-id="ea579-116">-Location</span></span>


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

### <span data-ttu-id="ea579-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea579-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea579-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea579-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="ea579-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ea579-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea579-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="ea579-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea579-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="ea579-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ea579-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ea579-122">-Confirm</span></span>
<span data-ttu-id="ea579-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea579-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea579-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea579-124">-WhatIf</span></span>
<span data-ttu-id="ea579-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea579-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea579-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea579-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea579-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea579-127">CommonParameters</span></span>
<span data-ttu-id="ea579-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea579-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea579-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea579-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea579-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ea579-130">INPUTS</span></span>

### <span data-ttu-id="ea579-131">IDisk []. ComputeAdmin [Api20180730Preview]。</span><span class="sxs-lookup"><span data-stu-id="ea579-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="ea579-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ea579-132">OUTPUTS</span></span>

### <span data-ttu-id="ea579-133">IDiskMigrationJob （ComputeAdmin）。 Api20180730Preview。</span><span class="sxs-lookup"><span data-stu-id="ea579-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="ea579-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ea579-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ea579-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ea579-135">NOTES</span></span>

<span data-ttu-id="ea579-136">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ea579-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea579-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ea579-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ea579-138">磁片 <IDisk [] >：</span><span class="sxs-lookup"><span data-stu-id="ea579-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="ea579-139">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ea579-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ea579-140">`[DiskId <String>]`：磁片 id。</span><span class="sxs-lookup"><span data-stu-id="ea579-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="ea579-141">`[SharePath <String>]`：磁片共用路徑。</span><span class="sxs-lookup"><span data-stu-id="ea579-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="ea579-142">`[Status <DiskState?>]`：磁片狀態。</span><span class="sxs-lookup"><span data-stu-id="ea579-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="ea579-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea579-143">RELATED LINKS</span></span>

