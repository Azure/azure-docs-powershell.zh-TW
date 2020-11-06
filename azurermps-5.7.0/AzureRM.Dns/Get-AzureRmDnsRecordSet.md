---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452268"
---
# Get-AzureRmDnsRecordSet

## 摘要
取得 DNS 記錄集。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 區域
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 面向
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDnsRecordSet** Cmdlet 會在指定的區域中，以指定的名稱與類型來取得網功能變數名稱稱系統 (DNS) 記錄集。

如果您沒有指定 *Name* 或 *RecordType* 參數，這個 Cmdlet 會傳回區域中指定類型的所有記錄集。
如果您指定 *RecordType* 參數而不是 *Name* 參數，這個 Cmdlet 會傳回指定記錄類型的所有記錄集。

您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定區域和資源群組。

## 示例

### 範例1：取得具有指定名稱和類型的記錄集
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

這個命令會在指定的資源群組和區域中取得一組記錄類型的記錄，並將它儲存在 $RecordSet 變數中。
因為已指定 *Name* 和 *RecordType* 參數，所以只會傳回一個 **記錄集** 物件。

### 範例2：取得指定類型的記錄集
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

這個命令會在名為 [MyResourceGroup] 的資源群組中，從名為「myzone.com」的區域中取得記錄類型 A 之所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。

### 範例3：取得區域中的所有記錄集
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

這個命令會在名為 MyResourceGroup 的資源群組中，從名為 myzone.com 的區域中取得所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。

### 範例4：使用 DnsZone 物件在區域中取得所有記錄集
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

這個範例與上述範例3相當。
這次，該區域是使用 zone 物件來指定的。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得的 **記錄集** 名稱。
如果您沒有指定 *Name* 參數，則會傳回指定類型的所有記錄集。

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
指定此 Cmdlet 取得的 DNS 記錄類型。

有效值為： 

- 是
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- DNS-SRV
- 文字檔

如果您沒有指定 *RecordType* 參數，也必須省略 *Name* 參數。 這個 Cmdlet 會傳回所有名稱和類型的區域 (中的所有記錄集) 。

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含 DNS 區域的資源群組。
您也必須使用 *ZoneName* 參數指定區功能變數名稱稱。

或者，您也可以使用 *zone* 參數傳入 **DnsZone** 物件來指定區域和資源群組。

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
指定包含此 Cmdlet 所取得之記錄集的 DNS 區域。
或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。

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

### -ZoneName
指定包含要取得之記錄集之 DNS 區域的名稱。
您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。

或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### DnsZone （）
您可以將 **DnsZone** 物件輸送到這個 Cmdlet。
**DnsZone** 物件代表要在其中尋找 **RecordSet** 物件的區域。

## 輸出

### DnsRecordSet （）
這個 Cmdlet 會傳回一個或多個代表找到之記錄集的物件。
如果指定 *Name* 與 *RecordType* 參數，則最多會傳回一個 **記錄集** ，否則會以陣列形式傳回多個 **記錄集** 物件。

## 筆記

## 相關連結

[新-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[移除-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


