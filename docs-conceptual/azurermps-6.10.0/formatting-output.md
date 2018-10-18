---
title: 格式化 Azure PowerShell Cmdlet 輸出
description: 如何格式化 Azure PowerShell 的 Cmdlet 輸出。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 99c635e7d94731d360b81c10b7f08086652ca81f
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2018
ms.locfileid: "49400040"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="c83e7-103">格式化 Azure PowerShell Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="c83e7-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="c83e7-104">根據預設，每個 Azure PowerShell Cmdlet 都已預先定義輸出的格式，以方便您閱讀輸出內容。</span><span class="sxs-lookup"><span data-stu-id="c83e7-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="c83e7-105">PowerShell 也會賦予您彈性，讓您可以使用下列 Cmdlet 來調整輸出或將 Cmdlet 輸出轉換成不同格式：</span><span class="sxs-lookup"><span data-stu-id="c83e7-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="c83e7-106">格式化</span><span class="sxs-lookup"><span data-stu-id="c83e7-106">Formatting</span></span>      | <span data-ttu-id="c83e7-107">轉換</span><span class="sxs-lookup"><span data-stu-id="c83e7-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="c83e7-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="c83e7-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="c83e7-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="c83e7-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="c83e7-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="c83e7-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="c83e7-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="c83e7-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="c83e7-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="c83e7-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="c83e7-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="c83e7-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="c83e7-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="c83e7-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="c83e7-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="c83e7-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="c83e7-116">格式化範例</span><span class="sxs-lookup"><span data-stu-id="c83e7-116">Format examples</span></span>

<span data-ttu-id="c83e7-117">在此範例中，我們會取得預設訂用帳戶中的 Azure VM 清單。</span><span class="sxs-lookup"><span data-stu-id="c83e7-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="c83e7-118">`Get-AzureRmVM` 命令將輸出預設為資料表格式。</span><span class="sxs-lookup"><span data-stu-id="c83e7-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="c83e7-119">如果您想要限制傳回的資料行數目，您可以使用 `Format-Table` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c83e7-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="c83e7-120">在下列範例中，我們會取得相同的虛擬機器清單，但輸出中僅有 VM 名稱、資源群組和 VM 的位置。</span><span class="sxs-lookup"><span data-stu-id="c83e7-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="c83e7-121">`-Autosize` 參數會根據資料大小來調整資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="c83e7-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="c83e7-122">輸出也可以格式化成清單。</span><span class="sxs-lookup"><span data-stu-id="c83e7-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="c83e7-123">下列範例示範如何使用 `Format-List` Cmdlet 來這麼做。</span><span class="sxs-lookup"><span data-stu-id="c83e7-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="c83e7-124">轉換成其他資料類型</span><span class="sxs-lookup"><span data-stu-id="c83e7-124">Convert to other data types</span></span>

<span data-ttu-id="c83e7-125">PowerShell 也可讓您取得命令輸出，並將它轉換成多種資料格式。</span><span class="sxs-lookup"><span data-stu-id="c83e7-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="c83e7-126">在下列範例中，我們使用 `Select-Object` Cmdlet 來取得訂用帳戶中的虛擬機器屬性，並將輸出轉換成 CSV 格式以方便您匯入資料庫或試算表中。</span><span class="sxs-lookup"><span data-stu-id="c83e7-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="c83e7-127">輸出也可以轉換成 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="c83e7-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="c83e7-128">下列範例會建立相同的 VM 清單，但會將輸出格式變更為 JSON。</span><span class="sxs-lookup"><span data-stu-id="c83e7-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
