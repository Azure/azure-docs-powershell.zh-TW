---
title: 使用 PowerShell 作業平行執行 Cmdlet
description: 如何使用 -AsJob 參數平行執行 Cmdlet。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516482"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="752ba-103">使用 PowerShell 作業平行執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="752ba-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="752ba-104">PowerShell 支援 [PowerShell 作業](/powershell/module/microsoft.powershell.core/about/about_jobs)的非同步動作。</span><span class="sxs-lookup"><span data-stu-id="752ba-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="752ba-105">Azure PowerShell 高度相依於進行或等待對 Azure 進行網路呼叫。</span><span class="sxs-lookup"><span data-stu-id="752ba-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="752ba-106">您常有可能需要進行非封鎖式呼叫。</span><span class="sxs-lookup"><span data-stu-id="752ba-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="752ba-107">為了因應這項需求，Azure PowerShell 提供了絕佳的 [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) 支援。</span><span class="sxs-lookup"><span data-stu-id="752ba-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="752ba-108">內容持續性和 PSJobs</span><span class="sxs-lookup"><span data-stu-id="752ba-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="752ba-109">PSJobs 會以個別程序的形式執行，因此您的 Azure 連線必須與它們共用。</span><span class="sxs-lookup"><span data-stu-id="752ba-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="752ba-110">使用 `Connect-AzAccount` 登入您的 Azure 帳戶後，請將內容傳至作業。</span><span class="sxs-lookup"><span data-stu-id="752ba-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="752ba-111">但是，若您已選擇使用 `Enable-AzContextAutosave` 自動儲存內容，則該內容會自動與您建立的所有作業共用。</span><span class="sxs-lookup"><span data-stu-id="752ba-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="752ba-112">使用 `-AsJob` 將作業自動化</span><span class="sxs-lookup"><span data-stu-id="752ba-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="752ba-113">為了便於作業， Azure PowerShell 也會在某些長期執行的 Cmdlet 中提供 `-AsJob` 開關。</span><span class="sxs-lookup"><span data-stu-id="752ba-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="752ba-114">`-AsJob` 開關能讓您更輕鬆地建立 PSJobs。</span><span class="sxs-lookup"><span data-stu-id="752ba-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="752ba-115">您可以使用 `Get-Job` 和 `Get-AzVM`，隨時檢查作業和進度。</span><span class="sxs-lookup"><span data-stu-id="752ba-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="752ba-116">作業完成後，請使用 `Receive-Job` 取得作業的結果。</span><span class="sxs-lookup"><span data-stu-id="752ba-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="752ba-117">若 `Receive-Job` 旗標並未顯示，`-AsJob` 會從 Cmdlet 傳回結果。</span><span class="sxs-lookup"><span data-stu-id="752ba-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="752ba-118">例如，`Do-Action -AsJob` 的 `Receive-Job` 結果與 `Do-Action` 結果的類型相同。</span><span class="sxs-lookup"><span data-stu-id="752ba-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="752ba-119">範例案例</span><span class="sxs-lookup"><span data-stu-id="752ba-119">Example Scenarios</span></span>

<span data-ttu-id="752ba-120">一次建立數個 VM：</span><span class="sxs-lookup"><span data-stu-id="752ba-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

<span data-ttu-id="752ba-121">在此範例中，`Wait-Job` Cmdlet 會在作業執行時暫停指令碼。</span><span class="sxs-lookup"><span data-stu-id="752ba-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="752ba-122">一旦所有作業完成之後，指令碼會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="752ba-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="752ba-123">以平行方式執行數個作業，指令碼即會等待作業完成再繼續。</span><span class="sxs-lookup"><span data-stu-id="752ba-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```