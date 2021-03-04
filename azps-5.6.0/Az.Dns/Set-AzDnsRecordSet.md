---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910121"
---
# Set-AzDnsRecordSet

## 簡介
更新 DNS 記錄集。

## 語法

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 描述
**Set-AzDnsRecordSet** Cmdlet 會從本地 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。
您可以將 **RecordSet 物件** 傳遞為參數，或是使用管線運算子。
您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。
如果記錄集在 Azure DNS 中已經變更，則自已取回本地 **RecordSet** 物件之後，記錄集不會更新。
這可保護同時進行變更。
您可以使用覆寫參數隱藏此行為，無論同時變更，都會更新記錄集。

## 例子

### 範例 1：更新記錄集
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

第一個命令使用 Get-AzDnsRecordSet Cmdlet 取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。
第二個和第三個命令是線下作業，在記錄集新增兩個 A 記錄。
最後一個命令使用 **Set-AzDnsRecordSet** Cmdlet 來提交更新。

### 範例 2：更新一個
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

第一個命令使用 **Get-AzDnsRecordset** Cmdlet 取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。
第二個命令會更新 $RecordSet 中指定的 $RECORDSET。
最後一個命令會使用 **Set-AzDnsRecordSet** Cmdlet 在 $RecordSet 中傳播更新。

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

### -覆寫
表示無論同時變更，都會更新記錄集。
如果記錄集在 Azure DNS 中自取取本地 **RecordSet** 物件之後已經變更，則記錄集將不會更新。
這可保護同時進行變更。
若要隱藏此行為，您可以使用 *覆* 寫參數，無論同時變更，都會更新記錄集。

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
指定要 **更新的 RecordSet。**

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。

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

### Microsoft.Azure.Commands.dns.DnsRecordSet

## 輸出

### Microsoft.Azure.Commands.dns.DnsRecordSet

## 筆記
您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。
根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。
如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。
如果您指定 *確認：$False，Cmdlet* 不會提示您確認。 

## 相關連結

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
