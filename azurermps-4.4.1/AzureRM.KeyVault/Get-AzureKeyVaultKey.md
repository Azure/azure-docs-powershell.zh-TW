---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446802"
---
# Get-AzureKeyVaultKey

## 摘要
取得金鑰保存庫金鑰。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByVaultName (預設) 
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。
這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。

## 示例

### 範例1：取得金鑰保存庫中的所有按鍵
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。

### 範例2：取得目前的金鑰版本
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

這個命令會取得名為 Contoso 的主要保存庫中名為 ITPfx 之金鑰的目前版本。

### 範例3：取得金鑰的所有版本
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

這個命令會取得所有版本金鑰 vaultnamed Contoso 中名為 ITPfx 的金鑰。

### 範例4：取得特定的金鑰版本
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

這個命令會在名為 Contoso 的主要保存庫中，取得名為 ITPfx 的特定金鑰版本。
執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。

### 範例5：取得已刪除但未針對此金鑰保存庫清除的所有索引鍵。
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。

### 範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 ITPfx。
這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。

## 參數

### -IncludeVersions
表示此 Cmdlet 會取得所有版本的金鑰。
索引鍵的目前版本是清單中的第一個版本。
如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。

如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
指定是否要在輸出中顯示先前刪除的金鑰。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得的金鑰捆綁的名稱。

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。
這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。

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
指定金鑰版本。
這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

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

### [KeyVault]<清單中的 [> KeyIdentityItem]。 KeyVault. KeyBundle、List><、、、KeyVault、、、、、、、、

## 筆記

## 相關連結

[附加 AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[移除-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[復原-AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

