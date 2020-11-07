---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967940"
---
# Remove-AzureApplicationGatewaySslCertificate

## 摘要
從應用程式閘道移除 SSL 憑證。

## 句法

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureApplicationGatewaySslCertificate** Cmdlet 會從應用程式閘道 (SSL) 憑證中移除安全通訊端層。

## 示例

### 範例1：移除 SSL 憑證
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

這個命令會將名為 SslCertificate13 的 SSL 憑證從名為 ApplicationGateway08 的應用程式閘道中移除。

## 參數

### -CertificateName
指定 SSL 憑證的名稱。
這個 Cmdlet 會移除此參數指定的憑證。

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

### -名稱
指定此 Cmdlet 移除 SSL 憑證之應用程式閘道的名稱。

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
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

[附加 AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[AzureApplicationGatewaySslCertificate](./Get-AzureApplicationGatewaySslCertificate.md)
