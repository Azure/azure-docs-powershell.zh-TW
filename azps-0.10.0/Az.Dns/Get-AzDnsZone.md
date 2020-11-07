---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795670"
---
# Get-AzDnsZone

## 摘要
取得 DNS 區域。

## 句法

### 預設 (預設) 
```
Get-AzDnsZone [<CommonParameters>]
```

### 資源
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## 說明
**AzDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。
如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。
如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。
您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。

## 示例

### 範例1：取得區域
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。

### 範例2：取得資源群組中的所有區域
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。

### 範例3：取得訂閱中的所有區域
```
PS C:\> $Zones = Get-AzDnsZone
```

這個範例會取得目前 Azure 訂閱中的所有 DNS 區域，然後將它們儲存在 $Zones 變數中。

## 參數

### -名稱
指定要取得的 DNS 區功能變數名稱稱。

如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得指定資源群組中的所有 DNS 區域。
如果您也省略 *ResourceGroupName* 參數，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要取得之 DNS 區域之資源群組的名稱。

如果您沒有指定 *ResourceGroupName* ，則您也必須省略 *Name* 參數。
在這種情況下，這個 Cmdlet 會取得目前 Azure 訂閱中的所有 DNS 區域。

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不允許您進行管道輸入。

## 輸出

### DnsZone （）
這個 Cmdlet 會傳回代表 DNS 區域的物件。
如果未指定區功能變數名稱稱，則會傳回區域物件的陣列。

## 筆記

## 相關連結

[新-AzDnsZone](./New-AzDnsZone.md)

[移除-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
