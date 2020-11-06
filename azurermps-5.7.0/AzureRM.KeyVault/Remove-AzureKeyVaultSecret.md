---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: a4b90f91c44fc54f60539c326a6b37caba868488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450596"
---
# Remove-AzureKeyVaultSecret

## 摘要
刪除金鑰保存庫中的密碼。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByVaultName (預設) 
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
Remove-AzureKeyVaultSecret Cmdlet 會刪除金鑰保存庫中的密碼。
如果不小心刪除了機密，您可以使用具有特殊「復原」許可權的使用者 Undo-AzureKeyVaultSecretRemoval 來復原機密。
這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。

## 示例

### 範例1：移除金鑰保存庫的密碼
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。

### 範例2：移除金鑰保存庫中不含使用者確認的密碼
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。
命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。

### 範例3：從金鑰保存庫永久清除已刪除的機密
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

這個命令會從名為 Contoso 的主要保存庫永久 premoves 名為 FinanceSecret 的密碼。
執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。

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

### -Force
強制執行命令，而不要求使用者確認。

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

### -InputObject
主要 Vault 密碼物件

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
如果有，則會永久移除先前刪除的機密。

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

### -名稱
指定秘密的名稱。
這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
表示此 Cmdlet 會傳回 **KeyVault** 物件的 [.]
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -VaultName
指定機密所屬之金鑰保存庫的名稱。
這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 字串

## 輸出

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret
這個 Cmdlet 只有在您指定 *PassThru* 參數時才會傳回值。

## 筆記

## 相關連結

[AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[復原-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

