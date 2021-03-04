---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910137"
---
# New-AzDnsRecordSet

## 簡介
建立 DNS 記錄集。

## 語法

### 欄位 (預設) 
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 物件
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**New-AzDnsRecordSet** Cmdlet 會以指定的名稱建立新的網域名稱系統 (DNS) 記錄集，並輸入指定的區域。
**RecordSet** 物件是一組名稱與類型相同的 DNS 記錄。
請注意，名稱是相對於區域，而非完整名稱。
*DnsRecords* 參數會指定記錄集的記錄。
此參數採用使用 New-AzDnsRecordConfig 建構的 DNS 記錄陣列。
您可以使用管線運算子將 **DnsZone** 物件傳遞到此 Cmdlet，或將 **DnsZone** 物件傳遞為 *Zone* 參數，或者您也可以按名稱指定區域。
您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。
如果符合 **的 RecordSet** 已存在 (名稱和記錄類型) ，您必須指定 *覆* 寫參數，否則 Cmdlet 不會建立 **新的 RecordSet。**

## 例子

### 範例 1：建立類型 A 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**
記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。

### 範例 2：建立類型 AAAA 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**
記錄集的類型為 AAAA，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 3：建立類型 CNAME 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**
記錄集的類型為 CNAME，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 4：建立類型 MX 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令在 myzone.com 區域中建立名為 www 的 **RecordSet。**
記錄集的類型為 MX，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 5：建立類型 NS 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令在活動區域建立名為 ns1 的 **RecordSet** myzone.com。
記錄集的類型為 NS，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 6：建立類型 PTR 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

此命令在 3.2.1.in-addr.arpa 區域中建立名為 4 的 RecordSet。
記錄集的類型為 PTR，且 TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 7：建立類型 SRV 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令會建立一個名為 _sip._tcp 的 **RecordSet，myzone.com。**
記錄集的類型為 SRV，TTL 為 1 小時， (3600 秒) 。
它包含指向 IP 位址 2001.2.3.4 的單一 DNS 記錄。
服務 (sip) 和 (tcp) 會指定為記錄集名稱的一部分，而不是記錄資料的一部分。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 8：建立類型 TXT 的 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令會在這個區域中建立名為文字的 **RecordSet** myzone.com。
記錄集的類型為 TXT，TTL 為 1 小時， (3600 秒) 。
它包含單一 DNS 記錄。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 9：在區域頂點建立 RecordSet
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令會建立 **一個 RecordSet，** 位於 (區域) 的myzone.com。
若要這麼做，記錄集名稱會指定為 "@" (包括雙引號) 。
您無法在一個區域的頂點建立 CNAME 記錄。
這是 DNS 標準的限制;這不是 Azure DNS 的限制。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 10：建立萬用字元記錄集
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

此命令會建立一個名為 ***的 RecordSet，myzone.com。**
這是萬用字元記錄集。
若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。

### 範例 11：建立空白記錄集
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

此命令在 myzone.com 區域中建立名為 www 的 **RecordSet。**
記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。
這是空白的記錄集，可做為預留位置，日後您可以新增記錄。

### 範例 12：建立記錄集並隱藏所有確認
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

此命令會建立 **RecordSet。**
覆 *寫* 參數可確保此記錄集覆寫任何名稱相同且類型相同的現有記錄集 (該記錄集的現有記錄會遺失) 。
包含 *值* $False的確認參數會隱藏確認提示。

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

### -DnsRecords
指定要納入記錄集的 DNS 記錄陣列。
您可以使用 Cmdlet New-AzDnsRecordConfig建立 DNS 記錄物件。
請參閱範例以瞭解更多資訊。

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -中繼資料
指定要與 RecordSet 建立關聯的中繼資料陣列。
中繼資料是使用以雜湊表格表示的名稱值組來指定，例如 @{"dept"="shopping";"env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要建立 **之 RecordSet** 的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -覆寫
表示此 Cmdlet 會覆寫指定的 **RecordSet** ，如果已經存在。

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

### -RecordType
指定要建立 DNS 記錄的類型。
有效的值為：
- A
- Aaaa
- CNAME
- Mx
- Ns
- Ptr
- SRV
- 當區域建立時，TXT 的 DNS 記錄會自動建立，而且無法手動建立。

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含 DNS 區域的資源群組。
您也必須指定 *ZoneName* 參數，以指定區功能變數名稱稱。
或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
別名目標資源識別碼。

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
指定 DNS RecordSet (TTL) 上的時間。

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -區域
指定要建立 RecordSet 的 **Dns 區域**。
或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
指定要建立 **RecordSet** 的區功能變數名稱稱。
您也必須使用 *ResourceGroupName* 參數指定包含區域的資源群組。
或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
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

### System.String

### Microsoft.Azure.Commands.dns.DnsZone

### System.UInt32

### Microsoft.Azure.management.dns.models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.dns.DnsRecordBase[]

## 輸出

### Microsoft.Azure.Commands.dns.DnsRecordSet

## 筆記
您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。
根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。
如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。
如果您指定 *確認：$False，Cmdlet* 不會提示您確認。

## 相關連結

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
