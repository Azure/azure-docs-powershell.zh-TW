---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452156"
---
# New-AzureRmApplicationGatewayProbeConfig

## 摘要
建立健全性探針。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
New-AzureRmApplicationGatewayProbeConfig Cmdlet 會建立健全性探測器。

## 示例

### Example1：建立健全性探針
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

這個命令會建立一個名為 Probe03 的健康情況探測，其 HTTP 通訊協定為30秒間隔，超時為120秒，且不正常的閾值為8次。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -HostName
指定此 Cmdlet 傳送探測的主機名稱。

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

### 間隔
指定探測間隔（以秒為單位）。
這是兩個連續探測器之間的時間間隔。
這個值介於1秒與86400秒之間。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 相符
在健康情況回應中必須包含的主體。
預設值為空白

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
最少標示為 [良好] 的伺服器數目。
預設值為0

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定探測器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定探測的相對路徑。
有效路徑是以斜線字元開頭 (/) 。
探測會傳送至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
是否應從後端 HTTP 設定中挑選主機標頭。
預設值為 false

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

### -通訊協定
指定用來傳送探測的通訊協定。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -超時
指定探測超時（以秒為單位）。
如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。
有效值為1秒到86400秒。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
指定 [探測重試計數]。
連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。
有效值為1秒到20秒。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSApplicationGatewayProbe 中的 [.]

## 筆記

## 相關連結

[使用 PowerShell for Azure 資源管理器建立應用程式閘道的自訂探測](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[附加 AzureRmApplicationGatewayProbeConfig]()

[AzureRmApplicationGatewayProbeConfig]()

[移除-AzureRmApplicationGatewayProbeConfig]()

[Set-AzureRmApplicationGatewayProbeConfig]()

