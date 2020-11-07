---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801674"
---
# Get-AzureRmDnsZone

## 摘要
取得 DNS 區域。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 預設 (預設) 
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### 資源
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## 說明
**AzureRmDnsZone** Cmdlet 會從指定的資源群組 (DNS) 區域中取得網功能變數名稱稱系統。
如果您指定 *Name* 參數，則會傳回單一 **DnsZone** 物件。
如果您沒有指定 *Name* 參數，則會傳回包含指定資源群組中所有區域的陣列。
您可以使用 **DnsZone** 物件來更新區域，例如，您可以將 **記錄集** 物件新增到其中。

## 示例

### 範例1：取得區域
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

這個範例會從指定的資源群組取得名為 myzone.com 的 DNS 區域，然後將它儲存在 $Zone 變數中。

### 範例2：取得資源群組中的所有區域
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

這個範例會取得指定資源群組中的所有 DNS 區域，然後將它儲存在 $Zones 變數中。

### 範例3：取得訂閱中的所有區域
```
PS C:\> $Zones = Get-AzureRmDnsZone
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不允許您進行管道輸入。

## 輸出

### DnsZone （）
這個 Cmdlet 會傳回代表 DNS 區域的物件。
如果未指定區功能變數名稱稱，則會傳回區域物件的陣列。

## 筆記

## 相關連結

[新-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[移除-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
