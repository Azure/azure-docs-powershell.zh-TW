---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904425"
---
# Backup-AzKeyVaultSecret

## 簡介
備份金鑰庫中的機密。

## 語法

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

## 描述
**Backup-AzKeyVaultSecret** Cmdlet 可下載並儲存于檔案中，以備份金鑰保存庫中的指定機密。
如果有多個版本的金鑰，所有版本會包含在備份中。
由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。
您可以將備份的機密還原到訂閱中任何備份的金鑰庫。
使用此 Cmdlet 的一般原因如下：
- 您想要代管您金鑰的一份副本，這樣一來，萬一您不小心在金鑰保存庫中刪除您的密碼，就擁有一份離線副本。
- 您新增了金鑰庫的機密，而現在想要將金鑰複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用它。 使用 Backup-AzKeyVaultSecret Cmdlet 以加密格式來取回密碼，然後使用 Restore-AzKeyVaultSecret Cmdlet，並指定第二個地區的金鑰保存庫。  (請注意，區域必須屬於相同的地理位置.) 

## 例子

### 範例 1：使用自動產生的檔案名備份機密
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

此命令會從名為 MyKeyVault 的金鑰保存庫中，取取名為 MySecret 的機密，並儲存該機密的備份至自動為您命名的檔案，並顯示檔案名。

### 範例 2：備份指定檔案名的機密，覆寫現有檔案而不提示
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

此命令會從名稱為 MyKeyVault 的金鑰保存庫取取名為 MySecret 的機密，並儲存該機密的備份至名為 Backup.blob 的檔案。

### 範例 3：備份先前取至指定檔案名的機密
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

此命令會使用$secret保存庫名稱和名稱來取回機密，並儲存其備份到名為 Backup.blob 的檔案。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -強制
提示您確認，然後再覆寫輸出檔案 ，如果有。

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
要備份的機密，從呼叫的取回輸出中輸入。

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
指定要備份的機密名稱。

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
指定儲存備份 Blob 的輸出檔案。
如果您未指定此參數，此 Cmdlet 會產生您的檔案名。
如果您指定現有輸出檔案的名稱，作業將不會完成，並返回備份檔案已存在的錯誤訊息。

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
指定包含要備份之機密之金鑰庫的名稱。

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
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem

## 輸出

### System.String

## 筆記

## 相關連結

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

