---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967943"
---
# Remove-AzureApplicationGateway

## 摘要
移除應用程式閘道。

## 句法

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureApplicationGateway** Cmdlet 會移除應用程式閘道。

## 示例

### 範例1：移除應用程式閘道
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

這個命令會移除名為 ApplicationGateway06 的應用程式閘道。

## 參數

### -名稱
指定此 Cmdlet 移除之應用程式閘道的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure

## 筆記

## 相關連結

[AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[新-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[開始-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[停止 AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[更新-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


