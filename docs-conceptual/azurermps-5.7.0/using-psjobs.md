---
title: 使用 PowerShell 作業平行執行 Cmdlet
description: 如何使用 -AsJob 參數平行執行 Cmdlet。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: 3f8617ade3afbf6a283f3696f6d688ba9529173a
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387984"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="fb466-103">使用 PowerShell 作業平行執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb466-103">Running cmdlets in parallel using PowerShell jobs</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="fb466-104">PowerShell 支援 [PowerShell 作業](/powershell/module/microsoft.powershell.core/about/about_jobs)的非同步動作。</span><span class="sxs-lookup"><span data-stu-id="fb466-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="fb466-105">Azure PowerShell 高度相依於進行或等待對 Azure 進行網路呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb466-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="fb466-106">身為開發人員，您可能會經常需要在指令碼中對 Azure 進行多個非封鎖呼叫；或是在並未封鎖目前工作階段的情況下在 REPL 中建立 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="fb466-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="fb466-107">若您有這些需求，Azure PowerShell 提供最佳的 [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) 支援。</span><span class="sxs-lookup"><span data-stu-id="fb466-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="fb466-108">內容持續性和 PSJobs</span><span class="sxs-lookup"><span data-stu-id="fb466-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="fb466-109">PSJobs 會以個別程序執行，表示您必須將 Azure 連線相關的資訊適當地與您建立的作業共用。</span><span class="sxs-lookup"><span data-stu-id="fb466-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="fb466-110">在使用 `Connect-AzureRmAccount` 將 Azure 帳戶連線到 PowerShell 工作階段時，您可以將內容傳送給作業。</span><span class="sxs-lookup"><span data-stu-id="fb466-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="fb466-111">但是，若您已選擇使用 `Enable-AzureRmContextAutosave` 自動儲存內容，則該內容會自動與您建立的所有作業共用。</span><span class="sxs-lookup"><span data-stu-id="fb466-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="fb466-112">使用 `-AsJob` 將作業自動化</span><span class="sxs-lookup"><span data-stu-id="fb466-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="fb466-113">為了便於作業， Azure PowerShell 也會在某些長期執行的 Cmdlet 中提供 `-AsJob` 開關。</span><span class="sxs-lookup"><span data-stu-id="fb466-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="fb466-114">`-AsJob` 開關能讓您更輕鬆地建立 PSJobs。</span><span class="sxs-lookup"><span data-stu-id="fb466-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="fb466-115">您可以使用 `Get-Job` 和 `Get-AzureRmVM`，隨時檢查作業和進度。</span><span class="sxs-lookup"><span data-stu-id="fb466-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="fb466-116">完成之後，您會透過 `Receive-Job` 獲得作業結果。</span><span class="sxs-lookup"><span data-stu-id="fb466-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="fb466-117">若 `Receive-Job` 旗標並未顯示，`-AsJob` 會從 Cmdlet 傳回結果。</span><span class="sxs-lookup"><span data-stu-id="fb466-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="fb466-118">例如，`Do-Action -AsJob` 的 `Receive-Job` 結果與 `Do-Action` 結果的類型相同。</span><span class="sxs-lookup"><span data-stu-id="fb466-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="fb466-119">範例案例</span><span class="sxs-lookup"><span data-stu-id="fb466-119">Example Scenarios</span></span>

<span data-ttu-id="fb466-120">一次建立多個 VM。</span><span class="sxs-lookup"><span data-stu-id="fb466-120">Create multiple VMs at once.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="fb466-121">在此範例中，`Wait-Job` Cmdlet 會在作業執行時暫停指令碼。</span><span class="sxs-lookup"><span data-stu-id="fb466-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="fb466-122">一旦所有作業完成之後，指令碼會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="fb466-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="fb466-123">如此可讓您建立數個平行執行的作業，並等待作業完成再繼續。</span><span class="sxs-lookup"><span data-stu-id="fb466-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
