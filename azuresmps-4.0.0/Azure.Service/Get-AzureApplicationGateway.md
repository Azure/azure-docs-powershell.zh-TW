---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967116"
---
# Get-AzureApplicationGateway

## 摘要
取得應用程式閘道。

## 句法

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureApplicationGateway** Cmdlet 會取得現有的 Azure 應用程式閘道。

## 示例

### 範例1：取得應用程式閘道
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

這個命令會取得名為 ApplicationGateway06 的應用程式閘道。

### 範例2：取得所有應用程式閘道
```
PS C:\> Get-AzureApplicationGateway
```

這個命令會在您的訂閱下取得所有的應用程式閘道。

## 參數

### -名稱
指定此 Cmdlet 所取得之應用程式閘道的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.object

## 輸出

### ApplicationGatewayObjectModel ApplicationGateway，IEnumerable. ApplicationGateway<ApplicationGatewayObjectModel..>

## 筆記

## 相關連結

[新-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[移除-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[開始-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[停止 AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[更新-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


