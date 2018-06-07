---
title: 將查詢結果格式化 | Microsoft Docs
description: 如何查詢 Azure 中的資源，並將結果格式化。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1c576aba64d2afd1bd11a0d260479e7761cb82f1
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819570"
---
# <a name="formatting-query-results"></a>將查詢結果格式化

根據預設，每個 PowerShell Cmdlet 都已預先定義輸出的格式，以方便您閱讀輸出內容。  PowerShell 也會賦予您彈性，讓您可以使用下列 Cmdlet 來調整輸出或將 Cmdlet 輸出轉換成不同格式：

| 格式化      | 轉換       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a>格式化範例

在這個範例中，我們會取得預設訂用帳戶中的 Azure VM 清單。  Get-AzureRmVM 命令將輸出預設為資料表格式。

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

如果您想要限制傳回的資料行數目，您可以使用 `Format-Table` Cmdlet。 在下列範例中，我們會取得相同的虛擬機器清單，但輸出中僅有 VM 名稱、資源群組和 VM 的位置。  `-Autosize` 參數會根據資料大小來調整資料行的大小。

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

如果您想要的話，也可以使用清單格式來檢視資訊。 下列範例示範如何使用 `Format-List` Cmdlet 來這麼做。

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a>轉換成其他資料類型

PowerShell 也提供多種輸出格式以供您滿足需求。  在下列範例中，我們使用 `Select-Object` Cmdlet 來取得訂用帳戶中的虛擬機器屬性，並將輸出轉換成 CSV 格式以方便您匯入資料庫或試算表中。

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

您也可以將輸出轉換成 JSON 格式。  下列範例會建立相同的 VM 清單，但會將輸出格式變更為 JSON。

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
