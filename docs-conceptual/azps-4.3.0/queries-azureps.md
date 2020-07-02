---
title: 查詢 Azure PowerShell Cmdlet 的輸出
description: 如何查詢 Azure 中的資源，並將結果格式化。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: ebd108a2c13bdb376213d054fb72188e6205a565
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/23/2020
ms.locfileid: "85267859"
---
# <a name="query-output-of-azure-powershell"></a>查詢 Azure PowerShell 的輸出 

每個 Azure PowerShell Cmdlet 的結果都是 Azure PowerShell 物件。 即使 Cmdlet 不是明確的 `Get-` 作業，也可能會傳回可進行檢查的值，以提供已建立或已修改資源的相關資訊。 大多數的 Cmdlet 會傳回單一物件，但有些會傳回應重複查看的陣列。

在大部分的情況下，您可以使用 [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) Cmdlet (通常縮寫為 `select`) 從 Azure PowerShell 查詢輸出。 您可以透過 [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) 或其別名 `where` 來篩選輸出。

## <a name="select-simple-properties"></a>選取簡單屬性

在預設的資料表格式中，Azure PowerShell Cmdlet 不會顯示所有可用的屬性。 您可以使用 [Format-List](/powershell/module/microsoft.powershell.utility/format-list) Cmdlet，或透過管道將輸出傳送至 `Select-Object *` 以取得完整屬性：

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

一旦知道您感興趣的屬性名稱後，您可以使用這些屬性名稱搭配 `Select-Object` 來直接取得這些屬性：

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

使用 `Select-Object` 的輸出一律會經過格式化，以顯示要求的資訊。 若要了解如何將格式化當作查詢 Cmdlet 結果的一部份使用，請參閱[格式化 Azure PowerShell Cmdlet 的輸出](formatting-output.md)。

## <a name="select-nested-properties"></a>選取巢狀屬性

Azure PowerShell Cmdlet 輸出中的某些屬性會使用巢狀物件，例如 `Get-AzVM` 輸出的 `StorageProfile` 屬性。 若要從巢狀屬性中取得要檢查的值，需提供值的顯示名稱和完整路徑，以作為 `Select-Object` 中字典引數的一部份：

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

每個字典引數都會從物件中選取一個屬性。 要擷取的屬性必須是運算式的一部分。

## <a name="filter-results"></a>篩選結果 

`Where-Object` Cmdlet 可讓您根據任何屬性值 (包括巢狀屬性) 來篩選結果。 下一個範例會示範如何使用 `Where-Object` 來尋找資源群組中的 Linux VM。

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

您可以使用管道將 `Select-Object` 和 `Where-Object` 的結果傳送給彼此。 基於效能目的，我們一律建議將 `Where-Object` 作業放在 `Select-Object` 之前：

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
