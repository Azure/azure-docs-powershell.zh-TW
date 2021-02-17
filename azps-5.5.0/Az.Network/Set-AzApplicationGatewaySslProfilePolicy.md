---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 7d04d73905bde7ab008c6910cab708e209125316
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407993"
---
# Set-AzApplicationGatewaySslProfilePolicy

## 簡介
修改應用程式閘道 SSL 設定檔的 SSL 策略。

## 語法

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 描述
**Set-AzApplicationGatewaySslProfilePolicy** Cmdlet 會修改應用程式閘道 SSL 設定檔的 SSL 策略。

## 例子

### 範例 1
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。 第二個命令會獲得名稱為 SslProfile01 的 ssl 設定檔$AppGw將設定儲存在$profile變數中。 最後一個命令會修改儲存在 $profile 中的 ssl 設定檔物件的 ssl $profile。

## 參數

### -CipherSuite
以指定的順序啟用應用程式閘道的 Ssl 密碼套件

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisabledSslProtocols
要停用的 SSL 通訊協定清單

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinProtocolVersion
應用程式閘道支援的最小 Ssl 通訊協定版本

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyName
Ssl 預先定義之策略的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyType
Ssl 策略類型

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
應用程式閘道 SSL 設定檔

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，系統會提示您確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile

## 輸出

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile

## 筆記

## 相關連結



[Get-AzApplicationGatewaySslProfilePolicy](./Get-AzApplicationGatewaySslProfilePolicy.md)

[Remove-AzApplicationGatewaySslProfilePolicy](./Remove-AzApplicationGatewaySslProfilePolicy.md)
