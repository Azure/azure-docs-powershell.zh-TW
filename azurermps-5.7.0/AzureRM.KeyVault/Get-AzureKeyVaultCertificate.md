---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447789"
---
# Get-AzureKeyVaultCertificate

## 摘要
從金鑰保存庫取得憑證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByName (預設) 
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateNameAndVersion
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateAllVersions
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNameInputObject
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateNameAndVersionInputObject
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateAllVersionsInputObject
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureKeyVaultCertificate** Cmdlet 會從 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證或憑證版本。

## 示例

### 範例1：取得憑證
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

這個命令會從名為 ContosoKV01 的主要電子倉庫中取得名為 TestCert01 的憑證。

### 範例2：取得已刪除但未針對此金鑰保存庫清除的所有憑證。
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有憑證。

### 範例3：取得已刪除但未針對此金鑰保存庫清除的憑證 MyCert。
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得名為「MyCert」的憑證，但尚未清除。
這個命令會傳回中繼資料，例如刪除日期，以及此刪除的憑證的排程清除日期。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -IncludeVersions
表示此操作會取得所有版本的憑證。

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
KeyVault 物件。

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
指定是否要在輸出中包含先前刪除的憑證

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得的憑證名稱。

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
指定主要電子倉庫的名稱。

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
指定憑證版本。

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### [System.object]. 清單 ' 1 [KeyVault]。 PSKeyVaultCertificateIdentityItem]

### PSKeyVaultCertificate 中的 KeyVault。

## 筆記

## 相關連結

[附加 AzureKeyVaultCertificate](./Add-AzureKeyVaultCertificate.md)

[匯入-AzureKeyVaultCertificate](./Import-AzureKeyVaultCertificate.md)

[移除-AzureKeyVaultCertificate](./Remove-AzureKeyVaultCertificate.md)

[復原-AzureKeyVaultSecretCertificate](./Undo-AzureKeyVaultSecretCertificate.md)
