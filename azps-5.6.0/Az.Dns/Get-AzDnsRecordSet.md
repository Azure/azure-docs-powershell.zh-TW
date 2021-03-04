---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910146"
---
# Get-AzDnsRecordSet

## 簡介
獲得 DNS 記錄集。

## 語法

### 領域
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 物件
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzDnsRecordSet** Cmdlet 會取得指定區域中具有指定名稱和類型的網域名稱系統 (DNS) 記錄集。
如果您未指定 *Name* 或 *RecordType* 參數，此 Cmdlet 會傳回區域中指定類型的所有記錄集。
如果您指定 *RecordType* 參數，但未指定 *Name* 參數，此 Cmdlet 會傳回指定記錄類型的所有記錄集。
您可以使用管線運算子將 **DnsZone** 物件傳遞到此 Cmdlet，或將 **DnsZone** 物件傳遞為 *Zone* 參數，或者您也可以根據名稱指定區域和資源群組。

## 例子

### 範例 1：取得具有指定名稱和類型的記錄集
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

此命令會獲得指定資源群組和區域中名為 www 的記錄類型 A 記錄集，然後將它儲存在$RecordSet變數。
由於會 *指定 Name* 和 *RecordType* 參數，因此只會 **傳回一個 RecordSet** 物件。

### 範例 2：取得指定類型的記錄集
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

此命令會從名為 MyResourceGroup 的資源群組中，將 A 記錄類型的所有記錄集陣列放在名為 myzone.com 的區域，然後將它們儲存在 $RecordSets 變數中。

### 範例 3：取得區域中的所有記錄集
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

此命令會獲得名為 MyResourceGroup 之資源群組中名為 myzone.com 之區域中所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。

### 範例 4：使用 DnsZone 物件取得區域中的所有記錄集
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

此範例相當於上述範例 3。
這一次，區域是使用區域物件指定。

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
指定要取得 **之 RecordSet** 的名稱。
如果您沒有指定 *Name* 參數，則會返回指定類型的所有記錄集。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
指定此 Cmdlet 所獲取的 DNS 記錄類型。
有效的值為： 
- A
- Aaaa
- CNAME
- Mx
- Ns
- Ptr
- Soa
- SRV
- TXT 如果您未指定 *RecordType* 參數，您也必須省略 *Name* 參數。 此 Cmdlet 接著會以所有名稱及類型 (區域的所有記錄集) 。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含 DNS 區域的資源群組。
區功能變數名稱稱也必須使用 *ZoneName* 參數指定。
或者，您也可以使用 Zone 參數傳遞 **DnsZone** 物件來指定 *區域* 和資源群組。

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
指定包含此 Cmdlet 所獲得記錄集的 DNS 區域。
或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
指定包含要取得之記錄集的 DNS 區功能變數名稱稱。
包含區域的資源群組也必須使用 *ResourceGroupName* 參數指定。
或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### Microsoft.Azure.Commands.dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.management.dns.models.RecordType，Microsoft.Azure.management.dns， Version=3.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]

## 輸出

### Microsoft.Azure.Commands.dns.DnsRecordSet

## 筆記

## 相關連結

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


