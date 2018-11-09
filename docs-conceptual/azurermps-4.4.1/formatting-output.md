---
title: 將查詢結果格式化 | Microsoft Docs
description: 如何查詢 Azure 中的資源，並將結果格式化。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9ae0d661630bf4e080b3bbaa7f357c384ef68cc4
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211497"
---
# <a name="formatting-query-results"></a><span data-ttu-id="aa01c-103">將查詢結果格式化</span><span class="sxs-lookup"><span data-stu-id="aa01c-103">Formatting query results</span></span>

<span data-ttu-id="aa01c-104">根據預設，每個 PowerShell Cmdlet 都已預先定義輸出的格式，以方便您閱讀輸出內容。</span><span class="sxs-lookup"><span data-stu-id="aa01c-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="aa01c-105">PowerShell 也會賦予您彈性，讓您可以使用下列 Cmdlet 來調整輸出或將 Cmdlet 輸出轉換成不同格式：</span><span class="sxs-lookup"><span data-stu-id="aa01c-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="aa01c-106">格式化</span><span class="sxs-lookup"><span data-stu-id="aa01c-106">Formatting</span></span>      | <span data-ttu-id="aa01c-107">轉換</span><span class="sxs-lookup"><span data-stu-id="aa01c-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="aa01c-108">格式化範例</span><span class="sxs-lookup"><span data-stu-id="aa01c-108">Formatting examples</span></span>

<span data-ttu-id="aa01c-109">在這個範例中，我們會取得預設訂用帳戶中的 Azure VM 清單。</span><span class="sxs-lookup"><span data-stu-id="aa01c-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="aa01c-110">Get-AzureRmVM 命令將輸出預設為資料表格式。</span><span class="sxs-lookup"><span data-stu-id="aa01c-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="aa01c-111">如果您想要限制傳回的資料行數目，您可以使用 `Format-Table` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa01c-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="aa01c-112">在下列範例中，我們會取得相同的虛擬機器清單，但輸出中僅有 VM 名稱、資源群組和 VM 的位置。</span><span class="sxs-lookup"><span data-stu-id="aa01c-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="aa01c-113">`-Autosize` 參數會根據資料大小來調整資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="aa01c-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="aa01c-114">如果您想要的話，也可以使用清單格式來檢視資訊。</span><span class="sxs-lookup"><span data-stu-id="aa01c-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="aa01c-115">下列範例示範如何使用 `Format-List` Cmdlet 來這麼做。</span><span class="sxs-lookup"><span data-stu-id="aa01c-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell-interactive
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

## <a name="converting-to-other-data-types"></a><span data-ttu-id="aa01c-116">轉換成其他資料類型</span><span class="sxs-lookup"><span data-stu-id="aa01c-116">Converting to other data types</span></span>

<span data-ttu-id="aa01c-117">PowerShell 也提供多種輸出格式以供您滿足需求。</span><span class="sxs-lookup"><span data-stu-id="aa01c-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="aa01c-118">在下列範例中，我們使用 `Select-Object` Cmdlet 來取得訂用帳戶中的虛擬機器屬性，並將輸出轉換成 CSV 格式以方便您匯入資料庫或試算表中。</span><span class="sxs-lookup"><span data-stu-id="aa01c-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="aa01c-119">您也可以將輸出轉換成 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="aa01c-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="aa01c-120">下列範例會建立相同的 VM 清單，但會將輸出格式變更為 JSON。</span><span class="sxs-lookup"><span data-stu-id="aa01c-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell-interactive
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
