---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: 5c53355daf364553accd4168f89d6bc1a3ccff03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787429"
---
# Backup-AzKeyVaultSecret

## 摘要
在金鑰保存庫中備份密碼。

## 句法

### BySecretName (預設) 
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzKeyVaultSecret** Cmdlet 會透過下載並儲存在一個檔案中，以在金鑰儲存庫中備份指定的密碼。
如果有多個版本的密碼，所有版本都包含在備份中。
因為下載的內容是經過加密的，所以無法在 Azure 金鑰保存庫外部使用。
您可以將備份的密碼還原到其備份之訂閱中的任何重要電子倉庫。
使用此 Cmdlet 的常見原因如下：
- 您想要保管您的機密複本，以便您在金鑰保存庫中不小心刪除您的機密時擁有離線複本。
- 您已將密碼新增到金鑰保存庫，現在想要將該秘密克隆至不同的 Azure 區域，以便您可以從分散式應用程式的所有實例中使用。 使用 Backup-AzKeyVaultSecret Cmdlet 以加密格式來檢索機密，然後使用 Restore-AzKeyVaultSecret Cmdlet，並在第二個區域中指定金鑰 vault。  (請注意，地區必須屬於相同的地理位置。 ) 

## 示例

### 範例1：使用自動產生的檔案名備份密碼
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

這個命令會從名為 MyKeyVault 的主要保存庫中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到自動為您命名的檔案，並顯示檔案名。

### 範例2：將機密備份到指定的檔案名，覆寫現有檔案而不提示
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

這個命令會從 [金鑰 vaultnamed MyKeyVault] 中檢索名為 MySecret 的密碼，並將該密碼的備份儲存到名為 [Backup.] 的檔案。

### 範例3：備份先前檢索到指定檔案名的密碼
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

這個命令會使用 $secret 物件的電子倉庫名稱和名稱來檢索機密，並將其備份儲存到名為 [Backup.] 的檔案。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -Force
會在您覆寫輸出檔案（如果有的話）時提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要備份的機密，從檢索呼叫的輸出中流水線。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定要備份之密碼的名稱。

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
指定儲存備份 blob 的輸出檔案。
如果您沒有指定此參數，這個 Cmdlet 會為您產生檔案名。
如果您指定現有輸出檔案的名稱，該作業將無法完成，而且會傳回備份檔案已經存在的錯誤訊息。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
指定包含要備份之密碼之金鑰保存庫的名稱。

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
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
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
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

### PSKeyVaultSecretIdentityItem 中的 KeyVault。

## 輸出

### System.object

## 筆記

## 相關連結

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[移除-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

