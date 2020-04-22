---
title: 在 PowerShell 作業中執行 Azure PowerShell Cmdlet
description: 了解如何使用 -AsJob 和 Start-Job，以平行方式或在背景工作中執行 Azure PowerShell Cmdlet。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740485"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>在 PowerShell 作業中執行 Azure PowerShell Cmdlet

使用 Azure PowerShell 時，必須連線至 Azure 雲端並等候回應，因此這些 Cmdlet 在取得雲端的回應之前，大多都會封鎖您的 PowerShell 工作階段。
Powershell 作業可讓您在背景中執行 Cmdlet，或從單一 PowerShell 工作階段中同時執行多個 Azure 工作。

本文將概略說明如何以 PowerShell 作業的形式執行 Azure PowerShell Cmdlet，並檢查作業是否完成。 要在 Azure PowerShell 中執行命令必須使用 Azure PowerShell 內容，其詳細說明請見 [Azure 內容和登入認證](context-persistence.md)。
若要深入了解 PowerShell 作業，請參閱[關於 PowerShell 作業](/powershell/module/microsoft.powershell.core/about/about_jobs)。

## <a name="azure-contexts-with-powershell-jobs"></a>PowerShell 作業的 Azure 內容

PowerShell 作業會以個別程序執行，而不會連結 PowerShell 工作階段，因此您的 Azure 認證必須與這些作業共用。 認證可使用下列其中一種方法以 Azure 內容物件的形式傳遞：

* 自動內容持續性。 內容持續性會預設為啟用，並且跨多個工作階段保留您的登入資訊。 內容持續性啟用時，會將目前的 Azure 內容傳至新的程序：

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* 使用 `-AzContext` 參數搭配任何 Azure PowerShell Cmdlet，以提供 Azure 內容物件：

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  如果內容持續性停用，則需要 `-AzContext` 引數。

* 請使用部分 Azure PowerShell Cmdlet 所提供的 `-AsJob` 參數。 此參數會使用目前有效的 Azure 內容，自動以 PowerShell 作業的形式啟動 Cmdlet：

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  若要確認 Cmdlet 是否支援 `-AsJob`，請查看其參考文件。 `-AsJob` 參數不需要啟用內容自動儲存。

您可以使用 [Get-Job](/powershell/module/microsoft.powershell.core/get-job) Cmdlet 來檢查執行中作業的狀態。 若要取得作業到目前為止的輸出，請使用 [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) Cmdlet。

若要在 Azure 上從遠端檢查作業進度，請使用與作業所修改的資源類型相關聯的 `Get-` Cmdlet：

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>另請參閱

* [Azure PowerShell 內容](context-persistence.md)
* [關於 PowerShell 作業](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Get-Job 參考](/powershell/module/microsoft.powershell.core/get-job)
* [Receive-Job 參考](/powershell/module/microsoft.powershell.core/receive-job)
