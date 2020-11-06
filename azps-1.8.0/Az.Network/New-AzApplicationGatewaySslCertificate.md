---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0749f964831962c946c5682db6c746da644cb0ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621823"
---
# New-AzApplicationGatewaySslCertificate

## 摘要
建立 Azure 應用程式閘道的 SSL 憑證。

## 句法

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的 AzApplicationGatewaySslCertificate** Cmdlet 會建立 Azure 應用程式閘道的 SSL 憑證。

## 示例

### 範例1：建立 Azure 應用程式閘道的 SSL 憑證。
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

這個命令會建立名為 Cert01 的 SSL 憑證，以用於預設的應用程式閘道，並將結果儲存在名為 $Cert 的變數中。

### 範例2：使用 KeyVault 機密建立 SSL 憑證 (版本較少的 secretId) 並新增至應用程式閘道。
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

取得密碼並使用建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。
注意：在這裡提供版本較少的 secretId，應用程式閘道會以定期間隔與 KeyVault 同步處理憑證。

### 範例3：使用 KeyVault 機密建立 SSL 憑證並新增至應用程式閘道。
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

取得密碼並使用建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。
注意：如果應用程式閘道需要使用 KeyVault 同步處理憑證，請提供版本較少的 secretId。

## 參數

### -CertificateFile
指定此 Cmdlet 建立之 SSL 憑證之 .pfx 檔案的路徑。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -KeyVaultSecretId
SecretId KeyVault 密碼的 (uri) 。 當需要使用特定的機密版本時，請使用這個選項。

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
Type: System.Security.SecureString
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

### 所有

## 輸出

### PSApplicationGatewaySslCertificate 中的 [.]

## 筆記

## 相關連結

[附加 AzApplicationGatewaySslCertificate](./Add-AzApplicationGatewaySslCertificate.md)

[AzApplicationGatewaySslCertificate](./Get-AzApplicationGatewaySslCertificate.md)

[移除-AzApplicationGatewaySslCertificate](./Remove-AzApplicationGatewaySslCertificate.md)

[Set-AzApplicationGatewaySslCertificate](./Set-AzApplicationGatewaySslCertificate.md)


