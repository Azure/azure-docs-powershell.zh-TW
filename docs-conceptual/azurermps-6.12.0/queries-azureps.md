---
title: 查詢 Azure PowerShell Cmdlet 的輸出
description: 如何查詢 Azure 中的資源，並將結果格式化。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bd1bea43303e9f5a2b46d63a3ac51b4c4031b9f
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575853"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="5fd1e-103">查詢 Azure PowerShell Cmdlet 的輸出</span><span class="sxs-lookup"><span data-stu-id="5fd1e-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="5fd1e-104">使用內建 Cmdlet 即可在 PowerShell 中完成查詢。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="5fd1e-105">在 PowerShell 中，Cmdlet 名稱採用**_動詞-名詞_** 的格式。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="5fd1e-106">使用動詞 **_Get_** 的 Cmdlet 是查詢 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="5fd1e-107">Cmdlet 名詞則是 Cmdlet 動詞要據以執行之 Azure 資源的類型。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="5fd1e-108">選取簡單屬性</span><span class="sxs-lookup"><span data-stu-id="5fd1e-108">Select simple properties</span></span>

<span data-ttu-id="5fd1e-109">Azure PowerShell 已為每個 Cmdlet 定義了預設格式。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="5fd1e-110">每個資源類型最常見的屬性則會以資料表或清單格式自動顯示。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="5fd1e-111">如需如何將輸出格式化的詳細資訊，請參閱[將查詢結果格式化](formatting-output.md)。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="5fd1e-112">使用 `Get-AzureRmVM` Cmdlet 來查詢帳戶中的 VM 清單。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="5fd1e-113">預設輸出會自動格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="5fd1e-114">`Select-Object` Cmdlet 可用來選取您感興趣的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="5fd1e-115">選取複雜的巢狀屬性</span><span class="sxs-lookup"><span data-stu-id="5fd1e-115">Select complex nested properties</span></span>

<span data-ttu-id="5fd1e-116">如果您需要的屬性內嵌於 JSON 輸出中，您必須將完整路徑提供給該屬性。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="5fd1e-117">下列範例顯示如何從 `Get-AzureRmVM` Cmdlet 選取 VM 名稱和 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="5fd1e-118">使用 Where-Object Cmdlet 來篩選結果</span><span class="sxs-lookup"><span data-stu-id="5fd1e-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="5fd1e-119">`Where-Object` Cmdlet 可讓您根據任何屬性值來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="5fd1e-120">在下列範例中，篩選器只會選取名稱中具有 "RGD" 文字的 VM。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="5fd1e-121">下一個範例中，結果會傳回具有 vmSize 'Standard_DS1_V2' 的 VM。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```