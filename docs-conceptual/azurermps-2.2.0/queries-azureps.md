---
title: 查詢 Azure 資源以及將結果格式化 | Microsoft Docs
description: 如何查詢 Azure 中的資源，並將結果格式化。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 139744596eba467f08be521385049dddcc43ae05
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821780"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="2c902-103">查詢 Azure 資源</span><span class="sxs-lookup"><span data-stu-id="2c902-103">Querying for Azure resources</span></span>

<span data-ttu-id="2c902-104">使用內建 Cmdlet 即可在 PowerShell 中完成查詢。</span><span class="sxs-lookup"><span data-stu-id="2c902-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="2c902-105">在 PowerShell 中，Cmdlet 名稱採用**_動詞-名詞_** 的格式。</span><span class="sxs-lookup"><span data-stu-id="2c902-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="2c902-106">使用動詞 **_Get_** 的 Cmdlet 是查詢 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c902-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="2c902-107">Cmdlet 名詞則是 Cmdlet 動詞要據以執行之 Azure 資源的類型。</span><span class="sxs-lookup"><span data-stu-id="2c902-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="2c902-108">選取簡單屬性</span><span class="sxs-lookup"><span data-stu-id="2c902-108">Selecting simple properties</span></span>

<span data-ttu-id="2c902-109">Azure PowerShell 已為每個 Cmdlet 定義了預設格式。</span><span class="sxs-lookup"><span data-stu-id="2c902-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="2c902-110">每個資源類型最常見的屬性則會以資料表或清單格式自動顯示。</span><span class="sxs-lookup"><span data-stu-id="2c902-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="2c902-111">如需如何將輸出格式化的詳細資訊，請參閱[將查詢結果格式化](formatting-output.md)。</span><span class="sxs-lookup"><span data-stu-id="2c902-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="2c902-112">使用 `Get-AzureRmVM` Cmdlet 來查詢帳戶中的 VM 清單。</span><span class="sxs-lookup"><span data-stu-id="2c902-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="2c902-113">預設輸出會自動格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="2c902-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="2c902-114">`Select-Object` Cmdlet 可用來選取您感興趣的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="2c902-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="2c902-115">選取複雜的巢狀屬性</span><span class="sxs-lookup"><span data-stu-id="2c902-115">Selecting complex nested properties</span></span>

<span data-ttu-id="2c902-116">如果您想要選取的屬性在 JSON 中輸出深入巢狀，您必須將完整路徑提供給該巢狀屬性。</span><span class="sxs-lookup"><span data-stu-id="2c902-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="2c902-117">下列範例顯示如何從 `Get-AzureRmVM` Cmdlet 選取 VM 名稱和 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="2c902-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="2c902-118">使用 Where-Object Cmdlet 來篩選結果</span><span class="sxs-lookup"><span data-stu-id="2c902-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="2c902-119">`Where-Object` Cmdlet 可讓您根據任何屬性值來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="2c902-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="2c902-120">在下列範例中，篩選器只會選取名稱中具有 "RGD" 文字的 VM。</span><span class="sxs-lookup"><span data-stu-id="2c902-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="2c902-121">下一個範例中，結果會傳回具有 vmSize 'Standard_DS1_V2' 的 VM。</span><span class="sxs-lookup"><span data-stu-id="2c902-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
