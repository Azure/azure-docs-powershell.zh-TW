---
title: 格式化 Azure PowerShell Cmdlet 輸出
description: 如何格式化 Azure PowerShell 的 Cmdlet 輸出。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: d655be02df40049d82d686667684b7b26a2c19ea
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342397"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="991fd-103">格式化 Azure PowerShell Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="991fd-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="991fd-104">依預設，每個 Azure PowerShell Cmdlet 的輸出格式都很容易讀取。</span><span class="sxs-lookup"><span data-stu-id="991fd-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="991fd-105">PowerShell 可讓您將 Cmdlet 輸出轉換或格式化為下列其中一個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="991fd-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="991fd-106">格式化</span><span class="sxs-lookup"><span data-stu-id="991fd-106">Formatting</span></span>      | <span data-ttu-id="991fd-107">轉換</span><span class="sxs-lookup"><span data-stu-id="991fd-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="991fd-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="991fd-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="991fd-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="991fd-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="991fd-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="991fd-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="991fd-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="991fd-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="991fd-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="991fd-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="991fd-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="991fd-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="991fd-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="991fd-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="991fd-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="991fd-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="991fd-116">格式化可用於在 PowerShell 終端中顯示內容，而轉換則用來產生供其他指令碼或程式使用的資料。</span><span class="sxs-lookup"><span data-stu-id="991fd-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="991fd-117">Table 輸出格式</span><span class="sxs-lookup"><span data-stu-id="991fd-117">Table output format</span></span>

<span data-ttu-id="991fd-118">依預設，Azure PowerShell Cmdlet 會以資料表格式輸出。</span><span class="sxs-lookup"><span data-stu-id="991fd-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="991fd-119">此格式不會顯示要求資源的所有資訊：</span><span class="sxs-lookup"><span data-stu-id="991fd-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="991fd-120">PowerShell 工作階段視窗的寬度會影響由 `Format-Table` 所顯示的資料量。</span><span class="sxs-lookup"><span data-stu-id="991fd-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="991fd-121">若要將輸出限制為特定屬性並加以排序，可以提供屬性名稱做為 `Format-Table` 的引數：</span><span class="sxs-lookup"><span data-stu-id="991fd-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="991fd-122">清單輸出格式</span><span class="sxs-lookup"><span data-stu-id="991fd-122">List output format</span></span>

<span data-ttu-id="991fd-123">清單輸出格式會產生兩個資料行，而值後面會緊接著屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="991fd-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="991fd-124">對於複雜的物件，則會改為顯示該物件的類型。</span><span class="sxs-lookup"><span data-stu-id="991fd-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="991fd-125">下列輸出會移除某些欄位。</span><span class="sxs-lookup"><span data-stu-id="991fd-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="991fd-126">例如 `Format-Table`，系統會提供屬性名稱以便將輸出排序，並限制輸出：</span><span class="sxs-lookup"><span data-stu-id="991fd-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="991fd-127">寬度輸出格式</span><span class="sxs-lookup"><span data-stu-id="991fd-127">Wide output format</span></span>

<span data-ttu-id="991fd-128">只會針對每個查詢產生一個屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="991fd-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="991fd-129">您可以提供做為引數的屬性來控制要顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="991fd-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="991fd-130">自訂輸出格式</span><span class="sxs-lookup"><span data-stu-id="991fd-130">Custom output format</span></span>

<span data-ttu-id="991fd-131">`Custom-Format` 輸出類型的作用是格式化自訂物件。</span><span class="sxs-lookup"><span data-stu-id="991fd-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="991fd-132">若沒有任何引數，其行為會類似 `Format-List`，但是會顯示自訂類別的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="991fd-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="991fd-133">下列輸出會移除某些欄位。</span><span class="sxs-lookup"><span data-stu-id="991fd-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="991fd-134">將屬性名稱做為 `Custom-Format` 的引數，會顯示設為值之自訂物件集的屬性/值組：</span><span class="sxs-lookup"><span data-stu-id="991fd-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="991fd-135">下列輸出會移除某些欄位。</span><span class="sxs-lookup"><span data-stu-id="991fd-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="991fd-136">轉換成其他資料格式</span><span class="sxs-lookup"><span data-stu-id="991fd-136">Conversion to other data formats</span></span>

<span data-ttu-id="991fd-137">`ConvertTo-*` 系列的 Cmdlet 是用來將 Azure PowerShell Cmdlet 的結果轉換成電腦可讀取的格式。</span><span class="sxs-lookup"><span data-stu-id="991fd-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="991fd-138">若只需從 Azure PowerShell 結果中獲得一些屬性，請在執行轉換之前，在管道中使用 `Select-Object` 命令。</span><span class="sxs-lookup"><span data-stu-id="991fd-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="991fd-139">下列範例會示範每個轉換產生的不同種類輸出。</span><span class="sxs-lookup"><span data-stu-id="991fd-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="991fd-140">轉換為 CSV</span><span class="sxs-lookup"><span data-stu-id="991fd-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="991fd-141">轉換為 JSON</span><span class="sxs-lookup"><span data-stu-id="991fd-141">Conversion to JSON</span></span>

<span data-ttu-id="991fd-142">根據預設，JSON 輸出不會展開所有屬性。</span><span class="sxs-lookup"><span data-stu-id="991fd-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="991fd-143">若要變更屬性展開的深度，請使用 `-Depth` 引數。</span><span class="sxs-lookup"><span data-stu-id="991fd-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="991fd-144">根據預設，展開的深度為 `2`。</span><span class="sxs-lookup"><span data-stu-id="991fd-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="991fd-145">下列輸出會移除某些欄位。</span><span class="sxs-lookup"><span data-stu-id="991fd-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="991fd-146">轉換為 XML</span><span class="sxs-lookup"><span data-stu-id="991fd-146">Conversion to XML</span></span>

<span data-ttu-id="991fd-147">`ConvertTo-XML` Cmdlet 會將 Azure PowerShell 回應物件轉換為純 XML 物件，可以使用處理 PowerShell 中任何其他 XML 物件的方式處理。</span><span class="sxs-lookup"><span data-stu-id="991fd-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="991fd-148">轉換為 HTML</span><span class="sxs-lookup"><span data-stu-id="991fd-148">Conversion to HTML</span></span>

<span data-ttu-id="991fd-149">將物件轉換為 HTML 時，會產生將轉譯為 HTML 表格的輸出。</span><span class="sxs-lookup"><span data-stu-id="991fd-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="991fd-150">HTML 轉譯方式會依瀏覽器轉譯資料表時不包含寬度資訊的行為處理。</span><span class="sxs-lookup"><span data-stu-id="991fd-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="991fd-151">不會展開自訂類別物件。</span><span class="sxs-lookup"><span data-stu-id="991fd-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```