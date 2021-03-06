---
title: 查詢 Azure PowerShell Cmdlet 的輸出
description: 如何查詢 Azure 中的資源，並將結果格式化。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 664829721843020745cf24a913e1d09a4e68a3da
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243679"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>查詢 Azure PowerShell Cmdlet 的輸出

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

使用內建 Cmdlet 即可在 PowerShell 中完成查詢。 在 PowerShell 中，Cmdlet 名稱採用 **_動詞-名詞_** 的格式。 使用動詞 **_Get_** 的 Cmdlet 是查詢 Cmdlet。 Cmdlet 名詞則是 Cmdlet 動詞要據以執行之 Azure 資源的類型。

## <a name="select-simple-properties"></a>選取簡單屬性

Azure PowerShell 已為每個 Cmdlet 定義了預設格式。 每個資源類型最常見的屬性則會以資料表或清單格式自動顯示。 如需如何將輸出格式化的詳細資訊，請參閱[將查詢結果格式化](formatting-output.md)。

使用 `Get-AzureRmVM` Cmdlet 來查詢帳戶中的 VM 清單。

```azurepowershell-interactive
Get-AzureRmVM
```

預設輸出會自動格式化為資料表。

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

`Select-Object` Cmdlet 可用來選取您感興趣的特定屬性。

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>選取複雜的巢狀屬性

如果您想要選取的屬性在 JSON 中輸出深入巢狀，您必須將完整路徑提供給該巢狀屬性。 下列範例顯示如何從 `Get-AzureRmVM` Cmdlet 選取 VM 名稱和 OS 類型。

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>使用 Where-Object Cmdlet 來篩選結果

`Where-Object` Cmdlet 可讓您根據任何屬性值來篩選結果。 在下列範例中，篩選器只會選取名稱中具有 "RGD" 文字的 VM。

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

下一個範例中，結果會傳回具有 vmSize 'Standard_DS1_V2' 的 VM。

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
