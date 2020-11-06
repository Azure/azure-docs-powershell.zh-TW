---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448850"
---
# New-AzureRmApplicationGatewaySslCertificate

## 摘要
建立 Azure 應用程式閘道的 SSL 憑證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的 AzureRmApplicationGatewaySslCertificate** Cmdlet 會建立 Azure 應用程式閘道的 SSL 憑證。

## 示例

### 範例1：建立 Azure 應用程式閘道的 SSL 憑證。
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

這個命令會建立名為 Cert01 的 SSL 憑證，以用於預設的應用程式閘道，並將結果儲存在名為 $Cert 的變數中。

## 參數

### -CertificateFile
指定此 Cmdlet 建立之 SSL 憑證之 .pfx 檔案的路徑。

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

### -名稱
指定此 Cmdlet 所建立之 SSL 憑證的名稱。

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

### -Password
指定此 Cmdlet 所建立之 SSL 的密碼。

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

### System.object

## 輸出

### PSApplicationGatewaySslCertificate 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmApplicationGatewaySslCertificate](./Add-AzureRmApplicationGatewaySslCertificate.md)

[AzureRmApplicationGatewaySslCertificate](./Get-AzureRmApplicationGatewaySslCertificate.md)

[移除-AzureRmApplicationGatewaySslCertificate](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[Set-AzureRmApplicationGatewaySslCertificate](./Set-AzureRmApplicationGatewaySslCertificate.md)


