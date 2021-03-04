---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906162"
---
# Backup-AzKeyVaultCertificate

## 簡介
備份金鑰庫中的憑證。

## 語法

### ByCertificateName (預設) 
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Backup-AzKeyVaultCertificate Cmdlet** 會下載並儲存于檔案中，以備份金鑰保存庫中的指定憑證。
如果憑證有多個版本，其所有版本都會包含在備份中。
由於下載的內容已加密，因此無法在 Azure 金鑰保存庫外部使用。
只要該憑證位於相同的 Azure 地理位置，您即可以將備份憑證還原到其備份之訂閱的任何金鑰庫。
使用此 Cmdlet 的一般原因如下： 
- 您想要保留憑證的離線副本，以防您不小心從保存庫刪除原始檔案。
 
- 您使用 Key Vault 建立憑證，而現在想要將物件複製至不同的 Azure 區域，以便從分散式應用程式的所有實例使用它。
使用 **Backup-AzKeyVaultCertificate** Cmdlet 以加密格式來取回憑證，然後使用 **Restore-AzKeyVaultCertificate** Cmdlet，並指定第二個地區的金鑰保存庫。

## 例子

### 範例 1：使用自動產生的檔案名備份憑證
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

此命令會從名為 MyKeyVault 的金鑰保存庫取取名為 MyCert 的憑證，並儲存該憑證的備份至自動為您命名的檔案，並顯示檔案名。

### 範例 2：將憑證備份到指定的檔案名
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

此命令會從名為 MyKeyVault 的金鑰保存庫取取名為 MyCert 的憑證，並儲存該憑證的備份至名為 Backup.blob 的檔案。

### 範例 3：將先前所取的憑證備份到指定的檔案名，覆寫目標檔案而不提示。
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

此命令會建立名為 $cert 的憑證備份。名稱為 $cert。保存庫名稱為名為 Backup.blob 的檔案，如果檔案已存在，會以無提示方式覆寫檔案。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
覆寫已存在的檔案

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要備份的機密，從呼叫的取回輸出中輸入。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
機密名稱。
Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
輸出檔案。
儲存憑證備份的輸出檔案。
如果未指定，將會產生預設檔案名。

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
儲存庫名稱。
Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByCertificateName
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIdentityItem

## 輸出

### System.String

## 筆記

## 相關連結
