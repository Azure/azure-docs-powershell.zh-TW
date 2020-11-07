---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967875"
---
# Set-AzureApplicationGatewayConfig

## 摘要
設定應用程式閘道。

## 句法

### Read-configfile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
AzureApplicationGatewayConfig Cmdlet 會 **設定** 應用程式閘道。

## 示例

### 範例1：使用設定物件來設定應用程式閘道
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

第一個命令會使用 **AzureApplicationGatewayConfig** Cmdlet，透過名為 ApplicationGateway02 的應用程式閘道取得 configuration 物件。
該命令會將它儲存在 $ConfigReturnObject 變數中。

第二個命令會使用 $ConfigReturnObject 變數中所儲存的應用程式閘道設定物件，來設定名為 ApplicationGateway06 之應用程式的配置。

### 範例2：使用設定檔設定應用程式閘道
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

這個命令會在指定位置中使用應用程式閘道設定檔案，來設定名為 ApplicationGateway06 的應用程式的設定。

### 範例3：使用設定物件修改配置
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

第一個命令會使用 **AzureApplicationGatewayConfig** Cmdlet，透過名為 ApplicationGateway06 的應用程式閘道取得 configuration 物件。
該命令會將它儲存在 $ConfigReturnObject 變數中。

第二個命令會將埠值指派給儲存在 $ConfigReturnObject 的物件中的 **port** 屬性。

最終命令會將更新的 $ConfigReturnObject 傳遞至目前的 Cmdlet。

## 參數

### -Config
指定應用程式閘道設定物件。
這個 Cmdlet 會將此參數指定的設定指派給應用程式閘道。

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Read-configfile
以 XML 格式指定應用程式閘道的設定檔路徑。
這個 Cmdlet 會將此參數指定的設定指派給應用程式閘道。

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所設定之應用程式閘道的名稱。

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### ApplicationGatewayObjectModel. ApplicationGatewayConfiguration （系統字串）

## 輸出

### ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure

## 筆記

## 相關連結

[AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


