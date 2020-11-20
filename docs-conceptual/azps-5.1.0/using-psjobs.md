---
title: 在 PowerShell 作業中執行 Azure PowerShell Cmdlet
description: 了解如何使用 -AsJob 和 Start-Job，以平行方式或在背景工作中執行 Azure PowerShell Cmdlet。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715152"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="9525b-103">在 PowerShell 作業中執行 Azure PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9525b-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="9525b-104">使用 Azure PowerShell 時，必須連線至 Azure 雲端並等候回應，因此這些 Cmdlet 在取得雲端的回應之前，大多都會封鎖您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="9525b-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="9525b-105">Powershell 作業可讓您在背景中執行 Cmdlet，或從單一 PowerShell 工作階段中同時執行多個 Azure 工作。</span><span class="sxs-lookup"><span data-stu-id="9525b-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="9525b-106">本文將概略說明如何以 PowerShell 作業的形式執行 Azure PowerShell Cmdlet，並檢查作業是否完成。</span><span class="sxs-lookup"><span data-stu-id="9525b-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="9525b-107">要在 Azure PowerShell 中執行命令必須使用 Azure PowerShell 內容，其詳細說明請見 [Azure 內容和登入認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="9525b-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="9525b-108">若要深入了解 PowerShell 作業，請參閱[關於 PowerShell 作業](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="9525b-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="9525b-109">PowerShell 作業的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="9525b-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="9525b-110">PowerShell 作業會以個別程序執行，而不會連結 PowerShell 工作階段，因此您的 Azure 認證必須與這些作業共用。</span><span class="sxs-lookup"><span data-stu-id="9525b-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="9525b-111">認證可使用下列其中一種方法以 Azure 內容物件的形式傳遞：</span><span class="sxs-lookup"><span data-stu-id="9525b-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="9525b-112">自動內容持續性。</span><span class="sxs-lookup"><span data-stu-id="9525b-112">Automatic context persistence.</span></span> <span data-ttu-id="9525b-113">內容持續性會預設為啟用，並且跨多個工作階段保留您的登入資訊。</span><span class="sxs-lookup"><span data-stu-id="9525b-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="9525b-114">內容持續性啟用時，會將目前的 Azure 內容傳至新的程序：</span><span class="sxs-lookup"><span data-stu-id="9525b-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="9525b-115">使用 `-AzContext` 參數搭配任何 Azure PowerShell Cmdlet，以提供 Azure 內容物件：</span><span class="sxs-lookup"><span data-stu-id="9525b-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="9525b-116">如果內容持續性停用，則需要 `-AzContext` 引數。</span><span class="sxs-lookup"><span data-stu-id="9525b-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="9525b-117">請使用部分 Azure PowerShell Cmdlet 所提供的 `-AsJob` 參數。</span><span class="sxs-lookup"><span data-stu-id="9525b-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9525b-118">此參數會使用目前有效的 Azure 內容，自動以 PowerShell 作業的形式啟動 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9525b-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="9525b-119">若要確認 Cmdlet 是否支援 `-AsJob`，請查看其參考文件。</span><span class="sxs-lookup"><span data-stu-id="9525b-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="9525b-120">`-AsJob` 參數不需要啟用內容自動儲存。</span><span class="sxs-lookup"><span data-stu-id="9525b-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="9525b-121">您可以使用 [Get-Job](/powershell/module/microsoft.powershell.core/get-job) Cmdlet 來檢查執行中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="9525b-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="9525b-122">若要取得作業到目前為止的輸出，請使用 [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9525b-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="9525b-123">若要在 Azure 上從遠端檢查作業進度，請使用與作業所修改的資源類型相關聯的 `Get-` Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9525b-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="9525b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9525b-124">See Also</span></span>

* [<span data-ttu-id="9525b-125">Azure PowerShell 內容</span><span class="sxs-lookup"><span data-stu-id="9525b-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="9525b-126">關於 PowerShell 作業</span><span class="sxs-lookup"><span data-stu-id="9525b-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="9525b-127">Get-Job 參考</span><span class="sxs-lookup"><span data-stu-id="9525b-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="9525b-128">Receive-Job 參考</span><span class="sxs-lookup"><span data-stu-id="9525b-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
