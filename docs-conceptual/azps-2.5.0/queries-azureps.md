---
title: 查詢 Azure PowerShell Cmdlet 的輸出
description: 如何查詢 Azure 中的資源，並將結果格式化。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657921"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="4a828-103">查詢 Azure PowerShell 的輸出</span><span class="sxs-lookup"><span data-stu-id="4a828-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="4a828-104">每個 Azure PowerShell Cmdlet 的結果都是 Azure PowerShell 物件。</span><span class="sxs-lookup"><span data-stu-id="4a828-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="4a828-105">即使 Cmdlet 不是明確的 `Get-` 作業，也可能會傳回可進行檢查的值，以提供已建立或已修改資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a828-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="4a828-106">大多數的 Cmdlet 會傳回單一物件，但有些會傳回應重複查看的陣列。</span><span class="sxs-lookup"><span data-stu-id="4a828-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="4a828-107">在大部分的情況下，您可以使用 [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) Cmdlet (通常縮寫為 `select`) 從 Azure PowerShell 查詢輸出。</span><span class="sxs-lookup"><span data-stu-id="4a828-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="4a828-108">您可以透過 [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) 或其別名 `where` 來篩選輸出。</span><span class="sxs-lookup"><span data-stu-id="4a828-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="4a828-109">選取簡單屬性</span><span class="sxs-lookup"><span data-stu-id="4a828-109">Select simple properties</span></span>

<span data-ttu-id="4a828-110">在預設的資料表格式中，Azure PowerShell Cmdlet 不會顯示所有可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="4a828-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="4a828-111">您可以使用 [Format-List](/powershell/module/microsoft.powershell.utility/format-list) Cmdlet，或透過管道將輸出傳送至 `Select-Object *` 以取得完整屬性：</span><span class="sxs-lookup"><span data-stu-id="4a828-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="4a828-112">一旦知道您感興趣的屬性名稱後，您可以使用這些屬性名稱搭配 `Select-Object` 來直接取得這些屬性：</span><span class="sxs-lookup"><span data-stu-id="4a828-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="4a828-113">使用 `Select-Object` 的輸出一律會經過格式化，以顯示要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a828-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="4a828-114">若要了解如何將格式化當作查詢 Cmdlet 結果的一部份使用，請參閱[格式化 Azure PowerShell Cmdlet 的輸出](formatting-output.md)。</span><span class="sxs-lookup"><span data-stu-id="4a828-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="4a828-115">選取巢狀屬性</span><span class="sxs-lookup"><span data-stu-id="4a828-115">Select nested properties</span></span>

<span data-ttu-id="4a828-116">Azure PowerShell Cmdlet 輸出中的某些屬性會使用巢狀物件，例如 `Get-AzVM` 輸出的 `StorageProfile` 屬性。</span><span class="sxs-lookup"><span data-stu-id="4a828-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="4a828-117">若要從巢狀屬性中取得要檢查的值，需提供值的顯示名稱和完整路徑，以作為 `Select-Object` 中字典引數的一部份：</span><span class="sxs-lookup"><span data-stu-id="4a828-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="4a828-118">每個字典引數都會從物件中選取一個屬性。</span><span class="sxs-lookup"><span data-stu-id="4a828-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="4a828-119">要擷取的屬性必須是運算式的一部分。</span><span class="sxs-lookup"><span data-stu-id="4a828-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="4a828-120">篩選結果</span><span class="sxs-lookup"><span data-stu-id="4a828-120">Filter results</span></span> 

<span data-ttu-id="4a828-121">`Where-Object` Cmdlet 可讓您根據任何屬性值 (包括巢狀屬性) 來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="4a828-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="4a828-122">下一個範例會示範如何使用 `Where-Object` 來尋找資源群組中的 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="4a828-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="4a828-123">您可以使用管道將 `Select-Object` 和 `Where-Object` 的結果傳送給彼此。</span><span class="sxs-lookup"><span data-stu-id="4a828-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="4a828-124">基於效能目的，我們一律建議將 `Where-Object` 作業放在 `Select-Object` 之前：</span><span class="sxs-lookup"><span data-stu-id="4a828-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```