---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446814"
---
# Set-AzureRmDnsRecordSet

## 摘要
更新 DNS 記錄集。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmDnsRecordSet** Cmdlet 會從本機 **RecordSet** 物件更新 Azure DNS 服務中的記錄集。

您可以將 **RecordSet** 物件作為參數傳遞，或使用管線運算子。

您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。

如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。
這可為併發變更提供保護。
您可以使用 *Overwrite* 參數來隱含此行為，不論併發變更為何，都會更新記錄集。

## 示例

### 範例1：更新記錄集
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

第一個命令使用 Get-AzureRmDnsRecordSet Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。

第二個和第三個命令是離線作業，可將兩筆記錄新增至記錄集。

最終命令會使用 **AzureRmDnsRecordSet** Cmdlet 來認可更新。

### 範例2：更新 SOA 記錄
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

第一個命令使用 **AzureRmDnsRecordset** Cmdlet 來取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。

第二個命令會更新 $RecordSet 中指定的 SOA 記錄。

Final 命令會使用 **AzureRmDnsRecordSet** Cmdlet 來傳播 $RecordSet 中的更新。

## 參數

### -Overwrite
指示更新記錄集（不論併發變更）。

如果自檢索到本機 **RecordSet** 物件之後，在 Azure DNS 中變更記錄集，則不會更新。
這可為併發變更提供保護。
若要取消此行為，您可以使用 *Overwrite* 參數，不論併發變更為何，都會更新記錄集合。

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
指定要更新的 **記錄集** 。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### DnsRecordSet （）
您可以將 **RecordSet** 物件傳遞到這個 Cmdlet。

## 輸出

### DnsRecordSet （）
這個 Cmdlet 會傳回代表更新之 **RecordSet** 物件的物件。

## 筆記
您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。
根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。

如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。
如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。 

## 相關連結

[AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[新-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[移除-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)
