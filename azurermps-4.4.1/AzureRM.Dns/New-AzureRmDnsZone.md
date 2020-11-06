---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452504"
---
# New-AzureRmDnsZone

## 摘要
建立新的 DNS 區域。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。 您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。 建立區域之後，請使用 New-AzureRmDnsRecordSet Cmdlet 來建立區域中的記錄集。

您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。

## 示例

### 範例1：建立 DNS 區域
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。

## 參數

### -名稱
指定要建立之 DNS 區域的名稱。

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

### -ResourceGroupName
指定要在其中建立區域的資源群組。

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

### -Tag
雜湊資料表形式的索引鍵/值對。 例如：

@ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### 所有
您無法將輸入管到這個 Cmdlet。

## 輸出

### DnsZone （）
這個 Cmdlet 會傳回代表新的 DNS 區域的 DnsZone 物件。

## 筆記
您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。
根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。

如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。
如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。

## 相關連結

[AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[新-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[移除-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
