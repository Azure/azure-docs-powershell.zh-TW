---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cb2fb6d8d113ec857ed5a69d84dcf5be8d1ee56d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915350"
---
# New-AzApplicationGatewayProbeConfig

## 簡介
建立健康狀態探索。

## 語法

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## 描述
Cmdlet New-AzApplicationGatewayProbeConfig建立健康狀態建議。

## 例子

### 範例 1：範例1：建立健康狀態
```powershell
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

此命令會建立名為 Command03 的健康情況修正程式，具有 HTTP 通訊協定、30 秒間隔、120 秒的超時，以及 8 次重試的不健康閥值。

### 範例 2

建立健康狀態探索。  (自動) 

<!-- Aladdin Generated Example -->
```powershell
New-AzApplicationGatewayProbeConfig -Interval 30 -Match <PSApplicationGatewayProbeHealthResponseMatch> -Name 'Probe03' -Path '/path/custompath.htm' -PickHostNameFromBackendHttpSettings -Protocol https -Timeout 120 -UnhealthyThreshold 8
```

## 參數

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -HostName
指定此 Cmdlet 傳送的主機名稱稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Interval
指定以秒為單位的間隔間隔。
這是兩個連續的間隔時間。
此值介於 1 秒到 86400 秒之間。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -符合
必須包含在健康回應中的內體。
預設值為空白

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
一直標示為健康狀態的最低伺服器數量。
預設值為 0

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定探索的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -路徑
指定建議的相對路徑。
有效路徑的開頭是 / (斜線) 。
此通知會寄至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
是否應該從後端 HTTP 設定挑選主機標題。
預設值為 False

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

### -通訊協定
指定用來傳送通知的通訊協定。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
指定以碼錶示的探索超時。
如果在此超時期間未收到有效的回應，此 Cmdlet 會將探索標記為失敗。
有效的值介於 1 秒到 86400 秒之間。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -不健康Threshold
指定重新嘗試嘗試的次次計數。
連續的啟動失敗計數達到不健康閾值之後，後端伺服器會標示為向下。
有效的值介於 1 秒到 20 秒之間。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -埠
指定用於探索後端伺服器的埠。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

