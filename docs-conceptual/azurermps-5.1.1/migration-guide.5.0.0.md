# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="f6f57-101">Microsoft Azure PowerShell 5.0.0 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="f6f57-102">本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。</span><span class="sxs-lookup"><span data-stu-id="f6f57-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f6f57-103">每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。</span><span class="sxs-lookup"><span data-stu-id="f6f57-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="f6f57-104">如需深入了解內容，請參閱與每次變更相關聯的提取要求。</span><span class="sxs-lookup"><span data-stu-id="f6f57-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="f6f57-105">目錄</span><span class="sxs-lookup"><span data-stu-id="f6f57-105">Table of Contents</span></span>

- [<span data-ttu-id="f6f57-106">ApiManagement Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="f6f57-107">Batch Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="f6f57-108">Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="f6f57-109">EventHub Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="f6f57-110">Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="f6f57-111">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="f6f57-112">Resources Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="f6f57-113">ServiceBus Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="f6f57-114">ApiManagement Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="f6f57-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="f6f57-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="f6f57-116">PSCredential 將取代 "UserName" 和 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="f6f57-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="f6f57-118">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="f6f57-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="f6f57-120">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="f6f57-121">Batch Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="f6f57-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="f6f57-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="f6f57-123">Secure 字串將取代 `Password` 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="f6f57-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="f6f57-125">Secure 字串將取代 `Password` 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="f6f57-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="f6f57-127">Secure 字串將取代 `Password` 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="f6f57-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="f6f57-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="f6f57-129">移除 `RunElevated` 參數，並以 `UserIdentity` 加以取代。</span><span class="sxs-lookup"><span data-stu-id="f6f57-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="f6f57-130">此動作額外影響了 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 上的 `RunElevated` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6f57-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="f6f57-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="f6f57-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="f6f57-132">`PSMultiInstanceSettings` 建構函式不再採用必要的 `numberOfInstances` 參數，而是採用必要的 `coordinationCommandLine` 參數。</span><span class="sxs-lookup"><span data-stu-id="f6f57-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="f6f57-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="f6f57-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="f6f57-134">已將 `RunElevated` 屬性從 `PSCloudTask` 上移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="f6f57-135">新增 `UserIdentity` 屬性以取代 `RunElevated`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="f6f57-136">此動作額外影響了 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 上的 `RunElevated` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6f57-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="f6f57-137">**多種類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-137">**Multiple types**</span></span>

- <span data-ttu-id="f6f57-138">已將 `PSExitConditions` 上的 `SchedulingError` 屬性重新命名為 `PreProcessingError`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="f6f57-139">**多種類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-139">**Multiple types**</span></span>

- <span data-ttu-id="f6f57-140">已將 `PSJobPreparationTaskExecutionInformation`、`PSJobReleaseTaskExecutionInformation`、`PSStartTaskInformation`、`PSSubtaskInformation` 和 `PSTaskExecutionInformation` 上的 `SchedulingError` 屬性重新命名為 `FailureInformation`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="f6f57-141">`FailureInformation` 會在每次工作失敗時傳回。</span><span class="sxs-lookup"><span data-stu-id="f6f57-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="f6f57-142">這包括所有先前排程的錯誤案例和非零工作結束代碼，以及新輸出檔案功能中的檔案上傳失敗情形。</span><span class="sxs-lookup"><span data-stu-id="f6f57-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="f6f57-143">此結構與之前相同，因此使用此類型時，不需要變更任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="f6f57-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="f6f57-144">這額外影響了以下項目：Get-AzureBatchPool、Get-AzureBatchSubtask 和 Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="f6f57-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="f6f57-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="f6f57-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="f6f57-146">移除 `TargetDedicated`，並以 `TargetDedicatedComputeNodes` 和 `TargetLowPriorityComputeNodes` 加以取代。</span><span class="sxs-lookup"><span data-stu-id="f6f57-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="f6f57-147">`TargetDedicatedComputeNodes` 有別名：`TargetDedicated`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="f6f57-148">這也會影響以下項目：Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f6f57-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="f6f57-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="f6f57-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="f6f57-150">將 `PSCloudPool` 上的 `TargetDedicated` 和 `CurrentDedicated` 屬性重新命名為 `TargetDedicatedComputeNodes` 和 `CurrentDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="f6f57-151">**PSCloudPool 類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="f6f57-152">已將 `PSCloudPool` 上的 `ResizeError` 重新命名為 `ResizeErrors`，其現在是集合。</span><span class="sxs-lookup"><span data-stu-id="f6f57-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="f6f57-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="f6f57-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="f6f57-154">已將 `PSPoolSpecification` 上的 `TargetDedicated` 屬性重新命名為 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="f6f57-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="f6f57-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="f6f57-156">移除 `Name`，並以 `Path` 加以取代。</span><span class="sxs-lookup"><span data-stu-id="f6f57-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="f6f57-157">`Path` 有別名：`Name`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="f6f57-158">這也會影響以下項目：Get-AzureBatchNodeFileContent、Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f6f57-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="f6f57-159">**PSNodeFile** 類型</span><span class="sxs-lookup"><span data-stu-id="f6f57-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="f6f57-160">已將 `PSNodeFile` 上的 `Name` 屬性重新命名為 `Path`。</span><span class="sxs-lookup"><span data-stu-id="f6f57-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="f6f57-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="f6f57-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="f6f57-162">`PSSubtaskInformation` 的 `PreviousState` 和 `State` 屬性已不再屬於 `TaskState` 類型，而是屬於 `SubtaskState` 類型。</span><span class="sxs-lookup"><span data-stu-id="f6f57-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="f6f57-163">不同於 `TaskState`，`SubtaskState` 沒有 `Active` 值，因為子工作不可能處於 `Active` 狀態。</span><span class="sxs-lookup"><span data-stu-id="f6f57-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="f6f57-164">Compute Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="f6f57-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="f6f57-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="f6f57-166">PSCredential 將取代 "UserName" 和 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="f6f57-167">EventHub Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-169">'New-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-170">請使用 'New-AzureRmEventHubAuthorizationRule' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-172">'Get-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-173">請使用 'Get-AzureRmEventHubAuthorizationRule' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-175">'Set-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-176">請使用 'Set-AzureRmEventHubAuthorizationRule' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-178">'Remove-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-179">請使用 'Remove-AzureRmEventHubAuthorizationRule' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="f6f57-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="f6f57-181">'New-AzureRmEventHubNamespaceKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-182">請使用 'New-AzureRmEventHubKey' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="f6f57-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="f6f57-184">'Get-AzureRmEventHubNamespaceKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-185">請使用 'Get-AzureRmEventHubKey' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6f57-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="f6f57-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="f6f57-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="f6f57-187">'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="f6f57-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="f6f57-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="f6f57-189">'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="f6f57-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="f6f57-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="f6f57-191">'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="f6f57-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="f6f57-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="f6f57-193">'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="f6f57-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="f6f57-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="f6f57-195">'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="f6f57-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="f6f57-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="f6f57-197">'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="f6f57-198">Insights Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="f6f57-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="f6f57-200">**Add-AzureRMLogAlertRule** Cmdlet 已受到取代</span><span class="sxs-lookup"><span data-stu-id="f6f57-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="f6f57-201">10 月 1 日之後，使用此 Cmdlet 將不再有任何效果，因為這項功能將轉換為活動記錄警示。</span><span class="sxs-lookup"><span data-stu-id="f6f57-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="f6f57-202">如需詳細資訊，請參閱 https://aka.ms/migratemealerts。</span><span class="sxs-lookup"><span data-stu-id="f6f57-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="f6f57-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="f6f57-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="f6f57-204">**Get-AzureRMUsage** Cmdlet 已受到取代</span><span class="sxs-lookup"><span data-stu-id="f6f57-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="f6f57-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="f6f57-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="f6f57-206">輸出變更：來自 EventData 物件的 EventChannels 欄位 (由這些 Cmdlet 所傳回) 已受到取代，因為物件現在會傳回常數值 (Admin、Operation)。</span><span class="sxs-lookup"><span data-stu-id="f6f57-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="f6f57-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="f6f57-208">輸出變更：此 Cmdlet 的輸出會經過壓平合併 (也就是刪除屬性欄位)，進而改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="f6f57-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="f6f57-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="f6f57-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="f6f57-210">輸出變更：AutoscaleSettingResourceName 欄位將受到取代，因為它一律等於 Name 欄位。</span><span class="sxs-lookup"><span data-stu-id="f6f57-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="f6f57-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="f6f57-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="f6f57-212">輸出變更：輸出類型會變更為傳回單一物件，其中包含要求識別碼和狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f6f57-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="f6f57-213">Network Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="f6f57-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="f6f57-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="f6f57-215">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="f6f57-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="f6f57-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="f6f57-217">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="f6f57-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="f6f57-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="f6f57-219">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="f6f57-220">Resources Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="f6f57-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="f6f57-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="f6f57-222">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="f6f57-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="f6f57-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="f6f57-224">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="f6f57-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="f6f57-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="f6f57-226">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="f6f57-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="f6f57-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="f6f57-228">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="f6f57-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="f6f57-230">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="f6f57-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="f6f57-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="f6f57-232">SecureString 將取代 "Password" 參數</span><span class="sxs-lookup"><span data-stu-id="f6f57-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="f6f57-233">ServiceBus Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="f6f57-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="f6f57-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-235">'Get-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-236">請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="f6f57-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="f6f57-238">'Get-AzureRmServiceBusTopicKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-239">請使用 'Get-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="f6f57-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-241">'New-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-242">請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="f6f57-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="f6f57-244">'New-AzureRmServiceBusTopicKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-245">請使用 'New-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="f6f57-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-247">'Remove-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-248">請使用 'Remove-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="f6f57-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-250">'Set-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-251">請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="f6f57-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="f6f57-253">'New-AzureRmServiceBusNamespaceKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-254">請使用 'New-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="f6f57-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-256">'Get-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-257">請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="f6f57-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="f6f57-259">'Get-AzureRmServiceBusQueueKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-260">請使用 'Get-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="f6f57-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-262">'New-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-263">請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="f6f57-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="f6f57-265">'New-AzureRmServiceBusQueueKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-266">請使用 'New-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="f6f57-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-268">'Remove-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-269">請使用 'GRemove-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="f6f57-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-271">'Set-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-272">請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-274">'Get-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-275">請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="f6f57-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="f6f57-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="f6f57-277">'Get-AzureRmServiceBusNamespaceKey' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-278">請使用 'Get-AzureRmServiceBusKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-280">'New-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-281">請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-283">'Remove-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-284">請使用 'Remove-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="f6f57-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="f6f57-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="f6f57-286">'Set-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。</span><span class="sxs-lookup"><span data-stu-id="f6f57-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="f6f57-287">請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6f57-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="f6f57-288">**NamespaceAttributes 類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="f6f57-289">下列屬性已移除</span><span class="sxs-lookup"><span data-stu-id="f6f57-289">The following properties have been removed</span></span>
    - <span data-ttu-id="f6f57-290">已啟用</span><span class="sxs-lookup"><span data-stu-id="f6f57-290">Enabled</span></span>
    - <span data-ttu-id="f6f57-291">狀態</span><span class="sxs-lookup"><span data-stu-id="f6f57-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="f6f57-292">**QueueAttribute 類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="f6f57-293">下列屬性會標示為已淘汰：</span><span class="sxs-lookup"><span data-stu-id="f6f57-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="f6f57-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="f6f57-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="f6f57-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="f6f57-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="f6f57-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="f6f57-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="f6f57-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="f6f57-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="f6f57-298">**TopicAttribute 類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="f6f57-299">下列屬性會標示為已淘汰：</span><span class="sxs-lookup"><span data-stu-id="f6f57-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="f6f57-300">位置</span><span class="sxs-lookup"><span data-stu-id="f6f57-300">Location</span></span>
    - <span data-ttu-id="f6f57-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="f6f57-301">IsExpress</span></span>
    - <span data-ttu-id="f6f57-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="f6f57-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="f6f57-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="f6f57-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="f6f57-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="f6f57-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="f6f57-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="f6f57-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="f6f57-306">**SubscriptionAttribute 類型**</span><span class="sxs-lookup"><span data-stu-id="f6f57-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="f6f57-307">下列屬性會標示為已淘汰</span><span class="sxs-lookup"><span data-stu-id="f6f57-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="f6f57-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="f6f57-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="f6f57-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="f6f57-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="f6f57-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="f6f57-310">IsReadOnly</span></span>
    - <span data-ttu-id="f6f57-311">位置</span><span class="sxs-lookup"><span data-stu-id="f6f57-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```