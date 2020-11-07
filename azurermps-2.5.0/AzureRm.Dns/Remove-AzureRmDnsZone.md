---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802514"
---
# Remove-AzureRmDnsZone

## 摘要
從資源群組中移除 DNS 區域。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 區域
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 面向
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
AzureRmDnsZone Cmdlet 會從指定 **的** 資源群組中永久刪除網域名稱系統 (DNS) 區域。
該區域中包含的所有記錄集也都會刪除。

您可以使用 *Name* 參數或使用管線運算子來傳遞 **DnsZone** 物件，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。

您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。

使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。
這可為併發區域變更提供保護。
這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。

## 示例

### 範例1：移除區域
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

這個命令會從名為 MyResourceGroup 的資源群組中移除名為 myzone.com 的區域。

## 參數

### -Force
此 Cmdlet 已棄用此 Cmdlet。
在未來版本中將會移除它。

若要控制此 Cmdlet 是否提示您進行確認，請使用 *Confirm* 參數。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 移除之 DNS 區域的名稱。
您也必須指定 *ResourceGroupName* 參數。

或者，您也可以使用 *zone* 參數指定 DNS 區域。

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。
這可為併發區域變更提供保護。

這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要移除之區域的資源群組的名稱。
您也必須指定 *ZoneName* 參數。

或者，您也可以使用 **DnsZone** 物件來指定 DNS 區域，方法是透過管線或 *zone* 參數傳遞。

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
指定要刪除的 DNS 區域。
傳遞的 **DnsZone** 物件也可以透過管線傳遞。

或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定要刪除的 DNS 區域。

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### DnsZone （）
您可以將 **DnsZone** 物件輸送到這個 Cmdlet。

## 輸出

### 所有
這個 Cmdlet 不會產生任何輸出。

## 筆記
由於刪除 DNS 區域可能會產生很大的影響，因此如果 $ConfirmPreference 的 Windows PowerShell 變數具有 None 以外的任何值，這個 Cmdlet 會提示您確認。

如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。
如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。 

## 相關連結

[AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[新-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
