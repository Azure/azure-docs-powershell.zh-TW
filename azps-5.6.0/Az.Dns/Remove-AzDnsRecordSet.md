---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910130"
---
# Remove-AzDnsRecordSet

## 簡介
刪除記錄集。

## 語法

### 領域
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 混合
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 物件
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Remove-AzDnsRecordSet** Cmdlet 會從指定的區域刪除指定的記錄集。
您無法刪除在區域 (自動) NS 記錄或名稱伺服器。
您可以使用管線運算子或參數，將 **RecordSet** 物件傳遞到此 Cmdlet。
若要在不使用 **RecordSet** 物件的情況下，根據名稱與類型識別記錄，您必須使用管線運算子或參數，將區域以 **DnsZone** 物件傳遞至此 Cmdlet，或者您也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。
您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。
使用 RecordSet 物件指定記錄集時，如果自已取回本地 **RecordSet** 物件之後，已在 Azure DNS 中變更記錄集， **則記錄** 集不會刪除。
這可保護同時進行變更。
您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除記錄集。

## 例子

### 範例 1：移除記錄集
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

第一個命令會獲得指定的記錄集，然後將它儲存在$RecordSet變數中。第二個命令會移除 $RecordSet。

### 範例 2：移除記錄集並隱藏所有確認
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

第一個命令會獲得指定的記錄集。
第二個命令會刪除記錄集，即使同時已變更。
確認提示會隱藏。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要移除 **的 RecordSet** 名稱。
在根據名稱指定記錄集時，必須使用 *Zone* 參數或 *ZoneName* 和 *ResourceGroupName* 參數來指定 DNS 區域。
或者，您可以使用 **RecordSet** 物件來指定記錄集，使用 *RecordSet* 參數傳遞。

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -覆寫
使用 RecordSet 物件指定記錄集時，如果自已取回本地 **RecordSet** 物件之後，已在 Azure DNS 中變更記錄集， **則記錄** 集不會刪除。
這可保護同時進行變更。
您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除記錄集。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Passthru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
指定 **要移除的 RecordSet** 物件。
或者，您可以使用名稱和區域參數，或是使用 *名稱**、ZoneName* 和 *ResourceGroupName* 參數來指定記錄集。 

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
指定 DNS 記錄的類型。
有效的值為：
- A
- Aaaa
- CNAME
- Mx
- Ns
- Ptr
- SRV
- 刪除區域時，會自動刪除 TXT 的 DNS 記錄。
您無法手動刪除 DNS 記錄。

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要刪除 **RecordSet** 之 DNS 區域的資源群組。
只有在使用 Name 和 *ZoneName* 參數指定記錄集和DNS 區域時，此參數才適用。
或者，您可以使用 *RecordSet* 參數或名稱和區域參數來指定 *記錄* 集。 

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -區域
指定包含要刪除 **之 RecordSet 的 DNS** 區域。
此參數僅適用于使用 Name 參數指定記錄 *集* 時。
或者，您可以使用 *RecordSet* 參數或 Name、ZoneName 及 *ResourceGroupName* 參數來指定記錄集。  

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
指定要刪除包含 **RecordSet 的區域** 名稱。
您也必須指定 *Name* 和 *ResourceGroupName* 參數。
或者，您可以使用 *RecordSet* 參數或 Name 和 Zone 參數來 *指定**記錄* 集。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.management.dns.models.RecordType

### System.String

### Microsoft.Azure.Commands.dns.DnsZone

### Microsoft.Azure.Commands.dns.DnsRecordSet

## 輸出

### System.Boolean

## 筆記
您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。
根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。
如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。
如果您指定 *確認：$False，Cmdlet* 不會提示您確認。

## 相關連結

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
