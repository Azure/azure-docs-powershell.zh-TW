---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446799"
---
# Get-AzureKeyVaultSecret

## 摘要
取得金鑰保存庫中的密碼。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByVaultName (預設) 
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureKeyVaultSecret** Cmdlet 會在金鑰保存庫中取得機密資訊。
這個 Cmdlet 會在金鑰保存庫中取得特定機密或所有機密。

## 示例

### 範例1：取得金鑰保存庫中所有機密的最新版本
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

這個命令會取得名為 Contoso 之金鑰保存庫中所有機密的目前版本。

### 範例2：取得特定機密的所有版本
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的所有版本。

### 範例3：取得特定機密的目前版本
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的目前版本。

### 範例4：取得特定機密的特定版本
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

這個命令會在名為 Contoso 的主要電子倉庫中取得名為 ITSecret 的特定密碼版本。

### 範例5：取得特定機密之目前版本的純文字值
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

這些命令會取得名為 ITSecret 之密碼的目前版本，然後顯示該秘密的純文字值。

### 範例6：取得已刪除但未針對此金鑰保存庫清除的所有機密。
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有機密。

### 範例7：取得已刪除但未針對此金鑰保存庫清除的機密 ITSecret。
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的機密 ITSecret。
這個命令會傳回中繼資料，例如刪除日期，以及此刪除的機密的排程清除日期。

## 參數

### -IncludeVersions
表示此 Cmdlet 會取得所有版本的密碼。
密碼的目前版本是清單中的第一個版本。
如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。

如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會以指定的 *名稱* 取得目前的機密版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
指定是否要在輸出中顯示先前刪除的機密。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得之密碼的名稱。

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
指定機密所屬之金鑰保存庫的名稱。
這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
指定機密版本。
這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### 字串

## 輸出

### [KeyVault]<清單中的 [SecretIdentityItem]。 [KeyVault]><、[]、[>]、、、、、、、、DeletedSecretIdentityItem

## 筆記

## 相關連結

[移除-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[復原-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

